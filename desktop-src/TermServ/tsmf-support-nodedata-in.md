---
title: Struttura TSMF_SUPPORT_NODEDATA_IN
description: Usati all'interno del TSMF \_ supportano i \_ dati \_ nella struttura per contenere informazioni sui formati multimediali supportati.
ms.assetid: 9aee9d6d-2182-44ec-ba8b-d2747d3edf71
ms.tgt_platform: multiple
keywords:
- Struttura TSMF_SUPPORT_NODEDATA_IN Servizi Desktop remoto
- Puntatore alla struttura PTSMF_SUPPORT_NODEDATA_IN Servizi Desktop remoto
topic_type:
- apiref
api_name:
- TSMF_SUPPORT_NODEDATA_IN
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4c36d18ea0e97da8df60475855c93755727fa87d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301854"
---
# <a name="tsmf_support_nodedata_in-structure"></a>TSMF \_ supporta \_ NODEDATA \_ nella struttura

Usati all'interno del [**TSMF \_ supportano i \_ dati \_ nella**](tsmf-support-data-in.md) struttura per contenere informazioni sui formati multimediali supportati.

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

**byteCount**
</dt> <dd>

Dimensioni in byte della struttura.

</dd> <dt>

**nodeId**
</dt> <dd>

Nodo.

</dd> <dt>

**numMediaTypes**
</dt> <dd>

Il numero di strutture di formato multimediale.

</dd> <dt>

**...**
</dt> <dd>

Numero variabile di strutture che definiscono formati di supporti audio o video. **FormatType** è **formato \_ WAVEFORMATEX** per l'audio o il **formato \_ MFVideoFormat** per il video.

Per informazioni dettagliate su questa struttura, [vedere \_ struttura \_ del \_ tipo di supporto di Servizi terminal](/openspecs/windows_protocols/ms-rdpev/22a57950-042e-48bd-8135-3580f3a3f934).

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

[**TSMF \_ supporta \_ i dati \_ in**](tsmf-support-data-in.md)
</dt> </dl>

 

