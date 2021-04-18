---
title: Estensioni di file
description: Estensioni di file
ms.assetid: c17bf4e5-b469-45b6-bc22-2b451723d85e
keywords:
- Metafile di Windows Media, estensioni
- Metafile di Windows Media, estensioni di file
- Metafile, estensioni
- Metafile, estensioni di file
- Windows Media, metafile
- estensioni dei nomi di file per i file multimediali di Windows
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d95d5bcba9bbad5f04b0d085ba712d5b9306c8b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298725"
---
# <a name="file-name-extensions"></a>Estensioni di file

Sono disponibili linee guida specifiche per l'utilizzo delle estensioni di file per i file multimediali di Windows. Le estensioni del nome Metafile di Windows Media vengono utilizzate per identificare i diversi tipi di file di Windows Media. Un'estensione di file fornisce un fornitore di software indipendente (ISV) con informazioni sui requisiti di rendering di un'applicazione che utilizza un'estensione specifica e consente agli autori di contenuti di specificare come destinazione tipi generali di lettori multimediali.

Nella tabella seguente sono elencate le linee guida relative all'estensione del nome file. È consigliabile usare il tipo MIME di un file, che si trova nell'intestazione del file, per l'identificazione del tipo di file.



| Estensione del file | tipo MIME      | Contenuto del file                                                                                                                                                                            |
|---------------------|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| wma                | audio/x-ms-WMA | File Windows Media con solo contenuto audio. Usato in genere per scaricare e riprodurre file o per trasmettere il contenuto.                                                                             |
| wmv                | video/x-MS-WMV | File Windows Media con contenuto audio e/o video. Usato in genere per scaricare e riprodurre file o per trasmettere il contenuto.                                                                     |
| .asf                | video/x-ms-asf | Contenuto legacy. Usato in genere per scaricare e riprodurre file o per trasmettere il contenuto. Può contenere contenuto audio e/o video. Usato in genere per scaricare e riprodurre file o per trasmettere il contenuto. |
| . WM                 | video/x-ms-WM  | Riservato                                                                                                                                                                                |
| . Wax                | audio/x-ms-Wax | Metafile che fanno riferimento a file di Windows Media con estensioni di file. ASF,. WMA o. Wax.                                                                                             |
| . wvx                | video/x-ms-wvx | Metafile che fanno riferimento a file Windows Media con file con estensione WMA, WMV, wvx o Wax.                                                                                       |
| .asx                | video/x-ms-asf | Metafile che fanno riferimento a file Windows Media con file con estensione WMA, Wax, WMV, WVX, ASF o ASX.                                                                           |
| . WMX                | video/x-ms-wvx | Riservato.                                                                                                                                                                               |



 

## <a name="remarks"></a>Commenti

Gli script e i Digital Rights Management (DRM) devono essere supportati da qualsiasi applicazione che esegua il rendering dei file di Windows Media.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Riferimento agli elementi metafile di Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Guida ai metafile di Windows Media**](windows-media-metafile-guide.md)
</dt> <dt>

[**Informazioni di riferimento sui metafile di Windows Media**](windows-media-metafile-reference.md)
</dt> </dl>

 

 




