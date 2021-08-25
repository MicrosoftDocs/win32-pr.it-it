---
description: Recupera il livello di isolamento e il valore di timeout di una transazione ospitata nel contesto della transazione radice.
ms.assetid: bb3ff03e-e69e-4a50-af36-4938eb4323df
title: Metodo IContextTransactionInfo::GetTxIsolationLevelAndTimeout
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
ms.openlocfilehash: 41888a859b6b665390290ba66bed69418cbddd9b708355dc78cc2670ba4d240f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119896081"
---
# <a name="icontexttransactioninfogettxisolationlevelandtimeout-method"></a>Metodo IContextTransactionInfo::GetTxIsolationLevelAndTimeout

Recupera il livello di isolamento e il valore di timeout di una transazione ospitata nel contesto della transazione radice.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetTxIsolationLevelAndTimeout(
  [out] ISOLEVEL *pIsoLevel,
  [out] DWORD    *dwTime
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pIsoLevel* \[ Cambio\]
</dt> <dd>

Valore [ISOLATIONLEVEL](/previous-versions/windows/desktop/ms679234(v=vs.85)) per la transazione.

</dd> <dt>

*dwTime* \[ Cambio\]
</dt> <dd>

Timeout della transazione, espresso in secondi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire i valori restituiti standard E \_ INVALIDARG, E \_ OUTOFMEMORY, E \_ UNEXPECTED e S \_ OK.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP solo con app desktop SP2 \[\]<br/>          |
| Server minimo supportato<br/> | Windows Solo Server 2003 con app desktop SP1 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IContextTransactionInfo**](icontexttransactioninfo.md)
</dt> </dl>

 

