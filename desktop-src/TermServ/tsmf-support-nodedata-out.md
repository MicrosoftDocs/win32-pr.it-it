---
title: Struttura TSMF_SUPPORT_NODEDATA_OUT
description: Usati all'interno \_ di TSMF supportano la \_ struttura dei dati \_ per contenere informazioni sui formati multimediali supportati.
ms.assetid: cac0af9e-6750-4735-b075-46c77aea7d41
ms.tgt_platform: multiple
keywords:
- Struttura TSMF_SUPPORT_NODEDATA_OUT Servizi Desktop remoto
- Puntatore alla struttura PTSMF_SUPPORT_NODEDATA_OUT Servizi Desktop remoto
topic_type:
- apiref
api_name:
- TSMF_SUPPORT_NODEDATA_OUT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 517170e9d6580f69b59f71e0994351ebe0484ddc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874069"
---
# <a name="tsmf_support_nodedata_out-structure"></a>TSMF \_ supporta \_ la \_ struttura NODEDATA out

Usati all'interno di [**TSMF supportano la struttura \_ \_ dei dati \_**](tsmf-support-data-out.md) per contenere informazioni sui formati multimediali supportati.

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

**nodeId**
</dt> <dd>

Nodo.

</dd> <dt>

**hrSupportStatus**
</dt> <dd>

Indica se il sink identificato dal parametro *clsidNewSink* è supportato.

I valori possibili sono.

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

[**TSMF \_ supporta \_ i dati in \_ uscita**](tsmf-support-data-out.md)
</dt> </dl>

 

 





