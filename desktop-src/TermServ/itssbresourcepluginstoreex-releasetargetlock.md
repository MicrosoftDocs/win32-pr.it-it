---
title: Metodo ITsSbResourcePluginStoreEx ReleaseTargetLock
description: Rilascia un blocco su una destinazione.
ms.assetid: ab2ae9f3-2d38-4b31-9889-58297c574bd4
ms.tgt_platform: multiple
keywords:
- Metodo ReleaseTargetLock Servizi Desktop remoto
- Metodo ReleaseTargetLock Servizi Desktop remoto, interfaccia ITsSbResourcePluginStoreEx
- Interfaccia ITsSbResourcePluginStoreEx Servizi Desktop remoto , metodo ReleaseTargetLock
topic_type:
- apiref
api_name:
- ITsSbResourcePluginStoreEx.ReleaseTargetLock
api_location:
- SbTsV.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7fbe40d0fc7a28697d0e2fa9727f9e844eb39759db0dddf02c1d9e01bd843c0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989911"
---
# <a name="itssbresourcepluginstoreexreleasetargetlock-method"></a>Metodo ITsSbResourcePluginStoreEx::ReleaseTargetLock

Rilascia un blocco su una destinazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ReleaseTargetLock(
  [in] IUnknown *pContext
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pContext* \[ Pollici\]
</dt> <dd>

Puntatore al contesto restituito dal [**metodo AcquireTargetLock.**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-acquiretargetlock)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Questo metodo è disponibile solo Windows Server 2012 R2 con [KB3091411](https://support.microsoft.com/kb/3091411) installato [**nell'interfaccia ITsSbResourcePluginStoreEx.**](itssbresourcepluginstoreex.md) Questo metodo è disponibile [**nell'interfaccia ITsSbResourcePluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore) a partire da Windows Server 2016.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Server minimo supportato<br/> | R2 per Windows Server 2012<br/>                                                             |
| Fine del supporto server<br/>    | R2 per Windows Server 2012<br/>                                                             |
| Idl<br/>                      | <dl> <dt>SbTsV.idl</dt> </dl>          |
| IID<br/>                      | ITsSbResourcePluginStoreEx IID è definito come \_ 80b83ffd-625d-11e5-bea1-a0481c7e9064<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITsSbResourcePluginStoreEx**](itssbresourcepluginstoreex.md)
</dt> </dl>

 

 





