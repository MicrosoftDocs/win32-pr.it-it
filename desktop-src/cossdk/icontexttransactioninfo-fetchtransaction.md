---
description: Recupera la transazione o il proxy di transazione associato al contesto corrente, se presente.
ms.assetid: 2f85f395-3ec5-4c5a-a6db-c902cb8f8486
title: 'Metodo IContextTransactionInfo:: FetchTransaction'
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
ms.openlocfilehash: 0e753974f93539f051465f13a1ea92d7e0e3bfa1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127031"
---
# <a name="icontexttransactioninfofetchtransaction-method"></a>Metodo IContextTransactionInfo:: FetchTransaction

Recupera la transazione o il proxy di transazione associato al contesto corrente, se presente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT FetchTransaction(
  [out, retval] IUnknown **pUnk
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*punk* \[ out, retval\]
</dt> <dd>

Transazione o proxy di transazione associato al contesto corrente. in caso contrario, **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire i valori restituiti standard E \_ INVALIDARG, e \_ OutOfMemory, e \_ imprevisto e S \_ OK.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP con SP2 \[\]<br/>          |
| Server minimo supportato<br/> | Windows Server 2003 con \[ solo app desktop SP1\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IContextTransactionInfo**](icontexttransactioninfo.md)
</dt> </dl>

 

 




