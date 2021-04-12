---
description: Specifica il formato di input corrente per il decodificatore.
ms.assetid: 8fddf8c3-268e-4706-9003-e4bfb03d5278
title: Proprietà AVDecCommonInputFormat (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7432d2a48727ec144d4206d4a11bfe65ce2c5d2a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482284"
---
# <a name="avdeccommoninputformat-property"></a>Proprietà AVDecCommonInputFormat

Specifica il formato di input corrente per il decodificatore.

Questa proprietà è di sola lettura.

## <a name="data-type"></a>Tipo di dati

**BSTR** (**VT \_ BSTR**)

## <a name="property-guid"></a>GUID proprietà

**Codecapis \_ AVDecCommonInputFormat**

## <a name="property-value"></a>Valore proprietà

Il valore di questa proprietà è un **BSTR** che contiene la rappresentazione di stringa di un GUID. Sono definiti i seguenti GUID.



| **GUID**                                            | Descrizione                                    |
|-----------------------------------------------------|------------------------------------------------|
| **\_GUID AVDecAudioInputAAC di CODEcapi \_**              | Codifica audio avanzata (AAC)                    |
| **\_GUID AVDecAudioInputDolbyDigitalPlus di CODEcapi \_** | Audio Dolby Digital Plus                       |
| **\_GUID AVDecAudioInputDolby di CODEcapi \_**            | Audio Dolby                                    |
| **\_GUID AVDecAudioInputDTS di CODEcapi \_**              | Audio DTS                                      |
| **\_GUID AVDecAudioInputHEAAC di CODEcapi \_**            | High-Efficiency codifica audio avanzata (HE-AAC) |
| **\_GUID AVDecAudioInputMPEG di CODEcapi \_**             | Audio MPEG                                     |
| **\_GUID AVDecAudioInputPCM di CODEcapi \_**              | Audio PCM                                      |
| **\_GUID AVDecAudioInputWMA di CODEcapi \_**              | Windows Media Audio                            |
| **\_GUID AVDecAudioInputWMAPro di CODEcapi \_**           | Windows Media Audio 9 Professional (WMA Pro)   |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App UWP di Windows 2000 Professional \[ desktop apps \|\]<br/>                     |
| Server minimo supportato<br/> | App desktop di Windows 2000 Server \[ \| UWP\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Codecapis. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà dell'API codec](codec-api-properties.md)
</dt> <dt>

[**Interfaccia ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




