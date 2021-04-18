---
description: Questa funzione recupera la versione della libreria del registro di sistema offline.
ms.assetid: 625f088a-db5e-47ea-aa48-39b1c70cf15b
title: Funzione ORGetVersion (offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORGetVersion
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: d909013d88c9a3abbe91f152e1333fb5faf35852
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328366"
---
# <a name="orgetversion-function"></a>ORGetVersion (funzione)

Questa funzione recupera la versione della libreria del registro di sistema offline.

## <a name="syntax"></a>Sintassi


```C++
VOID ORGetVersion(
  _Out_ PDWORD pdwMajorVersion,
  _Out_ PDWORD pdwMinorVersion
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pdwMajorVersion* \[ out\]
</dt> <dd>

Puntatore a una variabile per ricevere la versione principale della libreria del registro di sistema offline. Per la versione iniziale della libreria, il valore è 1.

</dd> <dt>

*pdwMinorVersion* \[ out\]
</dt> <dd>

Puntatore a una variabile per ricevere la versione secondaria della libreria del registro di sistema offline. Per la versione iniziale della libreria, il valore è 0.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|---------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | Windows offline Registry Library versione 1,0 o successiva<br/>                      |
| Intestazione<br/>          | <dl> <dt>Offreg. h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



 

 




