---
description: Uso Windows supporti in DirectShow
ms.assetid: 2fae0504-d1da-413a-80dd-de7818f506ef
title: Uso Windows supporti in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fea308943d4be732c75e774d3e0c3cb09ac7c6609a8399d2e6eca4666d99e6b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118651087"
---
# <a name="using-windows-media-in-directshow"></a>Uso Windows supporti in DirectShow

Questa sezione descrive come usare DirectShow per riprodurre e scrivere file ASF (Advanced Systems Format). I file ASF contengono in genere contenuto audio e video codificato Windows codec audio e video multimediali. Tuttavia, ASF può contenere qualsiasi tipo di dati.

I filtri DirectShow seguenti supportano la lettura e la scrittura di file ASF:

-   [Filtro lettore ASF WM](wm-asf-reader-filter.md). Legge i file ASF.
-   [Filtro del writer ASF WM.](wm-asf-writer-filter.md) File ASF Wrties.
-   [DMO filtro wrapper](dmo-wrapper-filter.md). Esegue il wrapping Windows codificatore multimediale e decodificatore DMO.

### <a name="versions"></a>Versioni

I filtri WM ASF Reader e WM ASF Writer sono in pacchetto nella DLL denominata qasf.dll e i filtri sono denominati collettivamente "componenti QASF". Questi filtri sono wrapper per l'SDK Windows Media Format. La DLL (qasf.dll) è stata pubblicata per la prima volta in DirectX SDK, ma in seguito è stata aggiornata in Windows Media Format SDK. Ecco la cronologia delle versioni dei filtri QASF:

-   DirectShow 8.1 supporta Windows Media Format SDK versione 7.0.
-   DirectShow 9.0 supporta Windows Media Format SDK versione 7.1.
-   Windows XP Service Pack 2 supporta Windows Media Format 9 SDK.
-   Windows Vista supporta Windows Media Format 11 SDK.
-   Windows Media Format 9 SDK e versioni successive contengono versioni corrispondenti di QASF.

Per ottenere la versione più recente di QASF, scaricare sempre la versione più recente Windows Media Format SDK.

### <a name="legacy-windows-media-source-filter"></a>Filtro origine Windows file multimediali legacy

In Windows XP Service Pack 1 e versioni precedenti, il filtro di origine predefinito per i file ASF (con estensione asf, wmv e wma) è il filtro origine multimediale [Windows obsoleto.](windows-media-source-filter.md) Questo comportamento è stato mantenuto per garantire la compatibilità con le versioni precedenti con le applicazioni che Windows Media Player 6.4. Le nuove applicazioni devono usare le versioni più recenti di QASF, che fanno filtrare wm ASF Reader come filtro predefinito per la riproduzione di file ASF.

Per altre informazioni sulla suite Windows media di software development kit, vedere la sezione [Audio e video](../audio-and-video.md) della libreria MDSN.

Questo articolo contiene gli argomenti seguenti:

-   [Lettura di file ASF in DirectShow](reading-asf-files-in-directshow.md)
-   [Creazione di file ASF in DirectShow](creating-asf-files-in-directshow.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di DirectShow](using-directshow.md)
</dt> </dl>

 

 
