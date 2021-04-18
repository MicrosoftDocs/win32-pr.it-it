---
title: Struttura WMDRMCryptoData (wmdrmsdk. h)
description: La struttura WMDRMCryptoData contiene informazioni sull'algoritmo di crittografia utilizzato per crittografare e decrittografare il contenuto.
ms.assetid: ad14c6d3-4305-47c0-8f67-7ef6d11cc326
keywords:
- Formato Windows Media della struttura WMDRMCryptoData
- struttura Windows Media Format
topic_type:
- apiref
api_name:
- WMDRMCryptoData
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce972cdf41ff1e587d40b5fc95021f568be95f9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330880"
---
# <a name="wmdrmcryptodata-structure"></a>Struttura WMDRMCryptoData

La struttura **WMDRMCryptoData** contiene informazioni sull'algoritmo di crittografia utilizzato per crittografare e decrittografare il contenuto.

## <a name="syntax"></a>Sintassi


```C++
typedef struct WMDRMCryptoData {
  DRM_CRYPTO_TYPE  cryptoType;
  unsigned __int64 qwCounterID;
  unsigned __int64 qwOffset;
} ;
```



## <a name="members"></a>Members

<dl> <dt>

**cryptoType**
</dt> <dd>

Membro dell'enumerazione [**del \_ \_ tipo di crittografia DRM**](drm-crypto-type.md) che specifica il tipo di algoritmo di crittografia.

</dd> <dt>

**qwCounterID**
</dt> <dd>

Bit 64 alti della modalità del contatore AES a 128 bit. Questo membro viene usato solo se il membro **cryptoType** è impostato su **Crypto \_ Type \_ MCE**.

</dd> <dt>

**qwOffset**
</dt> <dd>

Bit 64 bassi della modalità del contatore AES a 128 bit. Questo membro viene usato solo se il membro **cryptoType** è impostato su **Crypto \_ Type \_ MCE**.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Strutture**](drm-structures.md)
</dt> </dl>

 

 





