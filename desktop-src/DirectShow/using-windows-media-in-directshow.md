---
description: Uso di Windows Media in DirectShow
ms.assetid: 2fae0504-d1da-413a-80dd-de7818f506ef
title: Uso di Windows Media in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e73726f0d7251f1c19beee05cfd8f335d3fdd7a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104401828"
---
# <a name="using-windows-media-in-directshow"></a>Uso di Windows Media in DirectShow

In questa sezione viene descritto come utilizzare DirectShow per riprodurre e scrivere file con estensione ASF (Advanced Systems Format). I file ASF contengono in genere contenuti audio e video codificati con i codec Windows Media Audio e video. Tuttavia, ASF può contenere qualsiasi tipo di dati.

I filtri DirectShow seguenti supportano la lettura e la scrittura di file ASF:

-   [Filtro di lettura ASF WM](wm-asf-reader-filter.md). Legge i file ASF.
-   [Filtro del writer ASF WM](wm-asf-writer-filter.md). File ASF Wrties.
-   [Filtro wrapper DMO](dmo-wrapper-filter.md). Esegue il wrapping del codificatore Windows Media e del decodificatore DMOs.

### <a name="versions"></a>Versioni

I filtri WM ASF Reader e WM ASF Writer sono inclusi nella DLL denominata qasf.dll e i filtri sono collettivamente denominati "QASF Components". Questi filtri sono wrapper per Windows Media Format SDK. La DLL (qasf.dll) è stata pubblicata per la prima volta in DirectX SDK, ma in seguito è stata aggiornata in Windows Media Format SDK. Ecco la cronologia delle versioni dei filtri QASF:

-   DirectShow 8,1 supporta Windows Media Format SDK versione 7,0.
-   DirectShow 9,0 supporta Windows Media Format SDK versione 7,1.
-   Windows XP Service Pack 2 supporta Windows Media Format 9 SDK.
-   Windows Vista supporta Windows Media Format 11 SDK.
-   Windows Media Format 9 SDK e versioni successive contengono versioni corrispondenti di QASF.

Per ottenere la versione più recente di QASF, scaricare sempre la versione più recente di Windows Media Format SDK.

### <a name="legacy-windows-media-source-filter"></a>Filtro origine Windows Media legacy

In Windows XP Service Pack 1 e versioni precedenti, il filtro di origine predefinito per i file ASF (con estensione ASF, WMV e WMA) è il filtro di [origine Windows Media](windows-media-source-filter.md)obsoleto. Questo comportamento è stato mantenuto per garantire la compatibilità con le applicazioni che usavano Windows Media Player 6,4. Le nuove applicazioni devono usare le versioni più recenti di QASF, che fanno in modo che il lettore WM ASF filtri il filtro predefinito per la riproduzione di file ASF.

Per ulteriori informazioni su Windows Media Suite di Software Development Kit, vedere la sezione [audio e video](../audio-and-video.md) della libreria MDSN.

Questo articolo contiene gli argomenti seguenti:

-   [Lettura di file ASF in DirectShow](reading-asf-files-in-directshow.md)
-   [Creazione di file ASF in DirectShow](creating-asf-files-in-directshow.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di DirectShow](using-directshow.md)
</dt> </dl>

 

 
