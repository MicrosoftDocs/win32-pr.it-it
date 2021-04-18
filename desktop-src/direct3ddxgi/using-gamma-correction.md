---
description: La correzione gamma o la gamma Short è il nome di un'operazione non lineare utilizzata dai sistemi per codificare e decodificare i valori dei pixel nelle immagini.
ms.assetid: 97ACDAE3-514E-4AAF-A27D-E5FFC162DB2A
title: Uso della correzione gamma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c940db1a94fb41e9babecbeb3075aa9e01b3732
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104557644"
---
# <a name="using-gamma-correction"></a>Uso della correzione gamma

La correzione gamma o la gamma Short è il nome di un'operazione non lineare utilizzata dai sistemi per codificare e decodificare i valori dei pixel nelle immagini.

-   [Che cos'è gamma e a cosa serve?](#what-is-gamma-and-what-is-it-for)
-   [Sfondo di gamma per Windows](#background-of-gamma-on-windows)
-   [Evoluzione dell'hardware di visualizzazione](#evolution-of-display-hardware)
-   [Funzionalità di controllo gamma in DXGI](#gamma-control-capabilities-in-dxgi)
-   [Impostazione del controllo gamma con DXGI](#setting-gamma-control-with-dxgi)
-   [Praticità del controllo gamma](#gamma-control-practicalities)
-   [Argomenti correlati](#related-topics)

## <a name="what-is-gamma-and-what-is-it-for"></a>Che cos'è gamma e a cosa serve?

Alla fine della pipeline grafica, nel punto in cui l'immagine lascia il computer per eseguire il suo viaggio lungo il cavo di monitoraggio, c'è un piccolo componente hardware che può trasformare i valori dei pixel in tempo reale. Questo hardware usa in genere una tabella di ricerca per trasformare i pixel. Questo hardware usa i valori rosso, verde e blu che provengono dalla superficie da visualizzare per cercare valori con correzione gamma nella tabella e quindi invia i valori corretti al monitor anziché ai valori effettivi della superficie. Questa tabella di ricerca è quindi un'opportunità per sostituire qualsiasi colore con qualsiasi altro colore. Sebbene la tabella disponga di tale livello di potenza, l'utilizzo tipico consiste nel modificare le immagini in modo leggermente per compensare le differenze nella risposta del monitoraggio. La risposta del monitoraggio è la funzione che mette in correlazione il valore numerico dei componenti rosso, verde e blu di un pixel con la luminosità visualizzata di tale pixel.

Questo è il modo in cui questa tabella era destinata a, ma gli sviluppatori di giochi trovavano degli usi creativi, ad esempio l'intero schermo rosso per effetto psicologico. Nelle app di gioco moderne, come parte della post-elaborazione di ogni frame, in genere vengono forniti altri modi per eseguire queste operazioni. In realtà, è consigliabile lasciare solo la tabella gamma perché potrebbe essere utilizzata per calibrare la risposta del monitoraggio e le modifiche all'ingrosso per la rampa gamma elimineranno questa accurata taratura.

La scienza della determinazione della correzione gamma è complessa e non viene presentata in questo argomento, tranne che per illuminare il nome "gamma". La risposta di un monitor CRT (ovvero una vecchia vetrata) è una funzione complessa, ma la fisica di questi monitoraggi significa che presentano una risposta che può essere rappresentata in modo rozzo da questa funzione di risparmio energia:

luminosità (input) =<sup>gamma</sup> di input

Il valore gamma è in genere vicino a un valore di 2,0. I monitoraggi LCD e tutte le altre tecnologie più recenti sono progettati in modo specifico per presentare una risposta simile, quindi non è necessario ricalibrare tutto il software e le immagini per le nuove tecnologie. Lo standard sRGB dichiara che questo valore gamma è esattamente 2,2 e questo valore è diventato uno standard ampiamente implementato.

L'occhio umano dispone anche di una funzione di risposta che inverte approssimativamente la funzione di alimentazione CRT. Ciò significa che la luminosità percepita di un pixel aumenta approssimativamente in modo lineare con i valori RGB in quel pixel.

Poiché un valore gamma di 2,2 è diventato uno standard de facto, in genere non è necessario preoccuparsi troppo della curva gamma codificata in questa tabella e può lasciarla come mapping lineare e uno-a-uno. La corrispondenza dei colori appropriata naturalmente richiede una particolare attenzione a questa funzione, ma tale discussione esula dall'ambito di questo argomento. Windows include uno strumento che consente agli utenti di calibrare le proprie visualizzazioni per la gamma 2,2 e questo strumento usa l'hardware della tabella di ricerca per derivare una modifica sottile scelta con attenzione per i propri computer. Gli utenti possono eseguire questo strumento cercando "Calibra colore". Sono inoltre disponibili profili colori ben definiti per determinati monitoraggi che automatizzano il processo. Lo strumento "Calibra colore" può rilevare questi monitoraggi più recenti e informare gli utenti che la taratura è già in atto.

Questa nozione di codifica di una legge di risparmio energia in valori di colore è utile anche in altri punti della pipeline grafica, soprattutto nelle trame. Per le trame, si desidera maggiore precisione sui colori più scuri a causa della risposta logaritmica degli occhi umani di cui si è appena parlato. Una gestione attenta di gamma in questa parte della pipeline è importante. Per altre informazioni, vedere [conversione dei dati per lo spazio colore](converting-data-color-space.md).

Il resto di questo argomento è incentrato solo sulla correzione gamma nell'ultima parte della pipeline, tra i dati del buffer del frame e il monitoraggio. Se si vuole scrivere una procedura guidata di calibrazione o creare effetti speciali in un'app a schermo intero in cui un passaggio di post-elaborazione non è pratico, di seguito sono riportate le informazioni necessarie.

## <a name="background-of-gamma-on-windows"></a>Sfondo di gamma per Windows

Nei computer Windows è in genere presente una tabella gamma che è una tabella di ricerca che accetta una tripletta di byte e restituisce una tripletta di byte. Questi tripletti sono 768 (256 x 3) byte di RAM. Questo è corretto quando il formato di visualizzazione contiene una tripletta di valori di BYTE RGB ma non è sufficientemente espressivo per descrivere le trasformazioni che è possibile desiderare quando il formato di visualizzazione ha un intervallo maggiore di \[ 0, 1 \] , ad esempio i valori a virgola mobile. Le API di Windows che controllano gamma hanno seguito un'evoluzione perché i formati di visualizzazione sono diventati più complessi.

Le prime API Windows per offrire il controllo gamma sono [**SetDeviceGammaRamp**](/windows/win32/api/wingdi/nf-wingdi-setdevicegammaramp) e [**GetDeviceGammaRamp**](/windows/win32/api/wingdi/nf-wingdi-getdevicegammaramp)di Windows Graphics Device Interface (GDI). Queste API funzionano con matrici di parole di 3 256, con ogni parola che codifica zero fino a una, rappresentata da valori di WORD 0 e 65535. La precisione aggiuntiva di una parola non è in genere disponibile nelle tabelle di ricerca hardware effettive, ma queste API erano progettate per essere flessibili. Queste API, a differenza delle altre descritte più avanti in questa sezione, consentono solo una piccola deviazione da una funzione di identità. In realtà, qualsiasi voce nella rampa deve essere compresa tra 32768 del valore Identity. Questa restrizione significa che nessuna app può attivare la visualizzazione completamente nera o altri colori illeggibili.

L'API successiva è il [**SetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp)di Microsoft Direct3D 9, che segue lo stesso modello e lo stesso formato di dati di [**SetDeviceGammaRamp**](/windows/win32/api/wingdi/nf-wingdi-setdevicegammaramp). Il valore predefinito della rampa gamma Direct3D 9 non è particolarmente utile; si tratta di una rampa di parole inizializzata su 0-255, non 0-65535, anche se l'API è definita in termini di 0-65535.

L'API più recente è [**IDXGIOutput:: SetGammaControl**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-setgammacontrol). Questa API ha uno schema più flessibile per esprimere il controllo gamma, in quanto si adatta al set di formati di visualizzazione più ampio di DXGI, tra cui dieci bit integer per canale, formati float a 16 bit e il \_ formato di intervallo esteso per la distorsione XR.

Tutte queste API operano sullo stesso hardware e modificano gli stessi valori. Le API Direct3D 9 e DXGI sono "solo scrittura". Non è possibile leggere il valore dell'hardware, modificarlo e quindi impostarlo. È possibile impostare solo la rampa. Inoltre, è possibile impostare gamma solo quando l'app è a schermo intero. Questa restrizione è un altro modo per garantire che il desktop sia sempre leggibile. Ovvero, l'app può infastidire il proprio schermo, ma Windows ripristinerà la rampa gamma precedente quando l'app perderà schermo intero (ad esempio, tramite ALT-TAB o CTRL + ALT + CANC).

## <a name="evolution-of-display-hardware"></a>Evoluzione dell'hardware di visualizzazione

Alcuni monitoraggi più recenti possono visualizzare un'ampia gamma di intensità. Tuttavia, quando il formato di visualizzazione può rappresentare solo valori compresi tra zero e uno, la visualizzazione deve eseguire il mapping di zero al relativo valore più scuro e uno al suo valore più chiaro. Questo valore più chiaro potrebbe essere troppo chiaro per la visualizzazione di pagine Web con testo nero su sfondo bianco, ma è ideale per effetti speciali eccessivamente luminosi, ad esempio la visualizzazione della luce solare luccicante di un lago o un fulmine. Quindi, è necessario un modo per esprimere questi intervalli più ampi. DXGI 1,1 e versioni successive contengono valori di formato di visualizzazione che consentono a 1,0 di rappresentare un valore bianco comodo e riservano valori di formato di visualizzazione più ampi per effetti speciali eccessivamente luminosi. DXGI 1,1 supporta due formati di visualizzazione che consentono di esprimere i valori più estesi: DXGI \_ Format \_ R10G10B10 \_ XR \_ Bias \_ a2 \_ UNORM e a virgola mobile a 16 bit. Per una descrizione completa di questi formati, vedere [Dettagli del formato esteso](/windows-hardware/drivers/display/details-of-the-extended-format). A questo punto, si esamina il motivo per cui l'API DXGI di [**IDXGIOutput:: SetGammaControl**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-setgammacontrol) gamma richiede valori pixel maggiori di 1,0.

## <a name="gamma-control-capabilities-in-dxgi"></a>Funzionalità di controllo gamma in DXGI

DXGI consente al driver di visualizzazione di esprimere i propri controlli gamma come funzione lineare step-wise. Questa funzione lineare Step-Wise è definita dai punti di controllo di questa funzione, dall'intervallo di valori in cui la funzione può essere convertita e da un'operazione facoltativa di ridimensionamento e offset aggiuntiva che può essere applicata dopo la conversione. Un'app può chiamare il metodo [**IDXGIOutput:: GetGammaControlCapabilities**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-getgammacontrolcapabilities) per recuperare tutte le funzionalità di controllo nella struttura [**delle \_ \_ \_ funzionalità di controllo gamma di DXGI**](/previous-versions/windows/desktop/legacy/bb173062(v=vs.85)) .

Questo grafico mostra una funzione lineare con solo quattro punti di controllo.

![funzione lineare di correzione gamma](images/gamma-linear-function.png)

DXGI definisce i punti di controllo in base alla relativa posizione lungo l'asse dei colori della superficie. Nel grafico precedente, le posizioni dei punti di controllo sono 0, 0,5, 0,75 e 1,0. Questi punti di controllo indicano che l'hardware può convertire i valori nell'intervallo compreso tra 0 e 1,0. DXGI elenca questi punti di controllo nel  membro della matrice ControlPointPositions [**delle \_ \_ \_ funzionalità di controllo gamma di DXGI**](/previous-versions/windows/desktop/legacy/bb173062(v=vs.85)) e li dichiara sempre in ordine crescente. DXGI riempie solo i primi elementi della matrice **ControlPointPositions** e indica il numero di elementi con il membro **NumGammaControlPoints** delle **funzionalità di \_ \_ controllo \_ gamma DXGI**. Se **NumGammaControlPoints** è minore di 1025, DXGI lascia invariato il resto degli elementi **ControlPointPositions** .

L'hardware rappresentato da questo grafico può convertire i valori in un intervallo compreso tra 0 e 1,25. Quindi, DXGI imposta rispettivamente i membri **MinConvertedValue** e **MaxConvertedValue** su 0,0 f e 1.25 f.

DXGI imposta il membro **ScaleAndOffsetSupported** delle [**\_ \_ \_ funzionalità di controllo gamma DXGI**](/previous-versions/windows/desktop/legacy/bb173062(v=vs.85)) per indicare se l'hardware supporta la funzionalità di scalabilità e offset. Se l'hardware supporta la scalabilità e l'offset, mantiene una semplice tabella di ricerca uno-a-uno, ma quindi modifica l'output della tabella per estendere l'output a un intervallo maggiore di \[ 0, 1 \] . L'hardware ridimensiona innanzitutto i valori che provengono dalla tabella di ricerca e li compensa.

> [!Note]  
> Diversi monitoraggi connessi allo stesso computer potrebbero avere funzionalità di controllo gamma diverse. Inoltre, le funzionalità di controllo gamma possono cambiare in base alla modalità di visualizzazione dell'output. Di conseguenza, è consigliabile chiamare sempre [**IDXGIOutput:: GetGammaControlCapabilities**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-getgammacontrolcapabilities) per eseguire query sulle funzionalità di controllo gamma dopo che l'app entra in modalità schermo intero.

 

È possibile usare questi valori di funzionalità di controllo gamma per derivare i valori di controllo che è possibile impostare usando l'API [**IDXGIOutput:: SetGammaControl**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-setgammacontrol) .

## <a name="setting-gamma-control-with-dxgi"></a>Impostazione del controllo gamma con DXGI

Per impostare i controlli gamma, passare un puntatore a una struttura di [**\_ \_ controllo gamma DXGI**](/previous-versions/windows/desktop/legacy/bb173061(v=vs.85)) quando si chiama l'API [**IDXGIOutput:: SetGammaControl**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-setgammacontrol) .

È possibile impostare i membri di **ridimensionamento** e **offset** del [**\_ \_ controllo gamma DXGI**](/previous-versions/windows/desktop/legacy/bb173061(v=vs.85)) per specificare i valori di scala e offset che si desidera applicare all'hardware ai valori che si ottengono dalla tabella di ricerca. È possibile impostare in modo sicuro la **scala** su 1 e l' **offset** su zero (ovvero, una scala di uno non ha alcun effetto e un offset pari a zero non ha alcun effetto) se non si vuole usare la funzionalità di scalabilità e offset o se l'hardware non dispone di questa funzionalità.

Impostare il membro della matrice **GammaCurve** del [**\_ \_ controllo gamma DXGI**](/previous-versions/windows/desktop/legacy/bb173061(v=vs.85)) su un elenco di [**strutture \_ RGB DXGI**](/previous-versions/windows/desktop/legacy/bb173071(v=vs.85)) per i punti sulla curva gamma. Ogni **elemento \_ RGB DXGI** specifica i valori float che rappresentano i componenti rosso, verde e blu per quel punto. La curva gamma non usa valori alfa. Si usa il numero ottenuto da **NumGammaControlPoints** delle funzionalità di [**\_ \_ controllo \_ gamma DXGI**](/previous-versions/windows/desktop/legacy/bb173062(v=vs.85)) per riempire tale numero di elementi nella matrice **GammaCurve** . Ogni elemento inserito nella matrice **GammaCurve** è l'altezza di ogni punto di controllo.

Si noti che nel grafico precedente è ora possibile controllare la posizione verticale di ogni punto di controllo ed è disponibile un controllo separato per rosso, verde e blu. Ad esempio, è possibile impostare tutti i valori verde e blu su zero e impostare i valori rossi su una scala crescente da zero a uno. In questo scenario, l'immagine visualizzata Mostra solo le parti rosse, con blu e verde visualizzate come nero. È anche possibile impostare una scala discendente per tutti i colori, che comporta una visualizzazione invertita. Qualsiasi valore inserito nella matrice **GammaCurve** deve essere compreso tra i valori ottenuti dai membri **MinConvertedValue** e **MaxConvertedValue** delle [**\_ \_ \_ funzionalità di controllo gamma DXGI**](/previous-versions/windows/desktop/legacy/bb173062(v=vs.85)).

## <a name="gamma-control-practicalities"></a>Praticità del controllo gamma

I controlli gamma di DXGI si applicano solo finché l'app è a schermo intero. Windows ripristina lo stato precedente dello schermo quando l'app viene chiusa o torna alla modalità finestra. Tuttavia, Windows non ripristina lo stato gamma dell'app se l'app entra nuovamente in modalità schermo intero. L'app deve ripristinare in modo esplicito lo stato gamma quando viene nuovamente attivata la modalità schermo intero.

Non tutti gli adapter supportano il controllo gamma. Se un adapter non supporta il controllo gamma, ignora le chiamate per impostare una rampa gamma.

Le app eseguite in Desktop remoto non possono controllare la gamma.

Il cursore del mouse, se implementato nell'hardware (come la maggior parte di essi), in genere non risponde all'impostazione gamma.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida per programmatori per DXGI](dx-graphics-dxgi-overviews.md)
</dt> </dl>

 

 
