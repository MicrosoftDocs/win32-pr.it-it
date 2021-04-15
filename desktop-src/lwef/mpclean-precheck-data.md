---
title: Struttura MPCLEAN_PRECHECK_DATA (MpClient. h)
description: Dati di notifica passati per pulire la funzione di callback di verifica.
ms.assetid: 65B3B116-6E83-46F5-AE2B-92A41AE39480
keywords:
- Struttura MPCLEAN_PRECHECK_DATA le funzionalità legacy dell'ambiente Windows
- Funzionalità dell'ambiente Windows legacy del puntatore della struttura di PMPCLEAN_PRECHECK_DATA
topic_type:
- apiref
api_name:
- MPCLEAN_PRECHECK_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc3d67e0c71c95db49b633feeb3048cc9f104b2f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476115"
---
# <a name="mpclean_precheck_data-structure"></a>\_Struttura dei dati di PREVERIFICA MPCLEAN \_

Dati di notifica passati per pulire la funzione di callback di verifica.

## <a name="syntax"></a>Sintassi


```C++
typedef struct tagMPCLEAN_PRECHECK_DATA {
  PMPRESOURCE_INFO     BlockedResourceInfo;
  BlockingResourceInfo PMPRESOURCE_INFO;
} MPCLEAN_PRECHECK_DATA, *PMPCLEAN_PRECHECK_DATA;
```



## <a name="members"></a>Members

<dl> <dt>

**BlockedResourceInfo**
</dt> <dd>

Tipo: **PMPRESOURCE \_ info**

</dd> <dd>

Informazioni sulle risorse per la risorsa bloccata. Ad esempio, quando lo stato di avanzamento è **MPNOTIFY la \_ Preverifica della \_ risorsa \_ bloccata**. Vedere [**MPRESOURCE \_ info**](mpresource-info.md).

</dd> <dt>

**\_informazioni PMPRESOURCE**
</dt> <dd>

Tipo: **BlockingResourceInfo**

</dd> <dd>

Informazioni sulle risorse che stanno bloccando. Ad esempio, quando lo stato di avanzamento è **MPNOTIFY la \_ Preverifica della \_ risorsa \_ bloccata**. Vedere [**MPRESOURCE \_ info**](mpresource-info.md).

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
</dt> </dl>

 

 





