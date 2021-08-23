---
title: Sottotipi di supporti compressi
description: Sottotipi di supporti compressi
ms.assetid: 0ed6b4e8-6450-4484-90d6-efa2f9101782
keywords:
- Windows MEDIA Format SDK, tipi di supporti
- Advanced Systems Format (ASF), tipi di supporti
- ASF (Advanced Systems Format), tipi di supporti
- Windows Media Format SDK, sottotipi di supporti compressi
- Advanced Systems Format (ASF), sottotipi di supporti compressi
- ASF (Advanced Systems Format), sottotipi di supporti compressi
- tipi di supporti, sottotipi di supporti compressi
- sottotipi di supporti compressi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f231c9c8ff666c11d3fb3bf101dc3b43c1cd2ff90ca3a28ca1af0113fe8fccd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119548091"
---
# <a name="compressed-media-subtypes"></a>Sottotipi di supporti compressi

Nella tabella seguente sono elencati i sottotipi dei supporti compressi. Questi tipi vengono usati per identificare i flussi compressi in un file. Quando si configura un flusso video o audio, questi tipi vengono in genere utilizzati.



| Sottotipo di supporto compresso          | Descrizione                                                                                                                                                                                                                                                                                 |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WMMEDIASUBTYPE \_ ACELPnet          | Audio codificato con il codec Sipro Labs ACELP. Questo audio è in genere dati vocali. (Non più supportato per la codifica).                                                                                                                                                                       |
| WMMEDIASUBTYPE \_ MP43              | Video codificato dal codec Microsoft MPEG 4 versione 3. Questo codec non è più supportato da Windows Media Format SDK. Se questo codec è già installato in un computer, l'installazione di Windows Media Format SDK o del pacchetto di ridistribuzione in un computer non rimuoverà questo codec. |
| WMMEDIASUBTYPE \_ MP4S              | Video codificato con il codec ISO MPEG 4 versione 1.                                                                                                                                                                                                                                         |
| WMMEDIASUBTYPE \_ MPEG2 \_ VIDEO      | Video codificato in specifiche MPEG 2.                                                                                                                                                                                                                                                     |
| WMMEDIASUBTYPE \_ MSS1              | Video codificato con il codec Windows Media Screen versione 1.                                                                                                                                                                                                                                |
| WMMEDIASUBTYPE \_ MSS2              | Video codificato con il codec Windows Media Video 9 Screen.                                                                                                                                                                                                                                  |
| WMMEDIASUBTYPE \_ WMVP              | Video codificato con il codec Windows Media Video 9 Image per trasformare bitmap e dati di deformazioni in un flusso video.                                                                                                                                                                     |
| WMMEDIASUBTYPE \_ WVP2              | Video codificato con il codec Windows Media Video 9 Image v2.                                                                                                                                                                                                                                |
| WMMEDIASUBTYPE \_ WMAudio \_ Lossless | Audio codificato con il codec Windows Media Audio 9 Lossless o il codec Windows Media Audio 9.1.                                                                                                                                                                                           |
| WMMEDIASUBTYPE \_ WMAudioV2         | Audio codificato con il codec Windows Media Audio versione 2. Questo valore è identico a WMMEDIASUBTYPE \_ WMAudioV7 e WMMEDIASUBTYPE WMAudioV8, perché i bitstream per queste versioni \_ del codec sono compatibili.                                                                             |
| WMMEDIASUBTYPE \_ WMAudioV7         | Audio codificato con il codec Windows Media Audio versione 7. Questo valore è identico a WMMEDIASUBTYPE \_ WMAudioV2 e WMMEDIASUBTYPE WMAudioV8, perché i bitstream per queste versioni \_ del codec sono compatibili.                                                                             |
| WMMEDIASUBTYPE \_ WMAudioV8         | Audio codificato con il codec Windows Media Audio 8, Windows Media Audio 9 o Windows Media Audio 9.1. Questo valore è identico a WMMEDIASUBTYPE \_ WMAudioV2 e WMMEDIASUBTYPE WMAudioV7, perché i bitstream per queste versioni \_ del codec sono compatibili.              |
| WMMEDIASUBTYPE \_ WMAudioV9         | Audio codificato con il codec Windows Media Audio 9 Professional o Windows Media Audio 9.1 Professional codec.                                                                                                                                                                          |
| WMMEDIASUBTYPE \_ M4S2              | Video codificato con il codec ISO MPEG4 v1.1.                                                                                                                                                                                                                                                |
| WMMEDIASUBTYPE \_ WMSP1             | Audio codificato con il codec Windows Media Audio 9 Voice.                                                                                                                                                                                                                                   |
| WMMEDIASUBTYPE \_ WMV1              | Video codificato usando il codec Windows Media Video versione 7.                                                                                                                                                                                                                                |
| WMMEDIASUBTYPE \_ WMV2              | Video codificato usando il codec Windows Media Video 8.                                                                                                                                                                                                                                        |
| WMMEDIASUBTYPE \_ WMV3              | Video codificato usando il codec Windows Media Video 9.                                                                                                                                                                                                                                        |
| WMMEDIASUBTYPE \_ WMVA              | Video codificato usando la versione del codec Windows Media Video 9 Advanced Profile rilasciato con Windows Media Format 9 Series SDK.                                                                                                                                           |
| WMMEDIASUBTYPE \_ WVC1              | Video codificato usando la versione del codec Windows Media Video 9 Advanced Profile rilasciato con Windows Media Format 11 SDK. Questo sottotipo identifica un flusso di bit conforme allo standard SMPTE VC-1.                                                            |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Identificatori dei tipi di supporti**](media-type-identifiers.md)
</dt> <dt>

[**Tipi di supporti**](media-types.md)
</dt> <dt>

[**Sottotipi di supporti non compressi**](uncompressed-media-subtypes.md)
</dt> </dl>

 

 




