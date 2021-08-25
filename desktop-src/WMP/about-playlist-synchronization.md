---
title: Informazioni sulla sincronizzazione delle playlist
description: Informazioni sulla sincronizzazione delle playlist
ms.assetid: bc7d52e0-7906-4b5b-82e6-a84e9c4f0ff0
keywords:
- Windows Media Player, sincronizzazione playlist
- Windows Media Player a oggetti, sincronizzazione playlist
- modello a oggetti, sincronizzazione playlist
- Windows Media Player ActiveX, sincronizzazione playlist
- ActiveX, sincronizzazione playlist
- Windows Media Player Controllo di ActiveX per dispositivi mobili, sincronizzazione playlist
- Windows Media Player dispositivi mobili, sincronizzazione playlist
- sincronizzazione di dispositivi, playlist
- sincronizzazione dei dispositivi, playlist
- playlist, sincronizzazione
- Windows playlist di metafile multimediali, sincronizzazione
- playlist di metafile, sincronizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe54bef188fea2baee64da962dabf4eb8f700b72407772d591d73f52be2d4289
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956871"
---
# <a name="about-playlist-synchronization"></a>Informazioni sulla sincronizzazione delle playlist

Windows Media Player 10 o versione successiva è progettato per sincronizzare il contenuto multimediale digitale con i dispositivi usando un modello di sincronizzazione playlist. Ciò significa che il contenuto destinato a essere copiato in un dispositivo deve far parte di una playlist. Quando l'utente sceglie di trasferire singoli contenuti multimediali digitali dal proprio computer a un dispositivo, Windows Media Player aggiunge il contenuto a una playlist predefinita per la copia.

Le WINDOWS MEDIA PLAYER di sincronizzazione dei dispositivi sono progettate per funzionare in questo modo. Come Windows Media Player, il programma può presentare all'utente un elenco di playlist definite dall'utente. È quindi possibile consentire all'utente di scegliere le playlist da sincronizzare con un determinato dispositivo e di impostare l'ordine di priorità per il processo di sincronizzazione.

Poiché i dispositivi portatili hanno una capacità di archiviazione limitata, l'utente può scegliere di sincronizzare più contenuti multimediali digitali di quelli che il dispositivo può archiviare. Windows Media Player sincronizza il contenuto in ordine di priorità. L'utente può definire l'ordine di priorità usando una finestra di dialogo a cui è possibile accedere dalla **funzionalità** Dispositivi. In risposta all'input dell'utente per il programma, è possibile modificare l'ordine di priorità a livello di codice modificando i valori di determinati attributi della playlist. Collettivamente, questi attributi sono detti *attributi di* sincronizzazione.

Ogni playlist in una libreria ha 16 attributi di sincronizzazione: **Da Sync01** a **Sync16.** Ogni attributo rappresenta il dispositivo con l'indice di relazione corrispondente. Il valore di ogni attributo indica due elementi:

-   Indica se la playlist deve essere sincronizzata con il dispositivo.
-   Valore di priorità per la playlist.

Il valore zero indica che Windows Media Player non deve tentare di sincronizzare la playlist con il dispositivo. Qualsiasi altro valore è un numero di priorità. I valori più bassi ricevono una priorità più alta al momento della sincronizzazione.

Le playlist hanno anche un **attributo SyncOnly** che indica se la playlist è disponibile solo per la sincronizzazione.

Anche i singoli elementi del contenuto multimediale digitale contengono metadati sulla sincronizzazione. Quando si recupera un **oggetto** Media dalla libreria, è possibile esaminare il valore dell'attributo **SyncState.** Questo attributo fornisce informazioni estese sul fatto che il contenuto sia stato copiato correttamente nel dispositivo o se la copia del contenuto non è riuscita perché non è adatta.

> [!Note]  
> È consigliabile evitare di fornire elementi dell'interfaccia utente che consentono all'utente di creare playlist da tutto il contenuto della libreria per la sincronizzazione.

 

Per ottimizzare le prestazioni, Windows Media Player un set di regole per la creazione di playlist di sincronizzazione. Il programma deve creare solo playlist di sincronizzazione per il contenuto fornito. Consente Windows Media Player creare playlist di sincronizzazione per il contenuto che l'utente ha aggiunto alla raccolta da altre origini.

In alternativa alla creazione di un'interfaccia utente di playlist personalizzata, è possibile presentare agli utenti una finestra di dialogo predefinita per la scelta delle playlist e la gestione della relazione per un dispositivo. A tale scopo, chiamare [IWMPSyncDevice::showSettings](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-showsettings). Quando si richiama questo metodo, Windows Media Player finestra di dialogo delle impostazioni di sincronizzazione. Quando l'utente chiude la finestra di dialogo, Windows Media Player torna automaticamente allo stato di ancoraggio precedente e restituisce il controllo al programma remoto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sulla sincronizzazione dei dispositivi**](about-device-synchronization.md)
</dt> <dt>

[**Gestione delle playlist di sincronizzazione**](managing-synchronization-playlists.md)
</dt> <dt>

[**Attributi della playlist**](playlist-attributes.md)
</dt> </dl>

 

 




