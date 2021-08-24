---
description: Windows Dispositivi portatili supporta le proprietà video seguenti.
ms.assetid: e6df5b2d-ceb8-4de0-b60b-9102c77143fe
title: Proprietà video (PortableDevice.h)
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
ms.openlocfilehash: 6e7bbab3416f50a95d2ae29e2be0ef5ecdcad6eed0112f940e5c34b593f2b79a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083385"
---
# <a name="video-properties"></a>Proprietà video

Windows Dispositivi portatili supporta le proprietà video seguenti.



| Proprietà                                         | VarType        | Descrizione                                                                                                                                                                                                                                             |
|--------------------------------------------------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **AUTORE DI \_ VIDEO WPD \_**                           | **VT \_ LPWSTR** | Autore del file video.                                                                                                                                                                                                                           |
| **VELOCITÀ IN \_ BIT VIDEO WPD \_**                          | **VT \_ UI4**    | Velocità in bit del file video.                                                                                                                                                                                                                         |
| **DIMENSIONI DEL \_ BUFFER VIDEO WPD \_ \_**                     | **VT \_ UI4**    | Valore che specifica le dimensioni del buffer video necessarie per eseguire il rendering del file.                                                                                                                                                                              |
| **CREDITI VIDEO WPD \_ \_**                          | **VT \_ LPWSTR** | Crediti che elencano il cast e l'squadra per il video.                                                                                                                                                                                                    |
| **WPD \_ VIDEO \_ FOURCC \_ CODE**                     | **VT \_ DWORD**  | Codice FourCC registrato che indica il codec usato per il file video. Per un elenco dei formati FourCC, vedere l'articolo [Registered FOURCC Codes and WAVE Formats](https://msdn2.microsoft.com/library/ms867195.aspx) (Codici FOURCC registrati e formati WAVE) nel sito Web MSDN. |
| **FREQUENZA \_ FOTOGRAMMI VIDEO WPD \_**                        | **VT \_ UI4**    | Frequenza dei fotogrammi del file video, in fotogrammi al secondo x 1.000. Ad esempio, una frequenza dei fotogrammi di 29,97 è rappresentata come 29970.                                                                                                                                 |
| **GENERE VIDEO WPD \_ \_**                            | **VT \_ LPWSTR** | Genere di questo file video. Non sono presenti definizioni di genere standard.                                                                                                                                                                                  |
| **DISTANZA DEL \_ FOTOGRAMMA CHIAVE VIDEO WPD \_ \_ \_**             | **VT \_ UI4**    | Intervallo tra fotogrammi chiave, in millisecondi.                                                                                                                                                                                                       |
| **IMPOSTAZIONE QUALITÀ VIDEO WPD \_ \_ \_**                 | **VT \_ UI4**    | Impostazione di qualità per il file video. Questo dipende dal codec.                                                                                                                                                                                        |
| **WPD \_ VIDEO \_ RECORDEDTV \_ CHANNEL \_ NUMBER**      | **VT \_ UI4**    | Numero del canale tv da cui è stato registrato il video.                                                                                                                                                                                              |
| **WPD \_ VIDEO \_ RECORDEDTV \_ PROGRAM \_ DESCRIPTION** | **VT \_ LPWSTR** | Descrizione del programma tv registrato.                                                                                                                                                                                                       |
| **VIDEO WPD \_ \_ REGISTRATOTV \_ REPEAT**               | **VT \_ BOOL**   | Valore booleano che specifica se il programma tv era una ripetizione.                                                                                                                                                                     |
| **WPD \_ VIDEO \_ RECORDEDTV \_ STATION \_ NAME**        | **VT \_ LPWSTR** | Stazione tv da cui è stato registrato il video.                                                                                                                                                                                                |
| **TIPO DI ANALISI VIDEO WPD \_ \_ \_**                       | **VT \_ UI4**    | [**Enumeratore WPD \_ VIDEO SCAN \_ \_ TYPES**](wpd-video-scan-types.md) che specifica l'interlacciamento del file video.                                                                                                                                  |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà e attributi WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




