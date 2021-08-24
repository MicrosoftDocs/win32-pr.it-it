---
title: TSMF_SUPPORT_NODEDATA_OUT struttura
description: Utilizzato all'interno della struttura TSMF \_ SUPPORT DATA OUT per \_ \_ contenere informazioni sui formati multimediali supportati.
ms.assetid: cac0af9e-6750-4735-b075-46c77aea7d41
ms.tgt_platform: multiple
keywords:
- TSMF_SUPPORT_NODEDATA_OUT struttura Servizi Desktop remoto
- PTSMF_SUPPORT_NODEDATA_OUT puntatore alla struttura Servizi Desktop remoto
topic_type:
- apiref
api_name:
- TSMF_SUPPORT_NODEDATA_OUT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: df3eb4c515963e13d2a7919c58a6d55ca4b2a7600c429a33516093215b5ac0eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869011"
---
# <a name="tsmf_support_nodedata_out-structure"></a>Struttura \_ \_ NODEDATA OUT DI SUPPORTO TSMF \_

Utilizzato all'interno [**della struttura TSMF \_ SUPPORT DATA \_ \_ OUT**](tsmf-support-data-out.md) per contenere informazioni sui formati multimediali supportati.

## <a name="syntax"></a>Sintassi


```C++
typedef struct tagTSMF_SUPPORT_NODEDATA_OUT {
  INT64   nodeId;
  HRESULT hrSupportStatus;
  CLSID   clsidNewSink;
  UINT32  supportedMediaTypeIndex;
} TSMF_SUPPORT_NODEDATA_OUT, *PTSMF_SUPPORT_NODEDATA_OUT;
```



## <a name="members"></a>Members

<dl> <dt>

**Nodeid**
</dt> <dd>

Nodo.

</dd> <dt>

**hrSupportStatus**
</dt> <dd>

Indica se il sink identificato dal *parametro clsidNewSink* è supportato.

I valori possibili sono .

<dt>

0
</dt> <dd>

Non supportato

</dd> <dt>

1
</dt> <dd>

Supportato

</dd> </dl>

Altri valori non sono definiti.

</dd> <dt>

**clsidNewSink**
</dt> <dd>

Sink associato al tipo di supporto.

</dd> <dt>

**supportedMediaTypeIndex**
</dt> <dd>

Indice in base zero del tipo di supporto supportato dal sink.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>         |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**QueryProperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty)
</dt> <dt>

[**TSMF \_ SUPPORT \_ DATA \_ OUT**](tsmf-support-data-out.md)
</dt> </dl>

 

 





