---
title: Proprietà IWMPClosedCaption SAMIStyle
description: La proprietà SAMIStyle ottiene o imposta lo stile dei sottotitoli codificati.
ms.assetid: 0b1f92c6-b659-4ade-90c8-62a06e475f5c
keywords:
- Proprietà SAMIStyle Windows Media Player
- Proprietà SAMIStyle Windows Media Player, interfaccia IWMPClosedCaption
- Interfaccia IWMPClosedCaption Windows Media Player proprietà , SAMIStyle
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
ms.openlocfilehash: e147b48ffb80e1114133b59018cef514eefd2ae7
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885870"
---
# <a name="iwmpclosedcaptionsamistyle-property"></a>Proprietà IWMPClosedCaption::SAMIStyle

La **proprietà SAMIStyle** ottiene o imposta lo stile dei sottotitoli codificati.

## <a name="syntax"></a>Sintassi


```CSharp
public System.String SAMIStyle {get; set;}
```


```VB

Public Property SAMIStyle As System.String
```





## <a name="property-value"></a>Valore proprietà

**System.String che** rappresenta il nome specificato nell'identificatore di stile di un file SAMI.

## <a name="remarks"></a>Commenti

Un file SAMI può contenere diverse definizioni di stile di formato. Gli stili SAMI vengono definiti tra &lt; i tag STYLE e nel file &gt; </STYLE> SAMI. Uno stile viene definito con una stringa di testo preceduta da un \# carattere. Ad esempio:


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

[**Aggiunta di sottotitoli codificati a supporti digitali**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Interfaccia IWMPClosedCaption (VB e C#)**](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPClosedCaption2 (VB e C#)**](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





