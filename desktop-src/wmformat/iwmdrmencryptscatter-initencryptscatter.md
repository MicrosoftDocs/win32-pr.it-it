---
title: Metodo IWMDRMEncryptScatter InitEncryptScatter (Wmdrmsdk.h)
description: Il metodo InitEncryptScatter inizializza l'interfaccia IWMDRMEncryptScatter per l'uso.
ms.assetid: c5f2fa14-9465-4c53-bc42-ffcec34af083
keywords:
- Metodo InitEncryptScatter windows Media Format
- Metodo InitEncryptScatter windows Media Format , interfaccia IWMDRMEncryptScatter
- IWMDRMEncryptScatter interface windows Media Format , Metodo InitEncryptScatter
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
ms.openlocfilehash: 8e83cce80b218d4cc8482d013537b7fae562312f242bc3549f4fa5069b1c677c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027759"
---
# <a name="iwmdrmencryptscatterinitencryptscatter-method"></a>Metodo IWMDRMEncryptScatter::InitEncryptScatter

Il **metodo InitEncryptScatter** inizializza **l'interfaccia IWMDRMEncryptScatter** per l'uso.

## <a name="syntax"></a>Sintassi


```C++
HRESULT InitEncryptScatter(
  [in] DWORD                      cStreams,
  [in] WMDRM_ENCRYPT_SCATTER_INFO *rgInfos
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*cStreams* \[ Pollici\]
</dt> <dd>

Numero di elementi nella *matrice rgInfos.* Questo è anche il numero di flussi inclusi nei dati da crittografare.

</dd> <dt>

*rgInfos* \[ Pollici\]
</dt> <dd>

Matrice di una o più [**strutture WMDRM \_ ENCRYPT SCATTER \_ \_ INFO.**](wmdrm-encrypt-scatter-info.md) Ogni elemento contiene informazioni di crittografia per un flusso. Il numero di elementi in questa matrice deve essere uguale al valore di *cStreams*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

Nessuno.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**EncryptScatter**](iwmdrmencryptscatter-encryptscatter.md)
</dt> <dt>

[**Interfaccia IWMDRMEncryptScatter**](iwmdrmencryptscatter.md)
</dt> </dl>

 

 





