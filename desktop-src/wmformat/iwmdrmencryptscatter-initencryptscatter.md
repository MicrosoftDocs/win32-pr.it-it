---
title: Metodo IWMDRMEncryptScatter InitEncryptScatter (wmdrmsdk. h)
description: Il metodo InitEncryptScatter Inizializza l'interfaccia IWMDRMEncryptScatter per l'utilizzo.
ms.assetid: c5f2fa14-9465-4c53-bc42-ffcec34af083
keywords:
- Metodo InitEncryptScatter Windows Media Format
- Metodo InitEncryptScatter Windows Media Format, interfaccia IWMDRMEncryptScatter
- Interfaccia IWMDRMEncryptScatter-formato Windows Media, metodo InitEncryptScatter
topic_type:
- apiref
api_name:
- IWMDRMEncryptScatter.InitEncryptScatter
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef788ecbe85defc7d3593f0c12c035e516f095eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328536"
---
# <a name="iwmdrmencryptscatterinitencryptscatter-method"></a>Metodo IWMDRMEncryptScatter:: InitEncryptScatter

Il metodo **InitEncryptScatter** Inizializza l'interfaccia **IWMDRMEncryptScatter** per l'utilizzo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT InitEncryptScatter(
  [in] DWORD                      cStreams,
  [in] WMDRM_ENCRYPT_SCATTER_INFO *rgInfos
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*cStreams* \[ in\]
</dt> <dd>

Numero di elementi nella matrice *rgInfos* . Questo è anche il numero di flussi inclusi nei dati da crittografare.

</dd> <dt>

*rgInfos* \[ in\]
</dt> <dd>

Matrice di una o più strutture di [**\_ \_ \_ informazioni di dispersione crittografate WMDRM**](wmdrm-encrypt-scatter-info.md) . Ogni elemento contiene informazioni di crittografia per un flusso. Il numero di elementi nella matrice deve essere uguale al valore di *cStreams*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

Nessuna.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**EncryptScatter**](iwmdrmencryptscatter-encryptscatter.md)
</dt> <dt>

[**Interfaccia IWMDRMEncryptScatter**](iwmdrmencryptscatter.md)
</dt> </dl>

 

 





