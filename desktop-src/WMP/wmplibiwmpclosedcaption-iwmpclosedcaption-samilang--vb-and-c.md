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
ms.openlocfilehash: a9577f7d9030a12a12596fe2cdc2a999922658ce
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122887180"
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

Un file SAMI può contenere testo per una o più lingue. Le lingue disponibili per i sottotitoli codificati sono definite tra i tag &lt; STYLE e nel file &gt; </STYLE> SAMI. Un identificatore di lingua viene specificato con una stringa alfanumerica univoca preceduta da un punto (.). Il nome specificato per una lingua può essere qualsiasi stringa. Ad esempio, per definire l'inglese degli Stati Uniti è possibile usare quanto segue:


```
.ENUSCC {Name:'English Captions' lang: en-US; SAMIType:CC;}
```



Se non viene specificata alcuna lingua SAMI, per impostazione predefinita viene usata la prima lingua definita nel file SAMI.

La stringa impostata tramite **SAMILang** deve corrispondere **all'attributo Name** nell'identificatore di lingua.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player serie 9 o successiva<br/>                                                                      |
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

 

 





