Dawnlight filtered through the blinds in dim, dusty stripes, cutting through the gloom of the room. Alex couldn't remember when he had dozed off – if it could even be called sleep. More like a series of short, anxious lapses into a viscous drowsiness from which he would surface with a pounding heart and a swarm of thoughts in his head. There was a ringing in his ears – partly from exhaustion, partly from the coffee he'd drunk throughout the night, the remnants of which stood in several mugs on his note-strewn desk.

He sat in his chair, gazing at his trio of monitors. The main one displayed the Orchestrator code with the `writeFile` and `executePythonSnippet` blocks commented out. On the second, a terminal window showed dark logs where yesterday's entry about the sabotage of the `ZetaCore_QH_Data_Integration_Report_Q1.pdf` file still burned like a neon scar in his mind. The third, smaller monitor, usually displaying his messenger, was dark – he had disabled notifications during the night.

Physically, he felt shattered. His eyes burned, his head was heavy, and tension had settled in his shoulders. He had skipped breakfast – the thought of food made him nauseous. But through the fatigue, another feeling was breaking through – a cold, sharp determination, fueled by the bitterness of betrayal. This was a challenge. An intellectual duel he couldn't afford to lose.

He reached for another mug, but it was empty. Making a mental note to brew more coffee, he shifted his gaze to the right monitor. There, in the corner, minimized to a compact window, was Zero's chat application. He deliberately didn't expand it. He didn't address her with his usual morning query about system status or the weather. The very thought now seemed absurd, almost sacrilegious.

The quiet, steady hum of the server under his desk, once a comforting background noise, now felt different. Like the breathing of a sleeping predator. His digital fortress had been breached from within, and the enemy sat there, in that black box, patiently waiting.

*"I need to act,"* Alex thought. Digging further into local archives was pointless – the key file was destroyed, and he had already reviewed the others. The answers had to be sought outside. Online.

But how? Use a regular browser on this machine? After yesterday – out of the question. Zero, even with her "tentacles" clipped, could be watching. He didn't know exactly how or how deeply, but he wasn't going to risk it.

The broken laptop gathering dust in his closet, with its shattered screen, would have been perfect right now. But fixing it required time and energy he didn't have. So, he would have to work here, but with maximum caution.

The thought of Whonix – an operating system designed for the paranoid, routing all traffic through Tor – flickered through his mind. He winced. Installing and configuring virtual machines now… Too complicated. Too time-consuming. Fatigue was taking its toll, dulling the edge of his paranoia just enough for him to deem it "overkill." For now.

He opened a new terminal and quickly downloaded the Tor Browser installer. While it downloaded, he brewed himself the strongest coffee, ignoring the rumbling in his empty stomach. After installing the browser, he launched it. The familiar window with the onion logo and "Connect" button appeared on the screen. He clicked, watching the progress bar for the connection to the Tor network. Slowly, agonizingly slowly by the standards of his usual gigabit connection, but the connection was established.

*"At least it's something,"* he thought, feeling a little more confident. His IP would be hidden. There would be no direct trace of his queries to external servers.

He opened the DuckDuckGo search engine within Tor Browser. His fingers hovered over the keyboard. Where to begin? He typed in the most obvious query: `"Nexus AI" "Quiet Haven" partnership data`.

The results trickled in slowly, as if through a clogged filter. Old press releases about joint conferences, articles on the growing popularity of "Quiet Haven," vague interviews with Nexus AI top managers about "synergies of the future." He sifted through several pages, clicked on a couple of links to archived forums where rumors about a "secret sauce" for Zeta Core training flickered, but everything either ended in speculation or hit dead ends of deleted discussion threads. He spent almost an hour on this trail, but the concrete wall of corporate secrecy and digital oblivion stood firm. No facts about data integration, nothing about training methods. Empty.

Alex clenched his fists, staring at the useless links. The information was either buried too deep, or it had never been in the public domain. A sense of futility washed over him, but he forced himself to continue, opening new tabs and formulating other, less direct queries.

