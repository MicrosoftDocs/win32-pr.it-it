---
title: Struttura TSMF_SUPPORT_DATA_OUT
description: Contiene informazioni sui formati multimediali. | Struttura TSMF_SUPPORT_DATA_OUT
ms.assetid: 987ede31-ad15-489f-90e5-fb707c6b38a9
ms.tgt_platform: multiple
keywords:
- Struttura TSMF_SUPPORT_DATA_OUT Servizi Desktop remoto
- Puntatore alla struttura PTSMF_SUPPORT_DATA_OUT Servizi Desktop remoto
topic_type:
- apiref
api_name:
- TSMF_SUPPORT_DATA_OUT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9705c4c2c27eaff904e09364b029bd74ebd05d6c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103969074"
---
# <a name="tsmf_support_data_out-structure"></a>TSMF \_ supporta la \_ struttura dei dati in \_ uscita

Contiene informazioni sui formati multimediali. Questa struttura viene usata dal metodo [**QueryProperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty) durante le query di supporto per il **\_ \_ \_ \_ formato WRDS query MF** .

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

Deve corrispondere alla proprietà **guidMfSession** nei [**\_ \_ dati \_ di supporto TSMF corrispondenti nella**](tsmf-support-data-in.md) struttura.

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

[**\_NODEDATA di supporto TSMF \_ \_**](tsmf-support-nodedata-out.md)
</dt> </dl>

 

 





