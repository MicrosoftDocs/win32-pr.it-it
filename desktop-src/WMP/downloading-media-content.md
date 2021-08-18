---
title: Download di contenuto multimediale
description: Download di contenuto multimediale
ms.assetid: 0a057e13-6e0c-4a8f-9cab-051183e6b222
keywords:
- Windows Media Player negozi online, download di contenuti multimediali
- negozi online, download di contenuti multimediali
- tipo 1 negozi online, download di contenuti multimediali
- Windows Media Player negozi online, download di contenuti multimediali
- negozi online, download di contenuti multimediali
- tipo 1 negozi online, download di contenuti multimediali
- contenuto multimediale, download
- download di contenuto multimediale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a314dc4b59966fd779660a2c1ab26fc2b37d413e4add068f936a6109acd423a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997031"
---
# <a name="downloading-media-content"></a>Download di contenuto multimediale

Windows Media Player gestisce i download di file musicali per lo store online. Un download può essere avviato quando la pagina di individuazione chiama [External.download](external-download.md) o quando l'utente sceglie, nel lettore, di scaricare un set di tracce. In entrambi i casi, Windows Media Player chiama [IWMPContentPartner::D ownload](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-download), passando un elenco di contenitori di contenuto che descrive il set di tracce da scaricare e un cookie che rappresenta la transazione di download. Il plug-in partner del contenuto deve quindi chiamare [IWMPContentPartnerCallback::D ownloadTrack](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-downloadtrack) una volta per ogni traccia nel set. Quando il plug-in chiama **DownloadTrack,** passa **un HRESULT** nel *parametro hrDownload.* Se il plug-in passa un codice di esito positivo in *hrDownload,* Windows Media Player scarica la traccia. Se il plug-in passa un codice di errore in *hrDownload,* player non scarica la traccia. Per ogni chiamata a **Download,** il plug-in deve fornire il cookie della transazione e l'ID della traccia in questione. Per le tracce che verranno effettivamente scaricate, il plug-in deve fornire anche l'URL della traccia.

Dopo il download di un file, Windows Media Player automaticamente la libreria per riflettere la musica appena acquistata. Player fornisce informazioni sullo stato al plug-in sull'operazione di download chiamando [IWMPContentPartner::D ownloadTrackComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-downloadtrackcomplete). In questo metodo, Player fornisce un **HRESULT** per indicare l'esito positivo o negativo del download, l'ID traccia e la stringa dei parametri personalizzati forniti dal negozio online quando ha chiamato **DownloadTrack**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida per programmatori per i negozi online di tipo 1**](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




