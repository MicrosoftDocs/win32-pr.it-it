---
title: Informazioni sulla sincronizzazione della playlist
description: Informazioni sulla sincronizzazione della playlist
ms.assetid: bc7d52e0-7906-4b5b-82e6-a84e9c4f0ff0
keywords:
- Windows Media Player, sincronizzazione playlist
- Modello a oggetti di Windows Media Player, sincronizzazione della playlist
- modello a oggetti, sincronizzazione della playlist
- Controllo ActiveX Windows Media Player, sincronizzazione playlist
- Controllo ActiveX, sincronizzazione playlist
- Controllo ActiveX Windows Media Player Mobile, sincronizzazione playlist
- Windows Media Player Mobile, sincronizzazione playlist
- sincronizzazione di dispositivi, playlist
- sincronizzazione dei dispositivi, playlist
- playlist, sincronizzazione
- Playlist di Windows Media Metafile, sincronizzazione
- playlist di metafile, sincronizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecc019b31518fda1a49c8d3ae86f2d03c4ecefc8
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104336289"
---
# <a name="about-playlist-synchronization"></a>Informazioni sulla sincronizzazione della playlist

Windows Media Player 10 o versione successiva è progettato per sincronizzare il contenuto multimediale digitale con i dispositivi usando un modello di sincronizzazione della playlist. Ciò significa che il contenuto destinato a essere copiato in un dispositivo deve essere parte di una playlist. Quando l'utente sceglie di trasferire singoli contenuti multimediali digitali dal proprio computer a un dispositivo, Windows Media Player aggiunge il contenuto a una playlist predefinita per la copia.

Le API di sincronizzazione dei dispositivi Windows Media Player sono progettate per funzionare anche in questo modo. Analogamente a Windows Media Player, il programma può presentare all'utente un elenco di playlist che ha definito. È quindi possibile consentire all'utente di scegliere quali playlist sincronizzare con un determinato dispositivo e impostare l'ordine di priorità per il processo di sincronizzazione.

Poiché i dispositivi portatili hanno una capacità di archiviazione limitata, è possibile che l'utente scelga di sincronizzare un contenuto multimediale più digitale rispetto a quello che il dispositivo può archiviare. Windows Media Player sincronizza il contenuto in ordine di priorità. L'utente può definire l'ordine di priorità utilizzando una finestra di dialogo a cui è possibile accedere dalla funzionalità **dispositivi** . In risposta all'input dell'utente per il programma, è possibile modificare l'ordine di priorità a livello di codice modificando i valori di determinati attributi della playlist. Insieme, questi attributi sono detti attributi di *sincronizzazione* .

Ogni playlist in una raccolta ha 16 attributi di sincronizzazione: da **Sync01** a **Sync16**. Ogni attributo rappresenta il dispositivo con l'indice di partnership corrispondente. Il valore di ogni attributo indica due elementi:

-   Indica se la playlist deve essere sincronizzata con il dispositivo.
-   Valore di priorità per la playlist.

Un valore pari a zero indica che Windows Media Player non deve tentare di sincronizzare la playlist con il dispositivo. Qualsiasi altro valore è un numero di priorità. I valori inferiori ricevono una priorità più elevata al momento della sincronizzazione.

Le playlist hanno anche un attributo **SyncOnly** che indica se la playlist è disponibile solo per la sincronizzazione.

I singoli elementi del contenuto multimediale digitale contengono anche i metadati relativi alla sincronizzazione. Quando si recupera un oggetto **multimediale** dalla libreria, è possibile controllare il valore dell'attributo **SyncState** . Questo attributo fornisce informazioni estese sul fatto che il contenuto sia stato copiato correttamente nel dispositivo o che la copia del contenuto non sia riuscita perché non è sufficiente.

> [!Note]  
> È consigliabile evitare di fornire elementi dell'interfaccia utente che consentono all'utente di creare playlist da tutto il contenuto della libreria per la sincronizzazione.

 

Per ottimizzare le prestazioni, Windows Media Player impone un set di regole per la creazione di playlist di sincronizzazione. Il programma deve creare solo playlist di sincronizzazione per il contenuto fornito. Consenti a Windows Media Player di creare playlist di sincronizzazione per il contenuto aggiunto dall'utente alla libreria da altre origini.

In alternativa alla creazione di una propria interfaccia utente della playlist, è possibile presentare agli utenti una finestra di dialogo predefinita per la scelta delle playlist e la gestione della partnership per un dispositivo. A tale scopo, chiamare [IWMPSyncDevice:: ShowSettings](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-showsettings). Quando si richiama questo metodo, Windows Media Player Visualizza la finestra di dialogo Impostazioni di sincronizzazione. Quando l'utente chiude la finestra di dialogo, Windows Media Player torna automaticamente allo stato di ancoraggio precedente e passa di nuovo il controllo al programma remoto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sulla sincronizzazione dei dispositivi**](about-device-synchronization.md)
</dt> <dt>

[**Gestione delle playlist di sincronizzazione**](managing-synchronization-playlists.md)
</dt> <dt>

[**Attributi della playlist**](playlist-attributes.md)
</dt> </dl>

 

 




