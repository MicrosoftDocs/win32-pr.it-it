---
title: Struttura MPTHREAT_LOCALIZED_INFO (MpClient. h)
description: Informazioni localizzate per una minaccia.
ms.assetid: 99DC9737-9A61-4407-B544-A7A979C5B556
keywords:
- Struttura MPTHREAT_LOCALIZED_INFO le funzionalità legacy dell'ambiente Windows
- Funzionalità dell'ambiente Windows legacy del puntatore della struttura di PMPTHREAT_LOCALIZED_INFO
topic_type:
- apiref
api_name:
- MPTHREAT_LOCALIZED_INFO
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87ea0bee7c8cae15389b40b64038aad92a56dd5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400595"
---
# <a name="mpthreat_localized_info-structure"></a>\_Struttura delle informazioni localizzate MPTHREAT \_

Informazioni localizzate per una minaccia.

## <a name="syntax"></a>Sintassi


```C++
typedef struct tagMPTHREAT_LOCALIZED_INFO {
  MPTHREAT_ID           ThreatID;
  MP_MIDL_STRING LPWSTR CategoryName;
  MP_MIDL_STRING LPWSTR CategoryDescription;
  MP_MIDL_STRING LPWSTR SeverityName;
  MP_MIDL_STRING LPWSTR SeverityDescription;
  MP_MIDL_STRING LPWSTR ShortDescription;
  MP_MIDL_STRING LPWSTR DefaultActionName;;
  MP_MIDL_STRING LPWSTR Advice;
  MP_MIDL_STRING LPWSTR ThreatUrl;
} MPTHREAT_LOCALIZED_INFO, *PMPTHREAT_LOCALIZED_INFO;
```



## <a name="members"></a>Members

<dl> <dt>

**ThreatID**
</dt> <dd>

Tipo: **MPTHREAT \_ ID**

</dd> <dd>

Identificatore della minaccia. Il bit superiore è impostato in modo da identificare le minacce correlate all'antivirus.

</dd> <dt>

**CategoryName**
</dt> <dd>

Tipo: **\_ \_ LPWSTR stringa MIDL MP**

</dd> <dd>

Classificazione delle minacce, ad esempio un Trojan o un keylogger.

</dd> <dt>

**CategoryDescription**
</dt> <dd>

Tipo: **\_ \_ LPWSTR stringa MIDL MP**

</dd> <dd>

Descrizione della categoria di minacce.

</dd> <dt>

**Gravitàname**
</dt> <dd>

Tipo: **\_ \_ LPWSTR stringa MIDL MP**

</dd> <dd>

Livello di gravità della minaccia, ad esempio grave o moderato.

</dd> <dt>

**SeverityDescription**
</dt> <dd>

Tipo: **\_ \_ LPWSTR stringa MIDL MP**

</dd> <dd>

Descrizione del livello di gravità della minaccia.

</dd> <dt>

**ShortDescription**
</dt> <dd>

Tipo: **\_ \_ LPWSTR stringa MIDL MP**

</dd> <dd>

Breve descrizione della minaccia.

</dd> <dt>

**DefaultActionName;**
</dt> <dd>

Tipo: **\_ \_ LPWSTR stringa MIDL MP**

</dd> <dd>

Nome dell'azione predefinita, ad esempio Remove o Quarantine, suggerito dal motore.

</dd> <dt>

**Advice**
</dt> <dd>

Tipo: **\_ \_ LPWSTR stringa MIDL MP**

</dd> <dd>

Suggerimenti per la minaccia particolare.

</dd> <dt>

**ThreatUrl**
</dt> <dd>

Tipo: **\_ \_ LPWSTR stringa MIDL MP**

</dd> <dd>

URL di una pagina Web contenente informazioni sulla minaccia.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





