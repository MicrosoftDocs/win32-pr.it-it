---
title: Sostituzione dell'applicazione Windows Picture and Fax Viewer utilizzando il verbo di anteprima
description: A partire da Windows XP, gli utenti possono visualizzare, ruotare, stampare e ingrandire le immagini.
ms.assetid: cb08756b-6a5d-424d-ab6d-2e34d180ec4e
keywords:
- Visualizzatore immagini e fax di Windows
- Verbo di anteprima
- procedure consigliate, Visualizzatore immagini e fax di Windows
- procedure consigliate, verbo di anteprima
- prestazioni, Visualizzatore immagini e fax di Windows
- prestazioni, verbo di anteprima
- Register, verbo di anteprima
- Register, verbo slideshow
- Verbo slideshow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e6769e13aaea41b3b05bbf674ea95d7f88fb646
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103963087"
---
# <a name="replacing-the-windows-picture-and-fax-viewer-application-using-the-preview-verb"></a>Sostituzione dell'applicazione Windows Picture and Fax Viewer utilizzando il verbo di anteprima

\[La funzionalità Visualizzatore immagini e fax è supportata solo in Windows XP. \]

A partire da Windows XP, gli utenti possono visualizzare, ruotare, stampare e ingrandire le immagini. Alcune di queste funzionalità vengono fornite tramite la shell di Windows e altre tramite l'applicazione Windows Picture and Fax Viewer. Sebbene Windows Picture and Fax Viewer fornisca una linea di base eccellente per le funzionalità ed è una parte essenziale dell'esperienza di creazione dell'immagine, se si sceglie di, è possibile sostituirla con un'altra applicazione. Questo documento è stato progettato per consentire di sostituire in modo efficace l'applicazione Windows Picture and Fax Viewer senza perdere le funzionalità importanti o degradare l'esperienza utente.

