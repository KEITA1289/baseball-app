import React, { useState, useEffect } from 'react';
import { 
  Home, BarChart2, Calendar, LineChart, Settings, 
  ChevronRight, AlertCircle, BookOpen, CheckCircle, 
  Plus, Save, Loader2, ArrowLeft, TrendingUp,
  Target, Zap, Brain, Shield, Info
} from 'lucide-react';
import { LineChart as ReChart, Line, XAxis, YAxis, CartesianGrid, Tooltip, ResponsiveContainer } from 'recharts';

// --- 初期サンプルデータ ---
const INITIAL_RECORDS = [
  { id: 1, date: '2023-06-01', content: 'マシン打撃（変化球中心）', duration: 90, successRate: 65, note: '外角のスライダーへの見極めが良くなった。' },
  { id: 2, date: '2023-06-05', content: 'シート打撃', duration: 120, successRate: 55, note: '追い込まれてからのカットができるようになった。' },
];

const INITIAL_TEAM_STATS = {
  teamName: '勝鳳高校 野球部',
  ageGroup: '高校',
  battingAvg: 0.245,
  obp: 0.310,
  strikeoutRate: 22,
  swingMissRate: 15,
  breakingBallMissRate: 28,
  scoringPosAvg: 0.210,
  errors: 12,
  fieldingPct: 0.965
};

const EVIDENCE_LEVELS = {
  RESEARCH: { label: '研究・論文', color: 'bg-green-100 text-green-700 border-green-200', icon: '🟢' },
  ORG: { label: '専門機関・競技団体', color: 'bg-blue-100 text-blue-700 border-blue-200', icon: '🔵' },
  THEORY: { label: '専門家の指導理論', color: 'bg-yellow-100 text-yellow-700 border-yellow-200', icon: '🟡' },
  AI: { label: 'AIによる統合的な提案', color: 'bg-gray-100 text-gray-700 border-gray-200', icon: '⚪' },
};

