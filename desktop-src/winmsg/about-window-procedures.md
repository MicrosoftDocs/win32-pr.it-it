---
description: Ogni finestra è un membro di una particolare classe di finestra. La classe Window determina la routine della finestra predefinita utilizzata da una singola finestra per elaborare i messaggi.
ms.assetid: 3a8e8f4e-910d-4863-a4a7-dd37c2dfa402
title: Informazioni sulle routine della finestra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1f63586b9ca4ac6fe8486ba112316174533b44e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319096"
---
# <a name="about-window-procedures"></a>Informazioni sulle routine della finestra

Ogni finestra è un membro di una particolare classe di finestra. La classe Window determina la routine della finestra predefinita utilizzata da una singola finestra per elaborare i messaggi. Tutte le finestre appartenenti alla stessa classe utilizzano la stessa routine della finestra predefinita. Ad esempio, il sistema definisce una routine della finestra per la classe della casella combinata (**ComboBox**); tutte le caselle combinate usano quindi questa routine della finestra.

In genere, un'applicazione registra almeno una nuova classe di finestra e la relativa routine della finestra associata. Dopo la registrazione di una classe, l'applicazione può creare molte finestre della classe, che usano tutte la stessa routine della finestra. Poiché questo significa che diverse origini potrebbero chiamare contemporaneamente la stessa parte di codice, è necessario prestare attenzione quando si modificano le risorse condivise da una routine della finestra. Per altre informazioni, vedere [classi di finestra](window-classes.md).

Le routine della finestra per le finestre di dialogo (chiamate routine della finestra di dialogo) hanno una struttura simile e funzionano come routine di finestra normali. Tutti i punti che fanno riferimento alle routine della finestra in questa sezione si applicano anche alle routine della finestra di dialogo. Per ulteriori informazioni, vedere [finestre di dialogo](/windows/desktop/dlgbox/dialog-boxes).

In questa sezione vengono illustrati gli argomenti seguenti.

