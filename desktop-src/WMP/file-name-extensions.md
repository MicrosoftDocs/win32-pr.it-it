---
title: Estensioni di file
description: Estensioni di file
ms.assetid: c17bf4e5-b469-45b6-bc22-2b451723d85e
keywords:
- Windows metafile multimediali, estensioni
- Windows metafile multimediali, estensioni di file
- metafile, estensioni
- metafile, estensioni di file
- Windows Supporti, metafile
- Estensioni di file per Windows Media
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6c69c36a5865b3496cf63e8cc08d73b9187f5107b14bf0bbb0d52b462e90c88a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054989"
---
# <a name="file-name-extensions"></a>Estensioni di file

Esistono linee guida specifiche per l'uso delle estensioni di file per Windows media. Windows Le estensioni dei nomi dei metafile multimediali vengono usate per identificare i diversi tipi di Windows file multimediali. Un'estensione di file fornisce a un fornitore di software indipendente (ISV) informazioni sui requisiti di rendering di un'applicazione che usa una determinata estensione e consente agli autori di contenuti di scegliere come destinazione tipi generali di lettori multimediali.

Le linee guida per l'estensione di file sono elencate nella tabella seguente. È consigliabile usare il tipo MIME di un file, che si trova nell'intestazione del file, per l'identificazione del tipo di file.



| Estensione del file | tipo MIME      | Contenuto del file                                                                                                                                                                            |
|---------------------|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| wma                | audio/x-ms-wma | Windows File multimediale con solo contenuto audio. Usato in genere per scaricare e riprodurre file o per trasmettere contenuto in streaming.                                                                             |
| wmv                | video/x-ms-wmv | Windows File multimediale con contenuto audio e/o video. Usato in genere per scaricare e riprodurre file o per trasmettere contenuto in streaming.                                                                     |
| .asf                | video/x-ms-asf | Contenuto legacy. Usato in genere per scaricare e riprodurre file o per trasmettere contenuto in streaming. Può contenere contenuto audio e/o video. Usato in genere per scaricare e riprodurre file o per trasmettere contenuto in streaming. |
| File con estensione wm                 | video/x-ms-wm  | Riservato                                                                                                                                                                                |
| File con estensione endose                | audio/x-ms-sistema | Metafile che fanno riferimento Windows file multimediali con estensioni asf, wma o files.pdf.                                                                                             |
| .wvx                | video/x-ms-wvx | Metafile che fanno riferimento Windows file multimediali con estensioni di file wma, wmv, wvx o filesdei file con estensione files.                                                                                       |
| .asx                | video/x-ms-asf | Metafile che fanno riferimento Windows file multimediali con estensioni di file wma, wmv, wvx, asf o asx.                                                                           |
| File con estensione wmx                | video/x-ms-wvx | Riservato.                                                                                                                                                                               |



 

## <a name="remarks"></a>Commenti

Gli script e DRM (Digital Rights Management) devono essere supportati da qualsiasi applicazione che esegue il rendering Windows file multimediali.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Windows Informazioni di riferimento per gli elementi metafile multimediali**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Guida ai metafile multimediali**](windows-media-metafile-guide.md)
</dt> <dt>

[**Windows Informazioni di riferimento sui metafile multimediali**](windows-media-metafile-reference.md)
</dt> </dl>

 

 




