---
description: Recupera la transazione o il proxy di transazione associato al contesto corrente, se presente.
ms.assetid: 2f85f395-3ec5-4c5a-a6db-c902cb8f8486
title: Metodo IContextTransactionInfo::FetchTransaction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextTransactionInfo.FetchTransaction
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6d673483118feb02ec2f1172640b9972d883505f48bc1fd8d8803844b963b02b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991061"
---
# <a name="icontexttransactioninfofetchtransaction-method"></a>Metodo IContextTransactionInfo::FetchTransaction

Recupera la transazione o il proxy di transazione associato al contesto corrente, se presente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT FetchTransaction(
  [out, retval] IUnknown **pUnk
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pUnk* \[ out, retval\]
</dt> <dd>

Proxy di transazione o transazione associato al contesto corrente. in caso contrario, **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire i valori restituiti standard E \_ INVALIDARG, E \_ OUTOFMEMORY, E \_ UNEXPECTED e S \_ OK.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP solo con app desktop SP2 \[\]<br/>          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 con SP1 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IContextTransactionInfo**](icontexttransactioninfo.md)
</dt> </dl>

 

 




