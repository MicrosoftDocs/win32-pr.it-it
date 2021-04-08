---
title: Struttura MPCLEAN_DATA (MpClient. h)
description: Dati di notifica passati alla funzione di callback pulita.
ms.assetid: 475A6525-5BD8-4B29-A684-53EE2758C790
keywords:
- Struttura MPCLEAN_DATA le funzionalità legacy dell'ambiente Windows
- Funzionalità dell'ambiente Windows legacy del puntatore della struttura di PMPCLEAN_DATA
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
ms.openlocfilehash: 89f0c7e867918b6567279be7c41ce72e7e396576
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741026"
---
# <a name="mpclean_data-structure"></a>\_Struttura dei dati MPCLEAN

Dati di notifica passati alla funzione di callback pulita.

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

Identificatore di minaccia per **MPNOTIFY \_ Clean \_ Threat \_ Start** / **MPNOTIFY \_ Clean \_ Threat \_ succeeded** / **MPNOTIFY \_ Clean \_ Threat \_ failed** Events. Il bit superiore è impostato in modo da identificare le minacce correlate all'antivirus.

</dd> <dt>

**ThreatAction**
</dt> <dd>

Tipo: **[ **\_ azione MPTHREAT**](mpthreat-action.md)**

</dd> <dd>

Azione di minaccia per **MPNOTIFY \_ Clean \_ Threat \_ Start** / **MPNOTIFY \_ Clean \_ Threat \_ succeeded** / **MPNOTIFY \_ Clean \_ Threat \_ failed** Events. Vedere [**\_ azione MPTHREAT**](mpthreat-action.md).

</dd> <dt>

**dwStatus**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Stato o azioni aggiuntive associate all'azione eseguita. Si tratta di una combinazione di flag di bit del [**\_ flag MPSTATUS**](mpstatus-flag.md).

</dd> <dt>

**ResourceInfo**
</dt> <dd>

Tipo: **PMPRESOURCE \_ info**

</dd> <dd>

Informazioni sulle risorse per la **MPNOTIFY \_ Clean \_ Threat \_ Start** / **MPNOTIFY \_ Clean \_ Threat \_ succeeded** / **MPNOTIFY \_ Clean \_ Threat \_ failed** Events. Vedere [**MPRESOURCE \_ info**](mpresource-info.md).

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_informazioni MPRESOURCE**](mpresource-info.md)
</dt> <dt>

[**\_flag MPSTATUS**](mpstatus-flag.md)
</dt> <dt>

[**\_azione MPTHREAT**](mpthreat-action.md)
</dt> </dl>

 

 





