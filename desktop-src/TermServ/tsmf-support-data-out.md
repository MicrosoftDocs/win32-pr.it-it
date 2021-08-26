---
title: TSMF_SUPPORT_DATA_OUT struttura
description: Contiene informazioni sui formati multimediali. | TSMF_SUPPORT_DATA_OUT struttura
ms.assetid: 987ede31-ad15-489f-90e5-fb707c6b38a9
ms.tgt_platform: multiple
keywords:
- TSMF_SUPPORT_DATA_OUT struttura Servizi Desktop remoto
- PTSMF_SUPPORT_DATA_OUT puntatore alla struttura Servizi Desktop remoto
topic_type:
- apiref
api_name:
- TSMF_SUPPORT_DATA_OUT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8577266c2e259e7a7e4bb70310837eee1d743905e0e0d166e5797bc51a1f1b45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869021"
---
# <a name="tsmf_support_data_out-structure"></a>Struttura TSMF \_ SUPPORT \_ DATA \_ OUT

Contiene informazioni sui formati multimediali. Questa struttura viene usata dal metodo [**QueryProperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty) durante le **query WRDS \_ QUERY \_ MF FORMAT \_ \_ SUPPORT.**

## <a name="syntax"></a>Sintassi


```C++
typedef struct tagTSMF_SUPPORT_DATA_OUT {
  GUID                      guidMfSession;
  UINT32                    numEntries;
  TSMF_SUPPORT_NODEDATA_OUT ...;
} TSMF_SUPPORT_DATA_OUT, *PTSMF_SUPPORT_DATA_OUT;
```



## <a name="members"></a>Members

<dl> <dt>

**guidMfSession**
</dt> <dd>

Deve corrispondere alla proprietà **guidMfSession** nella struttura [**TSMF \_ SUPPORT DATA \_ \_ IN**](tsmf-support-data-in.md) corrispondente.

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

[**SUPPORTO DI TSMF \_ \_ PER NODEDATA \_ OUT**](tsmf-support-nodedata-out.md)
</dt> </dl>

 

 





