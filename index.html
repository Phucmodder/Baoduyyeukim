import React, { useState, useEffect, useRef } from 'react';
import { User, CreditCard, Phone, CheckCircle, Star, Crown, Shield, AlertTriangle, HelpCircle, MessageCircle, Send, Users } from 'lucide-react';

const App = () => {
  const [step, setStep] = useState(1); // 1: UID input, 2: Price selection, 3: Card input, 4: Success
  const [uid, setUid] = useState('');
  const [selectedPackage, setSelectedPackage] = useState(null);
  const [cardType, setCardType] = useState('mobifone'); // 'mobifone', 'vinaphone', 'viettel', 'garena', 'zing'
  const [cardCode, setCardCode] = useState('');
  const [cardSerial, setCardSerial] = useState('');
  const [isProcessing, setIsProcessing] = useState(false);
  const [recentTransactions, setRecentTransactions] = useState([]);
  const [chatMessages, setChatMessages] = useState([]);
  const [newMessage, setNewMessage] = useState('');
  const [showHelp, setShowHelp] = useState(false);
  const [onlineUsers, setOnlineUsers] = useState(1247);
  const [totalUsers, setTotalUsers] = useState(89432);
  const chatContainerRef = useRef(null);

  const pricePackages = [
    { id: 1, price: 50000, diamonds: 1100, doubled: 2200, warranty: true, firstTimeBonus: true },
    { id: 2, price: 100000, diamonds: 2600, doubled: 5200, warranty: true, firstTimeBonus: true },
    { id: 3, price: 200000, diamonds: 6000, doubled: 12000, warranty: true, firstTimeBonus: true },
    { id: 4, price: 300000, diamonds: 10100, doubled: 20200, warranty: true, firstTimeBonus: true },
    { id: 5, price: 500000, diamonds: 20000, doubled: 40000, warranty: true, firstTimeBonus: true },
    { id: 6, price: 1000000, diamonds: 45000, doubled: 90000, warranty: true, firstTimeBonus: true },
  ];

  const cardTypes = [
    { id: 'mobifone', name: 'MobiFone', color: 'from-orange-500 to-red-500' },
    { id: 'vinaphone', name: 'Vinaphone', color: 'from-green-500 to-blue-500' },
    { id: 'viettel', name: 'Viettel', color: 'from-red-500 to-pink-500' },
    { id: 'garena', name: 'Garena', color: 'from-purple-500 to-indigo-500' },
    { id: 'zing', name: 'Zing', color: 'from-yellow-500 to-orange-500' },
  ];

  // Vietnamese first names
  const firstNames = [
    'Nguyễn', 'Trần', 'Lê', 'Phạm', 'Hoàng', 'Huỳnh', 'Phan', 'Vũ', 'Võ', 'Đặng',
    'Bùi', 'Đỗ', 'Hồ', 'Ngô', 'Dương', 'Lý', 'Đào', 'Đoàn', 'Lưu', 'Trịnh'
  ];

  // Vietnamese last names
  const lastNames = [
    'Văn', 'Thị', 'Minh', 'Quốc', 'Tuấn', 'Hải', 'Đức', 'Nam', 'Hùng', 'Phúc',
    'Linh', 'Hà', 'Mai', 'Anh', 'Trung', 'Bình', 'Sơn', 'Dũng', 'Quang', 'Huy',
    'Tùng', 'Việt', 'Phương', 'Nhật', 'Khánh', 'Hiếu', 'Thắng', 'Long', 'Cường', 'Hòa'
  ];

  // Function to mask UID (show only some digits)
  const maskUid = (uid) => {
    if (uid.length !== 16) return uid;
    return `${uid.substring(0, 5)}*****${uid.substring(11, 16)}`;
  };

  // Function to mask name (show first name + last initial)
  const maskName = (fullName) => {
    const parts = fullName.split(' ');
    if (parts.length >= 2) {
      return `${parts[0]} ${parts[1].charAt(0)}***`;
    }
    return `${fullName.substring(0, 2)}***`;
  };

  // Generate random Vietnamese name
  const generateRandomName = () => {
    const firstName = firstNames[Math.floor(Math.random() * firstNames.length)];
    const lastName = lastNames[Math.floor(Math.random() * lastNames.length)];
    const middleName = Math.random() > 0.5 ? lastNames[Math.floor(Math.random() * lastNames.length)] + ' ' : '';
    return `${firstName} ${middleName}${lastName}`;
  };

  // Generate fake transactions with masked UIDs
  const generateFakeTransaction = () => {
    const fakeUid = Math.random().toString().substring(2, 18).padEnd(16, '0');
    const maskedUid = maskUid(fakeUid);
    const diamonds = [2200, 5200, 12000, 20200, 40000, 90000][Math.floor(Math.random() * 6)];
    const price = [50000, 100000, 200000, 300000, 500000, 1000000][Math.floor(Math.random() * 6)];
    const cardTypeName = ['MobiFone', 'Vinaphone', 'Viettel', 'Garena', 'Zing'][Math.floor(Math.random() * 5)];
    return {
      id: Date.now() + Math.random(),
      uid: maskedUid,
      diamonds: diamonds,
      price: price,
      cardType: cardTypeName,
      time: 'vừa xong'
    };
  };

  // Generate fake review with masked name
  const generateFakeReview = () => {
    const fakeMessages = [
      'Web nạp uy tín, nạp 2 phút là quân huy vào tài khoản!',
      'Nạp rất nhanh, hỗ trợ nhiệt tình, sẽ ủng hộ dài dài!',
      'Lần đầu nạp thử, uy tín thật sự. Cảm ơn shop!',
      'Nạp 50k được 2200 quân huy, quá hời. Web chuẩn!',
      'Giao diện đẹp, nạp dễ dàng, quân huy vào nhanh chóng!',
      'Nạp siêu nhanh, 2 phút là có quân huy!',
      'Web uy tín, nạp lần nào cũng thành công',
      'Hỗ trợ nhiệt tình, sẽ tiếp tục ủng hộ',
      'Giá tốt, nạp x2 lần đầu quá hời',
      'Giao diện đẹp, dễ sử dụng',
      'Nạp 100k được 5200 quân huy, quá ok!',
      'Quân huy vào tài khoản nhanh chóng',
      'Web chuẩn, nạp là có liền',
      'Nạp 200k được 12000 quân huy, quá đã!',
      'Dịch vụ chuyên nghiệp, nạp là có ngay',
      'Không cần lo lắng, nạp là thành công 100%',
      'Web nạp Liên Quân tốt nhất mình từng dùng',
      'Nạp xong 3 phút là quân huy vào, quá nhanh!',
      'Giá cả hợp lý, dịch vụ tốt, sẽ quay lại',
      'Cảm ơn web đã giúp mình có quân huy mua skin mới!'
    ];
    
    const randomName = generateRandomName();
    const maskedName = maskName(randomName);
    
    return {
      id: Date.now() + Math.random(),
      name: maskedName,
      message: fakeMessages[Math.floor(Math.random() * fakeMessages.length)],
      time: 'vừa xong'
    };
  };

  useEffect(() => {
    // Initialize with some fake transactions
    const initialTransactions = Array.from({ length: 6 }, () => generateFakeTransaction());
    setRecentTransactions(initialTransactions);
    
    // Add new fake transactions periodically
    const transactionInterval = setInterval(() => {
      const newTransaction = generateFakeTransaction();
      setRecentTransactions(prev => [newTransaction, ...prev.slice(0, 9)]);
      // Increase counters
      setOnlineUsers(prev => Math.min(prev + Math.floor(Math.random() * 3), 2000));
      setTotalUsers(prev => prev + Math.floor(Math.random() * 5));
    }, 8000);

    // Initialize fake reviews
    const initialReviews = Array.from({ length: 8 }, () => generateFakeReview());
    setChatMessages(initialReviews);

    // Add new fake reviews periodically
    const reviewInterval = setInterval(() => {
      const newReview = generateFakeReview();
      setChatMessages(prev => [newReview, ...prev.slice(0, 14)]);
    }, 6000);

    // Update online users periodically
    const onlineInterval = setInterval(() => {
      setOnlineUsers(prev => {
        const change = Math.floor(Math.random() * 10) - 3; // -3 to +6
        return Math.max(1000, Math.min(prev + change, 2500));
      });
    }, 10000);

    return () => {
      clearInterval(transactionInterval);
      clearInterval(reviewInterval);
      clearInterval(onlineInterval);
    };
  }, []);

  const handleUidSubmit = (e) => {
    e.preventDefault();
    if (uid.trim().length === 16 && /^\d+$/.test(uid)) {
      setStep(2);
    }
  };

  const handlePackageSelect = (pkg) => {
    setSelectedPackage(pkg);
    setStep(3);
  };

  const handleCardSubmit = (e) => {
    e.preventDefault();
    if (cardCode.trim() && cardSerial.trim()) {
      setIsProcessing(true);
      setTimeout(() => {
        setIsProcessing(false);
        setStep(4);
        
        // Add to recent transactions with masked UID
        const maskedUserUid = maskUid(uid);
        const selectedCardTypeName = cardTypes.find(type => type.id === cardType)?.name || '';
        const newTransaction = {
          id: Date.now(),
          uid: maskedUserUid,
          diamonds: selectedPackage.doubled,
          price: selectedPackage.price,
          cardType: selectedCardTypeName,
          time: 'vừa xong'
        };
        setRecentTransactions(prev => [newTransaction, ...prev.slice(0, 9)]);
        
        // Increase total users
        setTotalUsers(prev => prev + 1);
      }, 2000);
    }
  };

  const handleSendMessage = (e) => {
    e.preventDefault();
    if (newMessage.trim()) {
      const message = {
        id: Date.now(),
        name: 'Bạn',
        message: newMessage.trim(),
        time: 'bây giờ'
      };
      setChatMessages(prev => [message, ...prev.slice(0, 14)]);
      setNewMessage('');
    }
  };

  const formatPrice = (price) => {
    return new Intl.NumberFormat('vi-VN').format(price);
  };

  const formatDiamonds = (diamonds) => {
    return new Intl.NumberFormat('vi-VN').format(diamonds);
  };

  // Get selected card type name
  const selectedCardTypeName = cardTypes.find(type => type.id === cardType)?.name || '';

  return (
    <div className="min-h-screen bg-gradient-to-br from-purple-900 via-blue-900 to-indigo-900">
      {/* Help Modal */}
      {showHelp && (
        <div className="fixed inset-0 bg-black/70 backdrop-blur-sm flex items-center justify-center z-50 p-4">
          <div className="bg-white rounded-2xl p-6 max-w-md w-full max-h-96 overflow-y-auto">
            <div className="flex items-center justify-between mb-4">
              <h3 className="text-xl font-bold text-gray-900">Cách lấy UID Liên Quân</h3>
              <button
                onClick={() => setShowHelp(false)}
                className="text-gray-500 hover:text-gray-700"
              >
                ✕
              </button>
            </div>
            <div className="space-y-3 text-gray-700 text-sm">
              <p>Để lấy UID Liên Quân, bạn cần vào giao diện chính của game, chọn biểu tượng Tài khoản ở góc trên bên trái, rồi vào Cài đặt (hình bánh răng cưa) và chọn mục UID. UID của bạn sẽ hiển thị và bạn có thể nhấn nút "Chép" để sao chép mã này.</p>
              
              <div className="space-y-2">
                <p className="font-semibold">Các bước chi tiết để lấy UID Liên Quân:</p>
                <ol className="list-decimal list-inside space-y-1">
                  <li>Mở game Liên Quân Mobile và đăng nhập vào tài khoản của bạn.</li>
                  <li>Tại giao diện chính, nhấn vào biểu tượng Tài khoản (thường là ảnh đại diện của bạn) ở góc trên bên trái màn hình.</li>
                  <li>Tiếp theo, chọn biểu tượng Cài đặt (hình bánh răng cưa).</li>
                  <li>Chọn vào mục UID để xem mã định danh tài khoản của bạn.</li>
                  <li>Mã UID của bạn sẽ xuất hiện. Bạn có thể nhấn nút "Chép" để sao chép mã này vào bộ nhớ tạm của điện thoại.</li>
                </ol>
              </div>
            </div>
            <button
              onClick={() => setShowHelp(false)}
              className="w-full mt-4 py-2 bg-gradient-to-r from-blue-500 to-purple-600 text-white font-medium rounded-xl"
            >
              Đã hiểu
            </button>
          </div>
        </div>
      )}

      {/* Header */}
      <header className="bg-black/20 backdrop-blur-sm border-b border-white/10">
        <div className="max-w-7xl mx-auto px-4 py-4 flex items-center justify-between">
          <div className="flex items-center space-x-3">
            <div className="w-10 h-10 bg-gradient-to-r from-yellow-400 to-orange-500 rounded-full flex items-center justify-center">
              <Crown className="w-6 h-6 text-white" />
            </div>
            <h1 className="text-2xl font-bold text-white">Liên Quân Mobile</h1>
          </div>
          <div className="text-white/80 text-sm flex items-center space-x-4">
            <div className="flex items-center space-x-1">
              <Users className="w-4 h-4 text-green-400" />
              <span className="text-green-400 font-semibold">{onlineUsers.toLocaleString()}</span>
              <span className="text-white/60">online</span>
            </div>
            <div className="text-white/60">
              {totalUsers.toLocaleString()} người đã nạp
            </div>
          </div>
        </div>
      </header>

      <div className="max-w-7xl mx-auto px-4 py-8">
        {/* Step 1: UID Input */}
        {step === 1 && (
          <div className="max-w-md mx-auto">
            <div className="bg-white/10 backdrop-blur-sm rounded-2xl p-8 border border-white/20 text-center">
              <div className="w-16 h-16 bg-gradient-to-r from-blue-400 to-purple-500 rounded-full flex items-center justify-center mx-auto mb-6">
                <User className="w-8 h-8 text-white" />
              </div>
              <h2 className="text-2xl font-bold text-white mb-4">Nhập UID Người Chơi</h2>
              <p className="text-white/80 mb-6">
                Vui lòng nhập UID tài khoản Liên Quân của bạn (16 ký tự số) để tiếp tục nạp Quân Huy
              </p>
              <form onSubmit={handleUidSubmit} className="space-y-4">
                <div className="relative">
                  <input
                    type="text"
                    value={uid}
                    onChange={(e) => {
                      const value = e.target.value.replace(/\D/g, '');
                      if (value.length <= 16) {
                        setUid(value);
                      }
                    }}
                    placeholder="Nhập UID 16 ký tự..."
                    maxLength={16}
                    className="w-full px-4 py-3 rounded-xl bg-white/10 border border-white/20 text-white placeholder-white/60 focus:outline-none focus:ring-2 focus:ring-yellow-400 text-center font-mono"
                  />
                  <button
                    type="button"
                    onClick={() => setShowHelp(true)}
                    className="absolute right-3 top-1/2 transform -translate-y-1/2 text-white/60 hover:text-white transition-colors"
                  >
                    <HelpCircle className="w-5 h-5" />
                  </button>
                </div>
                <div className="mt-2 text-white/60 text-sm">
                  {uid.length}/16 ký tự
                </div>
                <button
                  type="submit"
                  disabled={uid.length !== 16}
                  className="w-full py-3 bg-gradient-to-r from-yellow-400 to-orange-500 text-black font-bold rounded-xl hover:from-yellow-500 hover:to-orange-600 transition-all duration-300 disabled:opacity-50 disabled:cursor-not-allowed"
                >
                  Tiếp Tục
                </button>
              </form>
            </div>
          </div>
        )}

        {/* Step 2: Price Selection */}
        {step === 2 && (
          <div className="max-w-6xl mx-auto">
            <div className="text-center mb-8">
              <h2 className="text-3xl font-bold text-white mb-2">Chọn Gói Nạp Quân Huy</h2>
              <p className="text-white/80">UID: <span className="text-yellow-400 font-semibold">{uid}</span></p>
            </div>

            <div className="bg-white/10 backdrop-blur-sm rounded-2xl border border-white/20 overflow-hidden">
              <div className="grid grid-cols-4 gap-4 p-4 bg-black/20 text-white font-semibold">
                <div>Mệnh giá</div>
                <div>Quân Huy</div>
                <div>Bảo hành</div>
                <div>x2 Nạp lần đầu</div>
              </div>
              
              <div className="divide-y divide-white/10">
                {pricePackages.map((pkg) => (
                  <div
                    key={pkg.id}
                    className="grid grid-cols-4 gap-4 p-4 hover:bg-white/5 cursor-pointer transition-all duration-200"
                    onClick={() => handlePackageSelect(pkg)}
                  >
                    <div className="text-white font-medium">
                      {formatPrice(pkg.price)}đ
                    </div>
                    <div className="text-yellow-400 font-bold">
                      {formatDiamonds(pkg.doubled)}
                    </div>
                    <div className="text-green-400 font-semibold">
                      Có
                    </div>
                    <div className="text-blue-400 font-semibold flex items-center justify-center">
                      <Star className="w-4 h-4 mr-1" />
                      Có
                    </div>
                  </div>
                ))}
              </div>
            </div>

            <div className="mt-6 text-center">
              <button
                onClick={() => setStep(1)}
                className="text-white/80 hover:text-white transition-colors duration-200"
              >
                ← Quay lại nhập UID
              </button>
            </div>
          </div>
        )}

        {/* Step 3: Card Input */}
        {step === 3 && (
          <div className="max-w-md mx-auto">
            <div className="bg-white/10 backdrop-blur-sm rounded-2xl p-8 border border-white/20">
              <div className="text-center mb-6">
                <h2 className="text-2xl font-bold text-white mb-2">Nhập Mã Thẻ</h2>
                <div className="bg-yellow-500/20 border border-yellow-500/30 rounded-lg p-3 mt-3">
                  <div className="flex items-center space-x-2 text-yellow-400 text-sm mb-1">
                    <AlertTriangle className="w-4 h-4" />
                    <span className="font-semibold">LƯU Ý QUAN TRỌNG</span>
                  </div>
                  <p className="text-yellow-300 text-xs">
                    Vui lòng chọn đúng loại thẻ và mệnh giá tương ứng. 
                    Nếu chọn sai (ví dụ: thẻ Viettel 50k nhưng chọn mệnh giá 100k), 
                    giao dịch sẽ bị lỗi và KHÔNG ĐƯỢC BẢO HÀNH.
                  </p>
                </div>
              </div>

              {/* Selected Info */}
              <div className="bg-white/5 rounded-xl p-4 mb-6 border border-white/10">
                <div className="grid grid-cols-1 md:grid-cols-3 gap-3 text-sm">
                  <div>
                    <span className="text-white/60">Loại thẻ:</span>
                    <div className="text-white font-semibold">{selectedCardTypeName}</div>
                  </div>
                  <div>
                    <span className="text-white/60">Mệnh giá:</span>
                    <div className="text-yellow-400 font-semibold">{formatPrice(selectedPackage.price)}đ</div>
                  </div>
                  <div>
                    <span className="text-white/60">Quân Huy nhận được:</span>
                    <div className="text-green-400 font-semibold">+{formatDiamonds(selectedPackage.doubled)}</div>
                  </div>
                </div>
              </div>

              <div className="space-y-6">
                <div className="grid grid-cols-2 gap-3">
                  {cardTypes.map((type) => (
                    <button
                      key={type.id}
                      onClick={() => setCardType(type.id)}
                      className={`py-3 rounded-xl font-medium transition-all duration-200 text-sm ${
                        cardType === type.id
                          ? `bg-gradient-to-r ${type.color} text-white shadow-lg`
                          : 'bg-white/10 text-white/80 hover:bg-white/20'
                      }`}
                    >
                      {type.name}
                    </button>
                  ))}
                </div>

                <form onSubmit={handleCardSubmit} className="space-y-4">
                  <div>
                    <label className="block text-white/80 text-sm mb-2">Mã thẻ</label>
                    <input
                      type="text"
                      value={cardCode}
                      onChange={(e) => setCardCode(e.target.value.toUpperCase())}
                      placeholder="Nhập mã thẻ..."
                      className="w-full px-4 py-3 rounded-xl bg-white/10 border border-white/20 text-white placeholder-white/60 focus:outline-none focus:ring-2 focus:ring-yellow-400 font-mono"
                    />
                  </div>
                  
                  <div>
                    <label className="block text-white/80 text-sm mb-2">Số seri</label>
                    <input
                      type="text"
                      value={cardSerial}
                      onChange={(e) => setCardSerial(e.target.value.toUpperCase())}
                      placeholder="Nhập số seri..."
                      className="w-full px-4 py-3 rounded-xl bg-white/10 border border-white/20 text-white placeholder-white/60 focus:outline-none focus:ring-2 focus:ring-yellow-400 font-mono"
                    />
                  </div>

                  <button
                    type="submit"
                    disabled={!cardCode.trim() || !cardSerial.trim() || isProcessing}
                    className="w-full py-3 bg-gradient-to-r from-yellow-400 to-orange-500 text-black font-bold rounded-xl hover:from-yellow-500 hover:to-orange-600 transition-all duration-300 disabled:opacity-50 disabled:cursor-not-allowed"
                  >
                    {isProcessing ? (
                      <div className="flex items-center justify-center space-x-2">
                        <div className="w-5 h-5 border-2 border-white/30 border-t-white rounded-full animate-spin"></div>
                        <span>Đang xử lý...</span>
                      </div>
                    ) : (
                      'Nạp Quân Huy'
                    )}
                  </button>
                </form>

                <div className="text-center mt-4">
                  <button
                    onClick={() => setStep(2)}
                    className="text-white/80 hover:text-white transition-colors duration-200"
                  >
                    ← Quay lại chọn gói
                  </button>
                </div>
              </div>
            </div>
          </div>
        )}

        {/* Step 4: Success */}
        {step === 4 && (
          <div className="max-w-md mx-auto">
            <div className="bg-white/10 backdrop-blur-sm rounded-2xl p-8 border border-white/20 text-center">
              <div className="w-16 h-16 bg-green-500 rounded-full flex items-center justify-center mx-auto mb-6">
                <CheckCircle className="w-8 h-8 text-white" />
              </div>
              <h2 className="text-2xl font-bold text-white mb-4">Nạp Thành Công!</h2>
              <div className="text-white/80 space-y-2 mb-6">
                <p>Đã nạp <span className="text-yellow-400 font-bold">{formatDiamonds(selectedPackage.doubled)}</span> Quân Huy</p>
                <p>cho tài khoản UID: <span className="text-yellow-400 font-bold">{uid}</span></p>
                <p className="text-green-400">Quân Huy sẽ vào tài khoản trong 5-10 phút</p>
              </div>
              <button
                onClick={() => {
                  setStep(1);
                  setUid('');
                  setSelectedPackage(null);
                  setCardCode('');
                  setCardSerial('');
                }}
                className="w-full py-3 bg-gradient-to-r from-blue-500 to-purple-600 text-white font-bold rounded-xl hover:from-blue-600 hover:to-purple-700 transition-all duration-300"
              >
                Nạp Tiếp
              </button>
            </div>
          </div>
        )}

        {/* Recent Transactions */}
        <div className="mt-12">
          <div className="flex items-center justify-center mb-6">
            <Shield className="w-6 h-6 text-green-400 mr-2" />
            <h3 className="text-xl font-bold text-white">Giao Dịch Gần Đây</h3>
            <Shield className="w-6 h-6 text-green-400 ml-2" />
          </div>
          
          <div className="bg-white/5 backdrop-blur-sm rounded-2xl p-6 border border-white/10">
            <div className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4">
              {recentTransactions.map((transaction) => (
                <div
                  key={transaction.id}
                  className="bg-white/10 rounded-xl p-4 border border-white/10 animate-pulse"
                >
                  <div className="text-white/80 text-xs mb-1">
                    <span className="font-semibold text-white">UID: {transaction.uid}</span>
                  </div>
                  <div className="text-green-400 text-sm font-semibold mb-1">
                    +{formatDiamonds(transaction.diamonds)} Quân Huy
                  </div>
                  <div className="text-white/60 text-xs mb-1">
                    Gói {formatPrice(transaction.price)}đ • {transaction.cardType}
                  </div>
                  <div className="text-white/40 text-xs">{transaction.time}</div>
                </div>
              ))}
            </div>
          </div>
        </div>

        {/* Chat Reviews */}
        <div className="mt-12">
          <div className="flex items-center justify-center mb-6">
            <MessageCircle className="w-6 h-6 text-blue-400 mr-2" />
            <h3 className="text-xl font-bold text-white">Đánh Giá Từ Người Dùng</h3>
            <MessageCircle className="w-6 h-6 text-blue-400 ml-2" />
          </div>
          
          <div className="bg-white/5 backdrop-blur-sm rounded-2xl border border-white/10">
            <div 
              ref={chatContainerRef}
              className="h-96 overflow-y-auto p-4 space-y-3"
            >
              {chatMessages.map((msg) => (
                <div key={msg.id} className="bg-white/10 rounded-lg p-3">
                  <div className="flex items-center justify-between mb-1">
                    <span className="text-white font-semibold text-sm">{msg.name}</span>
                    <span className="text-white/60 text-xs">{msg.time}</span>
                  </div>
                  <p className="text-white/90 text-sm">{msg.message}</p>
                </div>
              ))}
            </div>
            
            <div className="border-t border-white/10 p-4">
              <form onSubmit={handleSendMessage} className="flex space-x-2">
                <input
                  type="text"
                  value={newMessage}
                  onChange={(e) => setNewMessage(e.target.value)}
                  placeholder="Chia sẻ trải nghiệm của bạn..."
                  className="flex-1 px-3 py-2 rounded-lg bg-white/10 border border-white/20 text-white placeholder-white/60 focus:outline-none focus:ring-1 focus:ring-yellow-400 text-sm"
                />
                <button
                  type="submit"
                  disabled={!newMessage.trim()}
                  className="px-4 py-2 bg-gradient-to-r from-blue-500 to-purple-600 text-white rounded-lg hover:from-blue-600 hover:to-purple-700 transition-all duration-200 disabled:opacity-50 disabled:cursor-not-allowed"
                >
                  <Send className="w-4 h-4" />
                </button>
              </form>
            </div>
          </div>
        </div>

        {/* Footer Info */}
        <div className="mt-8 text-center text-white/60 text-sm">
          <p className="mb-2">Hệ thống bảo hành 100% - Hỗ trợ 24/7</p>
          <p>Liên hệ hỗ trợ: hotro@lienquan.com | Hotline: 1900-1234</p>
        </div>
      </div>
    </div>
  );
};

export default App;
```