-   [Procedure consigliate](#best-practices)
    -   [Prestazioni](#performance)
    -   [Funzionalità](#features)
    -   [Supporto del formato](#format-support)
-   [Registrazione per il verbo di anteprima](#registering-for-the-preview-verb)
-   [Registrazione per il verbo di modifica](#registering-for-the-edit-verb)
-   [Registrazione per il verbo slideshow](#registering-for-the-slideshow-verb)
-   [Argomenti correlati](#related-topics)

## <a name="best-practices"></a>Procedure consigliate

In Windows XP e versioni successive, la shell include un verbo che è possibile usare per consentire agli utenti di visualizzare in anteprima le immagini. Viene chiamato *Anteprima*. Questo verbo evidenzia l'attività principale dell'utente per le immagini, che sta visualizzando. Per garantire il corretto funzionamento di questa esperienza, l'applicazione Windows Picture and Fax Viewer è proprietaria dell'associazione di anteprima per impostazione predefinita.

Il Visualizzatore immagini e fax di Windows, o qualsiasi applicazione che possiede un'associazione di file, include un elemento che avvia l'applicazione di modifica dell'utente. Poiché il verbo di anteprima viene usato solo per visualizzare in anteprima le immagini anziché modificarle, l'applicazione deve prestare attenzione a seguire le indicazioni contenute in questo documento quando si reclama tale associazione.

Si vuole garantire che un'applicazione che modifichi le immagini possa ancora assumere il verbo di modifica. Ad esempio, se un utente dispone di un'immagine di Microsoft! installato, quando si fa doppio clic su un file con estensione jpg, il computer deve avviare l'applicazione Windows Picture and Fax Viewer. Tuttavia, quando si fa clic su **modifica** nella barra degli strumenti, il computer dovrebbe avviare l'immagine! con il file con estensione jpg.

Quando si sostituisce il Visualizzatore immagini e fax di Windows, è necessario prendere in considerazione tre considerazioni. Si tratta di:

-   [Prestazioni](#performance)
-   [Funzionalità](#features)
-   [Supporto del formato](#format-support)

### <a name="performance"></a>Prestazioni

La considerazione principale con le prestazioni è la velocità di caricamento delle immagini. Sebbene non venga fornita alcuna metrica di prestazioni, provare a sostituire il Visualizzatore immagini e fax di Windows con un'applicazione che corrisponda o aumenti le prestazioni.

È necessario caricare rapidamente l'applicazione stessa. Uno dei principali problemi riscontrati dagli utenti con le applicazioni che accettano le associazioni di immagini è il tempo di attesa durante il caricamento dell'applicazione. Questa operazione spesso deriva da un potente caricamento di applicazioni di modifica quando si fa doppio clic su un file di immagine, anche quando l'utente desidera semplicemente visualizzare il file. È consigliabile che l'utente fornisca opzioni che consentono di passare rapidamente a un'applicazione in cui è possibile modificare l'immagine solo quando si desidera.

### <a name="features"></a>Funzionalità

È disponibile un set minimo di funzionalità che l'applicazione deve fornire quando si sostituisce l'applicazione Windows Picture and Fax Viewer. Ecco quali sono:



| Funzionalità                            | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Mostra immagine più adatta             | Ciò consente all'utente di visualizzare l'intera immagine ridimensionata in modo da adattarla più facilmente allo spazio visualizzabile della finestra dell'applicazione. In questo modo, è possibile visualizzare l'intera immagine, anche se è leggermente degradata, eseguendo lo zoom indietro. Questa deve essere l'impostazione predefinita ogni volta che un'immagine viene caricata più grande dello spazio visualizzabile. In caso contrario, l'immagine dovrebbe essere visualizzata nelle dimensioni effettive. Ad esempio, un'immagine a 64 x 64 pixel non deve essere ridimensionata a una dimensione 600 x 600 semplicemente perché si tratta della dimensione della finestra dell'applicazione. |
| Mostra immagine alle dimensioni effettive          | Ciò consente all'utente di visualizzare l'intera immagine alla risoluzione effettiva. In questo modo è possibile visualizzarla con le dimensioni appropriate e la panoramica sull'immagine. Questa non deve corrispondere alla visualizzazione predefinita, a meno che l'immagine non sia più piccola dello spazio visualizzabile nell'applicazione.                                                                                                                                                                                                                                                              |
| Ingrandisci immagine                    | Ciò consente all'utente di ingrandire una parte dell'immagine per esaminare i dettagli più precisi o semplicemente ingrandire un'immagine piccola. Questa operazione è simile alla visualizzazione delle dimensioni effettive dell'immagine, ma consente all'utente di controllare il grado di visualizzazione dell'immagine.                                                                                                                                                                                                                                                                                            |
| Ingrandisci immagine                  | Ciò consente all'utente di eseguire lo zoom indietro e ottenere una visualizzazione più ampia. Si tratta di un aspetto simile a quello che mostra l'immagine più adatta, ma consente all'utente di controllare la distanza di visualizzazione dell'immagine.                                                                                                                                                                                                                                                                                                                                                          |
| Immagine successiva                         | Ciò consente all'utente di visualizzare l'immagine successiva nell'elenco. Questo elenco può essere costituito da tutte le immagini nella cartella corrente o da tutte le immagini selezionate dall'utente come parte di un'operazione di selezione. ovvero, quando fa clic e trascina per evidenziare le immagini o tenere premuto il pulsante di controllo e fare clic su singoli file.                                                                                                                                                                                                                       |
| Immagine precedente                     | Ciò consente all'utente di visualizzare l'immagine precedente nell'elenco.                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Ruota di 90 gradi in senso orario        | Ciò consente all'utente di ruotare l'immagine in senso orario per i trimestri. Windows XP Salva automaticamente l'immagine quando la ruota per ridurre la perdita di qualità dell'immagine. L'applicazione può anche ruotare incrementi più piccoli, ma 90 gradi è lo standard come la rotazione più comune per le immagini digitali.                                                                                                                                                                                                                                 |
| Ruota di 90 gradi in senso antiorario | Ciò consente all'utente di ruotare l'immagine in senso antiorario per quarti.                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Stampa                              | Ciò consente all'utente di stampare l'immagine attualmente visualizzata.                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Save As                            | Ciò consente all'utente di salvare l'immagine in una cartella specificata.                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Elimina immagine                       | Ciò consente all'utente di eliminare l'immagine.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Help                               | Questo consente all'utente di visualizzare la documentazione della Guida relativa all'utilizzo dell'applicazione di visualizzazione.                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Proprietà                         | Ciò consente all'utente di visualizzare o modificare le proprietà dell'immagine, in genere le informazioni del file di immagine scambiabile (EXIF) archiviate in ogni immagine.                                                                                                                                                                                                                                                                                                                                                                                      |
| Modifica                               | Ciò consente all'utente di avviare il programma di modifica preferito registrato per il verbo di modifica nell'immagine.                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

### <a name="format-support"></a>Supporto del formato

Poiché è difficile per un'applicazione supportare tutte le immagini diverse, è consigliabile usare Windows GDI+ per supportare i formati di immagine. Tuttavia, se si sceglie di non utilizzare GDI+, l'applicazione deve assumere solo le associazioni di file per le quali è stato testato e funzionante. Quindi, se l'utente deve visualizzare un formato non gestito, il Visualizzatore immagini e fax di Windows può comunque fornire l'accesso.

Windows Picture and Fax Viewer, ad esempio, offre una serie di strumenti per la modifica delle annotazioni nelle immagini TIFF. A meno che questa funzionalità non venga duplicata nell'applicazione, è consigliabile non registrare l'applicazione per gestire le immagini TIFF. Il principio di guida deve essere per assicurarsi che l'utente non perda alcuna funzionalità.

## <a name="registering-for-the-preview-verb"></a>Registrazione per il verbo di anteprima

La registrazione di un'applicazione per gestire il verbo di anteprima è piuttosto semplice. Individuare il valore seguente dell'applicazione nel registro di sistema, dove Application. jpeg rappresenta il nome della chiave di associazione file dell'applicazione. per altre informazioni, vedere [programmi predefiniti](/windows/desktop/shell/default-programs) :

```
HKEY_CLASSES_ROOT
   Application.Jpeg
      shell
         open
            command
               (Default) = app.exe %1
```

Modificare il nome della sottochiave **Open** in "Preview" come illustrato di seguito.

```
HKEY_CLASSES_ROOT
   Application.Jpeg
      shell
         preview
            command
               (Default) = app.exe %1
```

Questa operazione consente di registrare l'applicazione e di impostarla come applicazione predefinita per il verbo di anteprima per un file con estensione jpg. È necessario anche quanto segue.

**HKEY \_ Classi \_ root** \\ **. jpg** \( predefinite) = Application. jpeg

## <a name="registering-for-the-edit-verb"></a>Registrazione per il verbo di modifica

Questa operazione consente di registrare un'applicazione per il verbo di modifica e di impostarla come nuova applicazione predefinita per la modifica di un'immagine. L'applicazione registrata dovrebbe assumere la funzionalità di modifica dell'applicazione predefinita esistente al momento dell'installazione e installarla nuovamente come gestore al momento della disinstallazione. Questa operazione può essere eseguita registrando la nuova applicazione più in basso nell'elenco di associazioni rispetto all'applicazione predefinita. L'applicazione predefinita è registrata qui:

```
HKEY_CLASSES_ROOT
   SystemFileAssociations
      image
         shell
            edit
               command
                  (Default) = app.exe %1
```

La nuova applicazione dovrebbe registrarsi qui:

```
HKEY_CLASSES_ROOT
   Application.Jpeg
      shell
         edit
            command
               (Default) = app.exe %1
```

## <a name="registering-for-the-slideshow-verb"></a>Registrazione per il verbo slideshow

A partire da Windows Vista, un'applicazione può anche registrare il verbo di **presentazione** . Le applicazioni che implementano una presentazione possono registrarsi per essere richiamate quando viene scelto il verbo di presentazione. Questa registrazione viene eseguita esattamente in modo analogo a quanto illustrato per il verbo di anteprima riportato sopra. È vivamente consigliabile che le applicazioni implementino il form DropTarget del verbo. In questo modo, è possibile passare un set completo di elementi. L'implementazione di DropTarget è registrata come illustrato di seguito:

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

[Informazioni su GDI+](../gdiplus/-gdiplus-about-gdi--about.md)
</dt> </dl>

 

 