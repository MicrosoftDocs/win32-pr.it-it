---
title: Metodo ITsSbResourcePluginStoreEx AcquireTargetLock
description: Blocca una destinazione.
ms.assetid: 76707f1d-1f13-4d81-8954-2acf05cda2cd
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo AcquireTargetLock
- Metodo AcquireTargetLock Servizi Desktop remoto, interfaccia ITsSbResourcePluginStoreEx
- Interfaccia ITsSbResourcePluginStoreEx Servizi Desktop remoto, metodo AcquireTargetLock
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
ms.openlocfilehash: 8c18be0a544ebcea2d2cecb40dcea3a08e4bd35b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119262"
---
# <a name="itssbresourcepluginstoreexacquiretargetlock-method"></a>Metodo ITsSbResourcePluginStoreEx:: AcquireTargetLock

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

*TargetName* \[ in\]
</dt> <dd>

Nome della destinazione da bloccare.

</dd> <dt>

*dwTimeOut* \[ in\]
</dt> <dd>

Timeout per l'operazione, espresso in millisecondi.

</dd> <dt>

*ppContext* \[ out\]
</dt> <dd>

Restituisce un puntatore al contesto del blocco. Per rilasciare il blocco, fornire questo puntatore al metodo [**ReleaseTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Una volta acquisito il blocco, si presuppone che il thread chiamante disponga dell'accesso esclusivo all'oggetto di destinazione e che pertanto nessun altro thread (all'interno della stessa macchina) possa aggiornarlo. Pertanto, il thread chiamante deve chiamare il metodo [**ReleaseTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock) non appena ha effettuato gli aggiornamenti necessari per l'oggetto di destinazione.

> [!IMPORTANT]
> Questo blocco non impedisce completamente la modifica esterna degli oggetti di destinazione se nella distribuzione è presente più di un broker di connessione. Il thread chiamante deve essere preparato per gestire correttamente un errore e ripetere l'aggiornamento di destinazione.

 

Questo metodo è disponibile in Windows Server 2012 R2 con [KB3091411](https://support.microsoft.com/kb/3091411) installato nell'interfaccia [**ITsSbResourcePluginStoreEx**](itssbresourcepluginstoreex.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Server minimo supportato<br/> | Windows Server 2012 R2<br/>                                                             |
| Fine del supporto server<br/>    | Windows Server 2012 R2<br/>                                                             |
| IDL<br/>                      | <dl> <dt>SbTsV. idl</dt> </dl>          |
| IID<br/>                      | IID \_ ITsSbResourcePluginStoreEx è definito come 80b83ffd-625d-11e5-bea1-a0481c7e9064<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITsSbResourcePluginStoreEx**](itssbresourcepluginstoreex.md)
</dt> </dl>

 

 





