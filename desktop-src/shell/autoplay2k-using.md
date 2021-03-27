---
description: Quando la shell rileva l'inserimento di nuovi supporti o l'allegato di un dispositivo a collegamento a caldo, vengono determinati il contenuto del dispositivo o del supporto. AutoPlay, a seconda delle impostazioni correnti, esegue una delle operazioni seguenti.
title: Uso e configurazione di AutoPlay
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 096c7042-8cf0-4e4f-934f-274564218f4c
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 04a4f6dd09e03f26b13649e860beb7f2621ce952
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750303"
---
# <a name="using-and-configuring-autoplay"></a>Uso e configurazione di AutoPlay

Quando la shell rileva l'inserimento di nuovi supporti o l'allegato di un dispositivo a collegamento a caldo, vengono determinati il contenuto del dispositivo o del supporto. AutoPlay, a seconda delle impostazioni correnti, esegue una delle operazioni seguenti.

-   Riproduce automaticamente il contenuto.
-   Visualizza una finestra di dialogo in cui viene richiesto all'utente di scegliere un gestore predefinito per un singolo tipo di contenuto.
-   Presenta, nel caso di contenuto misto, un elenco di applicazioni di gestione disponibili da avviare. Il gestore scelto quindi riproduce automaticamente il tipo di contenuto associato.
-   Visualizza una visualizzazione cartella standard dei file.
-   Non esegue alcuna operazione se, in precedenza, l'utente ha scelto di **non eseguire alcuna azione** per quel tipo di contenuto, così come specificato, **eseguire sempre l'azione selezionata**.

Se il contenuto non soddisfa i criteri per AutoPlay, l'evento viene quindi passato a Windows Image Acquisition (WIA).

Gli argomenti seguenti illustrano l'installazione e l'uso di AutoPlay.

