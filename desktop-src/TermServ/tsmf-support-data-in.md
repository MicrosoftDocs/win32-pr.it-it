---
title: Struttura TSMF_SUPPORT_DATA_IN
description: Contiene informazioni sui formati multimediali. | Struttura TSMF_SUPPORT_DATA_IN
ms.assetid: cd1a8295-22b7-4d75-8325-94da4d7380d0
ms.tgt_platform: multiple
keywords:
- Struttura TSMF_SUPPORT_DATA_IN Servizi Desktop remoto
- Puntatore alla struttura PTSMF_SUPPORT_DATA_IN Servizi Desktop remoto
topic_type:
- apiref
api_name:
- TSMF_SUPPORT_DATA_IN
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2072363978cb0e70d64a09d855ed2861341e9cf0
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321541"
---
# <a name="tsmf_support_data_in-structure"></a>TSMF \_ supporta \_ i dati \_ nella struttura

Contiene informazioni sui formati multimediali. Questa struttura viene usata dal metodo [**QueryProperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty) durante le query di supporto per il **\_ \_ \_ \_ formato WRDS query MF** .

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

Numero variabile di strutture che contengono dati di formato multimediale.

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

[**\_supporto \_ di TSMF NODEDATA \_ in**](tsmf-support-nodedata-in.md)
</dt> </dl>

 

 





