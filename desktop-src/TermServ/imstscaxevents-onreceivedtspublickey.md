---
title: Metodo IMsTscAxEvents OnReceivedTSPublicKey
description: Chiamato durante la sequenza di connessione quando il client recupera la chiave pubblica dal server. Questo evento viene chiamato solo se la proprietà NotifyTSPublicKey è VARIANT \_ TRUE.
ms.assetid: 1db98b8b-2f08-4252-ad8b-6764fa25b300
ms.tgt_platform: multiple
keywords:
- Metodo OnReceivedTSPublicKey Servizi Desktop remoto
- Metodo OnReceivedTSPublicKey Servizi Desktop remoto , interfaccia IMsTscAxEvents
- Interfaccia IMsTscAxEvents Servizi Desktop remoto , metodo OnReceivedTSPublicKey
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
ms.openlocfilehash: 73f2b12b59cbe8e6b7c5f8e614e2aed047d4f467117fa211839521fedc7f333b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009481"
---
# <a name="imstscaxeventsonreceivedtspublickey-method"></a>Metodo IMsTscAxEvents::OnReceivedTSPublicKey

Chiamato durante la sequenza di connessione quando il client recupera la chiave pubblica dal server. Questo evento viene chiamato solo se la **proprietà NotifyTSPublicKey** è **VARIANT \_ TRUE.** Questo è dopo [**OnConnecting**](imstscaxevents-onconnecting.md), ma prima [**di OnAuthenticationWarningDisplayed**](imstscaxevents-onauthenticationwarningdisplayed.md) [**e OnConnected**](imstscaxevents-onconnected.md).

## <a name="syntax"></a>Sintassi


```C++
void OnReceivedTSPublicKey(
  [in]  BSTR         publicKey,
  [out] VARIANT_BOOL *pfContinueLogon
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*publicKey* \[ Pollici\]
</dt> <dd>

Contiene la chiave pubblica del computer remoto.

</dd> <dt>

*pfContinueLogon* \[ Cambio\]
</dt> <dd>

Puntatore a una **variabile VARIANT \_ BOOL** che riceve se il processo di accesso deve continuare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Per altre informazioni sui Connessione Web Desktop remoto, vedere [Requisiti per Connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

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

 

 





