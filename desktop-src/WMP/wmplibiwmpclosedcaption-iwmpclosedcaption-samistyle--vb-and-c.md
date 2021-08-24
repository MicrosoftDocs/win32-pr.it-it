---
title: Proprietà IWMPClosedCaption SAMIStyle
description: La proprietà SAMIStyle ottiene o imposta lo stile di sottotitoli codificati.
ms.assetid: 0b1f92c6-b659-4ade-90c8-62a06e475f5c
keywords:
- Proprietà SAMIStyle Windows Media Player
- Proprietà SAMIStyle Windows Media Player, interfaccia IWMPClosedCaption
- Interfaccia IWMPClosedCaption Windows Media Player , proprietà SAMIStyle
topic_type:
- apiref
api_name:
- IWMPClosedCaption.SAMIStyle
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cede8964636073c393cb34bfa1be22855467f4cb243834bd1e11a4ffc492665
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031421"
---
# <a name="iwmpclosedcaptionsamistyle-property"></a>Proprietà IWMPClosedCaption::SAMIStyle

La **proprietà SAMIStyle** ottiene o imposta lo stile di sottotitoli codificati.

## <a name="syntax"></a>Sintassi


```CSharp
public System.String SAMIStyle {get; set;}
```


```VB

Public Property SAMIStyle As System.String
```





## <a name="property-value"></a>Valore proprietà

Oggetto **System.String** che rappresenta il nome specificato nell'identificatore di stile di un file SAMI.

## <a name="remarks"></a>Commenti

Un file SAMI può contenere diverse definizioni di stile di formato. Gli stili SAMI vengono definiti tra <STYLE> i tag e </STYLE> nel file SAMI. Uno stile viene definito con una stringa di testo preceduta da un \# carattere. Esempio:


```
#Emphasis1 {Name: Big Bold Italic; font-size: 14pt; text-align: center;
            color: blue; font-family: sans-serif; font-weight: bold;
            font-style: italic;}
```



Specifica uno stile che produce un tipo di carattere specifico.

Se non viene specificato alcuno stile SAMI, per impostazione predefinita viene usato il primo stile definito nel file SAMI.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player serie 9 o successive<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Aggiunta di sottotitoli codificati ai supporti digitali**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Interfaccia IWMPClosedCaption (VB e C#)**](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPClosedCaption2 (VB e C#)**](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





