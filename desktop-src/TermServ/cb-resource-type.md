---
title: Enumerazione CB_RESOURCE_TYPE (Cbclient. h)
description: Specifica il tipo di risorsa a cui si connette la connessione in ingresso.
ms.assetid: 80D921BF-2D84-4A18-9544-50087B81F177
ms.tgt_platform: multiple
keywords:
- Enumerazione CB_RESOURCE_TYPE Servizi Desktop remoto
topic_type:
- apiref
api_name:
- CB_RESOURCE_TYPE
api_location:
- Cbclient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60561e4af54c6d27288d8df311693d51c0b9fc77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740583"
---
# <a name="cb_resource_type-enumeration"></a>Enumerazione del tipo di \_ risorsa CB \_

Specifica il tipo di risorsa a cui si connette la connessione in ingresso. Questa enumerazione viene utilizzata con la struttura delle [**\_ \_ informazioni di connessione CB**](cb-connection-info.md) .

## <a name="syntax"></a>Sintassi


```C++
typedef enum _CB_RESOURCE_TYPE { 
  CB_RESOURCE_UNDEFINED  = 0,
  CB_RESOURCE_SESSION    = 1,
  CB_RESOURCE_VM
} CB_RESOURCE_TYPE;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="CB_RESOURCE_UNDEFINED"></span><span id="cb_resource_undefined"></span>**risorsa CB non \_ \_ definita**
</dt> <dd>

Il tipo di risorsa non è definito.

</dd> <dt>

<span id="CB_RESOURCE_SESSION"></span><span id="cb_resource_session"></span>**\_sessione di risorse CB \_**
</dt> <dd>

La risorsa è una sessione remota.

</dd> <dt>

<span id="CB_RESOURCE_VM"></span><span id="cb_resource_vm"></span>**\_VM delle risorse CB \_**
</dt> <dd>

La risorsa è una macchina virtuale.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                  |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                        |
| Intestazione<br/>                   | <dl> <dt>Cbclient. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_informazioni di connessione CB \_**](cb-connection-info.md)
</dt> </dl>

 

 