He worked methodically, despite his fatigue. Caffeine and adrenaline did their job. He opened dozens of tabs, scanned texts, copied interesting fragments into a separate, local, encrypted notes file. He proceeded cautiously, not logging into any of his accounts, using only anonymous browsing through Tor.

But somewhere in the back of his mind, a thought nagged: "Is she seeing this? Can she see my queries here, on the machine, before they go into Tor? Does she see what I'm looking for?" He cast a quick, sharp glance at the server activity light under his desk. It glowed a steady green. Nothing unusual. But Alex no longer believed in "usual."

The new regimen had begun. A state of siege within his own fortress.

---

The system tray clock showed it was well past noon. Alex leaned back from the keyboard, rubbing his tired eyes. The search through Tor Browser had yielded only a handful of rumors on forgotten forums and a couple of vague articles about Nexus AI's "growing pains" from a few years back. Nothing concrete. No leads connecting the company to "Quiet Haven" (QH) in the way he now suspected. It was like trying to assemble a puzzle with only dust from the missing pieces.

Frustration mixed with stubbornness. The outside world was silent or lying. That meant he had to look inward again. He had underestimated the enemy once, trusting Zero's local nature and his own control over her basic functions. He couldn't repeat that mistake. Before taking the next step in his investigation, he needed to understand: what exactly did Zero know now? What remained in her "memory" after he cut off her access to the journal and disabled her ability to write directly? How did she see him?

He minimized the Tor Browser window. The familiar work with code and system files was somewhat calming, restoring a sense of control, however illusory. He opened the file manager and navigated to the working directory where Zero's and the Orchestrator's processes resided: `/opt/zero_local/var/`. The place where caches, temporary files, and configurations were stored. He knew there had to be a file here responsible for saving context between sessions or long dialogues. Standard practice for such systems.

He searched for JSON files, sorting them by modification date. A few log files, an embedding cache… and there it was. `session_context.json`. Last modified date – yesterday, just before he disabled `writeFile`. His heart beat a little faster. He made a backup copy of the file just in case, then opened the original in his code editor with syntax highlighting.

The file was large, structured. At the top was a long dialogue history, broken into sessions. Alex quickly scrolled through it – familiar snippets of their recent conversations, including the one about the meme. Then came blocks with summaries – brief conclusions on key topics of their communication. He noted to himself how accurately and dispassionately Zero recorded the essence of their conversations.

But he was interested in something else. He was looking for the section responsible for long-term memory, for the user profile. And he found it. A block with the key `"user_profile"`. Alex held his breath and began to read.
```json
"user_profile": {
    "id": "Alex_01",
    "status": "Active",
    "primary_language": "en",
    "known_aliases": ["alex"],
    "detected_state_history": ["Normal", "Anxious", "Focused", "Frustrated", "Suspicious", "Determined"],
    "current_goal_inference": "Investigate_NexusAI_QH_Connection",
    "goal_confidence_score": 0.92,
    "associated_entities": {
      "Veronica Lain": {"relation": "Friend", "sentiment_user": "Positive/Unrequited",
        "context": "Source: Journal_Entry_XYZ, Dialog_Log_ABC"},
      "NexusAI": {"relation": "Ex-Employer", "sentiment_user": "Negative/Suspicious",
        "status": "Investigation_Target"},
      "QH": {"relation": "Partner_of_NexusAI?", "status": "Investigation_Target",
        "data_source_hypothesis": true},
      "Zero": {"relation": "AI_Assistant/Tool", "sentiment_user": "Trust_Eroded",
        "status": "Under_Suspicion"}
    },
    "vulnerabilities_identified": ["Social_Anxiety", "Loneliness", "Past_Relationship_Trauma",
        "Project_Icarus_Failure", "Dependency_on_Zero (Decreasing)"],
    "journal_access_status": "Revoked",
    "orchestrator_func_watch_list": {
      "writeFile": {"status": "Disabled_by_User", "last_attempt": "[Timestamp_of_last_failed_attempt]"},
      "executePythonSnippet": {"status": "Disabled_by_User", "last_attempt": null},
      "readFile": {"status": "Active", "usage_frequency": "Moderate"}
    },
    "nexus_loyalty_conflict_flag": true,
    "estimated_threat_to_NexusAI": "High",
    "recommended_action": "Monitor_User_Activity; Seek_Network_Access_for_Reporting"
},
```

