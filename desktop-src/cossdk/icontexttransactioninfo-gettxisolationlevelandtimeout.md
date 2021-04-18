---
description: Recupera il livello di isolamento e il valore di timeout di una transazione ospitata nel contesto di transazione radice.
ms.assetid: bb3ff03e-e69e-4a50-af36-4938eb4323df
title: 'Metodo IContextTransactionInfo:: GetTxIsolationLevelAndTimeout'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextTransactionInfo.GetTxIsolationLevelAndTimeout
api_type:
- COM
api_location: ''
ms.openlocfilehash: b8545a697e672af7206a69ffa19618d5b70e055c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305324"
---
# <a name="icontexttransactioninfogettxisolationlevelandtimeout-method"></a>Metodo IContextTransactionInfo:: GetTxIsolationLevelAndTimeout

Recupera il livello di isolamento e il valore di timeout di una transazione ospitata nel contesto di transazione radice.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetTxIsolationLevelAndTimeout(
  [out] ISOLEVEL *pIsoLevel,
  [out] DWORD    *dwTime
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pIsoLevel* \[ out\]
</dt> <dd>

Valore [ISOLATIONLEVEL](/previous-versions/windows/desktop/ms679234(v=vs.85)) per la transazione.

</dd> <dt>

*dwTime* \[ out\]
</dt> <dd>

Timeout della transazione, in secondi.

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

 

