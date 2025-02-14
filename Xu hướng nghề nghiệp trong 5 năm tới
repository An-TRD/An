import React, { useState, useEffect } from "react";
import { Card, CardContent } from "@/components/ui/card";
import { motion } from "framer-motion";
import Draggable from "react-draggable";

const careers = [
  { title: "Trí tuệ nhân tạo & Machine Learning", category: "Công nghệ", trend: "Đang phát triển mạnh", skills: "Python, TensorFlow, Data Science", link: "https://www.youtube.com/watch?v=0JzYwMvWEXo" },
  { title: "Phát triển phần mềm & Kỹ sư dữ liệu", category: "Công nghệ", trend: "Nhu cầu cao", skills: "JavaScript, React, SQL", link: "https://www.youtube.com/watch?v=upDLs1sn7g4" },
  { title: "An ninh mạng", category: "Công nghệ", trend: "Rất quan trọng", skills: "Network Security, Ethical Hacking", link: "https://www.youtube.com/watch?v=1stySlpX2pI" },
  { title: "Chuyên gia Blockchain", category: "Công nghệ", trend: "Tiềm năng lớn", skills: "Solidity, Smart Contracts", link: "https://www.youtube.com/watch?v=bBC-nXj3Ng4" },
  { title: "Chăm sóc sức khỏe số hóa", category: "Y tế", trend: "Đang bùng nổ", skills: "Telemedicine, AI Healthcare", link: "https://www.youtube.com/watch?v=H9pt6DtkMUE" },
  { title: "Công nghệ bán dẫn", category: "Công nghệ", trend: "Rất quan trọng cho tương lai", skills: "VLSI, Chip Design, Manufacturing", link: "https://www.youtube.com/watch?v=f0rHjJVyS3g" },
  { title: "Bác sĩ & Chuyên gia y tế", category: "Y tế", trend: "Luôn cần thiết", skills: "Phẫu thuật, Chăm sóc bệnh nhân", link: "https://www.youtube.com/watch?v=wE0uS6MFb1o" }
];

export default function CareerTrends() {
  const [search, setSearch] = useState("");
  const [category, setCategory] = useState("Tất cả");
  const [petPosition, setPetPosition] = useState({ x: 50, y: 50 });

  useEffect(() => {
    const interval = setInterval(() => {
      setPetPosition(prev => ({
        x: prev.x + (Math.random() * 100 - 50),
        y: prev.y + (Math.random() * 100 - 50)
      }));
    }, 2000);
    return () => clearInterval(interval);
  }, []);

  return (
    <div className="p-6 max-w-6xl mx-auto bg-gradient-to-br from-green-200 to-blue-300 min-h-screen relative font-sans">
      <motion.h1
        className="text-4xl font-bold text-center mb-6 bg-yellow-500 text-white p-5 rounded-lg shadow-lg"
        initial={{ opacity: 0 }}
        animate={{ opacity: 1 }}
        transition={{ duration: 1 }}
      >
        🌟 Xu Hướng Nghề Nghiệp Trong Tương Lai 🌟
      </motion.h1>
      <Draggable>
        <div className="absolute left-1/2 transform -translate-x-1/2 top-4 bg-white p-4 rounded-lg shadow-md border border-gray-400 cursor-move">
          <h2 className="font-bold text-lg">Nhóm 3</h2>
        </div>
      </Draggable>
      <div className="absolute" style={{ top: petPosition.y, left: petPosition.x, transition: 'top 1s, left 1s' }}>
        <img src="https://i.imgur.com/JfPpwOA.png" alt="Pet" className="w-16 h-16" />
      </div>
      <div className="text-center mb-6">
        <a href="https://vt.tiktok.com/ZSMLFfjoj/" target="_blank" className="text-red-600 text-lg font-bold underline">💖 Xin mời mọi người ủng hộ video của Nhóm 3 💖</a>
      </div>
      <input
        type="text"
        placeholder="🔍 Tìm kiếm nghề nghiệp..."
        className="w-full p-3 border border-gray-400 rounded-lg mb-4 text-lg"
        value={search}
        onChange={(e) => setSearch(e.target.value)}
      />
      <select
        className="w-full p-3 border border-gray-400 rounded-lg mb-4 text-lg bg-white"
        value={category}
        onChange={(e) => setCategory(e.target.value)}
      >
        <option value="Tất cả">🌍 Tất cả</option>
        <option value="Công nghệ">💻 Công nghệ</option>
        <option value="Y tế">🏥 Y tế</option>
      </select>
      <div className="grid grid-cols-1 md:grid-cols-2 gap-6">
        {careers.filter(career => career.title.toLowerCase().includes(search.toLowerCase()) && (category === "Tất cả" || career.category === category)).map((career, index) => (
          <Card key={index} className="p-4 bg-white rounded-lg shadow-md">
            <CardContent>
              <h2 className="text-xl font-bold">{career.title}</h2>
              <p><strong>📌 Lĩnh vực:</strong> {career.category}</p>
              <p><strong>📈 Xu hướng:</strong> {career.trend}</p>
              <p><strong>🔧 Kỹ năng:</strong> {career.skills}</p>
              <a href={career.link} target="_blank" className="text-blue-600 underline">📺 Video giải thích</a>
            </CardContent>
          </Card>
        ))}
      </div>
      <div className="fixed bottom-0 left-0 w-full bg-white shadow-xl p-4 border border-gray-400 text-center bg-opacity-50">
        <h2 className="font-bold text-lg">📌 Thành viên Nhóm 3</h2>
        <p>Lâm Hoài An, Ngô Thị Huỳnh Như, Phạm Thị Hồng Ngọc, Trần Thị Mỹ Linh, Phạm Thị Yến Dương, Nguyễn Thị Ngọc Trâm, Trần Hồng Ngọc Hân</p>
      </div>
    </div>
  );
}
