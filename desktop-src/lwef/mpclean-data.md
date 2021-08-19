---
title: MPCLEAN_DATA struttura (MpClient.h)
description: Dati di notifica passati alla funzione di callback clean.
ms.assetid: 475A6525-5BD8-4B29-A684-53EE2758C790
keywords:
- MPCLEAN_DATA struttura Legacy Windows Environment Features
- PMPCLEAN_DATA puntatore alla struttura Legacy Windows Environment Features
topic_type:
- apiref
api_name:
- MPCLEAN_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ece20324fc06fb68a813b374a698b2e27264068c9051bb2a5fff328c7ad328d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118476339"
---
# <a name="mpclean_data-structure"></a>Struttura MPCLEAN \_ DATA

Dati di notifica passati alla funzione di callback clean.

## <a name="syntax"></a>Sintassi


```C++
typedef struct tagMPCLEAN_DATA {
  MPTHREAT_ID      ThreatID;
  MPTHREAT_ACTION  ThreatAction;
  DWORD            dwStatus;
  PMPRESOURCE_INFO ResourceInfo;
} MPCLEAN_DATA, *PMPCLEAN_DATA;
```



## <a name="members"></a>Members

<dl> <dt>

**ThreatID**
</dt> <dd>

Tipo: **MPTHREAT \_ ID**

</dd> <dd>

Identificatore di minaccia per gli **eventi MPNOTIFY \_ CLEAN THREAT \_ \_ START** / **MPNOTIFY \_ CLEAN THREAT \_ \_ SUCCEEDED** / **MPNOTIFY \_ CLEAN THREAT \_ \_ FAILED.** Il bit superiore è impostato per identificare le minacce correlate all'antivirus.

</dd> <dt>

**ThreatAction**
</dt> <dd>

Tipo: **[ **MPTHREAT \_ ACTION**](mpthreat-action.md)**

</dd> <dd>

Azione di minaccia per gli **eventi MPNOTIFY \_ CLEAN THREAT \_ \_ START** / **MPNOTIFY \_ CLEAN THREAT \_ \_ SUCCEEDED** / **MPNOTIFY \_ CLEAN THREAT \_ \_ FAILED.** Vedere [**MPTHREAT \_ ACTION**](mpthreat-action.md).

</dd> <dt>

**dwStatus**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Stato o azioni aggiuntive associate all'azione eseguita. Si tratta di una combinazione di flag di bit [**da MPSTATUS \_ FLAG**](mpstatus-flag.md).

</dd> <dt>

**ResourceInfo**
</dt> <dd>

Tipo: **PMPRESOURCE \_ INFO**

</dd> <dd>

Informazioni sulle risorse per gli **eventi MPNOTIFY \_ CLEAN THREAT \_ \_ START** / **MPNOTIFY \_ CLEAN THREAT \_ \_ SUCCEEDED** / **MPNOTIFY \_ CLEAN THREAT \_ \_ FAILED.** Vedere [**MPRESOURCE \_ INFO**](mpresource-info.md).

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                            |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INFORMAZIONI SU \_ MPRESOURCE**](mpresource-info.md)
</dt> <dt>

[**MPSTATUS \_ FLAG**](mpstatus-flag.md)
</dt> <dt>

[**AZIONE \_ MPTHREAT**](mpthreat-action.md)
</dt> </dl>

 

 





