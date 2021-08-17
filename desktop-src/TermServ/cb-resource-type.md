---
title: CB_RESOURCE_TYPE enumerazione (Cbclient.h)
description: Specifica il tipo di risorsa a cui si connette la connessione in ingresso.
ms.assetid: 80D921BF-2D84-4A18-9544-50087B81F177
ms.tgt_platform: multiple
keywords:
- CB_RESOURCE_TYPE di enumerazione Servizi Desktop remoto
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
ms.openlocfilehash: 63dfce0f575147233735dd943645eb51c26141cacaaa61c044698b29b8d118e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139114"
---
# <a name="cb_resource_type-enumeration"></a>Enumerazione CB \_ RESOURCE \_ TYPE

Specifica il tipo di risorsa a cui si connette la connessione in ingresso. Questa enumerazione viene utilizzata con la [**struttura \_ CONNECTION \_ INFO di CB.**](cb-connection-info.md)

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

<span id="CB_RESOURCE_UNDEFINED"></span><span id="cb_resource_undefined"></span>**RISORSA CB \_ \_ NON DEFINITA**
</dt> <dd>

Il tipo di risorsa non è definito.

</dd> <dt>

<span id="CB_RESOURCE_SESSION"></span><span id="cb_resource_session"></span>**SESSIONE DI \_ RISORSE \_ CB**
</dt> <dd>

La risorsa è una sessione remota.

</dd> <dt>

<span id="CB_RESOURCE_VM"></span><span id="cb_resource_vm"></span>**MACCHINA VIRTUALE DI \_ RISORSE \_ CB**
</dt> <dd>

La risorsa è una macchina virtuale.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                  |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                        |
| Intestazione<br/>                   | <dl> <dt>Cbclient.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INFORMAZIONI DI CONNESSIONE CB \_ \_**](cb-connection-info.md)
</dt> </dl>

 

 





