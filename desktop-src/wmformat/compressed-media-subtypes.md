---
title: Sottotipi di supporti compressi
description: Sottotipi di supporti compressi
ms.assetid: 0ed6b4e8-6450-4484-90d6-efa2f9101782
keywords:
- Windows Media Format SDK, tipi di supporto
- Formati di sistemi avanzati (ASF), tipi di supporto
- ASF (formato di sistemi avanzati), tipi di supporto
- Windows Media Format SDK, sottotipi di supporti compressi
- Formati di sistemi avanzati (ASF), sottotipi di supporti compressi
- ASF (Advanced Systems Format), sottotipi di supporti compressi
- tipi di supporti, sottotipi di supporti compressi
- sottotipi di supporti compressi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d92d192d04257f0375a618dda05aa97fd3f344b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104116761"
---
# <a name="compressed-media-subtypes"></a>Sottotipi di supporti compressi

Nella tabella seguente sono elencati i sottotipi di supporti compressi. Questi tipi vengono usati per identificare i flussi compressi in un file. Quando si configura un flusso video o audio, questi tipi vengono in genere utilizzati.



| Sottotipo di supporti compressi          | Descrizione                                                                                                                                                                                                                                                                                 |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ACELPNET WMMEDIASUBTYPE          | Codifica audio con il codec ACELP di SIPRO Labs. Si tratta in genere di dati vocali. Non è più supportato per la codifica.                                                                                                                                                                       |
| \_Mp43 WMMEDIASUBTYPE              | Video codificato da Microsoft MPEG 4 codec versione 3. Questo codec non è più supportato da Windows Media Format SDK. Se questo codec è già installato in un computer, l'installazione di Windows Media Format SDK o del pacchetto di ridistribuzione in un computer non comporterà la rimozione di questo codec. |
| \_Mp4s WMMEDIASUBTYPE              | Codifica video con il codec ISO MPEG 4 versione 1.                                                                                                                                                                                                                                         |
| VIDEO di WMMEDIASUBTYPE \_ MPEG2 \_      | Video codificato in specifiche MPEG 2.                                                                                                                                                                                                                                                     |
| \_MSS1 WMMEDIASUBTYPE              | Video codificato con Windows Media Screen codec versione 1.                                                                                                                                                                                                                                |
| \_Mss2 WMMEDIASUBTYPE              | Video codificato con il codec della schermata Windows Media Video 9.                                                                                                                                                                                                                                  |
| \_WMVP WMMEDIASUBTYPE              | Codifica video con il codec di immagine Windows Media Video 9 per trasformare le bitmap e i dati di deformazione in un flusso video.                                                                                                                                                                     |
| \_WVP2 WMMEDIASUBTYPE              | Codifica video con il codec Windows Media Video 9 image V2.                                                                                                                                                                                                                                |
| WMMEDIASUBTYPE \_ WMAudio \_ Lossless | Codifica audio con il codec Windows Media Audio 9 Lossless o il codec Windows Media Audio 9,1.                                                                                                                                                                                           |
| \_WMAUDIOV2 WMMEDIASUBTYPE         | Codifica audio con il codec Windows Media Audio versione 2. Questo valore è identico a WMMEDIASUBTYPE \_ WMAudioV7 e WMMEDIASUBTYPE \_ WMAudioV8, perché i bitstream per queste versioni di codec sono compatibili.                                                                             |
| \_WMAUDIOV7 WMMEDIASUBTYPE         | Codifica audio con il codec Windows Media Audio versione 7. Questo valore è identico a WMMEDIASUBTYPE \_ WMAudioV2 e WMMEDIASUBTYPE \_ WMAudioV8, perché i bitstream per queste versioni di codec sono compatibili.                                                                             |
| \_WMAUDIOV8 WMMEDIASUBTYPE         | Codifica audio con il codec Windows Media Audio 8, il codec Windows Media Audio 9 o il codec Windows Media Audio 9,1. Questo valore è identico a WMMEDIASUBTYPE \_ WMAudioV2 e WMMEDIASUBTYPE \_ WMAudioV7, perché i bitstream per queste versioni di codec sono compatibili.              |
| \_WMAUDIOV9 WMMEDIASUBTYPE         | Codifica audio con il codec Windows Media Audio 9 Professional o il codec Windows Media Audio 9,1 Professional.                                                                                                                                                                          |
| \_M4S2 WMMEDIASUBTYPE              | Video codificato con il codec ISO MPEG4 v 1.1.                                                                                                                                                                                                                                                |
| \_WMSP1 WMMEDIASUBTYPE             | Codifica audio con il codec Windows Media Audio 9 Voice.                                                                                                                                                                                                                                   |
| \_WMV1 WMMEDIASUBTYPE              | Codifica video con il codec Windows Media Video versione 7.                                                                                                                                                                                                                                |
| \_WMV2 WMMEDIASUBTYPE              | Codifica video con il codec Windows Media Video 8.                                                                                                                                                                                                                                        |
| \_WMV3 WMMEDIASUBTYPE              | Codifica video con il codec Windows Media Video 9.                                                                                                                                                                                                                                        |
| \_WMVA WMMEDIASUBTYPE              | Codifica video con la versione del codec di profilo avanzato Windows Media Video 9 rilasciato con Windows Media Format 9 Series SDK.                                                                                                                                           |
| \_WVC1 WMMEDIASUBTYPE              | Codifica video con la versione del codec del profilo avanzato Windows Media Video 9 rilasciato con Windows Media Format 11 SDK. Questo sottotipo identifica un flusso di bit conforme allo standard SMPTE VC-1.                                                            |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Identificatori del tipo di supporto**](media-type-identifiers.md)
</dt> <dt>

[**Tipi di supporto**](media-types.md)
</dt> <dt>

[**Sottotipi di supporti non compressi**](uncompressed-media-subtypes.md)
</dt> </dl>

 

 




