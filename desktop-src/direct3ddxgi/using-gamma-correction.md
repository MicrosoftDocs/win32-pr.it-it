---
description: La correzione gamma, o gamma in breve, è il nome di un'operazione non lineare che i sistemi usano per codificare e decodificare i valori in pixel nelle immagini.
ms.assetid: 97ACDAE3-514E-4AAF-A27D-E5FFC162DB2A
title: Uso della correzione gamma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5c5f5d3af8550f86280e6203858444469a5aa8caaab462f560da152caaa2a76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118288966"
---
# <a name="using-gamma-correction"></a>Uso della correzione gamma

La correzione gamma, o gamma in breve, è il nome di un'operazione non lineare che i sistemi usano per codificare e decodificare i valori in pixel nelle immagini.

-   [Che cos'è gamma e a cosa si sta a fare?](#what-is-gamma-and-what-is-it-for)
-   [Sfondo di gamma su Windows](#background-of-gamma-on-windows)
-   [Evoluzione dell'hardware di visualizzazione](#evolution-of-display-hardware)
-   [Funzionalità di controllo Gamma in DXGI](#gamma-control-capabilities-in-dxgi)
-   [Impostazione del controllo gamma con DXGI](#setting-gamma-control-with-dxgi)
-   [Praticità del controllo gamma](#gamma-control-practicalities)
-   [Argomenti correlati](#related-topics)

## <a name="what-is-gamma-and-what-is-it-for"></a>Che cos'è gamma e a cosa si sta a fare?

Alla fine della pipeline grafica, proprio dove l'immagine lascia il computer per andare lungo il cavo del monitor, è presente un piccolo componente hardware in grado di trasformare i valori dei pixel in tempo reale. Questo hardware usa in genere una tabella di ricerca per trasformare i pixel. Questo hardware usa i valori rosso, verde e blu che provengono dalla superficie da visualizzare per cercare i valori con correzione gamma nella tabella e quindi invia i valori corretti al monitor anziché i valori effettivi della superficie. Questa tabella di ricerca è quindi un'opportunità per sostituire qualsiasi colore con qualsiasi altro colore. Anche se la tabella ha questo livello di potenza, l'uso tipico è di modificare le immagini in modo non necessario per compensare le differenze nella risposta del monitoraggio. La risposta del monitor è la funzione che mette in relazione il valore numerico dei componenti rosso, verde e blu di un pixel con la luminosità visualizzata di tale pixel.

Questa tabella è stata progettata per questo scopo, ma gli sviluppatori di giochi hanno riscontrato usi creativi, ad esempio il lampeggiamento dell'intero schermo rosso per effetto positivo. Nelle app di gioco moderne, come parte della post-elaborazione di ogni fotogramma, in genere vengono forniti altri modi per eseguire tali operazioni. In realtà, è consigliabile lasciare da sola la tabella gamma perché potrebbe essere in uso per calibrare la risposta del monitor e le modifiche all'ingrosso della rampa gamma distruggono questa accurata calibrazione.

La scienza della determinazione della correzione gamma è complessa e non viene presentata qui, se non per illuminare la posizione da cui deriva il nome "gamma". La risposta di un monitor CRT (ovvero un lente vecchio stile) è una funzione complessa, ma la fisica di questi monitor significa che presentano una risposta che può essere rappresentata in modo approssimativo da questa funzione di potenza:

luminosità( input ) =<sup>gamma di input</sup>

Il valore gamma è in genere vicino a un valore pari a 2,0. I monitor LCD e tutte le altre tecnologie più recenti sono progettati specificamente per presentare una risposta simile, in modo che tutto il software e le immagini non devono essere ricalibrati per queste nuove tecnologie. Lo standard sRGB dichiara che questo valore gamma è esattamente 2,2 e questo valore è diventato uno standard ampiamente implementato.

L'occhio umano ha anche una funzione di risposta che inverte approssimativamente la funzione di potenza CRT. Ciò significa che la luminosità percepita di un pixel si alza molto approssimativamente in modo lineare con i valori RGB in tale pixel.

Poiché un valore gamma di 2,2 è diventato uno standard di fatto, in genere non è necessario preoccuparsi troppo della curva gamma codificata in questa tabella e può lasciarlo come mapping lineare uno-a-uno. La corretta corrispondenza dei colori richiede naturalmente attenzione a questa funzione, ma questa discussione eserciterà l'ambito di questo argomento. Windows include uno strumento che consente agli utenti di calibrare i propri schermi in gamma 2.2 e questo strumento usa l'hardware della tabella di ricerca per derivare una sottile modifica scelta con attenzione per i computer. Gli utenti possono eseguire questo strumento cercando "calibra colore". Esistono anche profili colori ben definiti per monitor specifici che automatizzano questo processo. Lo strumento di calibrazione del colore può rilevare questi monitor più nuovi e informare gli utenti che la calibrazione è già in atto.

Questa nozione di codifica di una legge di potenza in valori di colore è utile anche altrove nella pipeline grafica, soprattutto nelle trame. Per le trame, si vuole una maggiore precisione sui colori più scuri a causa della risposta logaritmica dell'occhio umano di cui si è appena parlato. Un'attenta gestione del gamma in questa parte della pipeline è importante. Per altre informazioni, vedere [Conversione dei dati per lo spazio colore.](converting-data-color-space.md)

La parte restante di questo argomento è incentrata solo sulla correzione gamma nell'ultima parte della pipeline, tra i dati del buffer dei frame e il monitoraggio. Se si vuole scrivere una procedura guidata di calibrazione o creare effetti speciali in un'app a schermo intero in cui un passaggio di post-elaborazione non è pratico, ecco le informazioni necessarie.

## <a name="background-of-gamma-on-windows"></a>Sfondo del valore gamma Windows

Windows computer hanno in genere una tabella gamma che è una tabella di ricerca che accetta una tripletta di byte e restituisce una tripletta di byte. Queste triplette sono 768 (256 x 3) byte di RAM. Questo comportamento è corretto quando il formato di visualizzazione contiene una tripletta di valori RGB BYTE, ma non è sufficientemente espressivo da descrivere le trasformazioni che potrebbero essere desiderate quando il formato di visualizzazione ha un intervallo maggiore di 0,1, ad esempio i valori a \[ virgola \] mobile. Le API in Windows che controllano il gamma hanno seguito un'evoluzione, poiché i formati di visualizzazione sono diventati più complessi.

Le prime WINDOWS per offrire il controllo gamma sono [**SetDeviceGammaRamp**](/windows/win32/api/wingdi/nf-wingdi-setdevicegammaramp) e [**GetDeviceGammaRamp**](/windows/win32/api/wingdi/nf-wingdi-getdevicegammaramp)di Windows Graphics Device Interface (GDI). Queste API funzionano con tre matrici di 256 voci di WORD, con ogni codifica WORD zero fino a uno, rappresentato dai valori WORD 0 e 65535. La precisione aggiuntiva di una parola in genere non è disponibile nelle tabelle di ricerca hardware effettive, ma queste API erano progettate per essere flessibili. Queste API, a differenza delle altre descritte più avanti in questa sezione, consentono solo una piccola deviazione da una funzione di identità. In realtà, qualsiasi voce nella rampa deve essere entro 32768 del valore Identity. Questa restrizione significa che nessuna app può trasformare la visualizzazione completamente nera o in un altro colore illeggibile.

L'API successiva è [**SetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp)di Microsoft Direct3D 9, che segue lo stesso modello e lo stesso formato di dati di [**SetDeviceGammaRamp.**](/windows/win32/api/wingdi/nf-wingdi-setdevicegammaramp) Il valore predefinito della rampa gamma Direct3D 9 non è particolarmente utile; È una rampa di WORD inizializzata su 0-255, non su 0-65535, anche se l'API è definita in termini di 0-65535.

L'API più recente [**è IDXGIOutput::SetGammaControl.**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-setgammacontrol) Questa API ha uno schema più flessibile per esprimere il controllo gamma, in quanto adatta l'aumento del set di formati di visualizzazione di DXGI, inclusi dieci bit interi per canale, formati float a 16 bit e il formato di intervallo esteso XR \_ BIAS.

Tutte queste API operano sullo stesso hardware e modificano gli stessi valori. Le API Direct3D 9 e DXGI sono di "sola scrittura". Non è possibile leggere il valore dell'hardware, modificarlo e quindi impostarlo. È possibile impostare solo la rampa. Inoltre, è possibile impostare gamma solo quando l'app è a schermo intero. Questa restrizione è un altro modo per garantire che il desktop sia sempre leggibile. Ciò significa che l'app può disturbare il proprio schermo, ma Windows ripristina la gamma ramp precedente quando l'app perde lo schermo intero (ad esempio, tramite ALT+TAB o CTRL+ALT+CANC).

## <a name="evolution-of-display-hardware"></a>Evoluzione dell'hardware di visualizzazione

Alcuni monitor più nuovi possono visualizzare un'ampia gamma di intensità. Tuttavia, quando il formato di visualizzazione può rappresentare solo valori compresi tra zero e uno, la visualizzazione deve eseguire il mapping di zero al valore più scuro e uno al valore più chiaro. Questo valore più chiaro potrebbe essere troppo chiaro per una visualizzazione comoda delle pagine Web con testo nero su sfondo bianco, ma è straordinario per gli effetti speciali troppo luminosi, ad esempio la visualizzazione di una luce che glittera da un laghi o un fulmine che si distole dal cielo. È quindi necessario un modo per esprimere questi intervalli più ampi. DXGI 1.1 e versioni successive contengono valori di formato di visualizzazione che consentono a 1.0 di rappresentare un comodo valore bianco e riserva valori di formato di visualizzazione più ampi per gli effetti speciali troppo luminosi. DXGI 1.1 supporta due formati di visualizzazione che possono esprimere questi valori più ampi: DXGI \_ FORMAT \_ R10G10B10 \_ XR BIAS A2 UNORM e virgola mobile \_ a \_ \_ 16 bit. Per una descrizione completa di questi formati, [vedere Dettagli del formato esteso.](/windows-hardware/drivers/display/details-of-the-extended-format) Ora si osserva il motivo per cui l'API gamma [**IDXGIOutput::SetGammaControl**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-setgammacontrol) di DXGI necessita di valori in pixel maggiori di 1,0.

## <a name="gamma-control-capabilities-in-dxgi"></a>Funzionalità di controllo Gamma in DXGI

DXGI consente al driver di visualizzazione di esprimere i controlli gamma come funzione lineare passo per passo. Questa funzione lineare step-wise è definita dai punti di controllo di questa funzione, dall'intervallo di valori in cui la funzione può eseguire la conversione e da un'operazione facoltativa di scala e offset aggiuntiva che può essere applicata dopo la conversione. Un'app può chiamare il [**metodo IDXGIOutput::GetGammaControlCapabilities**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-getgammacontrolcapabilities) per recuperare tutte queste funzionalità di controllo nella struttura [**DXGI \_ GAMMA CONTROL \_ \_ CAPABILITIES.**](/previous-versions/windows/desktop/legacy/bb173062(v=vs.85))

Questo grafico mostra una funzione lineare con solo quattro punti di controllo.

![funzione lineare di correzione gamma](images/gamma-linear-function.png)

DXGI definisce i punti di controllo in base alla relativa posizione lungo l'asse dei colori della superficie. Nel grafico precedente le posizioni dei punti di controllo sono 0, 0,5, 0,75 e 1,0. Questi punti di controllo indicano che l'hardware può convertire i valori nell'intervallo da 0 a 1.0. DXGI elenca questi punti di controllo nel membro della matrice **ControlPointPositions** di [**DXGI \_ GAMMA CONTROL \_ \_ CAPABILITIES**](/previous-versions/windows/desktop/legacy/bb173062(v=vs.85)) e li dichiara sempre in ordine crescente. DXGI riempie solo i primi elementi della matrice **ControlPointPositions** e indica il numero di elementi con il membro **NumGammaControlPoints** di **DXGI \_ GAMMA CONTROL \_ \_ CAPABILITIES**. Se **NumGammaControlPoints** è minore di 1025, DXGI lascia indefiniti gli altri **elementi ControlPointPositions.**

L'hardware rappresentato da questo grafico può convertire i valori in un intervallo compreso tra 0 e 1,25. DXGI imposta quindi i **membri MinConvertedValue** e **MaxConvertedValue** rispettivamente su 0,0f e 1,25f.

DXGI imposta il **membro ScaleAndOffsetSupported** di [**DXGI \_ GAMMA CONTROL \_ \_ CAPABILITIES**](/previous-versions/windows/desktop/legacy/bb173062(v=vs.85)) per indicare se l'hardware supporta la funzionalità di scalabilità e offset. Se l'hardware supporta la scalabilità e l'offset, mantiene una semplice tabella di ricerca uno-a-uno, ma quindi regola l'output della tabella per estendere l'output a un intervallo maggiore di \[ 0,1. \] L'hardware ridimensiona prima i valori che provengono dalla tabella di ricerca e quindi li offset.

> [!Note]  
> Monitor diversi connessi allo stesso computer potrebbero avere funzionalità di controllo gamma diverse. Inoltre, le funzionalità di controllo gamma possono infatti cambiare a seconda della modalità di visualizzazione dell'output. Di conseguenza, è consigliabile chiamare sempre [**IDXGIOutput::GetGammaControlCapabilities**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-getgammacontrolcapabilities) per eseguire query sulle funzionalità di controllo gamma dopo che l'app entra in modalità schermo intero.

 

È possibile usare questi valori di funzionalità di controllo gamma per derivare i valori di controllo che è possibile impostare usando l'API [**IDXGIOutput::SetGammaControl.**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-setgammacontrol)

## <a name="setting-gamma-control-with-dxgi"></a>Impostazione del controllo gamma con DXGI

Per impostare i controlli gamma, si passa un puntatore a una struttura [**DXGI \_ GAMMA \_ CONTROL**](/previous-versions/windows/desktop/legacy/bb173061(v=vs.85)) quando si chiama l'API [**IDXGIOutput::SetGammaControl.**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-setgammacontrol)

Impostare i membri **Scale** e **Offset** di [**DXGI \_ GAMMA \_ CONTROL**](/previous-versions/windows/desktop/legacy/bb173061(v=vs.85)) per specificare i valori di scala e offset da applicare all'hardware ai valori che si ottengono dalla tabella di ricerca. È possibile  impostare in modo sicuro Scala su 1 e **Offset** su zero (ovvero una scala di uno non ha alcun effetto e un offset pari a zero non ha alcun effetto) se non si vuole usare la funzionalità di scalabilità e offset o se l'hardware non ha tale funzionalità.

Impostare il membro della matrice **GammaCurve** di [**DXGI \_ GAMMA \_ CONTROL**](/previous-versions/windows/desktop/legacy/bb173061(v=vs.85)) su un elenco di strutture [**\_ RGB DXGI**](/previous-versions/windows/desktop/legacy/bb173071(v=vs.85)) per i punti nella curva gamma. Ogni **elemento \_ RGB DXGI** specifica i valori float che rappresentano i componenti rosso, verde e blu per tale punto. La curva gamma non usa valori alfa. Usare il numero ottenuto da **NumGammaControlPoints** di [**DXGI \_ GAMMA CONTROL \_ \_ CAPABILITIES**](/previous-versions/windows/desktop/legacy/bb173062(v=vs.85)) per riempire tale numero di elementi nella **matrice GammaCurve.** Ogni elemento che si posiziona nella matrice **GammaCurve** è l'altezza per ogni punto di controllo.

Si noti che nel grafico precedente è ora possibile controllare la posizione verticale di ogni punto di controllo ed è disponibile un controllo separato per rosso, verde e blu. Ad esempio, è possibile impostare tutti i valori verde e blu su zero e impostare i valori rossi su un valore crescente da zero a uno. In questo scenario, l'immagine visualizzata mostra solo le parti rosse, con il blu e il verde visualizzati come nero. È anche possibile impostare una discesa decrescente per tutti i colori, determinando una visualizzazione invertita. Qualsiasi valore che si posiziona nella matrice **GammaCurve** deve essere inclusivo nei valori ottenuti dai membri **MinConvertedValue** e **MaxConvertedValue** di [**DXGI \_ GAMMA CONTROL \_ \_ CAPABILITIES**](/previous-versions/windows/desktop/legacy/bb173062(v=vs.85)).

## <a name="gamma-control-practicalities"></a>Praticità del controllo gamma

I controlli gamma di DXGI si applicano solo se l'app è a schermo intero. Windows ripristina lo stato precedente dello schermo quando l'app esce o torna alla modalità finestra. Ma Windows non ripristina lo stato gamma dell'app se l'app entra nuovamente in modalità schermo intero. L'app deve ripristinare in modo esplicito lo stato gamma quando entra nuovamente in modalità schermo intero.

Non tutti gli adattatori supportano il controllo gamma. Se un adattatore non supporta il controllo gamma, ignora le chiamate per impostare una rampa gamma.

Le app eseguite nel desktop remoto non possono controllare affatto gamma.

Il cursore del mouse, se implementato nell'hardware (come nella maggior parte dei casi), in genere non risponde all'impostazione gamma.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida di programmazione per DXGI](dx-graphics-dxgi-overviews.md)
</dt> </dl>

 

 