const SPORTS_COACH_AI = () => {
  // --- States ---
  const [activeTab, setActiveTab] = useState('home');
  const [loading, setLoading] = useState(false);
  const [showResult, setShowResult] = useState(false);
  const [analysisType, setAnalysisType] = useState(null); // 'batting' or 'fielding'
  const [formData, setFormData] = useState({});
  const [records, setRecords] = useState(INITIAL_RECORDS);
  const [teamSettings, setTeamSettings] = useState(INITIAL_TEAM_STATS);
  const [toast, setToast] = useState(null);

  // --- LocalStorage persistence ---
  useEffect(() => {
    const savedRecords = localStorage.getItem('sca_records');
    if (savedRecords) setRecords(JSON.parse(savedRecords));
    const savedSettings = localStorage.getItem('sca_settings');
    if (savedSettings) setTeamSettings(JSON.parse(savedSettings));
  }, []);

  useEffect(() => {
    localStorage.setItem('sca_records', JSON.stringify(records));
    localStorage.setItem('sca_settings', JSON.stringify(teamSettings));
  }, [records, teamSettings]);

  // --- Helpers ---
  const showToast = (msg) => {
    setToast(msg);
    setTimeout(() => setToast(null), 3000);
  };

  const handleStartAnalysis = (e) => {
    e.preventDefault();
    setLoading(true);
    setTimeout(() => {
      setLoading(false);
      setShowResult(true);
    }, 2000);
  };

  // --- UI Components ---

  const Header = ({ title, showBack }) => (
    <div className="sticky top-0 z-10 bg-white border-b px-4 py-4 flex items-center shadow-sm">
      {showBack && (
        <button onClick={() => { setShowResult(false); setAnalysisType(null); }} className="mr-3">
          <ArrowLeft className="w-6 h-6 text-gray-600" />
        </button>
      )}
      <h1 className="text-xl font-bold text-blue-900">{title || 'SPORTS COACH AI'}</h1>
    </div>
  );

  const Toast = () => toast && (
    <div className="fixed bottom-24 left-1/2 transform -translate-x-1/2 z-50 bg-gray-800 text-white px-6 py-3 rounded-full shadow-lg animate-bounce">
      {toast}
    </div>
  );

  // --- Screens ---

  const HomeScreen = () => (
    <div className="pb-24 animate-fade-in">
      <div className="bg-gradient-to-br from-blue-700 to-blue-900 text-white p-6 rounded-b-3xl shadow-lg">
        <h2 className="text-2xl font-bold mb-2">SPORTS COACH AI</h2>
        <p className="text-blue-100 opacity-90 text-sm mb-6">チームの課題をAIと一緒に分析しましょう</p>
        
        <div className="bg-white/10 backdrop-blur-md rounded-2xl p-4 border border-white/20">
          <p className="text-xs text-blue-200 uppercase tracking-wider font-semibold">現在のチーム</p>
          <p className="text-xl font-bold">{teamSettings.teamName}</p>
          <div className="flex gap-2 mt-3">
            <span className="bg-blue-500/40 px-2 py-1 rounded text-xs">年代: {teamSettings.ageGroup}</span>
            <span className="bg-blue-500/40 px-2 py-1 rounded text-xs">分析ステータス: 良好</span>
          </div>
        </div>
      </div>

      <div className="px-4 -mt-4">
        <button 
          onClick={() => setActiveTab('analysis')}
          className="w-full bg-white shadow-xl rounded-2xl p-6 flex items-center justify-between border-2 border-blue-500 active:scale-95 transition-transform"
        >
          <div className="flex items-center gap-4">
            <div className="bg-blue-100 p-3 rounded-xl">
              <Zap className="w-6 h-6 text-blue-600" />
            </div>
            <div className="text-left">
              <p className="font-bold text-gray-800">新しく分析する</p>
              <p className="text-xs text-gray-500">最新データから課題を抽出</p>
            </div>
          </div>
          <ChevronRight className="text-blue-500" />
        </button>
      </div>

      <div className="p-4 space-y-6">
        <section>
          <h3 className="text-lg font-bold text-gray-800 mb-3 flex items-center gap-2">
            <Target className="w-5 h-5 text-blue-600" /> 分析カテゴリー
          </h3>
          <div className="grid grid-cols-2 gap-3">
            <button onClick={() => { setActiveTab('analysis'); setAnalysisType('batting'); }} className="bg-white p-4 rounded-2xl shadow-sm border border-gray-100 flex flex-col items-center gap-2">
              <span className="text-2xl">⚾</span>
              <span className="font-bold text-gray-700">打撃分析</span>
            </button>
            <button onClick={() => { setActiveTab('analysis'); setAnalysisType('fielding'); }} className="bg-white p-4 rounded-2xl shadow-sm border border-gray-100 flex flex-col items-center gap-2">
              <span className="text-2xl">🧤</span>
              <span className="font-bold text-gray-700">守備分析</span>
            </button>
            {['走塁分析', 'フィジカル', 'メンタル'].map(item => (
              <div key={item} className="bg-gray-50 p-4 rounded-2xl border border-gray-100 flex flex-col items-center gap-2 relative opacity-60">
                <span className="absolute top-2 right-2 text-[8px] bg-gray-400 text-white px-1.5 py-0.5 rounded-full font-bold">COMING SOON</span>
                <span className="text-2xl opacity-50">{item === '走塁分析' ? '🏃' : item === 'フィジカル' ? '💪' : '🧠'}</span>
                <span className="font-bold text-gray-500 text-sm">{item}</span>
              </div>
            ))}
          </div>
        </section>

        <section className="bg-blue-50 p-4 rounded-2xl border border-blue-100">
          <h3 className="font-bold text-blue-900 mb-2">直近の練習プラン</h3>
          <div className="bg-white p-3 rounded-xl shadow-sm flex justify-between items-center">
            <div>
              <p className="text-sm font-bold text-gray-800">WEEK 2: 技術改善フェーズ</p>
              <p className="text-xs text-gray-500">変化球への対応力強化</p>
            </div>
            <button onClick={() => setActiveTab('plan')} className="text-blue-600 text-xs font-bold underline">詳細</button>
          </div>
        </section>
      </div>
    </div>
  );

  const AnalysisForm = () => (
    <div className="pb-24 animate-fade-in">
      <Header title="チーム分析入力" showBack={analysisType} />
      
      {!analysisType ? (
        <div className="p-4 space-y-4">
          <p className="text-gray-600 font-medium">分析するカテゴリーを選択してください：</p>
          <div className="grid grid-cols-1 gap-4">
            <button 
              onClick={() => setAnalysisType('batting')}
              className="p-6 bg-white border-2 border-transparent hover:border-blue-500 rounded-2xl shadow-sm flex items-center gap-4 transition-all"
            >
              <span className="text-4xl">⚾</span>
              <div className="text-left">
                <p className="text-xl font-bold">打撃 (Batting)</p>
                <p className="text-sm text-gray-500">打率、三振率、空振り率など</p>
              </div>
            </button>
            <button 
              onClick={() => setAnalysisType('fielding')}
              className="p-6 bg-white border-2 border-transparent hover:border-blue-500 rounded-2xl shadow-sm flex items-center gap-4 transition-all"
            >
              <span className="text-4xl">🧤</span>
              <div className="text-left">
                <p className="text-xl font-bold">守備 (Fielding)</p>
                <p className="text-sm text-gray-500">守備率、エラー内訳、失点など</p>
              </div>
            </button>
          </div>
        </div>
      ) : (
        <form onSubmit={handleStartAnalysis} className="p-4 space-y-4">
          <div className="bg-white p-4 rounded-2xl shadow-sm border border-gray-100 space-y-4">
            <h3 className="font-bold text-gray-800 border-l-4 border-blue-500 pl-3">基本データ</h3>
            <div>
              <label className="block text-xs font-bold text-gray-500 mb-1">対象年代</label>
              <select className="w-full p-3 bg-gray-50 rounded-xl border-none ring-1 ring-gray-200 focus:ring-2 focus:ring-blue-500 transition-all">
                <option>少年野球</option>
                <option>中学</option>
                <option selected>高校</option>
                <option>大学</option>
                <option>社会人</option>
              </select>
            </div>
          </div>

          <div className="bg-white p-4 rounded-2xl shadow-sm border border-gray-100 space-y-4">
            <h3 className="font-bold text-gray-800 border-l-4 border-blue-500 pl-3">
              {analysisType === 'batting' ? '打撃詳細データ' : '守備詳細データ'}
            </h3>
            {analysisType === 'batting' ? (
              <div className="grid grid-cols-2 gap-4">
                {[
                  { label: 'チーム打率', val: '.245' },
                  { label: '出塁率', val: '.310' },
                  { label: '三振率 (%)', val: '22' },
                  { label: '空振り率 (%)', val: '15' },
                  { label: '変化球空振り率 (%)', val: '28' },
                  { label: '得点圏打率', val: '.210' },
                ].map(item => (
                  <div key={item.label}>
                    <label className="block text-[10px] font-bold text-gray-500 mb-1 uppercase tracking-tighter">{item.label}</label>
                    <input type="text" defaultValue={item.val} className="w-full p-3 bg-gray-50 rounded-xl border-none ring-1 ring-gray-200" />
                  </div>
                ))}
              </div>
            ) : (
              <div className="grid grid-cols-2 gap-4">
                {[
                  { label: 'チーム守備率', val: '.965' },
                  { label: 'エラー総数', val: '12' },
                  { label: '送球エラー', val: '8' },
                  { label: '捕球エラー', val: '4' },
                  { label: '内野エラー', val: '10' },
                  { label: '外野エラー', val: '2' },
                ].map(item => (
                  <div key={item.label}>
                    <label className="block text-[10px] font-bold text-gray-500 mb-1 uppercase tracking-tighter">{item.label}</label>
                    <input type="text" defaultValue={item.val} className="w-full p-3 bg-gray-50 rounded-xl border-none ring-1 ring-gray-200" />
                  </div>
                ))}
              </div>
            )}
            <div>
              <label className="block text-[10px] font-bold text-gray-500 mb-1 uppercase tracking-tighter">コーチが感じている課題（自由入力）</label>
              <textarea 
                className="w-full p-3 bg-gray-50 rounded-xl border-none ring-1 ring-gray-200 h-24"
                placeholder="例：追い込まれてから変化球で空振りするケースが多い。"
                defaultValue="練習では打てているが、試合になると変化球への対応ができず三振が増える。"
              />
            </div>
          </div>

          <button 
            type="submit"
            className="w-full bg-blue-600 text-white font-bold py-4 rounded-2xl shadow-lg flex items-center justify-center gap-2 active:scale-95 transition-all"
          >
            {loading ? <Loader2 className="w-5 h-5 animate-spin" /> : <Brain className="w-5 h-5" />}
            AI分析を開始する
          </button>
        </form>
      )}
    </div>
  );

  const AnalysisResultScreen = () => (
    <div className="pb-24 animate-fade-in bg-gray-50 min-h-screen">
      <Header title="AI分析結果" showBack />
      
      <div className="p-4 space-y-4">
        {/* 総合評価 */}
        <div className="bg-white p-6 rounded-3xl shadow-sm border border-blue-100">
          <div className="flex justify-between items-start mb-4">
            <div>
              <span className="bg-blue-600 text-white text-[10px] font-black px-2 py-1 rounded mb-2 inline-block uppercase tracking-widest">General Evaluation</span>
              <h2 className="text-2xl font-bold text-gray-800">総合評価：B-</h2>
            </div>
            <div className="text-right text-blue-600 font-bold text-xs">
              信頼度: 88%
            </div>
          </div>
          <p className="text-gray-600 text-sm leading-relaxed">
            基礎的な打撃力はありますが、<span className="text-blue-600 font-bold underline">変化球（特にスライダー・フォーク）に対するコンタクト率</span>に明確な課題が見られます。高校年代の平均的な空振り率を12%上回っています。
          </p>
        </div>

        {/* 主な課題 */}
        <div className="bg-white p-5 rounded-2xl shadow-sm">
          <h3 className="font-bold text-gray-800 mb-4 flex items-center gap-2">
            <AlertCircle className="w-5 h-5 text-red-500" /> 主な課題
          </h3>
          <div className="space-y-4">
            <div className="border-l-4 border-red-500 pl-4 py-1">
              <div className="flex justify-between items-center mb-1">
                <h4 className="font-bold text-gray-800">変化球への対応力</h4>
                <span className="bg-red-100 text-red-600 text-[10px] font-bold px-2 py-0.5 rounded">重要度：高</span>
              </div>
              <p className="text-xs text-gray-500">2ストライク後の変化球空振り率が42%に達しています。</p>
            </div>
            <div className="border-l-4 border-yellow-500 pl-4 py-1">
              <div className="flex justify-between items-center mb-1">
                <h4 className="font-bold text-gray-800">得点圏での力み</h4>
                <span className="bg-yellow-100 text-yellow-600 text-[10px] font-bold px-2 py-0.5 rounded">重要度：中</span>
              </div>
              <p className="text-xs text-gray-500">チャンス時におけるスイング軌道の乱れが見られます。</p>
            </div>
          </div>
        </div>

        {/* 考えられる原因 */}
        <div className="bg-blue-900 text-white p-5 rounded-2xl shadow-lg">
          <h3 className="font-bold mb-3 flex items-center gap-2">
            <Brain className="w-5 h-5 text-blue-300" /> AIが推測する要因
          </h3>
          <ul className="space-y-3 text-sm">
            <li className="flex items-start gap-2">
              <div className="mt-1 bg-blue-500 rounded-full p-0.5"><CheckCircle className="w-3 h-3" /></div>
              <span>球種の認識（回転による軌道予測）の遅れ</span>
            </li>
            <li className="flex items-start gap-2">
              <div className="mt-1 bg-blue-500 rounded-full p-0.5"><CheckCircle className="w-3 h-3" /></div>
              <span>変化球に対する「溜め（タメ）」の欠如</span>
            </li>
          </ul>
          <div className="mt-4 p-3 bg-white/10 rounded-lg text-[10px] leading-tight text-blue-200 italic border border-white/10">
            ※入力されたデータから考えられる要因です。実際の原因を特定するには、映像分析や現場での観察が必要です。
          </div>
        </div>

        {/* エビデンスセクション */}
        <div className="space-y-3">
          <h3 className="font-bold text-gray-800 flex items-center gap-2 px-1">
            <BookOpen className="w-5 h-5 text-green-600" /> 根拠・エビデンス
          </h3>
          <p className="text-[10px] text-gray-500 px-1 mb-2 tracking-tighter uppercase">この分析・提案を作成する際に参考にした情報</p>
          
          {[
            {
              level: 'RESEARCH',
              title: '打撃における球種識別と視覚的探索パターンの関係',
              source: '日本スポーツ科学学会誌',
              year: '2021',
              desc: '熟練打者はリリース直後のボールの回転情報から軌道を予測しており、未熟な打者はその反応が0.1秒遅れる傾向がある。'
            },
            {
              level: 'ORG',
              title: '高校野球における戦術トレンドとデータ活用',
              source: '全日本野球連盟 強化報告書',
              year: '2022',
              desc: '現代の高校野球ではスライダー系の投球割合が増加しており、対応力不足が打率低下の最大要因。'
            },
            {
              level: 'THEORY',
              title: 'トップハンドの使い方と変化球へのアジャスト',
              source: '元プロ野球選手 A氏 打撃理論',
              year: '2023',
              desc: 'グリップの握りの強さを変えることで、変化球に対する「遊び」を作り、手元まで呼び込む方法。'
            }
          ].map((item, idx) => (
            <div key={idx} className="bg-white border border-gray-100 p-4 rounded-2xl shadow-sm">
              <div className={`inline-flex items-center gap-1 px-2 py-0.5 rounded-full text-[10px] font-bold mb-2 border ${EVIDENCE_LEVELS[item.level].color}`}>
                <span>{EVIDENCE_LEVELS[item.level].icon}</span>
                <span>{EVIDENCE_LEVELS[item.level].label}</span>
              </div>
              <h4 className="font-bold text-sm text-gray-800 mb-1">{item.title}</h4>
              <p className="text-[10px] text-gray-400 mb-2">{item.source} ({item.year})</p>
              <p className="text-xs text-gray-600 leading-normal mb-3">{item.desc}</p>
              <button className="text-xs font-bold text-blue-600 flex items-center gap-1">
                詳細を見る <ChevronRight className="w-3 h-3" />
              </button>
            </div>
          ))}

          <div className={`p-4 rounded-2xl border ${EVIDENCE_LEVELS.AI.color}`}>
            <div className="inline-flex items-center gap-1 px-2 py-0.5 rounded-full text-[10px] font-bold mb-2 bg-white border border-gray-200">
              <span>{EVIDENCE_LEVELS.AI.icon}</span>
              <span>{EVIDENCE_LEVELS.AI.label}</span>
            </div>
            <p className="text-xs text-gray-600 italic">
              上記の複数の知見とチームデータを統合し、現在のチーム状況に最適化された個別の練習プランを生成しました。
            </p>
          </div>
        </div>

        <button 
          onClick={() => setActiveTab('plan')}
          className="w-full bg-blue-600 text-white font-black py-5 rounded-2xl shadow-xl active:scale-95 transition-all flex flex-col items-center justify-center gap-1"
        >
          <span className="text-lg">4週間練習プランを作成する</span>
          <span className="text-[10px] opacity-80 font-normal underline">AIが今の課題に合わせて自動構成</span>
        </button>
      </div>
    </div>
  );

  const PracticePlanScreen = () => (
    <div className="pb-24 animate-fade-in bg-gray-50 min-h-screen">
      <Header title="4週間練習プラン" />
      <div className="p-4 space-y-4">
        {[
          { week: 1, title: '基礎確認・課題の切り分け', color: 'blue' },
          { week: 2, title: '技術改善・反復練習', color: 'indigo' },
          { week: 3, title: '実戦形式・プレッシャー下', color: 'purple' },
          { week: 4, title: '実戦評価・再分析', color: 'emerald' },
        ].map((w) => (
          <div key={w.week} className="bg-white rounded-2xl shadow-sm border border-gray-100 overflow-hidden">
            <div className={`bg-${w.color}-600 text-white p-3 px-4 flex justify-between items-center`}>
              <span className="font-black">WEEK {w.week}</span>
              <span className="text-xs font-bold opacity-80">{w.title}</span>
            </div>
            <div className="p-4 space-y-3">
              <div className="flex justify-between items-center pb-2 border-b border-gray-50">
                <span className="text-[10px] font-bold text-gray-400 uppercase">主な内容</span>
                <span className="text-xs font-bold text-gray-800">{w.week === 1 ? '動画分析 & 近距離トス' : 'マシン変化球打ち'}</span>
              </div>
              <div className="flex justify-between items-center pb-2 border-b border-gray-50">
                <span className="text-[10px] font-bold text-gray-400 uppercase">推奨頻度</span>
                <span className="text-xs font-bold text-gray-800">週3回 / 各40分</span>
              </div>
              <div>
                <p className="text-[10px] font-bold text-gray-400 uppercase mb-1">コーチ向けポイント</p>
                <p className="text-xs text-gray-600 leading-relaxed">
                  {w.week === 1 
                    ? 'ボールを最後まで見るのではなく、リリースの瞬間に焦点を合わせる意識付けを徹底してください。' 
                    : '失敗を恐れず、どの軌道で空振りしたのかを選手に言葉にさせてください。'}
                </p>
              </div>
            </div>
          </div>
        ))}
      </div>
    </div>
  );

  const GrowthRecordScreen = () => (
    <div className="pb-24 animate-fade-in bg-gray-50 min-h-screen">
      <Header title="成長記録・データ分析" />
      
      <div className="p-4 space-y-6">
        {/* 統計グラフ */}
        <div className="bg-white p-4 rounded-3xl shadow-sm border border-gray-100">
          <div className="flex justify-between items-center mb-4 px-2">
            <h3 className="font-bold text-gray-800">打撃指標の推移</h3>
            <span className="text-[10px] bg-green-100 text-green-700 px-2 py-0.5 rounded-full font-bold">改善傾向</span>
          </div>
          <div className="h-48 w-full">
            <ResponsiveContainer width="100%" height="100%">
              <ReChart data={[
                {name: '5月', val: 32}, {name: '6月', val: 28}, {name: '7月', val: 24}, {name: '最新', val: 22}
              ]}>
                <CartesianGrid strokeDasharray="3 3" vertical={false} stroke="#f0f0f0" />
                <XAxis dataKey="name" axisLine={false} tickLine={false} tick={{fontSize: 10}} />
                <YAxis hide />
                <Tooltip />
                <Line type="monotone" dataKey="val" stroke="#2563eb" strokeWidth={3} dot={{r: 4}} name="三振率" />
              </ReChart>
            </ResponsiveContainer>
          </div>
          <p className="text-center text-[10px] text-gray-400 mt-2">※三振率(%)の推移</p>
        </div>

        {/* 前回比 */}
        <div className="grid grid-cols-2 gap-3">
          <div className="bg-white p-4 rounded-2xl shadow-sm border border-gray-100">
            <p className="text-[10px] font-bold text-gray-400 uppercase">チーム打率</p>
            <div className="flex items-end gap-2 mt-1">
              <span className="text-xl font-bold">.245</span>
              <span className="text-xs text-green-600 font-bold mb-1 flex items-center"><TrendingUp className="w-3 h-3" /> +0.012</span>
            </div>
          </div>
          <div className="bg-white p-4 rounded-2xl shadow-sm border border-gray-100">
            <p className="text-[10px] font-bold text-gray-400 uppercase">三振率</p>
            <div className="flex items-end gap-2 mt-1">
              <span className="text-xl font-bold">22%</span>
              <span className="text-xs text-blue-600 font-bold mb-1 flex items-center">- 4%</span>
            </div>
          </div>
        </div>

        {/* 新規入力 */}
        <div className="bg-blue-600 text-white p-5 rounded-2xl shadow-lg relative overflow-hidden">
          <div className="relative z-10">
            <h3 className="font-bold mb-1">本日の練習を記録</h3>
            <p className="text-xs text-blue-100 mb-4 opacity-80">データを蓄積してAIに再分析させましょう</p>
            <div className="space-y-3">
              <input type="date" className="w-full bg-white/20 border-none rounded-xl p-3 text-sm placeholder-blue-200" />
              <button className="w-full bg-white text-blue-600 font-bold py-3 rounded-xl shadow-md">記録を追加する</button>
            </div>
          </div>
          <Plus className="absolute -right-4 -bottom-4 w-32 h-32 opacity-10" />
        </div>

        {/* 再分析ボタン */}
        <button 
          onClick={() => {
            setLoading(true);
            setTimeout(() => {
              setLoading(false);
              showToast("再分析が完了しました");
            }, 1500);
          }}
          className="w-full py-4 bg-gray-800 text-white rounded-2xl font-bold shadow-lg flex items-center justify-center gap-2"
        >
          {loading ? <Loader2 className="w-5 h-5 animate-spin" /> : <LineChart className="w-5 h-5 text-blue-400" />}
          AIに再分析してもらう
        </button>

        {/* 履歴 */}
        <div>
          <h3 className="font-bold text-gray-800 mb-3 px-1">練習記録一覧</h3>
          <div className="space-y-3">
            {records.map(record => (
              <div key={record.id} className="bg-white p-4 rounded-2xl shadow-sm border border-gray-100">
                <div className="flex justify-between items-center mb-2">
                  <span className="text-xs font-bold text-gray-400">{record.date}</span>
                  <span className="text-xs font-bold text-blue-600">成功率: {record.successRate}%</span>
                </div>
                <h4 className="font-bold text-gray-800 mb-1">{record.content}</h4>
                <p className="text-xs text-gray-600 leading-normal">{record.note}</p>
              </div>
            ))}
          </div>
        </div>
      </div>
    </div>
  );

  const SettingsScreen = () => {
    const [tempSettings, setTempSettings] = useState(teamSettings);
    
    return (
      <div className="pb-24 animate-fade-in bg-gray-50 min-h-screen">
        <Header title="チーム設定" />
        <div className="p-4 space-y-4">
          <div className="bg-white p-6 rounded-3xl shadow-sm border border-gray-100 space-y-4">
            <div>
              <label className="block text-xs font-bold text-gray-400 mb-2 uppercase">チーム名</label>
              <input 
                type="text" 
                value={tempSettings.teamName} 
                onChange={(e) => setTempSettings({...tempSettings, teamName: e.target.value})}
                className="w-full p-4 bg-gray-50 border-none ring-1 ring-gray-100 rounded-2xl font-bold focus:ring-2 focus:ring-blue-500"
              />
            </div>
            <div>
              <label className="block text-xs font-bold text-gray-400 mb-2 uppercase">年代</label>
              <select 
                value={tempSettings.ageGroup}
                onChange={(e) => setTempSettings({...tempSettings, ageGroup: e.target.value})}
                className="w-full p-4 bg-gray-50 border-none ring-1 ring-gray-100 rounded-2xl font-bold"
              >
                <option>少年野球</option>
                <option>中学</option>
                <option>高校</option>
                <option>大学</option>
                <option>社会人</option>
              </select>
            </div>
            <div>
              <label className="block text-xs font-bold text-gray-400 mb-2 uppercase">チームカラー</label>
              <div className="flex gap-3">
                {['blue', 'red', 'green', 'black'].map(color => (
                  <button 
                    key={color}
                    className={`w-10 h-10 rounded-full border-4 ${color === 'blue' ? 'border-blue-200' : 'border-transparent'} bg-${color === 'blue' ? 'blue-600' : color === 'red' ? 'red-600' : color === 'green' ? 'green-600' : 'gray-800'}`}
                  />
                ))}
              </div>
            </div>
          </div>
          
          <button 
            onClick={() => {
              setTeamSettings(tempSettings);
              showToast("設定を保存しました");
            }}
            className="w-full bg-blue-600 text-white font-bold py-5 rounded-2xl shadow-xl flex items-center justify-center gap-2"
          >
            <Save className="w-5 h-5" />
            設定を保存する
          </button>

          <div className="p-4 bg-gray-200/50 rounded-2xl border border-dashed border-gray-300">
            <h4 className="text-xs font-bold text-gray-500 mb-2 tracking-widest uppercase">Developer Info</h4>
            <ul className="text-[10px] text-gray-400 space-y-1">
              <li>・Googleアカウント連携: 未設定</li>
              <li>・プラン: フリープラン</li>
              <li>・AI Engine: SPORTS-COACH-v1.2</li>
            </ul>
          </div>
        </div>
      </div>
    );
  };

  // --- Main Render ---

  return (
    <div className="max-w-md mx-auto bg-white min-h-screen relative shadow-2xl font-sans text-gray-900 overflow-x-hidden">
      {/* Screens */}
      {showResult ? <AnalysisResultScreen /> : (
        <>
          {activeTab === 'home' && <HomeScreen />}
          {activeTab === 'analysis' && <AnalysisForm />}
          {activeTab === 'plan' && <PracticePlanScreen />}
          {activeTab === 'growth' && <GrowthRecordScreen />}
          {activeTab === 'settings' && <SettingsScreen />}
        </>
      )}

      {/* Bottom Nav */}
      <nav className="fixed bottom-0 left-0 right-0 max-w-md mx-auto bg-white border-t border-gray-100 flex justify-around items-center py-3 px-2 z-40 shadow-[0_-5px_15px_rgba(0,0,0,0.05)]">
        {[
          { id: 'home', icon: Home, label: 'ホーム' },
          { id: 'analysis', icon: BarChart2, label: '分析' },
          { id: 'plan', icon: Calendar, label: 'プラン' },
          { id: 'growth', icon: LineChart, label: '成長記録' },
          { id: 'settings', icon: Settings, label: '設定' },
        ].map((tab) => (
          <button 
            key={tab.id}
            onClick={() => { setActiveTab(tab.id); setShowResult(false); setAnalysisType(null); }}
            className={`flex flex-col items-center min-w-[64px] transition-all ${activeTab === tab.id ? 'text-blue-600' : 'text-gray-400'}`}
          >
            <tab.icon className={`w-6 h-6 ${activeTab === tab.id ? 'stroke-[2.5px]' : 'stroke-[1.5px]'}`} />
            <span className={`text-[10px] mt-1 font-bold ${activeTab === tab.id ? 'opacity-100' : 'opacity-70'}`}>{tab.label}</span>
            {activeTab === tab.id && <div className="w-1 h-1 bg-blue-600 rounded-full mt-1" />}
          </button>
        ))}
      </nav>

      <Toast />

      {/* Global CSS for animations */}
      <style>{`
        @keyframes fadeIn {
          from { opacity: 0; transform: translateY(10px); }
          to { opacity: 1; transform: translateY(0); }
        }
        .animate-fade-in {
          animation: fadeIn 0.4s ease-out forwards;
        }
      `}</style>
    </div>
  );
};

export default SPORTS_COACH_AI;
