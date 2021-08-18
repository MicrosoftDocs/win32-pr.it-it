---
title: TSMF_SUPPORT_NODEDATA_IN struttura
description: Usato all'interno della struttura TSMF \_ SUPPORT DATA IN per \_ \_ contenere informazioni sui formati multimediali supportati.
ms.assetid: 9aee9d6d-2182-44ec-ba8b-d2747d3edf71
ms.tgt_platform: multiple
keywords:
- TSMF_SUPPORT_NODEDATA_IN struttura Servizi Desktop remoto
- PTSMF_SUPPORT_NODEDATA_IN puntatore alla struttura Servizi Desktop remoto
topic_type:
- apiref
api_name:
- TSMF_SUPPORT_NODEDATA_IN
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5e1920ca627a7da8aef2d49a6930b03f0906cfd912e2a2a584b20d8e8382b706
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117755723"
---
# <a name="tsmf_support_nodedata_in-structure"></a>Struttura \_ \_ NODEDATA DI SUPPORTO TSMF \_

Usato all'interno [**della struttura TSMF \_ SUPPORT DATA \_ \_ IN**](tsmf-support-data-in.md) per contenere informazioni sui formati multimediali supportati.

## <a name="syntax"></a>Sintassi


```C++
typedef struct tagTSMF_SUPPORT_NODEDATA_IN {
  UINT32           byteCount;
  INT64            nodeId;
  UINT32           numMediaTypes;
  TS_AM_MEDIA_TYPE ...;
} TSMF_SUPPORT_NODEDATA_IN, *PTSMF_SUPPORT_NODEDATA_IN;
```



## <a name="members"></a>Members

<dl> <dt>

**Bytecount**
</dt> <dd>

Dimensioni della struttura in byte.

</dd> <dt>

**Nodeid**
</dt> <dd>

Nodo.

</dd> <dt>

**numMediaTypes**
</dt> <dd>

Numero di strutture di formato multimediale.

</dd> <dt>

**...**
</dt> <dd>

Numero variabile di strutture che definiscono formati multimediali audio o video. FormatType **è** FORMAT **\_ WaveFormatEx per** audio o **FORMAT \_ MFVideoFormat** per il video.

Per informazioni dettagliate su questa struttura, vedere [TS \_ AM MEDIA \_ TYPE \_ Structure](/openspecs/windows_protocols/ms-rdpev/22a57950-042e-48bd-8135-3580f3a3f934).

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

[**DATI DI SUPPORTO TSMF \_ \_ \_ IN**](tsmf-support-data-in.md)
</dt> </dl>

 

