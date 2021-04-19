---
description: I dispositivi portatili Windows supportano le proprietà audio seguenti.
ms.assetid: 5d6c6a95-abb7-4191-a961-bcb30ca96bb6
title: Proprietà audio (PortableDevice. h)
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
ms.openlocfilehash: 1bdab201fc987d5bc1aff3638fbb57358115fdce
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325947"
---
# <a name="audio-properties"></a>Proprietà audio

I dispositivi portatili Windows supportano le proprietà audio seguenti.



| Proprietà                         | VarType     | Descrizione                                                                                                                                                                                                        |
|----------------------------------|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_ \_ profondità bit audio \_ WPD**       | **\_UI4 VT** | Profondità di bit dell'audio.                                                                                                                                                                                        |
| **\_velocità in \_ bit audio WPD**          | **\_UI4 VT** | Velocità in bit dell'audio, in bit al secondo.                                                                                                                                                                     |
| **\_ \_ allineamento blocchi audio \_ WPD** | **\_UI4 VT** | Allineamento del blocco del file audio, in byte.                                                                                                                                                                   |
| **\_numero di \_ canali \_ audio WPD**   | **\_R4 VT**  | Il numero di canali in questo file audio, ad esempio 1, 2 o 5,1.                                                                                                                                              |
| **\_codice del \_ formato \_ audio WPD**     | **\_UI4 VT** | Numero di codice del formato WAVE registrato. Per un elenco dei formati WAVE registrati, vedere l'articolo [codici FourCC registrati e formati Wave](https://msdn2.microsoft.com/library/ms867195.aspx) nel sito Web MSDN. |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà e attributi di WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




