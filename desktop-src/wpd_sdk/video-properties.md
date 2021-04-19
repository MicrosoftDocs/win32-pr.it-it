---
description: Dispositivi portatili Windows supporta le seguenti proprietà video.
ms.assetid: e6df5b2d-ceb8-4de0-b60b-9102c77143fe
title: Proprietà video (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Video
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 1f44f32ab19c5ad10cc9c8dd5bdb8816ccc944f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326590"
---
# <a name="video-properties"></a>Proprietà video

Dispositivi portatili Windows supporta le seguenti proprietà video.



| Proprietà                                         | VarType        | Descrizione                                                                                                                                                                                                                                             |
|--------------------------------------------------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_autore video \_ WPD**                           | **\_LPWSTR VT** | Autore del file video.                                                                                                                                                                                                                           |
| **\_velocità in \_ bit video WPD**                          | **\_UI4 VT**    | Velocità in bit del file video.                                                                                                                                                                                                                         |
| **\_dimensioni del \_ buffer \_ video WPD**                     | **\_UI4 VT**    | Valore che specifica la dimensione del buffer video necessaria per il rendering di questo file.                                                                                                                                                                              |
| **\_crediti video \_ WPD**                          | **\_LPWSTR VT** | Crediti che elencano il cast e la troupe del video.                                                                                                                                                                                                    |
| **\_ \_ Codice FourCC video \_ WPD**                     | **\_DWORD VT**  | Codice FourCC registrato che indica il codec usato per il file video. Per un elenco dei formati FourCC, vedere l'articolo [codici FourCC registrati e formati Wave](https://msdn2.microsoft.com/library/ms867195.aspx) nel sito Web MSDN. |
| **\_framerate video \_ WPD**                        | **\_UI4 VT**    | Frequenza dei fotogrammi del file video, in frame al secondo x 1.000. Una frequenza di fotogrammi di 29,97, ad esempio, viene rappresentata come 29970.                                                                                                                                 |
| **\_genere video \_ WPD**                            | **\_LPWSTR VT** | Genere di questo file video. Non sono presenti definizioni di genere standard.                                                                                                                                                                                  |
| **\_ \_ \_ distanza fotogramma chiave video WPD \_**             | **\_UI4 VT**    | Intervallo tra fotogrammi chiave, in millisecondi.                                                                                                                                                                                                       |
| **\_ \_ impostazione qualità video \_ WPD**                 | **\_UI4 VT**    | Impostazione qualità per il file video. Si tratta di un dipendente dal codec.                                                                                                                                                                                        |
| **WPD \_ video \_ - \_ numero di canale RECORDEDTV \_**      | **\_UI4 VT**    | Il numero del canale televisivo dal quale è stato registrato il video.                                                                                                                                                                                              |
| **\_Descrizione del programma WPD video \_ RECORDEDTV \_ \_** | **\_LPWSTR VT** | Una descrizione del programma TV registrato.                                                                                                                                                                                                       |
| **\_ \_ ripetizione RECORDEDTV video \_ WPD**               | **\_bool VT**   | Valore booleano che specifica se il programma televisivo è stato visualizzato ripetutamente.                                                                                                                                                                     |
| **\_nome della \_ \_ stazione RECORDEDTV del video \_ WPD**        | **\_LPWSTR VT** | Stazione televisiva dalla quale è stato registrato il video.                                                                                                                                                                                                |
| **\_tipo di \_ analisi \_ video WPD**                       | **\_UI4 VT**    | Enumeratore [**WPD \_ video \_ Scan \_ types**](wpd-video-scan-types.md) che specifica l'interlacciamento del file video.                                                                                                                                  |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà e attributi di WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




