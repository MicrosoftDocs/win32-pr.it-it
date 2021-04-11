---
description: Specifica le autorizzazioni di controllo di accesso per una directory in una smart card.
ms.assetid: 361d9fa0-286e-4d2c-8452-3b5f48e77779
title: Enumerazione CARD_DIRECTORY_ACCESS_CONDITION (cardmod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CARD_DIRECTORY_ACCESS_CONDITION
api_type:
- HeaderDef
api_location:
- Cardmod.h
ms.openlocfilehash: 9879fa73f6bb45b56f433d7bca7765ab5fc0daef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226022"
---
# <a name="card_directory_access_condition-enumeration"></a>\_Enumerazione della \_ condizione di accesso alla directory della scheda \_

L'enumerazione della condizione di accesso alla directory delle schede specifica le autorizzazioni di controllo di accesso per una directory in una [*Smart Card*](../secgloss/s-gly.md). **\_ \_ \_**

## <a name="syntax"></a>Sintassi


```C++
typedef enum  { 
  InvalidAc               = 0,
  UserCreateDeleteDirAc   = 1,
  AdminCreateDeleteDirAc  = 2
} CARD_DIRECTORY_ACCESS_CONDITION;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="InvalidAc"></span><span id="invalidac"></span><span id="INVALIDAC"></span>**InvalidAc**
</dt> <dd>

Questo valore non è valido.

</dd> <dt>

<span id="UserCreateDeleteDirAc"></span><span id="usercreatedeletedirac"></span><span id="USERCREATEDELETEDIRAC"></span>**UserCreateDeleteDirAc**
</dt> <dd>

Utenti specifici possono leggere, scrivere ed eliminare la directory.

</dd> <dt>

<span id="AdminCreateDeleteDirAc"></span><span id="admincreatedeletedirac"></span><span id="ADMINCREATEDELETEDIRAC"></span>**AdminCreateDeleteDirAc**
</dt> <dd>

Gli amministratori possono leggere, scrivere ed eliminare la directory.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP, \[ solo app desktop Windows XP\]<br/>                              |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2003, Windows Server 2003 \[\]<br/>            |
| Intestazione<br/>                   | <dl> <dt>Cardmod. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Provider del servizio di crittografia Smart Card di Microsoft base](/previous-versions/windows/desktop/secsmart/microsoft-base-smart-card-cryptographic-service-provider)
</dt> <dt>

[**CardCreateDirectory**](/previous-versions/windows/desktop/secsmart/cardcreatedirectory)
</dt> <dt>

[**CardDeleteDirectory**](/previous-versions/windows/desktop/secsmart/carddeletedirectory)
</dt> </dl>

 

 
