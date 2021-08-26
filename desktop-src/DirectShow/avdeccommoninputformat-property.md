---
description: Specifica il formato di input corrente per il decodificatore.
ms.assetid: 8fddf8c3-268e-4706-9003-e4bfb03d5278
title: Proprietà AVDecCommonInputFormat (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 187e923be9c53cebbb55663d55ec6351be38f84c33f8c03277f587d61a4db719
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079491"
---
# <a name="avdeccommoninputformat-property"></a>AVDecCommonInputFormat - proprietà

Specifica il formato di input corrente per il decodificatore.

Questa proprietà è di sola lettura.

## <a name="data-type"></a>Tipo di dati

**BSTR** (**VT \_ BSTR**)

## <a name="property-guid"></a>GUID proprietà

**CODECAPI \_ AVDecCommonInputFormat**

## <a name="property-value"></a>Valore proprietà

Il valore di questa proprietà è un **BSTR** che contiene la rappresentazione di stringa di un GUID. Sono definiti i GUID seguenti.



| **GUID**                                            | Descrizione                                    |
|-----------------------------------------------------|------------------------------------------------|
| **CODECAPI \_ GUID \_ AVDecAudioInputAAC**              | Codifica audio avanzata (AAC)                    |
| **CODECAPI \_ GUID \_ AVDecAudioInputDolbyDigitalPlus** | Dolby Digital Plus audio                       |
| **CODECAPI \_ GUID \_ AVDecAudioInputDolby**            | Audio Dolby                                    |
| **CODECAPI \_ GUID \_ AVDecAudioInputDTS**              | Audio DTS                                      |
| **CODECAPI \_ GUID \_ AVDecAudioInputHEAAC**            | High-Efficiency codifica audio avanzata (HE-AAC) |
| **CODECAPI \_ GUID \_ AVDecAudioInputMPEG**             | Audio MPEG                                     |
| **CODECAPI \_ GUID \_ AVDecAudioInputPCM**              | Audio PCM                                      |
| **CODECAPI \_ GUID \_ AVDecAudioInputWMA**              | Windows Media Audio                            |
| **CODECAPI \_ GUID \_ AVDecAudioInputWMAPro**           | Windows Audio multimediale 9 Professional (WMA Pro)   |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional app \[ desktop \| app UWP\]<br/>                     |
| Server minimo supportato<br/> | Windows 2000 App desktop UWP per le app \[ desktop di 2000 \| Server\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà API codec](codec-api-properties.md)
</dt> <dt>

[**Interfaccia ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




