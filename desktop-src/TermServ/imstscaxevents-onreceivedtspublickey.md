---
title: Metodo IMsTscAxEvents OnReceivedTSPublicKey
description: Chiamato durante la sequenza di connessione quando il client recupera la chiave pubblica dal server. Questo evento viene chiamato solo se la proprietà NotifyTSPublicKey è VARIANT \_ true.
ms.assetid: 1db98b8b-2f08-4252-ad8b-6764fa25b300
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo OnReceivedTSPublicKey
- Metodo OnReceivedTSPublicKey Servizi Desktop remoto, interfaccia IMsTscAxEvents
- Interfaccia IMsTscAxEvents Servizi Desktop remoto, metodo OnReceivedTSPublicKey
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnReceivedTSPublicKey
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 337a9efabe48dee7a5a4194c3b796b95f35a0592
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477434"
---
# <a name="imstscaxeventsonreceivedtspublickey-method"></a>Metodo IMsTscAxEvents:: OnReceivedTSPublicKey

Chiamato durante la sequenza di connessione quando il client recupera la chiave pubblica dal server. Questo evento viene chiamato solo se la proprietà **NotifyTSPublicKey** è **Variant \_ true**. Questa operazione è successiva alla [**connessione**](imstscaxevents-onconnecting.md), ma prima di [**OnAuthenticationWarningDisplayed**](imstscaxevents-onauthenticationwarningdisplayed.md) e [**OnConnected**](imstscaxevents-onconnected.md).

## <a name="syntax"></a>Sintassi


```C++
void OnReceivedTSPublicKey(
  [in]  BSTR         publicKey,
  [out] VARIANT_BOOL *pfContinueLogon
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*publicKey* \[ in\]
</dt> <dd>

Contiene la chiave pubblica del computer remoto.

</dd> <dt>

*pfContinueLogon* \[ out\]
</dt> <dd>

Puntatore a una variabile **\_ bool Variant** che riceve se il processo di accesso deve continuare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008, Windows Server 2008 con SP1<br/>                           |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents è definito come 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





