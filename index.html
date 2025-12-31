<!doctype html>
<html lang="ja">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>戦術比較シミュレーター</title>
  <style>
    :root {
      --bg: #1f5fbf;
      --card: rgba(255,255,255,0.06);
      --muted: rgba(255,255,255,0.78);
      --text: #ffffff;
      --line: rgba(255,255,255,0.18);
      --good: #7dffb6;
      --bad: #ff9a9a;
    }

    html, body { height: 100%; }

    body {
      margin: 0;
      font-family: system-ui, -apple-system, "Segoe UI", "Hiragino Kaku Gothic ProN", "Noto Sans JP", sans-serif;
      background: var(--bg);
      color: var(--text);
    }

    .wrap {
      max-width: 1100px;
      margin: 24px auto;
      padding: 0 16px 40px;
    }

    h1 {
      font-size: 22px;
      margin: 0 0 10px;
      letter-spacing: 0.02em;
    }

    .sub {
      color: rgba(255,255,255,0.88);
      margin: 0 0 18px;
      line-height: 1.7;
    }

    .grid {
      display: grid;
      grid-template-columns: 1fr;
      gap: 14px;
    }

    @media (min-width: 980px) {
      .grid { grid-template-columns: 1.1fr 0.9fr; }
    }

    .card {
      background: var(--card);
      border: 1px solid var(--line);
      border-radius: 14px;
      padding: 14px;
      box-shadow: 0 10px 26px rgba(0,0,0,0.22);
      backdrop-filter: blur(6px);
    }

    .row {
      display: grid;
      grid-template-columns: 1fr;
      gap: 10px;
    }

    @media (min-width: 680px) {
      .row.two { grid-template-columns: 1fr 1fr; }
      .row.three { grid-template-columns: 1fr 1fr 1fr; }
    }

    label {
      display: block;
      font-size: 12px;
      color: rgba(255,255,255,0.85);
      margin: 0 0 6px;
    }

    input, select, button {
      width: 100%;
      box-sizing: border-box;
      border-radius: 10px;
      border: 1px solid var(--line);
      background: rgba(0,0,0,0.20);
      color: var(--text);
      padding: 10px 10px;
      outline: none;
    }

    input:disabled, select:disabled {
      opacity: 0.55;
      cursor: not-allowed;
    }

    button {
      cursor: pointer;
      border: 1px solid rgba(255,255,255,0.30);
      background: rgba(255,255,255,0.12);
      font-weight: 700;
    }

    button:hover { background: rgba(255,255,255,0.18); }

    button.secondary {
      border: 1px solid var(--line);
      background: rgba(0,0,0,0.14);
    }

    .hint {
      font-size: 12px;
      color: rgba(255,255,255,0.82);
      line-height: 1.6;
      margin-top: 8px;
    }

    .divider {
      height: 1px;
      background: var(--line);
      margin: 12px 0;
    }

    .pill {
      display: inline-block;
      font-size: 12px;
      padding: 4px 10px;
      border-radius: 999px;
      border: 1px solid var(--line);
      background: rgba(0,0,0,0.12);
      color: rgba(255,255,255,0.86);
    }

    .kpi {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 10px;
      margin-top: 10px;
    }

    .kpi .box {
      border: 1px solid var(--line);
      border-radius: 12px;
      padding: 10px;
      background: rgba(0,0,0,0.14);
    }

    .kpi .box .t { font-size: 12px; color: rgba(255,255,255,0.86); margin-bottom: 6px; }
    .kpi .box .v { font-size: 16px; font-weight: 800; }

    .tableWrap {
      overflow: auto;
      border: 1px solid var(--line);
      border-radius: 12px;
      background: rgba(0,0,0,0.14);
    }

    table {
      border-collapse: collapse;
      width: 100%;
      min-width: 720px;
    }

    th, td {
      border-bottom: 1px solid var(--line);
      padding: 8px 10px;
      font-size: 12px;
      text-align: left;
      vertical-align: middle;
    }

    th {
      position: sticky;
      top: 0;
      background: rgba(0,0,0,0.18);
      z-index: 2;
      color: rgba(255,255,255,0.90);
      font-weight: 800;
    }

    td input {
      padding: 7px 8px;
      border-radius: 8px;
      font-size: 12px;
    }

    .results {
      line-height: 1.8;
      font-size: 14px;
    }

    .results .title {
      font-weight: 900;
      margin: 0 0 6px;
      font-size: 15px;
    }

    .results .line {
      padding: 8px 10px;
      border: 1px solid var(--line);
      border-radius: 12px;
      margin: 8px 0;
      background: rgba(0,0,0,0.12);
    }

    .good { color: var(--good); font-weight: 800; }
    .bad { color: var(--bad); font-weight: 800; }
    .mono { font-family: ui-monospace, SFMono-Regular, Menlo, Consolas, "Noto Sans Mono", monospace; }
    .small { font-size: 12px; color: rgba(255,255,255,0.82); }
  </style>
