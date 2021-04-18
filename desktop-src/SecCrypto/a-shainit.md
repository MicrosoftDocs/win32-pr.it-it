---
description: Avvia l'hashing di un flusso di dati.
ms.assetid: 0EA7C98E-777C-4B2A-AF35-04F90BA3D024
title: Funzione A_SHAInit (SHA. h)
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
ms.openlocfilehash: 831c86b02c946896014fa9eec02270f2e963e484
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324602"
---
# <a name="a_shainit-function"></a>\_Funzione SHAInit

Avvia l'hashing di un flusso di dati.

## <a name="syntax"></a>Sintassi


```C++
void RSA32API A_SHAInit(
  _Inout_ A_SHA_CTX *Context
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Contesto* \[ in uscita\]
</dt> <dd>

Contesto SHA.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Questa funzione è molto simile a SHAInit, ma viene chiamata direttamente dalla libreria, anziché essere instradata tramite l'infrastruttura di crittografia. Per ulteriori informazioni, vedere [provider NTCryptographic Windows](/previous-versions/tn-archive/cc723484(v=technet.10)).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Sha. h</dt> </dl>     |
| Libreria<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |
| DLL<br/>     | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
