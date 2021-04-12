---
description: Associa un'implementazione di ITransactionProxy al contesto corrente.
ms.assetid: 64009632-b536-41fb-95ac-b23e2cbf18da
title: 'Metodo IContextTransactionInfo:: RegisterTransactionProxy'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextTransactionInfo.RegisterTransactionProxy
api_type:
- COM
api_location: ''
ms.openlocfilehash: 7b559453b0d4ed75f92f7a421be4c3a47e07fdf7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342391"
---
# <a name="icontexttransactioninforegistertransactionproxy-method"></a>Metodo IContextTransactionInfo:: RegisterTransactionProxy

Associa un'implementazione di [**ITransactionProxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) al contesto corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT RegisterTransactionProxy(
  [in]  ITransactionProxy *pProxy,
  [out] GUID              *pGuid
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pProxy* \[ in\]
</dt> <dd>

Implementazione di [**ITransactionProxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) da associare al contesto corrente.

</dd> <dt>

*pGuid* \[ out\]
</dt> <dd>

GUID che identifica il proxy di transazione. COM+ utilizza questo GUID quando viene chiamato [**ITransactionProxy:: commit**](/windows/desktop/api/ComSvcs/nf-comsvcs-itransactionproxy-commit) sul proxy di transazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire i valori restituiti standard E \_ INVALIDARG, e \_ OutOfMemory e e \_ imprevisto, oltre ai valori seguenti.



| Codice restituito                                                                                                     | Descrizione                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                            | Metodo completato correttamente.<br/>                                                                           |
| <dl> <dt>**CONTESTO \_ E \_ ALREADYINTRANSACTION**</dt> </dl> | Al contesto corrente è già associata un'implementazione di [**ITransactionProxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) .<br/> |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>                       | Il contesto corrente ospita una transazione BYOT (Bring Your Own Transaction) o una transazione non radice.<br/>    |



 

## <a name="remarks"></a>Commenti

Il metodo **RegisterTransactionProxy** può essere chiamato solo se il contesto corrente è un contesto di transazione radice. Non può essere chiamato se il contesto ospita una transazione BYOT o una transazione non radice.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP con SP2 \[\]<br/>          |
| Server minimo supportato<br/> | Windows Server 2003 con \[ solo app desktop SP1\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IContextTransactionInfo**](icontexttransactioninfo.md)
</dt> </dl>

 

 




