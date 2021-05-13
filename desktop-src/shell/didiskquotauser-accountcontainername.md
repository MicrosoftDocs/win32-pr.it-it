---
description: Ottiene il nome del contenitore di account dell'utente.
title: DIDiskQuotaUser.AccountContainerName - proprietà
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.AccountContainerName
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 5b9b0355-ea69-4c34-b0be-fc8e5855ec73
ms.openlocfilehash: 1cb709ccc4fa0afcb56314bd097b1b0120b8b59a
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843352"
---
# <a name="didiskquotauseraccountcontainername-property"></a>DIDiskQuotaUser.AccountContainerName - proprietà

Ottiene il nome del contenitore di account dell'utente.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
AccountContainerName = DIDiskQuotaUser.AccountContainerName
```



## <a name="property-value"></a>Valore proprietà

Valore stringa impostato sul nome del contenitore dell'account dell'utente.

## <a name="remarks"></a>Commenti

Per gli account senza informazioni sui servizi directory, questa proprietà contiene il nome di dominio. Per gli account con informazioni sui servizi directory, questa proprietà contiene un nome canonico con il nome dell'oggetto di terminazione rimosso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 5.0 o successiva)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto DIDiskQuotaUser**](didiskquotauser-object.md)
</dt> </dl>

 

 