-   [Struttura di una routine della finestra](#structure-of-a-window-procedure)
-   [Routine della finestra predefinita](#default-window-procedure)
-   [Sottoclasse delle routine della finestra](#window-procedure-subclassing)
    -   [Sottoclasse dell'istanza](#instance-subclassing)
    -   [Sottoclassi globali](#global-subclassing)
-   [Superclasse delle routine della finestra](#window-procedure-superclassing)

## <a name="structure-of-a-window-procedure"></a>Struttura di una routine della finestra

Una routine della finestra è una funzione che presenta quattro parametri e restituisce un valore con segno. I parametri sono costituiti da un handle di finestra, un identificatore di messaggio **uint** e due parametri di messaggio dichiarati con i tipi di dati **wParam** e **lParam** . Per ulteriori informazioni, vedere [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)).

I parametri dei messaggi contengono spesso informazioni sia nelle parole più basse che in quelle di ordine superiore. Sono disponibili diverse macro che possono essere utilizzate da un'applicazione per estrarre informazioni dai parametri del messaggio. La macro [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) , ad esempio, estrae la parola meno ordinata (BITS da 0 a 15) da un parametro del messaggio. Altre macro includono [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)), [**LOBYTE**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85))e [**HIBYTE**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85)).

L'interpretazione del valore restituito dipende dal messaggio specifico. Per determinare il valore restituito appropriato, consultare la descrizione di ogni messaggio.

Poiché è possibile chiamare una routine della finestra in modo ricorsivo, è importante ridurre al minimo il numero di variabili locali utilizzate. Quando si elaborano singoli messaggi, un'applicazione deve chiamare funzioni esterne alla routine della finestra per evitare un uso eccessivo di variabili locali, causando probabilmente l'overflow dello stack durante la ricorsione profonda.

## <a name="default-window-procedure"></a>Routine della finestra predefinita

La funzione predefinita della routine della finestra, [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) , definisce un comportamento fondamentale condiviso da tutte le finestre. La routine della finestra predefinita fornisce la funzionalità minima per una finestra. Una routine della finestra definita dall'applicazione deve passare tutti i messaggi che non elabora alla funzione **DefWindowProc** per l'elaborazione predefinita.

## <a name="window-procedure-subclassing"></a>Sottoclasse delle routine della finestra

Quando un'applicazione crea una finestra, il sistema alloca un blocco di memoria per archiviare le informazioni specifiche della finestra, incluso l'indirizzo della routine della finestra che elabora i messaggi per la finestra. Quando il sistema deve passare un messaggio alla finestra, Cerca le informazioni specifiche della finestra per l'indirizzo della routine della finestra e passa il messaggio a tale procedura.

La *sottoclasse* è una tecnica che consente a un'applicazione di intercettare ed elaborare i messaggi inviati o pubblicati in una determinata finestra prima che la finestra abbia la possibilità di elaborarli. Tramite una sottoclasse di una finestra, un'applicazione può aumentare, modificare o monitorare il comportamento della finestra. Un'applicazione può eseguire la sottoclasse di una finestra appartenente a una classe globale di sistema, ad esempio un controllo di modifica o una casella di riepilogo. Un'applicazione potrebbe ad esempio sottoporre a sottoclasse un controllo di modifica per impedire che il controllo accetti determinati caratteri. Tuttavia, non è possibile sottoclassare una finestra o una classe che appartiene a un'altra applicazione. Tutte le sottoclassi devono essere eseguite all'interno dello stesso processo.

Un'applicazione sottoclassa una finestra sostituendo l'indirizzo della routine della finestra originale della finestra con l'indirizzo di una nuova routine della finestra, denominata *routine* della sottoclasse. Successivamente, la procedura di sottoclasse riceve tutti i messaggi inviati o inviati alla finestra.

La procedura di sottoclasse può eseguire tre azioni alla ricezione di un messaggio: può passare il messaggio alla routine della finestra originale, modificare il messaggio e passarlo alla routine della finestra originale oppure elaborare il messaggio e non passarlo alla routine della finestra originale. Se la procedura di sottoclasse elabora un messaggio, è possibile eseguire questa operazione prima, dopo o prima e dopo il passaggio del messaggio alla procedura della finestra originale.

Il sistema fornisce due tipi di sottoclassi: [istanza](#instance-subclassing) e [globale](#global-subclassing). Nella *sottoclasse dell'istanza*, un'applicazione sostituisce l'indirizzo della routine della finestra di una singola istanza di una finestra. Un'applicazione deve usare la sottoclasse dell'istanza per sottoporre a una classe una finestra esistente. Nella *sottoclasse globale*, un'applicazione sostituisce l'indirizzo della routine della finestra nella struttura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) di una classe di finestra. Tutte le finestre successive create con la classe hanno l'indirizzo della routine della sottoclasse, ma le finestre esistenti della classe non sono interessate.

### <a name="instance-subclassing"></a>Sottoclasse dell'istanza

Un'applicazione sottoclasse un'istanza di una finestra tramite la funzione [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) . L'applicazione passa il **flag \_ WndProc GWL** , l'handle per la finestra alla sottoclasse e l'indirizzo della procedura di sottoclasse a **SetWindowLong**. La routine della sottoclasse può risiedere nel file eseguibile dell'applicazione o in una DLL.

[**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) restituisce l'indirizzo della routine della finestra originale della finestra. L'applicazione deve salvare l'indirizzo, usandolo nelle chiamate successive alla funzione [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) , per passare i messaggi intercettati alla routine della finestra originale. L'applicazione deve avere anche l'indirizzo della routine della finestra originale per rimuovere la sottoclasse dalla finestra. Per rimuovere la sottoclasse, l'applicazione chiama di nuovo **SetWindowLong** , passando l'indirizzo della routine della finestra originale con il flag **\_ WndProc GWL** e l'handle alla finestra.

Il sistema è proprietario delle classi globali del sistema e gli aspetti dei controlli possono variare da una versione del sistema a quella successiva. Se l'applicazione deve sottoclassare una finestra che appartiene a una classe globale di sistema, lo sviluppatore potrebbe dover aggiornare l'applicazione quando viene rilasciata una nuova versione del sistema.

Poiché la sottoclasse dell'istanza si verifica dopo la creazione di una finestra, non è possibile aggiungere altri byte alla finestra. Le applicazioni che sottoclassano una finestra devono usare l'elenco di proprietà della finestra per archiviare tutti i dati necessari per un'istanza della finestra sottoclassata. Per altre informazioni, vedere [proprietà della finestra](window-properties.md).

Quando un'applicazione crea una sottoclasse di una finestra sottoclassata, deve rimuovere le sottoclassi nell'ordine inverso in cui sono state eseguite. Se l'ordine di rimozione non è invertito, potrebbe verificarsi un errore di sistema irreversibile.

### <a name="global-subclassing"></a>Sottoclassi globali

Per eseguire la sottoclasse globale di una classe di finestra, l'applicazione deve disporre di un handle per una finestra della classe. L'applicazione necessita anche dell'handle per rimuovere la sottoclasse. Per ottenere l'handle, un'applicazione crea in genere una finestra nascosta della classe da sottoclassare. Dopo aver ottenuto l'handle, l'applicazione chiama la funzione [**SetClassLong**](/windows/win32/api/winuser/nf-winuser-setclasslonga) , specificando l'handle, il flag **\_ WndProc di GCL** e l'indirizzo della routine della sottoclasse. **SetClassLong** restituisce l'indirizzo della routine della finestra originale per la classe.

L'indirizzo della routine della finestra originale viene utilizzato nella sottoclasse globale nello stesso modo in cui viene utilizzato nella sottoclasse dell'istanza. La routine della sottoclasse passa i messaggi alla routine della finestra originale chiamando [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca). L'applicazione rimuove la sottoclasse dalla classe Window chiamando di nuovo [**SetClassLong**](/windows/win32/api/winuser/nf-winuser-setclasslonga) , specificando l'indirizzo della routine della finestra originale, il flag **GCL \_ WndProc** e l'handle di una finestra della classe sottoclassata. Un'applicazione che esegue la sottoclasse globale di una classe di controlli deve rimuovere la sottoclasse quando l'applicazione termina; in caso contrario, potrebbe verificarsi un errore di sistema irreversibile.

La sottoclasse globale presenta le stesse limitazioni della sottoclasse dell'istanza, oltre ad alcune restrizioni aggiuntive. Un'applicazione non deve usare i byte aggiuntivi per la classe o l'istanza della finestra senza conoscere esattamente il modo in cui vengono usati dalla routine della finestra originale. Se l'applicazione deve associare dati a una finestra, deve usare le proprietà della finestra.

## <a name="window-procedure-superclassing"></a>Superclasse delle routine della finestra

La *superclasse* è una tecnica che consente a un'applicazione di creare una nuova classe di finestra con la funzionalità di base della classe esistente, oltre ai miglioramenti forniti dall'applicazione. Una superclasse è basata su una classe di finestra esistente denominata *classe base*. Spesso la classe base è una classe di finestra globale di sistema, ad esempio un controllo di modifica, ma può essere qualsiasi classe di finestra.

Una superclasse dispone di una propria routine della finestra, denominata routine superclass. La *procedura superclasse* può eseguire tre azioni alla ricezione di un messaggio: può passare il messaggio alla routine della finestra originale, modificare il messaggio e passarlo alla routine della finestra originale oppure elaborare il messaggio e non passarlo alla routine della finestra originale. Se la procedura superclass elabora un messaggio, può farlo prima, dopo o prima e dopo il passaggio del messaggio alla routine della finestra originale.

A differenza di una routine di sottoclasse, una procedura di superclasse può elaborare i messaggi di creazione della finestra ([**WM \_ NCCREATE**](wm-nccreate.md), [**WM \_ create**](wm-create.md)e così via), ma è necessario passarli anche alla routine della finestra della classe base originale, in modo che la routine della finestra della classe base possa eseguire la procedura di inizializzazione.

Per superclasse una classe della finestra, un'applicazione chiama prima di tutto la funzione [**GetClassInfo**](/windows/win32/api/winuser/nf-winuser-getclassinfoa) per recuperare le informazioni sulla classe di base. **GetClassInfo** riempie una struttura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) con i valori della struttura **WNDCLASS** della classe di base. Successivamente, l'applicazione copia il proprio handle di istanza nel membro **HINSTANCE** della struttura **WNDCLASS** e copia il nome della superclasse nel membro **lpszClassName** . Se la classe base dispone di un menu, l'applicazione deve fornire un nuovo menu con gli stessi identificatori di menu e copiare il nome del menu nel membro **lpszMenuName** . Se la procedura superclass elabora il messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) e non la passa alla routine della finestra della classe di base, non è necessario che nel menu siano presenti identificatori corrispondenti. **GetClassInfo** non restituisce il membro **lpszMenuName**, **LpszClassName** o **HINSTANCE** della struttura **WNDCLASS** .

Un'applicazione deve inoltre impostare il membro **lpfnWndProc** della struttura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) . La funzione [**GetClassInfo**](/windows/win32/api/winuser/nf-winuser-getclassinfoa) riempie questo membro con l'indirizzo della routine della finestra originale per la classe. L'applicazione deve salvare questo indirizzo per passare i messaggi alla routine della finestra originale, quindi copiare l'indirizzo della procedura superclasse nel membro **lpfnWndProc** . Se necessario, l'applicazione può modificare qualsiasi altro membro della struttura **WNDCLASS** . Una volta riempita la struttura **WNDCLASS** , l'applicazione registra la superclasse passando l'indirizzo della struttura alla funzione [**registerClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) . La superclasse può quindi essere usata per creare finestre.

Poiché la superclasse registra una nuova classe di finestra, un'applicazione può aggiungere sia ai byte di classe aggiuntivi che ai byte aggiuntivi della finestra. La superclasse non deve usare i byte aggiuntivi originali per la classe di base o per la finestra per gli stessi motivi per cui una sottoclasse di istanza o una sottoclasse globale non devono usarla. Inoltre, se l'applicazione aggiunge byte aggiuntivi per l'utilizzo alla classe o all'istanza della finestra, deve fare riferimento ai byte aggiuntivi relativi al numero di byte aggiuntivi utilizzati dalla classe base originale. Poiché il numero di byte usati dalla classe base può variare da una versione della classe di base a quella successiva, l'offset iniziale per i byte aggiuntivi della superclasse può variare anche da una versione della classe di base a quella successiva.

 

 
