---
title: Proprietà SAMILang IWMPClosedCaption
description: La proprietà SAMILang ottiene o imposta la lingua visualizzata per i sottotitoli codificati.
ms.assetid: dcdd6bcd-b869-439f-b500-df26d3873b04
keywords:
- Proprietà SAMILang Windows Media Player
- Proprietà SAMILang Windows Media Player, interfaccia IWMPClosedCaption
- Interfaccia IWMPClosedCaption Windows Media Player , proprietà SAMILang
topic_type:
- apiref
api_name:
- IWMPClosedCaption.SAMILang
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98354d5e1e4f796442dd0347a4ed2796cafdf7297d3829af9b8839d48df00c3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117930314"
---
# <a name="iwmpclosedcaptionsamilang-property"></a>Proprietà IWMPClosedCaption::SAMILang

La **proprietà SAMILang** ottiene o imposta la lingua visualizzata per i sottotitoli codificati.

## <a name="syntax"></a>Sintassi


```CSharp
public System.String SAMILang {get; set;}
```


```VB

Public Property SAMILang As System.String
```





## <a name="property-value"></a>Valore proprietà

Oggetto **System.String** che rappresenta il nome specificato nell'identificatore di lingua di un file SAMI.

## <a name="remarks"></a>Commenti

Un file SAMI può contenere testo per una o più lingue. Le lingue disponibili per i sottotitoli codificati sono definite tra <STYLE> i tag e </STYLE> nel file SAMI. Un identificatore di lingua viene specificato con una stringa alfanumerica univoca preceduta da un punto (.). Il nome specificato per una lingua può essere qualsiasi stringa. Ad esempio, per definire l'inglese degli Stati Uniti è possibile usare quanto segue:


```
.ENUSCC {Name:'English Captions' lang: en-US; SAMIType:CC;}
```



Se non viene specificata alcuna lingua SAMI, per impostazione predefinita viene usata la prima lingua definita nel file SAMI.

La stringa impostata tramite **SAMILang** deve corrispondere **all'attributo Name** nell'identificatore di lingua.

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

 

 