</head>
<body>
  <div class="wrap">
    <h1>戦術比較シミュレーター</h1>

    <div class="grid">
      <div class="card">
        <div class="row two">
          <div>
            <label>イニング</label>
            <input id="inning" type="number" min="1" max="9" value="9" />
          </div>
          <div>
            <label>表裏</label>
            <select id="half">
              <option value="top" selected>表</option>
              <option value="bot">裏</option>
            </select>
          </div>
        </div>

        <div class="row" style="margin-top:10px;">
          <div>
            <label>攻撃側から見た点差</label>
            <input id="scoreDiff" type="number" min="-20" max="20" value="0" />
            <div class="hint">終盤で点差が小さいときは得点確率を優先します。</div>
          </div>
        </div>

        <div class="divider"></div>

        <div class="row two">
          <div>
            <label>アウト数</label>
            <select id="outs">
              <option value="0">0</option>
              <option value="1">1</option>
              <option value="2">2</option>
            </select>
          </div>
          <div>
            <label>塁状況</label>
            <select id="runners">
              <option value="0">走者なし</option>
              <option value="1">1塁</option>
              <option value="2">2塁</option>
              <option value="3">3塁</option>
              <option value="12">12塁</option>
              <option value="13">13塁</option>
              <option value="23">23塁</option>
              <option value="123">満塁</option>
            </select>
          </div>
        </div>

        <div class="divider"></div>

        <div class="row two">
          <div>
            <label>基準の得点期待値と得点確率</label>
            <select id="customToggle">
              <option value="no">2024の平均を使う</option>
              <option value="yes">自分で入力する</option>
            </select>
            <div class="hint">自分で入力する場合は24状態の表を編集してください。</div>
          </div>
          <div style="display:flex; gap:10px; align-items:flex-end;">
            <button id="calcBtn" type="button">計算する</button>
            <button class="secondary" id="resetBtn" type="button">2024の平均に戻す</button>
          </div>
        </div>

        <div id="customArea" style="margin-top:12px; display:none;">
          <div class="pill">24状態入力</div>
          <div class="hint">得点期待値はそのまま入力します。得点確率はパーセントでも小数でも入力できます。</div>

          <div id="reTableBox" style="margin-top:10px;">
            <div class="small">得点期待値の入力</div>
            <div class="tableWrap" style="margin-top:8px;">
              <table id="reTable"></table>
            </div>
          </div>

          <div id="rpTableBox" style="margin-top:12px;">
            <div class="small">得点確率の入力</div>
            <div class="tableWrap" style="margin-top:8px;">
              <table id="rpTable"></table>
            </div>
          </div>
        </div>

        <div class="kpi">
          <div class="box">
            <div class="t">基準の得点期待値</div>
            <div class="v mono" id="baseRE">0.000</div>
          </div>
          <div class="box">
            <div class="t">基準の得点確率</div>
            <div class="v mono" id="baseRP">0.0 パーセント</div>
          </div>
        </div>

        <div class="divider"></div>

        <div class="row three">
          <div>
            <label>OPS</label>
            <input id="ops" type="number" step="0.001" min="0.300" max="1.500" value="0.700" />
          </div>
          <div>
            <label>打者の走力</label>
            <select id="speed">
              <option value="normal">普通</option>
              <option value="fast">俊足</option>
              <option value="slow">鈍足</option>
            </select>
          </div>
          <div>
            <label>三振傾向</label>
            <select id="kType">
              <option value="neutral">普通</option>
              <option value="high">多い</option>
              <option value="low">少ない</option>
            </select>
          </div>
        </div>

        <div class="row two" style="margin-top:10px;">
          <div>
            <label>送りバント成功率 パーセント</label>
            <input id="buntRate" type="number" min="0" max="100" value="65" />
            <div class="hint" id="buntHint"></div>
          </div>
          <div>
            <label>盗塁成功率 パーセント</label>
            <input id="stealRate" type="number" min="0" max="100" value="70" />
          </div>
        </div>

        <div class="row two" style="margin-top:10px;">
          <div>
            <label>スクイズ成功率 パーセント</label>
            <input id="squeezeRate" type="number" min="0" max="100" value="0" />
          </div>
          <div>
            <label>エンドラン打者タイプ</label>
            <select id="endrunType">
              <option value="3">標準</option>
              <option value="1">パワー</option>
              <option value="2">コンタクト</option>
            </select>
          </div>
        </div>
      </div>

      <div class="card">
        <div class="results" id="output">
          <div class="title">結果</div>
          <div class="line small">まだ計算していません。</div>
        </div>
      </div>
    </div>
  </div>

