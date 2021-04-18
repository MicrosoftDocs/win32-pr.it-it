---
description: Specifica le autorizzazioni di controllo di accesso per un file in una smart card.
ms.assetid: 995d959f-30dc-4e5c-be2d-6b447499415a
title: Enumerazione CARD_FILE_ACCESS_CONDITION (cardmod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CARD_FILE_ACCESS_CONDITION
api_type:
- HeaderDef
api_location:
- Cardmod.h
ms.openlocfilehash: d3ef9fc81c9ab3bff5f3992c3aedeb3f923648ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306546"
---
# <a name="card_file_access_condition-enumeration"></a>\_Enumerazione della \_ condizione di accesso ai file delle schede \_

L'enumerazione della condizione di accesso ai file di scheda specifica le autorizzazioni di controllo di accesso per un file in una [*Smart Card*](../secgloss/s-gly.md). **\_ \_ \_**

## <a name="syntax"></a>Sintassi


```C++
typedef enum  { 
  InvalidAc                 = 0,
  EveryoneReadUserWriteAc   = 1,
  UserWriteExecuteAc        = 2,
  EveryoneReadAdminWriteAc  = 3,
  UnknownAc                 = 4
} CARD_FILE_ACCESS_CONDITION;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="InvalidAc"></span><span id="invalidac"></span><span id="INVALIDAC"></span>**InvalidAc**
</dt> <dd>

Questo valore non è valido.

</dd> <dt>

<span id="EveryoneReadUserWriteAc"></span><span id="everyonereaduserwriteac"></span><span id="EVERYONEREADUSERWRITEAC"></span>**EveryoneReadUserWriteAc**
</dt> <dd>

Tutti possono leggere il file. Utenti specifici possono scrivere nel file.

</dd> <dt>

<span id="UserWriteExecuteAc"></span><span id="userwriteexecuteac"></span><span id="USERWRITEEXECUTEAC"></span>**UserWriteExecuteAc**
</dt> <dd>

Solo utenti specifici possono leggere o scrivere nel file.

</dd> <dt>

<span id="EveryoneReadAdminWriteAc"></span><span id="everyonereadadminwriteac"></span><span id="EVERYONEREADADMINWRITEAC"></span>**EveryoneReadAdminWriteAc**
</dt> <dd>

Tutti possono leggere il file. Gli amministratori possono scrivere nel file.

</dd> <dt>

<span id="UnknownAc"></span><span id="unknownac"></span><span id="UNKNOWNAC"></span>**UnknownAc**
</dt> <dd>

Le autorizzazioni di accesso per il file sono sconosciute.

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

[**\_informazioni sul file di scheda \_**](/previous-versions/windows/desktop/secsmart/card-file-info)
</dt> <dt>

[**CardCreateFile**](/previous-versions/windows/desktop/secsmart/cardcreatefile)
</dt> </dl>

 

 
