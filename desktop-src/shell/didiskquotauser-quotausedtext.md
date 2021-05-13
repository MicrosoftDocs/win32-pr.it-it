---
description: Ottiene l'utilizzo corrente del disco dell'utente come stringa di testo.
title: DIDiskQuotaUser.QuotaUsedText - proprietà
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.QuotaUsedText
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: be27a17c-77ec-4016-8c2e-16fbc88c7c7a
ms.openlocfilehash: bf818bdcd22b734c6f4638a837af97bfecef1695
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843212"
---
# <a name="didiskquotauserquotausedtext-property"></a>DIDiskQuotaUser.QuotaUsedText - proprietà

Ottiene l'utilizzo corrente del disco dell'utente come stringa di testo.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
QuotaUsedText = DIDiskQuotaUser.QuotaUsedText
```



## <a name="property-value"></a>Valore proprietà

Valore stringa impostato sulla quantità di spazio su disco attualmente in uso. Se la compressione file NTFS è abilitata, questa proprietà riflette la quantità di spazio su disco necessaria per i dati in uno stato non compresso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 5.0 o successiva)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto DIDiskQuotaUser**](didiskquotauser-object.md)
</dt> <dt>

[**QuotaLimitText**](didiskquotauser-quotalimittext.md)
</dt> <dt>

[**QuotaThresholdText**](didiskquotauser-quotathresholdtext.md)
</dt> <dt>

[**QuotaUsed**](didiskquotauser-quotaused.md)
</dt> </dl>

 

 




