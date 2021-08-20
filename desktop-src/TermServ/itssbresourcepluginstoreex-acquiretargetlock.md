---
title: Metodo ITsSbResourcePluginStoreEx AcquireTargetLock
description: Blocca una destinazione.
ms.assetid: 76707f1d-1f13-4d81-8954-2acf05cda2cd
ms.tgt_platform: multiple
keywords:
- Metodo AcquireTargetLock Servizi Desktop remoto
- Metodo AcquireTargetLock Servizi Desktop remoto, interfaccia ITsSbResourcePluginStoreEx
- Interfaccia ITsSbResourcePluginStoreEx Servizi Desktop remoto , metodo AcquireTargetLock
topic_type:
- apiref
api_name:
- ITsSbResourcePluginStoreEx.AcquireTargetLock
api_location:
- SbTsV.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f80a2ab7068ec754a89e384028f2d43989345e9801c4ededb800117d211b0f8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118128458"
---
# <a name="itssbresourcepluginstoreexacquiretargetlock-method"></a>Metodo ITsSbResourcePluginStoreEx::AcquireTargetLock

Blocca una destinazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT AcquireTargetLock(
  [in]  BSTR     targetName,
  [in]  DWORD    dwTimeout,
  [out] IUnknown **ppContext
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*targetName* \[ Pollici\]
</dt> <dd>

Nome della destinazione da bloccare.

</dd> <dt>

*dwTimeout* \[ Pollici\]
</dt> <dd>

Timeout dell'operazione, espresso in millisecondi.

</dd> <dt>

*ppContext* \[ Cambio\]
</dt> <dd>

Restituisce un puntatore al contesto del blocco. Per rilasciare il blocco, fornire questo puntatore al [**metodo ReleaseTargetLock.**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Dopo l'acquisizione del blocco, si presuppone che il thread chiamante abbia accesso esclusivo all'oggetto di destinazione e pertanto nessun altro thread (all'interno dello stesso computer) può aggiornarlo. Pertanto, il thread chiamante deve chiamare il [**metodo ReleaseTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock) non appena ha apportato gli aggiornamenti necessari all'oggetto di destinazione.

> [!IMPORTANT]
> Questo blocco non impedisce completamente la modifica esterna degli oggetti di destinazione se nella distribuzione sono presenti più broker di connessione. Il thread chiamante deve essere preparato per gestire correttamente un errore e ripetere l'aggiornamento di destinazione.

 

Questo metodo è disponibile Windows Server 2012 R2 con [KB3091411](https://support.microsoft.com/kb/3091411) installato [**nell'interfaccia ITsSbResourcePluginStoreEx.**](itssbresourcepluginstoreex.md)

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

 

 





