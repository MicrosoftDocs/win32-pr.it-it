---
description: Struttura che identifica l'host e il file di origine da valutare.
ms.assetid: 547EF59E-7DE5-45E4-948F-109547FAAEE7
title: Struttura WLDP_HOST_INFORMATION (Wldp. h)
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
ms.openlocfilehash: ad20be7fa5887e42c09248d04e14f5ff8cffcd54
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049097"
---
# <a name="wldp_host_information-structure"></a>\_ \_ Struttura delle informazioni sull'host WLDP

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

Deve essere **la \_ \_ \_ revisione delle informazioni sull'host WLDP**.

</dd> <dt>

**dwHostId**
</dt> <dd>

Valore di enumerazione [**dell' \_ \_ ID host WLDP**](wldp-host-id.md) che descrive l'ID host.

</dd> <dt>

**szSource**
</dt> <dd>

Percorso completo e nome di script con l'estensione. NULL per **l' \_ ID host WLDP \_ \_ globale** o l'esecuzione di script manuale.

</dd> <dt>

**hSource**
</dt> <dd>

Oltre al nome, il chiamante può specificare un handle per il file utilizzato per la convalida.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                              |
| Intestazione<br/>                   | <dl> <dt>Wldp. h</dt> </dl> |



 

 




