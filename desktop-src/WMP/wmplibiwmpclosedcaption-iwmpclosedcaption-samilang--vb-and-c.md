---
title: Proprietà SAMILang di IWMPClosedCaption
description: La proprietà SAMILang Ottiene o imposta la lingua visualizzata per la didascalia chiusa.
ms.assetid: dcdd6bcd-b869-439f-b500-df26d3873b04
keywords:
- Finestra delle proprietà di SAMILang Media Player
- Proprietà di SAMILang Media Player Windows, interfaccia IWMPClosedCaption
- Interfaccia IWMPClosedCaption Windows Media Player, proprietà SAMILang
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
ms.openlocfilehash: fe29defa3736795c88613ee7ab2ef11a914a3f80
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332507"
---
# <a name="iwmpclosedcaptionsamilang-property"></a>Proprietà IWMPClosedCaption:: SAMILang

La proprietà **SAMILang** Ottiene o imposta la lingua visualizzata per la didascalia chiusa.

## <a name="syntax"></a>Sintassi


```CSharp
public System.String SAMILang {get; set;}
```


```VB

Public Property SAMILang As System.String
```





## <a name="property-value"></a>Valore proprietà

**System. String** che rappresenta il nome specificato nell'identificatore di lingua di un file Sami.

## <a name="remarks"></a>Commenti

Un file SAMI può contenere testo per una o più lingue. Le lingue disponibili per la didascalia chiusa sono definite tra i tag <STYLE> e </STYLE> nel file Sami. Un identificatore di lingua viene specificato con una stringa alfanumerica univoca preceduta da un punto (.). Il nome specificato per una lingua può essere qualsiasi stringa. È ad esempio possibile utilizzare il codice seguente per definire l'inglese (Stati Uniti):


```
.ENUSCC {Name:'English Captions' lang: en-US; SAMIType:CC;}
```



Se non si specifica alcun linguaggio SAMI, per impostazione predefinita viene usata la prima lingua definita nel file SAMI.

La stringa impostata utilizzando **SAMILang** deve corrispondere all'attributo **Name** nell'identificatore di linguaggio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 9 serie o versione successiva<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Aggiunta di didascalie chiuse a file multimediali digitali**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Interfaccia IWMPClosedCaption (VB e C#)**](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPClosedCaption2 (VB e C#)**](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





