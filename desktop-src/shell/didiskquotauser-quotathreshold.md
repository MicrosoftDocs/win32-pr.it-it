---
description: Imposta o ottiene la soglia di avviso dell'utente, in byte.
ms.assetid: 5289d472-d591-4604-91f9-252dd4a1b62b
title: Proprietà DIDiskQuotaUser. QuotaThreshold
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.QuotaThreshold
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 7ce336c84d086c4e4be369278a77e40e59474bc5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878758"
---
# <a name="didiskquotauserquotathreshold-property"></a>Proprietà DIDiskQuotaUser. QuotaThreshold

Imposta o ottiene la soglia di avviso dell'utente, in byte.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```JScript
iQuotaThreshold = DIDiskQuotaUser.QuotaThreshold
DIDiskQuotaUser.QuotaThreshold = iQuotaThreshold
```



## <a name="property-value"></a>Valore proprietà

Valore **intero** che specifica o riceve la soglia di avviso dell'utente. Se l'utilizzo del disco di un utente supera questo valore e la proprietà [**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md) è impostata su **true**, il sistema genera una voce del registro eventi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 5,0 o successiva)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DefaultQuotaThreshold**](diskquotacontrol-defaultquotathreshold.md)
</dt> <dt>

[**DIDiskQuotaUser**](didiskquotauser-object.md)
</dt> <dt>

[**QuotaLimit**](didiskquotauser-quotalimit.md)
</dt> <dt>

[**QuotaThresholdText**](didiskquotauser-quotathresholdtext.md)
</dt> </dl>

 

 




