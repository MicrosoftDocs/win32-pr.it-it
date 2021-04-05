---
title: Flussi audio
description: Flussi audio
ms.assetid: 7bb39c48-5d0b-483d-83ee-946adfc9724f
keywords:
- Windows Media Player Online Store, flussi audio
- archivi online, flussi audio
- digitare 1 negozi online, flussi audio
- Windows Media Player Online Stores, flussi da server musicali
- archivi online, flussi da server musicali
- digitare 1 archivi online, flussi da server musicali
- Windows Media Player Online Stores, flussi server musicali
- archivi online, flussi di server musicali
- digitare 1 archivi online, flussi di server musicali
- flussi audio
- flussi di Music Server
- flussi da server musicali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7164a703417e2efb8e32b2632890972957f7adf7
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104046333"
---
# <a name="audio-streams"></a>Flussi audio

Gli archivi online possono fornire musica come flusso da un server musicale. Questa operazione è utile per fornire esempi, articoli promozionali speciali o per consentire agli utenti della sottoscrizione di usufruire di musica senza dover scaricare il contenuto. Spesso non è possibile archiviare l'URL del flusso come parte del catalogo musicale, bensì per risolvere l'URL immediatamente prima della riproduzione in base all'ID traccia. Per abilitare questa operazione, Windows Media Player chiama [IWMPContentPartner:: GetStreamingURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getstreamingurl) e fornisce il tipo di flusso (come valore di enumerazione [WMPStreamingType](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmpstreamingtype) ) e l'ID per il flusso. Il plug-in restituisce l'URL per il flusso tramite il parametro *pbstrURL* .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sugli archivi online di tipo 1**](about-type-1-online-stores.md)
</dt> </dl>

 

 




