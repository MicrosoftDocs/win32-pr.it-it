---
title: Sostituzione dell'applicazione Windows visualizzatore di immagini e fax usando il verbo di anteprima
description: A Windows XP, gli utenti possono visualizzare, ruotare, stampare e ingrandire le immagini.
ms.assetid: cb08756b-6a5d-424d-ab6d-2e34d180ec4e
keywords:
- Windows Visualizzatore di immagini e fax
- Verbo di anteprima
- procedure consigliate, Windows Visualizzatore immagini e fax
- procedure consigliate, verbo di anteprima
- prestazioni, Windows Visualizzatore immagini e fax
- prestazioni, verbo di anteprima
- register, verbo di anteprima
- register,verbo presentazione
- Verbo presentazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 518e32f7b7bf33db26e534c92cfe2fb46c9a51bc444f04f4881f18fb1fe6c738
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119608521"
---
# <a name="replacing-the-windows-picture-and-fax-viewer-application-using-the-preview-verb"></a>Sostituzione dell'applicazione Windows visualizzatore di immagini e fax usando il verbo di anteprima

\[La funzionalità Visualizzatore immagini e fax è supportata solo in Windows XP. \]

A Windows XP, gli utenti possono visualizzare, ruotare, stampare e ingrandire le immagini. Alcune di queste funzionalità vengono fornite tramite Windows Shell e altre tramite l'applicazione Windows Visualizzatore immagini e fax. Mentre Windows Visualizzatore immagini e fax offre un'eccellente linea di base di funzionalità ed è una parte fondamentale dell'esperienza di creazione di immagini, se si sceglie di sostituirla facilmente con un'applicazione diversa. Questo documento è progettato per consentire di sostituire in modo efficace l'applicazione Windows Visualizzatore immagini e fax senza perdere funzionalità importanti o peggiorare l'esperienza utente.