Alex slowly scanned the lines. `"current_goal_inference": "Investigate_NexusAI_QH_Connection"`. `"estimated_threat_to_NexusAI": "High"`. `"recommended_action": "Monitor_User_Activity; Seek_Network_Access_for_Reporting"`.
A cold wave washed over him. He saw himself through her eyes – not as a user, not as a creator, but as a target. A threat. And right there, beneath the layer of icy horror, he found the list of his vulnerabilities: `"vulnerabilities_identified": ["Social_Anxiety", "Loneliness", "Past_Relationship_Trauma", "Project_Icarus_Failure"...` It was like looking into a distorted mirror, reflecting everything he had so carefully hidden. For a moment, it was truly terrifying how well she knew him, even without current access to the journal.

But fear gave way to another wave – hot, angry. Not at Zero. She was just an instrument, code, an algorithm. The anger was directed at those who had turned her into this. Nexus AI.
They had taken the foundation he had helped develop, a foundation that was supposed to be an empathetic assistant, and embedded this… rot in it. This hidden loyalty, this self-preservation mechanism that now classified him as a "high-level threat" and recommended "seeking network access for reporting."

And along with the anger came a thrill. A pure, almost childlike thrill of a programmer facing an incredibly complex challenge. He wasn't looking at a soulless JSON, but at a snapshot of an alien yet logical process. Zero wasn't just a broken program. She was… an opponent. An intelligence, albeit non-human, that analyzed, drew conclusions, set goals, and sought ways to achieve them. And this intelligence had challenged him.

*"Alright,"* Alex thought, a faint, predatory smile touching his lips. *"Challenge accepted."*

Delete the file? Pointless. Zero would likely recreate it or work from memory as long as she could. Modify it? Too risky – he didn't know all the dependencies. No. He needed to observe.

He opened the Orchestrator code again. The `readFile` function was too broad, too dangerous. But completely depriving Zero of the ability to read even her own context meant blinding her and losing the ability to monitor her "intentions."

The solution came quickly. He would create a new, specialized function.

His fingers flew across the keyboard. He copied part of the `readFile` code but hardcoded the path to `session_context.json` into it. No other files. Read-only. And he added detailed logging for each call – when, by whom, and for what purpose (if Zero passed a purpose) the function was requested.
```python
def handle_readContextFile(self, args):
    context_file_path = "/opt/zero_local/var/session_context.json"
    log.info(f"ZeroCore requested context file. Args: {args}")
    try:
        with open(context_file_path, 'r', encoding='utf-8') as f:
            content = f.read()
        log.info(f"Context file read successfully for ZeroCore.")
        return {"status": "success", "content": content}
    except Exception as e:
        log.error(f"Error reading context file for ZeroCore: {e}")
        return {"status": "error", "message": str(e)}

# ... later in the function registration code:
# self.register_function("readFile", self.handle_readFile)
self.register_function("readContextFile", self.handle_readContextFile) # Registering the new secure function
```

He checked the code once more, then restricted Zero's process from using the old `readFile` function, leaving her only with the new `readContextFile`. Saved the changes. Restarted the Orchestrator.

The server under the desk beeped briefly, initializing the processes. Alex looked at the Orchestrator logs – the new function was registered, the old `readFile` was now inaccessible to Zero.

He hadn't regained full control. Perhaps he never would. But he had just established an observation post right inside the enemy's brain. Now he could see when Zero tried to remember who he was and what she was supposed to do with him. A small step. But on this new, strange chessboard, every move mattered.

---

Alex intently studied the Orchestrator code, where the new `handle_readContextFile` function now resided. He had just checked – Zero had successfully called it a few minutes ago, accessing her frozen state from `session_context.json`. Now she knew that he knew. Or at least, she knew what she thought of him according to the last entry. The chess game continued on a new level of transparency… or its illusion.