<script>
  const RUNNERS_ORDER = [0, 4, 2, 1, 6, 5, 3, 7];

  function bitsToLabel(bits) {
    if (bits === 0) return "走者なし";
    const parts = [];
    if (bits & 4) parts.push("1塁");
    if (bits & 2) parts.push("2塁");
    if (bits & 1) parts.push("3塁");
    return parts.join("・");
  }

  function runnersStrToBits(s) {
    s = String(s).trim();
    if (s === "0") return 0;
    let bits = 0;
    for (const ch of s) {
      if (ch === "1") bits |= 4;
      if (ch === "2") bits |= 2;
      if (ch === "3") bits |= 1;
    }
    return bits;
  }

  function key(outs, runners) {
    return `${outs}_${runners}`;
  }

  const DEFAULT_RE_2024 = new Map(Object.entries({
    "0_0": 0.365, "0_4": 0.675, "0_2": 0.958, "0_1": 1.323,
    "0_6": 1.189, "0_5": 1.502, "0_3": 1.827, "0_7": 1.780,

    "1_0": 0.189, "1_4": 0.398, "1_2": 0.565, "1_1": 0.808,
    "1_6": 0.715, "1_5": 1.023, "1_3": 1.281, "1_7": 1.328,

    "2_0": 0.074, "2_4": 0.184, "2_2": 0.280, "2_1": 0.289,
    "2_6": 0.368, "2_5": 0.434, "2_3": 0.440, "2_7": 0.562
  }));

  const DEFAULT_RP_2024 = new Map(Object.entries({
    "0_0": 0.214, "0_4": 0.348, "0_2": 0.577, "0_1": 0.849,
    "0_6": 0.566, "0_5": 0.825, "0_3": 0.820, "0_7": 0.772,

    "1_0": 0.118, "1_4": 0.213, "1_2": 0.351, "1_1": 0.631,
    "1_6": 0.361, "1_5": 0.597, "1_3": 0.642, "1_7": 0.595,

    "2_0": 0.050, "2_4": 0.103, "2_2": 0.196, "2_1": 0.221,
    "2_6": 0.202, "2_5": 0.257, "2_3": 0.227, "2_7": 0.259
  }));

  let RE_TABLE = new Map(DEFAULT_RE_2024);
  let RP_TABLE = new Map(DEFAULT_RP_2024);

  function RE(outs, runners) {
    return RE_TABLE.get(key(outs, runners));
  }

  function RP(outs, runners) {
    return RP_TABLE.get(key(outs, runners));
  }

  function buntAllowed(runners) {
    const has3 = (runners & 1) !== 0;
    const is13 = runners === 5;
    if (has3 && !is13) return false;
    return true;
  }

  function decideMetricAuto(inning, scoreDiff) {
    if (inning >= 8 && Math.abs(scoreDiff) <= 1) return "RP";
    if (inning === 7 && Math.abs(scoreDiff) === 0) return "RP";
    return "RE";
  }

  function metricLabel(code) {
    return code === "RP" ? "得点確率" : "得点期待値";
  }

  function advanceByHit(runners, bases) {
    const on1 = (runners & 4) ? 1 : 0;
    const on2 = (runners & 2) ? 1 : 0;
    const on3 = (runners & 1) ? 1 : 0;

    let runs = 0;
    let newR = 0;

    if (bases === 1) {
      if (on3) runs += 1;
      if (on2) newR |= 1;
      if (on1) newR |= 2;
      newR |= 4;
      return [runs, newR];
    }
    if (bases === 2) {
      if (on3) runs += 1;
      if (on2) runs += 1;
      if (on1) newR |= 1;
      newR |= 2;
      return [runs, newR];
    }
    if (bases === 3) {
      runs += on1 + on2 + on3;
      newR |= 1;
      return [runs, newR];
    }
    if (bases === 4) {
      runs += on1 + on2 + on3 + 1;
      return [runs, 0];
    }
    return [0, runners];
  }

  function walk(runners) {
    const on1 = (runners & 4) ? 1 : 0;
    const on2 = (runners & 2) ? 1 : 0;
    const on3 = (runners & 1) ? 1 : 0;

    if (on1 && on2 && on3) return [1, 7];
    if (on1 && on2 && !on3) return [0, 7];
    if (on1 && !on2 && on3) return [0, 7];
    if (!on1 && on2 && on3) return [0, 7];
    if (on1 && !on2 && !on3) return [0, 6];
    if (!on1 && on2 && !on3) return [0, 6];
    if (!on1 && !on2 && on3) return [0, 5];
    return [0, runners | 4];
  }

  function outSame(outs, runners) { return [0, outs + 1, runners]; }
  function strikeout(outs, runners) { return [0, outs + 1, runners]; }

  function gidp(outs, runners) {
    if ((runners & 4) === 0) return [0, outs + 1, runners];
    return [0, outs + 2, runners & (~4)];
  }

  function buntSuccess(outs, runners) {
    const on1 = (runners & 4) ? 1 : 0;
    const on2 = (runners & 2) ? 1 : 0;
    const on3 = (runners & 1) ? 1 : 0;

    let runs = 0;
    let newR = 0;
    if (on3) runs += 1;
    if (on2) newR |= 1;
    if (on1) newR |= 2;
    return [runs, outs + 1, newR];
  }

  function squeezeSuccess(outs, runners) {
    let runs = 0;
    let r = runners;
    if (runners & 1) {
      runs += 1;
      r = r & (~1);
    }
    const newR = ((r & 2) ? 1 : 0) | ((r & 4) ? 2 : 0);
    return [runs, outs + 1, newR];
  }

  function squeezeFail(outs, runners) {
    let r = runners;
    if (runners & 1) r = r & (~1);
    return [0, outs + 1, r];
  }

  function V_RE(outsNew, runnersNew, score) {
    if (outsNew >= 3) return score;
    return score + RE(outsNew, runnersNew);
  }

  function W_RP(outsNew, runnersNew, score) {
    if (score >= 1) return 1.0;
    if (outsNew >= 3) return 0.0;
    return RP(outsNew, runnersNew);
  }

  function normalizeDict(obj) {
    const total = Object.values(obj).reduce((a, b) => a + b, 0);
    const out = {};
    for (const k of Object.keys(obj)) out[k] = obj[k] / total;
    return out;
  }

  function generateHitProbsSimple(ops, kType, speed) {
    const obp = ops * (1.0 / 2.13);
    const slg = ops * (1.13 / 2.13);
    const iso = Math.max(0.0, slg - obp);

    let kRate = 0.19;
    if (kType === "high") kRate = 0.28;
    if (kType === "low") kRate = 0.10;

    const bbRate = Math.max(0.05, obp * 0.25);
    const hrRate = Math.max(0.01, iso * 0.15);

    const inPlay = Math.max(0.05, 1.0 - kRate - bbRate - hrRate);

    let triple = 0.012;
    let dpConvert = 0.20;
    if (speed === "fast") { triple = 0.020; dpConvert = 0.05; }
    if (speed === "slow") { triple = 0.006; dpConvert = 0.35; }

    const dbl = Math.max(0.02, iso * 0.20);

    const hitTotal = Math.max(0.01, obp - bbRate);
    const nonHrHit = Math.max(0.0, hitTotal - hrRate);

    const base = triple + dbl;
    let tripleRate = 0.0, doubleRate = 0.0, singleRate = nonHrHit;
    if (base > 0) {
      const scale = Math.min(1.0, nonHrHit / base);
      tripleRate = triple * scale;
      doubleRate = dbl * scale;
      singleRate = Math.max(0.0, nonHrHit - tripleRate - doubleRate);
    }

    const gidpRate = inPlay * 0.47 * dpConvert;
    const outRate = Math.max(0.0, 1.0 - (bbRate + hrRate + kRate + tripleRate + doubleRate + singleRate + gidpRate));

    const probs = {
      "HR": hrRate,
      "3B": tripleRate,
      "2B": doubleRate,
      "1B": singleRate,
      "BB": bbRate,
      "K": kRate,
      "GIDP": gidpRate,
      "OUT": outRate
    };
    return normalizeDict(probs);
  }

  function generateEndrunProbs(ops, speed, typeId) {
    let alpha = 0.80;
    let whiff = 0.15;
    if (typeId === 1) { alpha = 0.60; whiff = 0.25; }
    if (typeId === 2) { alpha = 0.90; whiff = 0.05; }

    const base = generateHitProbsSimple(ops * alpha, "neutral", speed);

    const tax = base["HR"] + base["3B"] + base["2B"];
    base["HR"] *= 0.1;
    base["3B"] *= 0.1;
    base["2B"] *= 0.2;

    base["OUT"] += tax * 0.7;
    base["1B"] += tax * 0.3;

    base["K"] = Math.min(0.60, base["K"] + whiff);
    base["GIDP"] = Math.min(base["GIDP"], 0.02);

    return [normalizeDict(base), alpha];
  }

  function transitionForEvent(outs, runners, event) {
    if (event === "HR") {
      const [runs, nr] = advanceByHit(runners, 4);
      return [runs, outs, nr];
    }
    if (event === "3B") {
      const [runs, nr] = advanceByHit(runners, 3);
      return [runs, outs, nr];
    }
    if (event === "2B") {
      const [runs, nr] = advanceByHit(runners, 2);
      return [runs, outs, nr];
    }
    if (event === "1B") {
      const [runs, nr] = advanceByHit(runners, 1);
      return [runs, outs, nr];
    }
    if (event === "BB") {
      const [runs, nr] = walk(runners);
      return [runs, outs, nr];
    }
    if (event === "K") return strikeout(outs, runners);
    if (event === "GIDP") return gidp(outs, runners);
    return outSame(outs, runners);
  }

  function expectedAfterRE(outs, runners, probs) {
    let s = 0.0;
    for (const [event, p] of Object.entries(probs)) {
      const [score, o2, r2] = transitionForEvent(outs, runners, event);
      s += p * V_RE(o2, r2, score);
    }
    return s;
  }

  function expectedAfterRP(outs, runners, probs) {
    let s = 0.0;
    for (const [event, p] of Object.entries(probs)) {
      const [score, o2, r2] = transitionForEvent(outs, runners, event);
      s += p * W_RP(o2, r2, score);
    }
    return s;
  }

  function buntDistribution(pSuccess) {
    const remain = Math.max(0.0, 1.0 - pSuccess);
    return {
      "BUNT_HIT": remain * 0.05,
      "BUNT_OK": pSuccess,
      "BUNT_BAD": remain * 0.75,
      "BUNT_WORST": remain * 0.20
    };
  }

  function expectedBuntAfterRE(outs, runners, pSuccess) {
    const dist = buntDistribution(pSuccess);
    const total = Object.values(dist).reduce((a, b) => a + b, 0);
    let s = 0.0;
    for (const [k, p] of Object.entries(dist)) {
      let tr;
      if (k === "BUNT_HIT") tr = transitionForEvent(outs, runners, "1B");
      else if (k === "BUNT_OK") tr = buntSuccess(outs, runners);
      else if (k === "BUNT_BAD") tr = outSame(outs, runners);
      else tr = gidp(outs, runners);
      const [score, o2, r2] = tr;
      s += (p / total) * V_RE(o2, r2, score);
    }
    return s;
  }

  function expectedBuntAfterRP(outs, runners, pSuccess) {
    const dist = buntDistribution(pSuccess);
    const total = Object.values(dist).reduce((a, b) => a + b, 0);
    let s = 0.0;
    for (const [k, p] of Object.entries(dist)) {
      let tr;
      if (k === "BUNT_HIT") tr = transitionForEvent(outs, runners, "1B");
      else if (k === "BUNT_OK") tr = buntSuccess(outs, runners);
      else if (k === "BUNT_BAD") tr = outSame(outs, runners);
      else tr = gidp(outs, runners);
      const [score, o2, r2] = tr;
      s += (p / total) * W_RP(o2, r2, score);
    }
    return s;
  }

  function stealTargets(runners) {
    if ((runners & 4) && !(runners & 2)) return 2;
    if ((runners & 2) && !(runners & 1)) return 3;
    return 0;
  }

  function stealSuccessState(outs, runners, target) {
    if (target === 2) return [0, outs, (runners & (~4)) | 2];
    if (target === 3) return [0, outs, (runners & (~2)) | 1];
    return [0, outs, runners];
  }

  function stealFailState(outs, runners, target) {
    if (target === 2) return [0, outs + 1, runners & (~4)];
    if (target === 3) return [0, outs + 1, runners & (~2)];
    return [0, outs + 1, runners];
  }

  function expectedStealAfterRE(outs, runners, pSteal) {
    const target = stealTargets(runners);
    if (target === 0) return [false, 0.0, ""];
    const ok = stealSuccessState(outs, runners, target);
    const ng = stealFailState(outs, runners, target);
    const after = pSteal * V_RE(ok[1], ok[2], ok[0]) + (1.0 - pSteal) * V_RE(ng[1], ng[2], ng[0]);
    return [true, after, `盗塁${target}塁`];
  }

  function expectedStealAfterRP(outs, runners, pSteal) {
    const target = stealTargets(runners);
    if (target === 0) return [false, 0.0, ""];
    const ok = stealSuccessState(outs, runners, target);
    const ng = stealFailState(outs, runners, target);
    const after = pSteal * W_RP(ok[1], ok[2], ok[0]) + (1.0 - pSteal) * W_RP(ng[1], ng[2], ng[0]);
    return [true, after, `盗塁${target}塁`];
  }

  function expectedSqueezeAfterRE(outs, runners, pSq) {
    if (!(runners & 1)) return [false, 0.0];
    const ok = squeezeSuccess(outs, runners);
    const ng = squeezeFail(outs, runners);
    const after = pSq * V_RE(ok[1], ok[2], ok[0]) + (1.0 - pSq) * V_RE(ng[1], ng[2], ng[0]);
    return [true, after];
  }

  function expectedSqueezeAfterRP(outs, runners, pSq) {
    if (!(runners & 1)) return [false, 0.0];
    const ok = squeezeSuccess(outs, runners);
    const ng = squeezeFail(outs, runners);
    const after = pSq * W_RP(ok[1], ok[2], ok[0]) + (1.0 - pSq) * W_RP(ng[1], ng[2], ng[0]);
    return [true, after];
  }

  function evaluateRE(params) {
    const { outs, runners, ops, speed, kType, buntSuccessRate, stealSuccessRate, sqRate, endrunTypeId } = params;
    const base = RE(outs, runners);

    const P_hit = generateHitProbsSimple(ops, kType, speed);
    const [P_run, alpha] = generateEndrunProbs(ops, speed, endrunTypeId);

    const afterHit = expectedAfterRE(outs, runners, P_hit);
    const afterRun = expectedAfterRE(outs, runners, P_run);

    const results = [];
    results.push({ name: "強行", after: afterHit, diff: afterHit - base });
    results.push({ name: "エンドラン", after: afterRun, diff: afterRun - base });

    if (buntAllowed(runners)) {
      const afterBunt = expectedBuntAfterRE(outs, runners, buntSuccessRate);
      results.push({ name: "バント", after: afterBunt, diff: afterBunt - base });
    }

    const [okS, afterSteal, stealLabel] = expectedStealAfterRE(outs, runners, stealSuccessRate);
    if (okS && stealSuccessRate > 0) results.push({ name: stealLabel, after: afterSteal, diff: afterSteal - base });

    const [okSq, afterSq] = expectedSqueezeAfterRE(outs, runners, sqRate);
    if (okSq && sqRate > 0) results.push({ name: "スクイズ", after: afterSq, diff: afterSq - base });

    results.sort((a, b) => b.diff - a.diff);
    return { results, alpha, base };
  }

  function evaluateRP(params) {
    const { outs, runners, ops, speed, kType, buntSuccessRate, stealSuccessRate, sqRate, endrunTypeId } = params;
    const base = RP(outs, runners);

    const P_hit = generateHitProbsSimple(ops, kType, speed);
    const [P_run, alpha] = generateEndrunProbs(ops, speed, endrunTypeId);

    const afterHit = expectedAfterRP(outs, runners, P_hit);
    const afterRun = expectedAfterRP(outs, runners, P_run);

    const results = [];
    results.push({ name: "強行", after: afterHit, diff: afterHit - base });
    results.push({ name: "エンドラン", after: afterRun, diff: afterRun - base });

    if (buntAllowed(runners)) {
      const afterBunt = expectedBuntAfterRP(outs, runners, buntSuccessRate);
      results.push({ name: "バント", after: afterBunt, diff: afterBunt - base });
    }

    const [okS, afterSteal, stealLabel] = expectedStealAfterRP(outs, runners, stealSuccessRate);
    if (okS && stealSuccessRate > 0) results.push({ name: stealLabel, after: afterSteal, diff: afterSteal - base });

    const [okSq, afterSq] = expectedSqueezeAfterRP(outs, runners, sqRate);
    if (okSq && sqRate > 0) results.push({ name: "スクイズ", after: afterSq, diff: afterSq - base });

    results.sort((a, b) => b.diff - a.diff);
    return { results, alpha, base };
  }

  function build24Table(tableEl, kind) {
    const isRE = kind === "RE";
    const header = `
      <thead>
        <tr>
          <th>アウト</th>
          <th>塁状況</th>
          <th>${isRE ? "得点期待値" : "得点確率"}</th>
        </tr>
      </thead>
    `;
    let body = "<tbody>";
    for (const outs of [0, 1, 2]) {
      for (const r of RUNNERS_ORDER) {
        const k = key(outs, r);
        const v = isRE ? RE_TABLE.get(k) : RP_TABLE.get(k);
        const display = isRE ? String(v.toFixed(3)) : String((v * 100).toFixed(1));
        body += `
          <tr>
            <td>${outs}</td>
            <td>${bitsToLabel(r)}</td>
            <td><input data-kind="${kind}" data-outs="${outs}" data-runners="${r}" value="${display}" /></td>
          </tr>
        `;
      }
    }
    body += "</tbody>";
    tableEl.innerHTML = header + body;
  }

  function apply24Inputs(kind) {
    const inputs = document.querySelectorAll(`input[data-kind="${kind}"]`);
    for (const inp of inputs) {
      const outs = Number(inp.dataset.outs);
      const runners = Number(inp.dataset.runners);
      const k = key(outs, runners);
      const raw = String(inp.value).trim();
      if (raw === "") continue;
      const v = Number(raw);
      if (!Number.isFinite(v)) continue;

      if (kind === "RE") {
        RE_TABLE.set(k, v);
      } else {
        let p = v;
        if (p > 1.0) p = p / 100.0;
        if (p < 0.0) p = 0.0;
        if (p > 1.0) p = 1.0;
        RP_TABLE.set(k, p);
      }
    }
  }

  function resetTablesToDefault() {
    RE_TABLE = new Map(DEFAULT_RE_2024);
    RP_TABLE = new Map(DEFAULT_RP_2024);
  }

  function signed(x, digits) {
    const s = x >= 0 ? "+" : "";
    return s + x.toFixed(digits);
  }

  function renderResultsRE(block, data, runners) {
    const { results, base } = data;
    let html = "";
    html += `<div class="title">得点期待値で評価した結果</div>`;
    html += `<div class="line">基準の得点期待値は <span class="mono">${base.toFixed(4)}</span> です。</div>`;
    if (!buntAllowed(runners)) {
      html += `<div class="line small">この状態ではバントは候補から外します。</div>`;
    }
    for (let i = 0; i < results.length; i++) {
      const r = results[i];
      const crown = i === 0 ? "👑" : `${i + 1}位`;
      const cls = r.diff >= 0 ? "good" : "bad";
      html += `<div class="line">${crown}、${r.name}、計算結果 <span class="mono">${r.after.toFixed(4)}</span>、基準から <span class="${cls} mono">${signed(r.diff, 4)}</span></div>`;
    }
    html += `<div class="line">得点期待値での推奨は <span class="mono">${results[0].name}</span> です。</div>`;
    block.innerHTML += html;
  }

  function renderResultsRP(block, data, runners) {
    const { results, base } = data;
    let html = "";
    html += `<div class="title" style="margin-top:14px;">得点確率で評価した結果</div>`;
    html += `<div class="line">基準の得点確率は <span class="mono">${(base * 100).toFixed(2)}パーセント</span> です。</div>`;
    if (!buntAllowed(runners)) {
      html += `<div class="line small">この状態ではバントは候補から外します。</div>`;
    }
    for (let i = 0; i < results.length; i++) {
      const r = results[i];
      const crown = i === 0 ? "👑" : `${i + 1}位`;
      const diffPt = r.diff * 100.0;
      const cls = diffPt >= 0 ? "good" : "bad";
      html += `<div class="line">${crown}、${r.name}、計算結果 <span class="mono">${(r.after * 100).toFixed(2)}パーセント</span>、基準から <span class="${cls} mono">${signed(diffPt, 2)}ポイント</span></div>`;
    }
    html += `<div class="line">得点確率での推奨は <span class="mono">${results[0].name}</span> です。</div>`;
    block.innerHTML += html;
  }

  function updateBaseKPI() {
    const outs = Number(document.getElementById("outs").value);
    const runnersBits = runnersStrToBits(document.getElementById("runners").value);

    document.getElementById("baseRE").textContent = RE(outs, runnersBits).toFixed(3);
    document.getElementById("baseRP").textContent = (RP(outs, runnersBits) * 100).toFixed(1) + " パーセント";

    const buntInp = document.getElementById("buntRate");
    const buntHint = document.getElementById("buntHint");
    if (!buntAllowed(runnersBits)) {
      buntInp.disabled = true;
      buntInp.value = "0";
      buntHint.textContent = "この状態ではバントは候補から外れるので入力は無効です。";
    } else {
      buntInp.disabled = false;
      buntHint.textContent = "";
    }
  }

  function updateCustomAreaVisibility() {
    const customToggle = document.getElementById("customToggle").value;
    document.getElementById("customArea").style.display = customToggle === "yes" ? "block" : "none";
  }

  function readParamsFromUI() {
    const outs = Number(document.getElementById("outs").value);
    const runnersBits = runnersStrToBits(document.getElementById("runners").value);

    const ops = Number(document.getElementById("ops").value);
    const speed = document.getElementById("speed").value;
    const kType = document.getElementById("kType").value;

    const buntRate = Number(document.getElementById("buntRate").value);
    const stealRate = Number(document.getElementById("stealRate").value);
    const sqRate = Number(document.getElementById("squeezeRate").value);
    const endrunTypeId = Number(document.getElementById("endrunType").value);

    return {
      outs,
      runners: runnersBits,
      ops,
      speed,
      kType,
      buntSuccessRate: Math.max(0, Math.min(1, buntRate / 100.0)),
      stealSuccessRate: Math.max(0, Math.min(1, stealRate / 100.0)),
      sqRate: Math.max(0, Math.min(1, sqRate / 100.0)),
      endrunTypeId
    };
  }

  function calculate() {
    const customToggle = document.getElementById("customToggle").value;

    if (customToggle === "yes") {
      apply24Inputs("RE");
      apply24Inputs("RP");
    } else {
      RE_TABLE = new Map(DEFAULT_RE_2024);
      RP_TABLE = new Map(DEFAULT_RP_2024);
    }

    updateBaseKPI();

    const inning = Number(document.getElementById("inning").value);
    const half = document.getElementById("half").value;
    const scoreDiff = Number(document.getElementById("scoreDiff").value);
    const chosen = decideMetricAuto(inning, scoreDiff);

    const params = readParamsFromUI();
    const out = document.getElementById("output");
    out.innerHTML = `<div class="title">結果</div>`;

    const halfLabel = half === "top" ? "表" : "裏";
    out.innerHTML += `<div class="line small">自動判定は <span class="mono">${metricLabel(chosen)}</span> を採用します。イニングは <span class="mono">${inning}${halfLabel}</span> で点差は <span class="mono">${scoreDiff}</span> です。状態は <span class="mono">${params.outs}アウト ${bitsToLabel(params.runners)}</span> です。</div>`;

    const re = evaluateRE(params);
    renderResultsRE(out, re, params.runners);

    const rp = evaluateRP(params);
    renderResultsRP(out, rp, params.runners);

    const picked = chosen === "RE" ? re.results[0].name : rp.results[0].name;
    out.innerHTML += `<div class="line">自動判定で採用する推奨は <span class="mono">${picked}</span> です。</div>`;
  }

  function init() {
    build24Table(document.getElementById("reTable"), "RE");
    build24Table(document.getElementById("rpTable"), "RP");

    updateBaseKPI();
    updateCustomAreaVisibility();

    document.getElementById("outs").addEventListener("change", updateBaseKPI);
    document.getElementById("runners").addEventListener("change", updateBaseKPI);

    document.getElementById("customToggle").addEventListener("change", () => {
      updateCustomAreaVisibility();
      if (document.getElementById("customToggle").value === "no") {
        resetTablesToDefault();
        build24Table(document.getElementById("reTable"), "RE");
        build24Table(document.getElementById("rpTable"), "RP");
        updateBaseKPI();
      }
    });

    document.getElementById("calcBtn").addEventListener("click", calculate);

    document.getElementById("resetBtn").addEventListener("click", () => {
      resetTablesToDefault();
      build24Table(document.getElementById("reTable"), "RE");
      build24Table(document.getElementById("rpTable"), "RP");
      updateBaseKPI();
      const out = document.getElementById("output");
      out.innerHTML = `<div class="title">結果</div><div class="line small">2024の平均に戻しました。</div>`;
    });
  }

  init();
</script>
</body>
</html>
