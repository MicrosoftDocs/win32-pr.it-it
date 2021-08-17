---
title: TSMF_SUPPORT_DATA_IN struttura
description: Contiene informazioni sui formati multimediali. | TSMF_SUPPORT_DATA_IN struttura
ms.assetid: cd1a8295-22b7-4d75-8325-94da4d7380d0
ms.tgt_platform: multiple
keywords:
- TSMF_SUPPORT_DATA_IN struttura Servizi Desktop remoto
- PTSMF_SUPPORT_DATA_IN puntatore alla struttura Servizi Desktop remoto
topic_type:
- apiref
api_name:
- TSMF_SUPPORT_DATA_IN
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8ae90099b69494425344ff65b73090cce574b843cd1589572203a4786b38ff6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117755777"
---
# <a name="tsmf_support_data_in-structure"></a>Struttura TSMF \_ SUPPORT \_ DATA \_ IN

Contiene informazioni sui formati multimediali. Questa struttura viene usata dal metodo [**QueryProperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty) durante le **query WRDS \_ QUERY \_ MF FORMAT \_ \_ SUPPORT.**

## <a name="syntax"></a>Sintassi


```C++
typedef struct tagTSMF_SUPPORT_DATA_IN {
  GUID                     guidMfSession;
  UINT32                   numEntries;
  TSMF_SUPPORT_NODEDATA_IN ...;
} TSMF_SUPPORT_DATA_IN, *PTSMF_SUPPORT_DATA_IN;
```



## <a name="members"></a>Members

<dl> <dt>

**guidMfSession**
</dt> <dd>

Sessione.

</dd> <dt>

**numEntries**
</dt> <dd>

Numero di strutture nei dati a lunghezza variabile.

</dd> <dt>

**...**
</dt> <dd>

Numero variabile di strutture contenenti dati in formato multimediale.

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

[**TSMF \_ SUPPORTA \_ NODEDATA \_ IN**](tsmf-support-nodedata-in.md)
</dt> </dl>

 

 





