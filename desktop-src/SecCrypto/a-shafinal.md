---
description: Calcola l'hash finale dei dati immessi dalla funzione MD5Update.
ms.assetid: A0457D26-F4E3-4ED4-B374-0AFCB6F661FB
title: Funzione A_SHAFinal (SHA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- A_SHAFinal
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: 2a206005a686d02891a593243bc0ef3a4ad7db23
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324605"
---
# <a name="a_shafinal-function"></a>\_Funzione SHAFinal

Calcola l'hash finale dei dati immessi dalla funzione MD5Update.

## <a name="syntax"></a>Sintassi


```C++
VOID RSA32API A_SHAFinal(
  _Inout_ A_SHA_CTX     *Context,
  _Out_   UNSIGNED CHAR Result
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Contesto* \[ in uscita\]
</dt> <dd>

Contesto SHA.

</dd> <dt>

*Risultato* \[ out\]
</dt> <dd>

Tabella hash risultante.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Questa funzione è molto simile a SHAFinal, ma viene chiamata direttamente dalla libreria, anziché essere instradata tramite l'infrastruttura di crittografia. Per ulteriori informazioni, vedere [provider NTCryptographic Windows](/previous-versions/tn-archive/cc723484(v=technet.10)).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Sha. h</dt> </dl>     |
| Libreria<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |
| DLL<br/>     | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