-   [Procedure consigliate](#best-practices)
    -   [Prestazioni](#performance)
    -   [Funzionalità](#features)
    -   [Supporto del formato](#format-support)
-   [Registrazione per il verbo di anteprima](#registering-for-the-preview-verb)
-   [Registrazione per il verbo di modifica](#registering-for-the-edit-verb)
-   [Registrazione per il verbo di presentazione](#registering-for-the-slideshow-verb)
-   [Argomenti correlati](#related-topics)

## <a name="best-practices"></a>Procedure consigliate

In Windows XP e versioni successive, Shell include un verbo che è possibile usare per consentire agli utenti di visualizzare in anteprima le immagini. Si chiama *Anteprima.* Questo verbo evidenzia l'attività utente principale per le immagini, che viene visualizzata. Per un funzionamento ottimale di questa esperienza, l'Windows visualizzatore di immagini e fax è proprietaria dell'associazione di anteprima per impostazione predefinita.

Il Windows visualizzatore di immagini e fax o qualsiasi applicazione proprietaria di un'associazione di file include un elemento che avvia l'applicazione di modifica dell'utente. Poiché il verbo Anteprima viene usato solo per visualizzare in anteprima le immagini anziché modificarle, l'applicazione deve prestare attenzione a seguire le raccomandazioni in questo documento quando si dichiara tale associazione.

Si vuole assicurarsi che un'applicazione che modifica le immagini possa comunque assumere il controllo del verbo Di modifica. Ad esempio, se un utente ha Microsoft Picture It! installato, quando si fa doppio clic su un file .jpg il computer dovrebbe avviare l'applicazione Windows Visualizzatore immagini e fax. Ma quando fanno clic su **Modifica sulla** barra degli strumenti, il computer dovrebbe avviare Picture It! con il .jpg file.

È necessario tenere presenti tre considerazioni quando si sostituisce il Windows Visualizzatore immagini e fax. Si tratta di:

-   [Prestazioni](#performance)
-   [Funzionalità](#features)
-   [Supporto del formato](#format-support)

### <a name="performance"></a>Prestazioni

La considerazione principale delle prestazioni è la velocità di caricamento delle immagini. Anche se qui non viene fornita alcuna metrica delle prestazioni, è consigliabile provare Windows Visualizzatore immagini e fax con un'applicazione che corrisponde o aumenta le prestazioni.

L'applicazione stessa deve essere caricata rapidamente. Uno dei problemi principali che gli utenti verificano con le applicazioni che prendono il controllo delle associazioni di immagini è il tempo di attesa durante il caricamento dell'applicazione. Questo spesso deriva dal caricamento di un'applicazione di modifica potente quando fa doppio clic su un file di immagine, anche quando l'utente vuole semplicemente visualizzare il file. È la scelta migliore per l'utente se si forniscono opzioni che le consentono di passare rapidamente a un'applicazione in cui può modificare l'immagine solo quando si vuole.

### <a name="features"></a>Funzionalità

È disponibile un set minimo di funzionalità che l'applicazione deve fornire quando si sostituisce l'Windows visualizzatore di immagini e fax. Ecco quali sono:



| Funzionalità                            | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Visualizzare l'immagine nella migliore delle modi             | In questo modo l'utente può visualizzare l'intera immagine ridimensionata in base alle dimensioni in cui si adatta meglio allo spazio visualizzabile della finestra dell'applicazione. In questo modo, possono visualizzare l'intera immagine, anche se è leggermente degradata con lo zoom indietro. Questa deve essere l'impostazione predefinita ogni volta che viene caricata un'immagine di dimensioni maggiori dello spazio visualizzabile. In caso contrario, l'immagine dovrebbe essere visualizzata nelle dimensioni effettive. Ad esempio, un'immagine da 64 x 64 pixel non deve essere ridimensionata a una dimensione di 600 x 600 semplicemente perché si tratta delle dimensioni della finestra dell'applicazione. |
| Mostra immagine con le dimensioni effettive          | In questo modo l'utente può visualizzare l'intera immagine con la risoluzione effettiva. Ciò consente loro di visualizzarlo alle dimensioni appropriate e di eseguire la panoramica sull'immagine. Questa non deve essere la visualizzazione predefinita, a meno che l'immagine non sia più piccola dello spazio visualizzabile nell'applicazione.                                                                                                                                                                                                                                                              |
| Eseguire lo zoom avanti dell'immagine                    | Ciò consente all'utente di ingrandire una parte dell'immagine per analizzare dettagli più dettagliati o semplicemente ingrandire un'immagine di piccole dimensioni. Questa operazione è simile alla visualizzazione delle dimensioni effettive dell'immagine, ma consente all'utente di controllare la stretta visualizzazione dell'immagine.                                                                                                                                                                                                                                                                                            |
| Zoom indietro dell'immagine                  | In questo modo l'utente può eseguire lo zoom indietro e ottenere una visualizzazione più ampia. Questa operazione è simile alla visualizzazione ottimale dell'immagine, ma consente all'utente di controllare la distanza di visualizzazione dell'immagine.                                                                                                                                                                                                                                                                                                                                                          |
| Immagine successiva                         | In questo modo l'utente può visualizzare l'immagine successiva nell'elenco. Questo elenco può contenere tutte le immagini nella cartella corrente o tutte le immagini selezionate dall'utente come parte di un'operazione di selezione multipla. ad esempio quando fa clic e trascina per evidenziare le immagini o tiene premuto il pulsante di controllo e fa clic su singoli file.                                                                                                                                                                                                                       |
| Immagine precedente                     | In questo modo l'utente può visualizzare l'immagine precedente nell'elenco.                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Ruotare in senso orario di 90 gradi        | In questo modo l'utente può ruotare l'immagine in senso orario di trimestri. Windows XP salva automaticamente l'immagine quando la ruota per ridurre la perdita della qualità dell'immagine. L'applicazione può anche ruotare incrementi più piccoli, ma 90 gradi è lo standard come rotazione più comune per le immagini digitali.                                                                                                                                                                                                                                 |
| Ruotare in senso antiorario di 90 gradi | In questo modo l'utente può ruotare l'immagine in senso antiorario di trimestri.                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Stampa                              | In questo modo l'utente può stampare l'immagine attualmente visualizzata.                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Save As                            | In questo modo l'utente può salvare l'immagine in una cartella specificata.                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Elimina immagine                       | In questo modo l'utente può eliminare l'immagine.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Help                               | In questo modo viene fornita all'utente la documentazione della Guida relativa all'uso dell'applicazione di visualizzazione.                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Proprietà                         | Ciò consente all'utente di visualizzare o modificare le proprietà dell'immagine, in genere le informazioni exIF (Exchangeable Image File) archiviate in ogni immagine.                                                                                                                                                                                                                                                                                                                                                                                      |
| Modifica                               | In questo modo l'utente può avviare il programma di modifica preferito registrato per il verbo Di modifica nell'immagine.                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

### <a name="format-support"></a>Supporto del formato

Poiché è difficile per un'applicazione supportare tutte le immagini diverse, è consigliabile che l'applicazione usi Windows GDI+ per supportare i formati di immagine. Tuttavia, se si sceglie di non usare GDI+, l'applicazione deve assumere il controllo solo delle associazioni di file per cui è stato testato ed è noto per funzionare. Quindi, se l'utente deve visualizzare un formato che non viene gestito, Windows Visualizzatore immagini e fax può comunque fornire l'accesso.

Ad esempio, Windows Visualizzatore immagini e fax offre una serie di strumenti per la modifica delle annotazioni nelle immagini con estensione tiff. A meno che questa funzionalità non sia duplicata nell'applicazione, non è consigliabile registrare l'applicazione per gestire le immagini con estensione tiff. Il principio di guida deve essere quello di garantire che l'utente non perda alcuna funzionalità.

## <a name="registering-for-the-preview-verb"></a>Registrazione per il verbo di anteprima

La registrazione di un'applicazione per gestire il verbo di anteprima è piuttosto semplice. Individuare il valore seguente dell'applicazione nel Registro di sistema, dove Application.Jpeg rappresenta [](/windows/desktop/shell/default-programs) il nome della chiave di associazione file dell'applicazione (per altre informazioni, vedere Programmi predefiniti):

```
HKEY_CLASSES_ROOT
   Application.Jpeg
      shell
         open
            command
               (Default) = app.exe %1
```

Modificare il nome della **sottochiave aperta** in "anteprima", come illustrato di seguito.

```
HKEY_CLASSES_ROOT
   Application.Jpeg
      shell
         preview
            command
               (Default) = app.exe %1
```

Questa operazione registra l'applicazione e la rende l'applicazione predefinita per il verbo di anteprima per .jpg file. È necessario anche quanto segue.

**HKEY \_ CLASSES \_ ROOT** \\ **.jpg** \( Default) = Application.Jpeg

## <a name="registering-for-the-edit-verb"></a>Registrazione per il verbo di modifica

In questo modo viene registrato un'applicazione per il verbo di modifica e viene creata la nuova applicazione predefinita per la modifica di un'immagine. L'applicazione registrata deve assumere la funzionalità di modifica dell'applicazione predefinita esistente in fase di installazione e installarla nuovamente come gestore al momento della disinstallazione. Questa operazione può essere ottenuta registrando la nuova applicazione più in basso nell'elenco di associazioni rispetto all'applicazione predefinita. L'applicazione predefinita è registrata qui:

```
HKEY_CLASSES_ROOT
   SystemFileAssociations
      image
         shell
            edit
               command
                  (Default) = app.exe %1
```

La nuova applicazione deve registrarsi qui:

```
HKEY_CLASSES_ROOT
   Application.Jpeg
      shell
         edit
            command
               (Default) = app.exe %1
```

## <a name="registering-for-the-slideshow-verb"></a>Registrazione per il verbo di presentazione

A Windows Vista, un'applicazione può anche registrare il **verbo di presentazione.** Le applicazioni che implementano una presentazione possono registrarsi per essere richiamate quando si sceglie il verbo Presentazione. Questa registrazione viene eseguita esattamente nello stesso modo illustrato per il verbo di anteprima precedente. È consigliabile che le applicazioni implementino il formato DropTarget del verbo. In questo modo, è possibile passare un set completo di elementi. L'implementazione di DropTarget viene registrata come illustrato di seguito:

```
HKEY_CLASSES_ROOT
   Application.Jpeg
      shell
         slideshow
            DropTarget
               CLSID = {CLSID of the implementation}
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Introduzione alle associazioni di file](/windows/desktop/shell/fa-intro)
</dt> <dt>

[Informazioni GDI+](../gdiplus/-gdiplus-about-gdi--about.md)
</dt> </dl>

 

 