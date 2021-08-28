---
description: Aggiunge dati a un oggetto hash specificato.
ms.assetid: 8E32BBC4-C2DD-4174-9FF1-9001E4A7D87B
title: A_SHAUpdate funzione (Sha.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- A_SHAUpdate
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: 103438e3ef0747aa6170848398621b0246bd15366be4d1171ce5735942011007
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101071"
---
# <a name="a_shaupdate-function"></a>Funzione \_ SHAUpdate

Aggiunge dati a un oggetto hash specificato.

## <a name="syntax"></a>Sintassi


```C++
void RSA32API A_SHAUpdate(
  _Inout_ A_SHA_CTX     *Context,
  _Out_   UNSIGNED CHAR *Buffer,
          UNSIGNED INT  BufferSize
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Contesto* \[ in, out\]
</dt> <dd>

Contesto SHA.

</dd> <dt>

*Buffer* \[ Cambio\]
</dt> <dd>

Tabella hash.

</dd> <dt>

*BufferSize* 
</dt> <dd>

Dimensione del buffer.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Questa funzione può essere chiamata più volte per calcolare l'hash su flussi di dati lunghi o flussi di dati discontinui. La [**funzione \_ SHAFinal**](a-shafinal.md) deve essere chiamata prima di recuperare il valore hash.

Questa funzione è molto simile a SHAUpdate, ma viene chiamata direttamente dalla libreria, anziché essere instradata tramite l'infrastruttura di crittografia. Per altre informazioni, vedere [Windows NTCryptographic Providers](/previous-versions/tn-archive/cc723484(v=technet.10)).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Sha.h</dt> </dl>     |
| Libreria<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |
| DLL<br/>     | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
