---
title: Masterizzazione di playlist contenenti file protetti
description: Masterizzazione di playlist contenenti file protetti
ms.assetid: 0d9415a1-a154-4fe4-af4c-cce4cb05ade5
keywords:
- Windows Media Format SDK, masterizzare playlist con file protetti
- Windows Media Format SDK, playlist con file protetti
- ASF (Advanced Systems Format), masterizzazione di playlist con file protetti
- ASF (Advanced Systems Format), masterizzazione di playlist con file protetti
- ASF (Advanced Systems Format), playlist con file protetti
- ASF (Advanced Systems Format), playlist con file protetti
- Digital Rights Management (DRM), masterizzare playlist con file protetti
- DRM (Digital Rights Management), masterizzare playlist con file protetti
- Digital Rights Management (DRM), playlist con file protetti
- DRM (Digital Rights Management), playlist con file protetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 214c1dbd4ee08f90b3e5e8aa6186508af5044f29
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/21/2020
ms.locfileid: "106299502"
---
# <a name="burning-playlists-that-contain-secure-files"></a>Masterizzazione di playlist contenenti file protetti

Le licenze create con gli oggetti di Windows Media Rights Manager 10 SDK possono specificare il diritto di copiare un file in Compact disk come parte di una playlist. Questa funzionalità, denominata playlist Burning, richiede la verifica delle licenze di tutti i file nella playlist prima di iniziare a copiare i dati. Windows Media Format SDK fornisce l'interfaccia [**IWMReaderPlaylistBurn**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderplaylistburn) per eseguire la verifica dei file.

Per implementare la masterizzazione della playlist, seguire questa procedura:

1.  Creare un'istanza dell'oggetto Reader o l'oggetto Reader sincrono. Per ulteriori informazioni, vedere la pagina relativa alla [lettura di file ASF](reading-asf-files.md).
2.  Chiamare il metodo **QueryInterface** dell'interfaccia Reader ([**IWMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader) o [**IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)) per ottenere un puntatore all'interfaccia [**IWMReaderPlaylistBurn**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderplaylistburn) .
3.  Copiare i nomi dei file dalla playlist in una matrice di stringhe a caratteri wide. I nomi di file nella matrice devono essere nello stesso ordine in cui compaiono nella playlist.
4.  Chiamare il metodo [**IWMReaderPlaylistBurn:: InitPlaylistBurn**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-initplaylistburn) , passando un puntatore alla matrice creata nel passaggio 3, per inizializzare la verifica della licenza per i file.
5.  Al termine della verifica della licenza, l'oggetto Reader Invia un \_ \_ \_ messaggio di masterizzazione della playlist WMT init all'implementazione del metodo [**IWMStatusCallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) callback. Quando il callback riceve questo messaggio, chiamare il metodo [**IWMReaderPlaylistBurn:: GetInitResults**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-getinitresults) per ottenere i risultati del controllo della licenza. Questo metodo accetta una matrice di variabili **HRESULT** che corrispondono ai nomi di file nella matrice passata a **InitPlaylistBurn**. Se tutti i valori nella matrice di risultati sono uguali a S \_ OK, è possibile continuare. Se il risultato è un codice di errore, la playlist non deve essere copiata.
6.  Utilizzando la stessa istanza del lettore, aprire e leggere ogni file. È necessario aprire i file nell'ordine in cui sono stati visualizzati i nomi dei file nella matrice di nomi di file passata a **InitPlaylistBurn**.
7.  Dopo aver copiato tutti i file nella playlist, chiamare [**IWMReaderPlaylistBurn:: EndPlaylistBurn**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-endplaylistburn) per completare il processo di masterizzazione della playlist e liberare le risorse usate dal reader.

> [!Note]  
> Il DRM non è supportato dalla versione basata su x64 di questo SDK.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Abilitazione del supporto DRM**](enabling-drm-support.md)
</dt> </dl>

 

 




