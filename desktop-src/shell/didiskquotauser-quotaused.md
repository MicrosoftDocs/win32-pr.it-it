---
description: Ottiene l'utilizzo corrente del disco dell'utente, in byte.
title: DIDiskQuotaUser.QuotaUsed - proprietà
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.QuotaUsed
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 3e3ade59-b925-4ff5-ae7e-ed97eff506c7
ms.openlocfilehash: c1584f2abd7fbb6d11d345ec78499b08dc0337e0ddd6bd6300e42a4ec3c2acec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118459932"
---
# <a name="didiskquotauserquotaused-property"></a>DIDiskQuotaUser.QuotaUsed - proprietà

Ottiene l'utilizzo corrente del disco dell'utente, in byte.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
iQuotaUsed = DIDiskQuotaUser.QuotaUsed
```



## <a name="property-value"></a>Valore proprietà

Valore **Intero** impostato sulla quantità di spazio su disco attualmente in uso. Se la compressione file NTFS è abilitata, **QuotaUsed** riflette la quantità di spazio su disco necessaria per i dati in uno stato non compresso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 5.0 o successiva)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DIDiskQuotaUser**](didiskquotauser-object.md)
</dt> <dt>

[**QuotaLimit**](didiskquotauser-quotalimit.md)
</dt> <dt>

[**QuotaThreshold**](didiskquotauser-quotathreshold.md)
</dt> <dt>

[**QuotaUsedText**](didiskquotauser-quotausedtext.md)
</dt> </dl>

 

 




