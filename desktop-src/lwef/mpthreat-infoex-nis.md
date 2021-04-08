---
title: Struttura MPTHREAT_INFOEX_NIS (MpClient. h)
description: Contiene informazioni specifiche di NIS.
ms.assetid: 3887C5BF-B1F6-4420-B40A-9585E44BE7A9
keywords:
- Struttura MPTHREAT_INFOEX_NIS le funzionalità legacy dell'ambiente Windows
- Funzionalità dell'ambiente Windows legacy del puntatore della struttura di PMPTHREAT_INFOEX_NIS
topic_type:
- apiref
api_name:
- MPTHREAT_INFOEX_NIS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b4ed68432a2d0ebe78535a139fcc7b0882b9ba7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048312"
---
# <a name="mpthreat_infoex_nis-structure"></a>MPTHREAT \_ INFOEX- \_ struttura NIS

Contiene informazioni specifiche di NIS.

## <a name="syntax"></a>Sintassi


```C++
typedef struct tagMPTHREAT_INFOEX_NIS {
  MP_MIDL_STRING LPWSTR SourceIP;
  MP_MIDL_STRING LPWSTR DestinationIP;
  DWORD                 dwSourceport;
  DWORD                 dwDestinationport;
  MP_MIDL_STRING LPWSTR Protocol;
  MP_MIDL_STRING LPWSTR Link;
} MPTHREAT_INFOEX_NIS, *PMPTHREAT_INFOEX_NIS;
```



## <a name="members"></a>Members

<dl> <dt>

**SourceIP**
</dt> <dd>

Tipo: **\_ \_ LPWSTR stringa MIDL MP**

</dd> <dd></dd> <dt>

**DestinationIP**
</dt> <dd>

Tipo: **\_ \_ LPWSTR stringa MIDL MP**

</dd> <dd></dd> <dt>

**dwSourceport**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd></dd> <dt>

**dwDestinationport**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd></dd> <dt>

**Protocollo**
</dt> <dd>

Tipo: **\_ \_ LPWSTR stringa MIDL MP**

</dd> <dd></dd> <dt>

**Collegamento**
</dt> <dd>

Tipo: **\_ \_ LPWSTR stringa MIDL MP**

</dd> <dd></dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





