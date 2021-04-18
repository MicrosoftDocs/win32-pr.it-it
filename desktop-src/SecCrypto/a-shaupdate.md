---
description: Aggiunge dati a un oggetto hash specificato.
ms.assetid: 8E32BBC4-C2DD-4174-9FF1-9001E4A7D87B
title: Funzione A_SHAUpdate (SHA. h)
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
ms.openlocfilehash: a0f8ac49d8221538a168ade536e55766e209d3d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324601"
---
# <a name="a_shaupdate-function"></a>\_Funzione SHAUpdate

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

*Contesto* \[ in uscita\]
</dt> <dd>

Contesto SHA.

</dd> <dt>

*Buffer* \[ out\]
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

Questa funzione può essere chiamata più volte per calcolare l'hash su flussi di dati lunghi o flussi di dati discontinui. Prima [**di \_**](a-shafinal.md) recuperare il valore hash, è necessario chiamare la funzione SHAFinal.

Questa funzione è molto simile a SHAUpdate, ma viene chiamata direttamente dalla libreria, anziché essere instradata tramite l'infrastruttura di crittografia. Per ulteriori informazioni, vedere [provider NTCryptographic Windows](/previous-versions/tn-archive/cc723484(v=technet.10)).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Sha. h</dt> </dl>     |
| Libreria<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |
| DLL<br/>     | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