-   [Preparazione dell'hardware e del software per l'uso con AutoPlay](#preparing-hardware-and-software-for-use-with-autoplay)
-   [Modalità di ricerca di AutoPlay nei supporti](#how-autoplay-searches-media)
-   [Definizione di tipi di contenuto singoli e misti](#defining-single-and-mixed-content-types)
-   [Scenari di esempio](#sample-scenarios)
    -   [AutoPlay per i dispositivi di archiviazione con supporti immagine](#autoplay-for-storage-devices-with-picture-media)
    -   [AutoPlay per la riproduzione di file musicali e dispositivi di archiviazione contenenti supporti musicali](#autoplay-for-music-file-playback-devices-and-storage-devices-containing-music-media)
    -   [AutoPlay per la riproduzione video nella prima presentazione](#autoplay-for-video-playback-on-first-presentation)
-   [Assegnazione di applicazioni gestore predefinite](#assigning-default-handler-applications)
-   [Gestione di supporti contenenti tipi di contenuto misto](#handling-media-containing-mixed-content-types)
-   [Interfacce utente AutoPlay](#autoplay-user-interfaces)
    -   [Finestra di dialogo tipo di contenuto singolo](#single-content-type-dialog-box)
    -   [Finestra di dialogo supporto misto](#mixed-media-dialog-box)
    -   [Pagina Proprietà](#property-page)

## <a name="preparing-hardware-and-software-for-use-with-autoplay"></a>Preparazione dell'hardware e del software per l'uso con AutoPlay

Per il funzionamento di AutoPlay è necessario che nel registro di sistema siano presenti diverse informazioni. Queste informazioni interagiscono e fanno riferimento l'uno all'altro per formare l'intero ambiente AutoPlay. In questo documento viene illustrata la configurazione di ognuna di queste informazioni come una singola procedura autonoma.

Per altre istruzioni, vedere gli argomenti seguenti.

-   [Come assegnare un gestore di dispositivo a un dispositivo](how-to-assign-a-device-handler-to-a-device.md)
-   [Come specificare un'icona, un'etichetta o un gestore di dispositivo per un dispositivo usando un gruppo di dispositivi](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-group.md)
-   [Come specificare un'icona, un'etichetta o un gestore di dispositivo per un dispositivo usando una classe Device](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-class.md)
-   [Come impedire AutoPlay per un componente](how-to-prevent-autoplay-for-a-component.md)
-   [Come registrare un gestore per un evento del dispositivo](how-to-register-a-handler-for-a-device-event.md)
-   [Come usare gli eventi AutoPlay nelle applicazioni in esecuzione](how-to-use-autoplay-events-in-running-applications.md)
-   [Come registrare un gestore eventi](how-to-register-an-event-handler.md)

## <a name="how-autoplay-searches-media"></a>Modalità di ricerca di AutoPlay nei supporti

AutoPlay Cerca i media di quattro livelli di directory sotto la directory radice per trovare i tipi di file noti. Usa il valore PerceivedType associato a un'estensione del nome di file nel registro di sistema per determinare la categoria di file, sia che si tratti di un'immagine, di un file audio o di un file video. Con queste informazioni, AutoPlay avvia il gestore appropriato per il dispositivo e il tipo di file. Per ulteriori informazioni, vedere la pagina relativa alla [registrazione delle applicazioni e dei tipi percepiti](fa-perceivedtypes.md).

## <a name="defining-single-and-mixed-content-types"></a>Definizione di tipi di contenuto singoli e misti

AutoPlay definisce tre categorie di contenuto principali.

-   Immagini
-   Musica
-   Video

Se tutti i file nel supporto rientrano in una sola di queste tre categorie, viene considerato un supporto di tipo contenuto singolo. Si noti che questo non significa che i file devono avere lo stesso tipo di *file* ; jpg, gif e BMP sono tipi di file diversi, ma un tipo di contenuto (immagini).

Se i tipi di contenuto supportati sono presenti sul supporto, ma nessun tipo di contenuto singolo può tenere conto del 100% del totale, il supporto viene considerato che contiene il tipo di contenuto misto e viene gestito di conseguenza. Per ulteriori informazioni, vedere [gestione di supporti contenenti tipi di contenuto misti](#handling-media-containing-mixed-content-types).

## <a name="sample-scenarios"></a>Scenari di esempio

Negli scenari seguenti viene fornita una conoscenza di base di ciò che si prevede da AutoPlay.

### <a name="autoplay-for-storage-devices-with-picture-media"></a>AutoPlay per i dispositivi di archiviazione con supporti immagine

1.  L'utente connette un dispositivo USB SanDisk CompactFlash Reader che dispone già di un supporto inserito contenente il tipo di contenuto immagine del 100% sotto forma di file con estensione jpg.
2.  Sono stati **trovati nuovi componenti hardware-SanDisk ImageMate**.
3.  AutoPlay avvia l'applicazione di immagine appropriata.

Analogamente, quando l'utente inserisce lo stesso supporto CompactFlash nel lettore quando il lettore è già collegato al sistema, l'evento media INSERT fa sì che AutoPlay avvii l'applicazione di presentazione dell'immagine. L'utente ha la possibilità di passare alla pagina delle proprietà del dispositivo multimediale SanDisk per modificare il valore predefinito in un'altra applicazione di riproduzione automatica registrata, ad esempio la procedura guidata per lo scanner e la fotocamera o l'immagine.

### <a name="autoplay-for-music-file-playback-devices-and-storage-devices-containing-music-media"></a>AutoPlay per la riproduzione di file musicali e dispositivi di archiviazione contenenti supporti musicali

1.  L'utente connette un lettore USB Diamond Rio MP3.
2.  Viene visualizzato un **nuovo lettore hardware Diamond Rio MP3**.
3.  AutoPlay riproduce i file utilizzando il gestore predefinito registrato, ad esempio Windows Media Player.

Analogamente, se l'utente inserisce contenuti multimediali contenenti file con estensione MP3 (ad esempio, CompactFlash, SmartMedia, Memory Stick o CD-ROM) che rappresentano il 100% del contenuto supportato totale in un dispositivo di archiviazione, l'evento media INSERT genera anche la riproduzione automatica dei file con Windows Media Player. L'utente può accedere alla finestra delle proprietà del dispositivo di archiviazione e modificare l'azione predefinita in un'altra applicazione AutoPlay registrata, ad esempio WinAmp o Real Player.

### <a name="autoplay-for-video-playback-on-first-presentation"></a>AutoPlay per la riproduzione video nella prima presentazione

1.  L'utente inserisce una videocamera digitale 1394 per la prima volta.
2.  All'utente viene visualizzata una semplice finestra di dialogo in cui viene chiesto quale applicazione eseguire. È possibile scegliere di eseguire una delle applicazioni AutoPlay registrate o di aprire una cartella per visualizzare i file. L'utente può impostare il comportamento selezionato in modo che venga salvato come azione predefinita per gli eventi di collegamento rapido della fotocamera video digitale successiva.

## <a name="assigning-default-handler-applications"></a>Assegnazione di applicazioni gestore predefinite

Una nuova installazione di Windows trova AutoPlay con un set di applicazioni gestore registrate. Le applicazioni registrate per impostazione predefinita durante un'installazione di Windows sono le seguenti.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tipo supporto</th>
<th>Applicazioni</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Immagini</td>
<td><ul>
<li>Slide Show (impostazione predefinita)</li>
<li>Creazione guidata fotocamera e scanner</li>
<li>Stampa guidata</li>
<li>Aprire la cartella</li>
</ul></td>
</tr>
<tr class="even">
<td>Musica</td>
<td><ul>
<li>Windows Media Player (impostazione predefinita)</li>
<li>Aprire la cartella</li>
</ul></td>
</tr>
<tr class="odd">
<td>Video</td>
<td><ul>
<li>Windows Media Player (impostazione predefinita)</li>
<li>Aprire la cartella</li>
</ul></td>
</tr>
</tbody>
</table>



 

Nel caso di tipi non supportati, agli utenti viene richiesto di assegnare l'impostazione predefinita per l'azione AutoPlay associata a ogni dispositivo di archiviazione alla prima introduzione al sistema. A questo punto, all'utente viene richiesto di scegliere un'azione da un elenco fornito di applicazioni registrate o di visualizzare una visualizzazione di cartelle in cui è elencato il contenuto multimediale. L'utente ha anche la possibilità di scegliere di essere richiesto ogni volta che viene rilevato il tipo di supporto, anziché salvare un'applicazione specifica come predefinita.

> [!Note]  
> I produttori di dispositivi hanno la possibilità di registrare e assegnare applicazioni predefinite da usare con i prodotti specifici. In questi casi, la finestra di dialogo che offre una scelta all'utente non viene visualizzata.

 

Per essere offerta come opzione del gestore da AutoPlay, le applicazioni appena installate devono registrarsi nel registro di sistema. Per informazioni dettagliate, vedere [preparazione dell'hardware e del software per l'uso con AutoPlay](#preparing-hardware-and-software-for-use-with-autoplay).

Gli utenti possono sempre modificare il gestore AutoPlay predefinito per qualsiasi dispositivo di archiviazione o tipo di contenuto. La pagina delle proprietà AutoPlay è accessibile per le modifiche nella finestra delle proprietà del dispositivo di archiviazione in **computer locale**.

Per esempi di richieste utente e pagine delle proprietà, vedere [AutoPlay User Interfaces](#autoplay-user-interfaces).

## <a name="handling-media-containing-mixed-content-types"></a>Gestione di supporti contenenti tipi di contenuto misto

Quando AutoPlay viene visualizzato con un supporto misto per il contenuto, richiede l'input dell'utente prima di poter eseguire un'azione. In questo caso, all'utente viene visualizzata una finestra di dialogo contenente un elenco filtrato di tutte le applicazioni registrate appropriate disponibili per i tipi di contenuto presenti nei supporti. L'utente può scegliere una di queste applicazioni per AutoPlay quel particolare tipo di contenuto, mentre il resto rimane invariato. Poiché la composizione di un supporto di contenuto misto varia a seconda del singolo disco, non è possibile salvare questa opzione come impostazione predefinita.

Per esempi di prompt utente, vedere [interfacce utente AutoPlay](#autoplay-user-interfaces).

## <a name="autoplay-user-interfaces"></a>Interfacce utente AutoPlay

Sono disponibili tre interfacce utente possibili.

-   Finestra di dialogo in cui viene richiesto all'utente di immettere un'azione per un singolo tipo di contenuto
-   Finestra di dialogo in cui viene richiesto all'utente di immettere un'azione per i tipi di contenuto misto
-   Una pagina delle proprietà

### <a name="single-content-type-dialog-box"></a>Finestra di dialogo tipo di contenuto singolo

Una finestra di dialogo simile alla seguente viene visualizzata quando un supporto supportato non ancora assegnato a un'azione AutoPlay predefinita viene presentato al sistema.

![screenshot della finestra di dialogo tipo di contenuto singolo](images/pix.png)

Gli utenti possono eseguire una delle operazioni seguenti.

-   Scegliere un'azione dall'elenco di applicazioni registrate.
-   Elencare i file sul supporto in una normale visualizzazione cartelle.
-   Non eseguire alcuna azione.

Un utente può anche salvare una scelta come azione predefinita per questo supporto facendo clic sulla casella **Esegui sempre l'azione selezionata** . Una volta effettuata questa scelta, la finestra di dialogo non viene visualizzata nuovamente. Tuttavia, in Windows XP Service Pack 1 (SP1), se al computer viene aggiunta una nuova applicazione in grado di gestire un particolare tipo di supporto, la finestra di dialogo viene nuovamente presentata all'utente, offrendo loro la possibilità di selezionare la nuova applicazione come azione AutoPlay predefinita. Le applicazioni possono inoltre impostare se stesse come selezione predefinita al momento dell'installazione.

Windows XP SP1 aggiunge inoltre una funzionalità che mantiene la scelta dell'azione AutoPlay da parte dell'utente se non fa clic sulla casella **Esegui sempre l'azione selezionata** . Se un utente sceglie un'azione AutoPlay per una singola istanza, alla successiva visualizzazione della finestra di dialogo per quel tipo di supporto, la stessa azione è la selezione predefinita.

Per includere un'applicazione nell'elenco delle azioni possibili, è necessario registrarla con AutoPlay. Per altre informazioni, vedere [preparazione dell'hardware e del software per l'uso con AutoPlay](#preparing-hardware-and-software-for-use-with-autoplay).

### <a name="mixed-media-dialog-box"></a>Finestra di dialogo supporto misto

La finestra di dialogo seguente viene visualizzata quando al sistema vengono presentati tutti i supporti che contengono una combinazione di tipi di file supportati. Si tratta essenzialmente della finestra di dialogo Media contenuto singolo, ma con due differenze significative. In primo luogo, le opzioni di azione disponibili sono costituite da un elenco filtrato di applicazioni rilevanti per tutti i tipi di contenuto presenti sul supporto. In secondo luogo, non è possibile scegliere un'azione predefinita permanente perché i tipi di contenuto e le percentuali di supporti di contenuto misto sono troppo imprevedibili.

![screenshot della finestra di dialogo supporto misto](images/mix.png)

Per includere un'applicazione nell'elenco delle azioni possibili, è necessario registrarla con AutoPlay. Per altre informazioni, vedere [preparazione dell'hardware e del software per l'uso con AutoPlay](#preparing-hardware-and-software-for-use-with-autoplay).

### <a name="property-page"></a>Pagina Proprietà

Di seguito è riportato un esempio di pagina delle proprietà AutoPlay per un dispositivo DVD/CD-ROM.

![screenshot della pagina delle proprietà](images/apdlg.png)

Ogni tipo di dispositivo offre un subset appropriato di tipi di contenuto per la configurazione AutoPlay. A sua volta, ogni tipo di contenuto, se selezionato, offre un elenco appropriato di opzioni di azione nella casella di riepilogo. È possibile scegliere un'azione diversa per ogni tipo di contenuto.

 

 



