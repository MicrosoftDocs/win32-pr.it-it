---
title: Struttura WMDRMCryptoData (Wmdrmsdk.h)
description: La struttura WMDRMCryptoData contiene informazioni sull'algoritmo di crittografia usato per crittografare e decrittografare il contenuto.
ms.assetid: ad14c6d3-4305-47c0-8f67-7ef6d11cc326
keywords:
- Formato windows Media della struttura WMDRMCryptoData
- Struttura windows Media Format
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
ms.openlocfilehash: 8a732b7c1c4a4ca8d664255d39573b10ac1bdd4d004deb73d723a43b55db70ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083805"
---
# <a name="wmdrmcryptodata-structure"></a>Struttura WMDRMCryptoData

La **struttura WMDRMCryptoData** contiene informazioni sull'algoritmo di crittografia usato per crittografare e decrittografare il contenuto.

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

Membro [**dell'enumerazione DRM \_ CRYPTO \_ TYPE**](drm-crypto-type.md) che specifica il tipo di algoritmo di crittografia.

</dd> <dt>

**qwCounterID**
</dt> <dd>

I 64 bit alti della modalità contatore AES a 128 bit. Questo membro viene usato solo se il membro **cryptoType** è impostato su **CRYPTO TYPE \_ \_ MCE.**

</dd> <dt>

**qwOffset**
</dt> <dd>

I 64 bit bassi della modalità contatore AES a 128 bit. Questo membro viene usato solo se il membro **cryptoType** è impostato su **CRYPTO TYPE \_ \_ MCE.**

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Strutture**](drm-structures.md)
</dt> </dl>

 

 





