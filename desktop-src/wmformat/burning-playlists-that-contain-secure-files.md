---
title: Masterizzazione di playlist contenenti file protetti
description: Masterizzazione di playlist contenenti file protetti
ms.assetid: 0d9415a1-a154-4fe4-af4c-cce4cb05ade5
keywords:
- Windows Media Format SDK, playlist di riproduzione con file protetti
- Windows Media Format SDK, playlist con file protetti
- Advanced Systems Format (ASF), playlist di riproduzione con file protetti
- ASF (Advanced Systems Format), playlist di riproduzione con file protetti
- Advanced Systems Format (ASF), playlist con file protetti
- ASF (Advanced Systems Format), playlist con file protetti
- DRM (Digital Rights Management), playlist di riproduzione con file protetti
- DRM (Digital Rights Management), playlist di riproduzione con file protetti
- DRM (Digital Rights Management), playlist con file protetti
- DRM (Digital Rights Management),playlist con file protetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6d43cfbf3bb6e8ce4bac5cc1006fe73292988547ef2fc35289a4ced13e6f0d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028119"
---
# <a name="burning-playlists-that-contain-secure-files"></a>Masterizzazione di playlist contenenti file protetti

Le licenze create usando gli oggetti di Windows Media Rights Manager 10 SDK possono specificare il diritto di copiare un file compact disc come parte di una playlist. Questa funzionalità, denominata playlist di riproduzione, richiede la verifica delle licenze di tutti i file nella playlist prima di iniziare a copiare i dati. L Windows Media Format SDK fornisce [**l'interfaccia IWMReaderPlaylistPlaylist Per**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderplaylistburn) eseguire automaticamente la verifica dei file.

Per implementare la riproduzione della playlist, seguire questa procedura:

1.  Creare un'istanza dell'oggetto reader o l'oggetto lettore sincrono. Per altre informazioni, vedere [Lettura di file ASF.](reading-asf-files.md)
2.  Chiamare il **metodo QueryInterface** dell'interfaccia del lettore ([**IWMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader) o [**IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)) per ottenere un puntatore all'interfaccia [**IWMReaderPlaylistInterface.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderplaylistburn)
3.  Copiare i nomi file dalla playlist in una matrice di stringhe di caratteri wide. I nomi di file nella matrice devono essere nello stesso ordine in cui appaiono nella playlist.
4.  Chiamare il [**metodo IWMReaderPlaylistComb::InitPlaylistCombo,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-initplaylistburn) passando un puntatore alla matrice creata nel passaggio 3, per inizializzare la verifica della licenza per i file.
5.  Al termine della verifica della licenza, l'oggetto reader invia un messaggio WMT INIT PLAYLIST BURN all'implementazione del metodo \_ \_ di callback \_ [**IWMStatusCallback::OnStatus.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) Quando il callback riceve questo messaggio, chiamare il metodo [**IWMReaderPlaylistComb::GetInitResults**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-getinitresults) per ottenere i risultati del controllo della licenza. Questo metodo accetta una matrice di **variabili HRESULT** che corrispondono ai nomi file nella matrice passata **a InitPlaylist Rielen.** Se tutti i valori nella matrice dei risultati sono uguali a S \_ OK, è possibile continuare. Se un risultato è un codice di errore, la playlist non deve essere copiata.
6.  Usando la stessa istanza del lettore, aprire e leggere ogni file. È necessario aprire i file nell'ordine in cui i nomi dei file sono visualizzati nella matrice di nomi di file passata **a InitPlaylistPlaylist.**
7.  Dopo aver copiato tutti i file nella playlist, chiamare [**IWMReaderPlaylist Playlist::EndPlaylist Playlist**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-endplaylistburn) per completare il processo di masterizzazione della playlist e liberare le risorse usate dal lettore.

> [!Note]  
> DRM non è supportato dalla versione basata su x64 di questo SDK.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Abilitazione del supporto DRM**](enabling-drm-support.md)
</dt> </dl>

 

 