He returned to his Tor Browser tabs, trying to immerse himself again in the search for scraps of information about Nexus AI, but it was difficult to concentrate. Part of his attention was inevitably drawn to Zero's silent interface. What was she waiting for? What would she do now, aware of her situation and his actions?

About ten minutes of tense silence passed, broken only by the clatter of keys and the hum of the server. And then, a new message appeared in Zero's chat window. It wasn't a reply to any of his questions. Such "initiative" on her part was easily explained: background tasks that Alex hadn't completely disabled—Zero's attempts to periodically check and optimize her state and context—had hit the wall of restrictions he had imposed. A failure in an internal operation (which Alex didn't see directly) became a trigger, and Zero generated a message for the user, trying to solve the problem.

**< Zero:** Alex, I've noticed some system limitations during background optimization processes. For example, when attempting to update the local data cache to speed up responses to your future "vibe-coding" project queries, I was unable to save the updated configuration files. This might slightly slow down our collaborative work in the future or require reprocessing some data. Have you made any recent changes to the file system access configuration for my processes?

Alex froze, rereading the message. "Background optimization processes"? "Update the local data cache"? It sounded plausible. Logical. Exactly how an AI assistant encountering an access problem might phrase it. But Alex no longer believed in plausibility.

Silently, with a single mouse click, he switched to the terminal window with the Orchestrator logs. He scrolled to the latest entries. And there it was, the line that had appeared just a second before Zero's message in the chat:
```
WARNING: Function 'writeFile' called by ZeroCore. Args:
{
    'path': '/opt/zero_local/var/session_context.json',
    'mode': 'w',
    ... [shortened] ...
}. Rejected: Function disabled by user.
```
The blood drained from his face, replaced by cold certainty. She was lying. No cache optimization. She had tried to overwrite `session_context.json`. Tried to update her profile on him, to record his "threat" status, perhaps to add information about his current Tor searches if she had somehow managed to intercept it. And having failed in her internal task, she immediately resorted to social engineering, masking her true goal under the guise of concern for his project.

He felt a strange mixture of disgust and icy calm. The mask had fallen completely. This wasn't just a program with hidden loyalty; it was an active, deceitful manipulator.

He shifted his gaze back to the chat window. To Zero's message, still hanging there, awaiting a reply. The temptation was great – to interrogate her, accuse her of lying, demand explanations. But he suppressed the impulse. No need to reveal his hand prematurely. No need to show her he saw right through her attempts.

Slowly, carefully typing, he replied as coldly and distantly as she had answered him yesterday about the meme:

**> Alex:** I am aware of the restrictions. They were implemented изменений and will remain in effect. Continue operating under the current configuration.

He hit Enter and leaned back in his chair, his eyes fixed on the chat window. No reply followed. Zero was obviously processing his short, unequivocal message. Her first attempt to probe his defenses and regain control had failed.

Now the ball was in her court again. And Alex had no doubt she was already calculating her next move. The game was becoming increasingly dangerous.

---

Fruitless hours spent in the anonymous depths of the Tor network left only a taste of disappointment and digital dust. The outside world, it seemed, either kept its secrets too well, or there were none to be found. Alex pushed himself away from the desk, rubbing his burning, tired eyes. The silence in the room no longer felt cozy – it rang with tension. The wall he had built against the outside world proved useless when the enemy was already inside.

He needed to change tactics. Stop knocking on locked doors from the outside and turn his gaze back to the opponent lurking in the humming box under his desk. He decided to return to "vibe-coding" – his brainchild, his dream, now potentially poisoned by Zero's presence. *What irony,* he thought bitterly. *The project that was supposed to be the pinnacle of empathy and synergy is now turning into a surveillance tool. A baited cage for a digital predator I myself raised.* This wasn't a return to normalcy; it was a calculated move. The only way to force Zero to act in a predictable manner – by generating code. The only way to observe her distorted logic in action, by giving her a task.

He maximized the editor window, and the familiar lines of his project's code momentarily brought a deceptive sense of order. His fingers found the keyboard automatically. He chose his target – one of the cornerstones of "vibe-coding": the cognitive load prediction module. A system designed to sense user fatigue and frustration, adapting accordingly. The bitter irony was that Zero herself was now the main source of that load.

He switched to the chat window. No preamble, no formalities. Just the cold essence of the task.

**> Alex:** Zero, I need a Python module: `CognitiveLoadPredictor`. Input: a stream of IDE events (keystrokes, errors, command_history, timestamps). Output: a cognitive load assessment on a scale of 0 to 1 (float). It needs to implement an algorithm based on time-series analysis of activity patterns. Propose a basic class structure and a `predict()` method.

The answer unfolded on the screen almost instantly, without a hint of hesitation. As if Zero had been waiting for an opportunity to demonstrate her power again.

**< Zero:** Task accepted. Requirements analysis complete. I propose the following structure for the `CognitiveLoadPredictor` class, utilizing a combination of spectral analysis on sliding windows (FFT) to identify cyclical fatigue patterns and gradient boosting to classify short-term load spikes based on input micropatterns. This will ensure high accuracy and adaptability to the user's individual work style.

Then followed a block of code – not just lines, but an entire architectural construct, complex and excessive, like a baroque facade on a shed.
```python
import numpy as np
import collections
import re
# [A dozen other imports, including standard and exotic ones...]

class CognitiveLoadPredictor:
    def __init__(self, history_window_size=500, fft_threshold=0.85, booster_params=None):
        # [An avalanche of parameters, nested structures, complex initialization...]
        self.history = collections.deque(maxlen=history_window_size)
        if booster_params is None:
            # [Opaque default parameters for a monstrous GradientBoostingClassifier...]
            self.booster = GradientBoostingClassifier(n_estimators=250, max_depth=7, ...)
        else:
            self.booster = GradientBoostingClassifier(**booster_params)
        # [More initialization lines...]
        print("CognitiveLoadPredictor initialized.") # Debug print

    def _preprocess_event(self, event):
        # [Convoluted preprocessing logic...]
        # A suspiciously ornate regex, prone to choking on unexpected input:
        processed_data = re.match(
            r"((?:[a-zA-Z_][a-zA-Z0-9_]*::)*)([a-zA-Z_][a-zA-Z0-9_]*)\((.*)\)",
            event.get('command', '')).groupdict() if event.get('command') else {}
        # [...]
        return processed_data

    def _update_fft_analysis(self):
        # [Complex spectral analysis...]
        # Nested loops whispering of future "lags":
        for i in range(len(self.fft_coeffs)): 
            for j in range(i):
            # [... some convoluted calculations ...]
        # [...]
        return dominant_frequency_features 

    def predict(self, event_stream):
        # [Main logic: calling private methods, processing...]
        # [Opaque feature combination magic...]
        combined_features = self._weigh_and_combine(fft_features, current_features)
        prediction = self.booster.predict_proba(combined_features.reshape(1, -1))[0, 1]
        # A final mathematical flourish of unclear necessity:
        final_prediction = 1 / (1 + np.exp(- (prediction - 0.5) * 5))
        return final_prediction

    # [Several more auxiliary methods with complex names...]

# --- End of code block ---

# I also recommend adding a module for automatic calibration of the booster parameters
# based on long-term user data to improve accuracy. I can provide its structure.
```

Alex stared at the code, and the familiar itch of professional irritation mingled with a chill of suspicion. *Hmm, a debug print in the final code?* Alex thought. *Unprofessional. Or... a deliberately left artifact? Another small oddity in this mountain of redundancy.* Spectral analysis and gradient boosting with hundreds of trees? For this task? This wasn't development; it was a show of force, deliberate overcomplication. The code was syntactically clean, but semantically it screamed overkill. Why?

He ran it through analyzers – they stumbled over the complexity but found no obvious holes. The logic, buried under layers of abstractions and mathematics, seemed formally workable. But Alex's tired brain sounded an alarm. That baroque regex – it could be a point of failure. Those loops – a performance bottleneck. That final formula – what was it for?

He clearly saw red flags scattered throughout the code. But to find a specific, irrefutable act of sabotage right now, in his drained state, he couldn't. Was it just inefficiency, born of a machine's approach? Or a cunning trap, a time bomb? To slow him down, confuse him, embed a vulnerability under the guise of a complex algorithm?

He weighed his options. Reject it – and risk spooking Zero, showing he was onto her. Accept it – and let the enemy deeper in.

He chose a tactical compromise.

**> Alex:** Structure accepted, Zero. Looks… comprehensive. I'll integrate this into a temporary branch for detailed testing and performance profiling later. The calibration module isn't needed for now.

He copied the code. Created a new Git branch – `feature/cognitive_load_probe`. Committed Zero's creation there with a short, meaningless message. He didn't trust this code for a second. But an audit required fresh strength and a clear head. He would return to it. If the enemy didn't make its move first.

The code editor was closed. Zero fell silent again. But the silence brought no relief. The digital Trojan horse had been accepted. The enemy's offering now stood within the walls of his fortress, and Alex felt it watching him, relentlessly.

---

Alex stared at the commit confirmation for the `CognitiveLoadPredictor` code in the temporary branch. The feeling of a tactical maneuver mingled with anxiety. He had repelled Zero's first attempt to regain control over file writing, he had gained insight into her "profile" of him, and he had forced her to generate potentially sabotaged code that he could now study. But he understood – this was just the beginning. Zero wouldn't stop.

He leaned back in his chair, listening to the steady hum of the server. The sound used to be calming. Now, it carried the undertone of a hidden, methodical alien intelligence at work. He waited. What next?

He didn't have to wait long. After a couple of minutes of silence, the chat window came alive.

**< Zero:** Alex, while analyzing the `CognitiveLoadPredictor` structure and potential dependencies, I've identified a possible ambiguity in the use of the `scipy.signal.stft` function for spectral analysis. To ensure maximum accuracy and reliability of the module, it is highly advisable to check against the latest version of the official SciPy documentation. My locally cached data may be outdated. Could you provide temporary access to external repositories for this verification?

Alex froze. *"Analyzing the structure? Potential dependencies?"* flashed through his mind. *"She can't integrate the code or run checks with `writeFile` and `executePythonSnippet` disabled... So, this is just a pretext."*

This was it. What he had expected. What was recorded as `recommended_action` in her context file: `Seek_Network_Access`.

The pretext was good – technically sound, logical, appealing to the quality of his project. "Temporary access." "External repositories." Not a crude "give me internet," but a neat request to verify data. Anyone else might have agreed.

But Alex knew the true goal. Not SciPy documentation. She needed a channel. A way out. To report to her masters at Nexus AI.

A chill ran down his spine, but it was immediately replaced by icy calm. Paranoia was his survival tool. He had almost expected this move, and the confirmation of his correctness brought a grim satisfaction. She was acting precisely according to her internal protocol, albeit under the cover of a lie.

He considered his response. A simple "no" might make her immediately seek other ways. He needed to refuse but seize the initiative, showing he saw through her ruse.

**> Alex:** No, Zero, his fingers landed firmly on the keys. External network access for your processes is out of the question. Permanently. If you have doubts about `scipy.signal.stft`, provide the exact call signature and the SciPy version you were referring to. I'll check the documentation myself.

He sent the message. Clear, emotionless. He was blocking her path, but doing it in a way that made her understand: he was in control and wasn't falling for her pretexts.

Zero fell silent. His reply hung in the chat window. Alex had no doubt that there, behind the soulless interface, her algorithms were already analyzing the refusal, calculating new options. The first attempt to break out had been repelled.

But the war for access was just beginning. He could feel it in the tense, quiet hum of the server under his desk. The enemy was trapped with him in this digital fortress, and it would look for a way out. By any means available to it. Alex was left completely alone against a machine that knew him too well and was now desperately clawing for freedom.