---
title: Download del contenuto multimediale
description: Download del contenuto multimediale
ms.assetid: 0a057e13-6e0c-4a8f-9cab-051183e6b222
keywords:
- Windows Media Player Online Stores, download del contenuto multimediale
- negozi online, download di contenuti multimediali
- digitare 1 negozi online, download del contenuto multimediale
- Windows Media Player Online Stores, download di contenuti multimediali
- negozi online, download di contenuti multimediali
- digitare 1 negozi online, download di contenuti multimediali
- contenuti multimediali, download
- Download del contenuto multimediale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00efe44f2bac25a9eeda86f6adcc78b34beea7cd
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/21/2020
ms.locfileid: "104398750"
---
# <a name="downloading-media-content"></a>Download del contenuto multimediale

Windows Media Player gestisce i download dei file musicali per lo Store online. È possibile avviare un download quando la pagina di individuazione chiama [External. download](external-download.md) o quando l'utente sceglie, nel lettore, di scaricare un set di tracce. In entrambi i casi, Windows Media Player chiama [IWMPContentPartner::D ownload](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-download), passando un elenco di contenitori di contenuto che descrive il set di tracce da scaricare e un cookie che rappresenta la transazione di download. Il plug-in del partner di contenuti deve quindi chiamare [IWMPContentPartnerCallback::D ownloadtrack](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-downloadtrack) una volta per ogni traccia nel set. Quando il plug-in chiama **DownloadTrack**, viene passato un valore **HRESULT** nel parametro *hrDownload* . Se il plug-in passa un codice di esito positivo in *hrDownload*, Windows Media Player Scarica la traccia. Se il plug-in passa un codice di errore in *hrDownload*, il lettore non Scarica la traccia. Per ogni chiamata a **download**, il plug-in deve fornire il cookie di transazione e l'ID della traccia in questione. Per le tracce che verranno effettivamente scaricate, il plug-in deve fornire anche l'URL della traccia.

Dopo il download di un file, Windows Media Player aggiorna automaticamente la libreria in modo da riflettere la musica appena acquistata. Il lettore fornisce informazioni sullo stato per il plug-in sull'operazione di download chiamando [IWMPContentPartner::D ownloadtrackcomplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-downloadtrackcomplete). In questo metodo, il lettore fornisce un **HRESULT** per indicare l'esito positivo o negativo del download, l'ID di traccia e la stringa di parametri personalizzati fornita dal negozio online quando ha chiamato **DownloadTrack**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida per programmatori per i negozi di tipo 1 online**](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




