---
description: Avvia l'hashing di un flusso di dati.
ms.assetid: 0EA7C98E-777C-4B2A-AF35-04F90BA3D024
title: A_SHAInit funzione (Sha.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- A_SHAInit
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: a0081311988a5da0ae5ca21e924305918bb1e713a6cde3be1b77821c9b458cb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117774266"
---
# <a name="a_shainit-function"></a>Una \_ funzione SHAInit

Avvia l'hashing di un flusso di dati.

## <a name="syntax"></a>Sintassi


```C++
void RSA32API A_SHAInit(
  _Inout_ A_SHA_CTX *Context
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Contesto* \[ in, out\]
</dt> <dd>

Contesto SHA.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Questa funzione è molto simile a SHAInit, ma viene chiamata direttamente dalla libreria, anziché essere instradata tramite l'infrastruttura di crittografia. Per altre informazioni, vedere [Windows NTCryptographic Providers](/previous-versions/tn-archive/cc723484(v=technet.10)).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Sha.h</dt> </dl>     |
| Libreria<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |
| DLL<br/>     | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
