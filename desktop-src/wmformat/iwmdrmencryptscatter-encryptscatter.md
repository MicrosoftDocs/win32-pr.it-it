---
title: Metodo IWMDRMEncryptScatter EncryptScatter (wmdrmsdk. h)
description: Il metodo EncryptScatter consente di decodificare e crittografare i dati.
ms.assetid: e7f87aac-387b-4483-956e-bfbca0cec0f2
keywords:
- Metodo EncryptScatter Windows Media Format
- Metodo EncryptScatter Windows Media Format, interfaccia IWMDRMEncryptScatter
- Interfaccia IWMDRMEncryptScatter-formato Windows Media, metodo EncryptScatter
topic_type:
- apiref
api_name:
- IWMDRMEncryptScatter.EncryptScatter
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58b2d1d6182aed55b60aa1cedfbce5dd870691bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324286"
---
# <a name="iwmdrmencryptscatterencryptscatter-method"></a>Metodo IWMDRMEncryptScatter:: EncryptScatter

Il metodo **EncryptScatter** consente di decodificare e crittografare i dati.

## <a name="syntax"></a>Sintassi


```C++
HRESULT EncryptScatter(
  [in]  DWORD                       cBlocks,
  [in]  WMDRM_ENCRYPT_SCATTER_BLOCK *rgBlocks,
  [in]  WMDRMCryptoData             *pWMCryptoData,
  [in]  DWORD                       cbOutput,
  [out] BYTE                        *pbOutput
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*cBlocks* \[ in\]
</dt> <dd>

Numero di elementi nella matrice *rgBlocks* .

</dd> <dt>

*rgBlocks* \[ in\]
</dt> <dd>

Matrice di una o più strutture di [**\_ \_ \_ blocco a dispersione crittografate WMDRM**](wmdrm-encrypt-scatter-block.md) . Ogni elemento descrive un blocco di dati da non codificare e crittografare.

</dd> <dt>

*pWMCryptoData* \[ in\]
</dt> <dd>

Puntatore a una struttura [**WMDRMCryptoData**](wmdrmcryptodata.md) che contiene i parametri di crittografia. Impostare su **null** per usare i parametri predefiniti.

</dd> <dt>

*cbOutput* \[ in\]
</dt> <dd>

Dimensioni del buffer dei dati di output passati come *pbOutput*.

</dd> <dt>

*pbOutput* \[ out\]
</dt> <dd>

Buffer di output.

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

[**InitEncryptScatter**](iwmdrmencryptscatter-initencryptscatter.md)
</dt> <dt>

[**Interfaccia IWMDRMEncryptScatter**](iwmdrmencryptscatter.md)
</dt> </dl>

 

 





