---
description: Windows Dispositivi portatili supporta le proprietà audio seguenti.
ms.assetid: 5d6c6a95-abb7-4191-a961-bcb30ca96bb6
title: Proprietà audio (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Audio
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 93ddbee0eb078c1b9d5a1e7c64288e95b47e2bdb0363bf8b7b19cb773129d0ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119590411"
---
# <a name="audio-properties"></a>Proprietà audio

Windows Dispositivi portatili supporta le proprietà audio seguenti.



| Proprietà                         | VarType     | Descrizione                                                                                                                                                                                                        |
|----------------------------------|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **PROFONDITÀ IN \_ BIT AUDIO WPD \_ \_**       | **VT \_ UI4** | Profondità in bit dell'audio.                                                                                                                                                                                        |
| **VELOCITÀ IN \_ BIT AUDIO WPD \_**          | **VT \_ UI4** | Velocità in bit dell'audio, in bit al secondo.                                                                                                                                                                     |
| **ALLINEAMENTO DEI BLOCCHI AUDIO WPD \_ \_ \_** | **VT \_ UI4** | Allineamento del blocco del file audio, in byte.                                                                                                                                                                   |
| **NUMERO DI CANALI \_ AUDIO WPD \_ \_**   | **VT \_ R4**  | Numero di canali in questo file audio, ad esempio 1, 2 o 5,1.                                                                                                                                              |
| **CODICE DI FORMATO AUDIO WPD \_ \_ \_**     | **VT \_ UI4** | Numero di codice del formato WAVE registrato. Per un elenco dei formati WAVE registrati, vedere l'articolo [Registered FOURCC Codes and WAVE Formats](https://msdn2.microsoft.com/library/ms867195.aspx) (Codici FOURCC registrati e formati WAVE) nel sito Web MSDN. |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà e attributi WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




