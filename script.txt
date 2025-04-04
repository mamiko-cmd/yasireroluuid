// generateUUID fonksiyonu, UUID oluşturuyor
function generateUUID() {
    // Bu, rastgele bir UUID oluşturur
    const uuid = 'xxxxxxxx-xxxx-4xxx-yxxx-xxxxxxxxxxxx'.replace(/[xy]/g, function(c) {
        const r = Math.random() * 16 | 0, // 0 ile 15 arasında rastgele bir sayı
              v = c === 'x' ? r : (r & 0x3 | 0x8); // 'x' yerine rastgele sayı, 'y' için özel bir işlem
        return v.toString(16); // Sayıyı 16'lık (hexadecimal) sisteme çevirir
    });

    // Oluşturulan UUID'yi sayfada gösteriyoruz
    document.getElementById('uuidDisplay').textContent = uuid;
}
