---
description: Struttura che identifica l'host e il file di origine da valutare.
ms.assetid: 547EF59E-7DE5-45E4-948F-109547FAAEE7
title: WLDP_HOST_INFORMATION (Wldp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WLDP_HOST_INFORMATION
api_type:
- HeaderDef
api_location:
- wldp.h
ms.openlocfilehash: cc1bed8fd104b4aa6abb83d3eb7e19faa37a0301429312c8f0799e256ce32ec6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118404070"
---
# <a name="wldp_host_information-structure"></a>Struttura delle informazioni host WLDP \_ \_

Struttura che identifica l'host e il file di origine da valutare.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _WLDP_HOST_INFORMATION {
  DWORD        dwRevision;
  WLDP_HOST_ID dwHostId;
  PCWSTR       szSource;
  HANDLE       hSource;
} WLDP_HOST_INFORMATION, *PWLDP_HOST_INFORMATION;
```



## <a name="members"></a>Members

<dl> <dt>

**dwRevision**
</dt> <dd>

Deve essere **WLDP \_ HOST INFORMATION \_ \_ REVISION**.

</dd> <dt>

**dwHostId**
</dt> <dd>

Valore di enumerazione [**\_ \_ dell'ID HOST WLDP**](wldp-host-id.md) che descrive l'ID host.

</dd> <dt>

**szSource**
</dt> <dd>

Percorso completo e nome dello script con l'estensione. NULL per **l'ID HOST WLDP \_ \_ \_ GLOBAL** o l'esecuzione manuale di script.

</dd> <dt>

**hSource**
</dt> <dd>

Oltre al nome, il chiamante può specificare un handle per il file utilizzato per la convalida.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                        |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                              |
| Intestazione<br/>                   | <dl> <dt>Wldp.h</dt> </dl> |



 

 




