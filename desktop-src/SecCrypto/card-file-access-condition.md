---
description: Specifica le autorizzazioni di controllo di accesso per un file in un smart card.
ms.assetid: 995d959f-30dc-4e5c-be2d-6b447499415a
title: CARD_FILE_ACCESS_CONDITION enumerazione (Cardmod.h)
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
ms.openlocfilehash: e9a38e7d67e413352de693f52b07ba11bf34858854fa708b41a735152ad3ed2f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771987"
---
# <a name="card_file_access_condition-enumeration"></a>Enumerazione CARD \_ FILE \_ ACCESS \_ CONDITION

**L'enumerazione CARD FILE ACCESS \_ \_ \_ CONDITION** specifica le autorizzazioni di controllo di accesso per un file in un [*smart card*](../secgloss/s-gly.md).

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

Tutti gli utenti possono leggere il file. Utenti specifici possono scrivere nel file.

</dd> <dt>

<span id="UserWriteExecuteAc"></span><span id="userwriteexecuteac"></span><span id="USERWRITEEXECUTEAC"></span>**UserWriteExecuteAc**
</dt> <dd>

Solo utenti specifici possono leggere o scrivere nel file.

</dd> <dt>

<span id="EveryoneReadAdminWriteAc"></span><span id="everyonereadadminwriteac"></span><span id="EVERYONEREADADMINWRITEAC"></span>**EveryoneReadAdminWriteAc**
</dt> <dd>

Tutti gli utenti possono leggere il file. Gli amministratori possono scrivere nel file.

</dd> <dt>

<span id="UnknownAc"></span><span id="unknownac"></span><span id="UNKNOWNAC"></span>**UnknownAc**
</dt> <dd>

Le autorizzazioni di accesso per il file sono sconosciute.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP, Windows solo \[ app desktop XP\]<br/>                              |
| Server minimo supportato<br/> | Windows Solo app desktop Windows Server 2003 Server 2003 \[\]<br/>            |
| Intestazione<br/>                   | <dl> <dt>Cardmod.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Provider del servizio di crittografia smart card di base Microsoft](/previous-versions/windows/desktop/secsmart/microsoft-base-smart-card-cryptographic-service-provider)
</dt> <dt>

[**INFORMAZIONI \_ SUL FILE DI \_ SCHEDA**](/previous-versions/windows/desktop/secsmart/card-file-info)
</dt> <dt>

[**CardCreateFile**](/previous-versions/windows/desktop/secsmart/cardcreatefile)
</dt> </dl>

 

 
