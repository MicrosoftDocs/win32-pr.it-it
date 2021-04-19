---
description: Decodifica e archivia una stringa.
ms.assetid: 6ababd6e-57b7-49eb-98c9-a4bcb558a377
title: CchLszOfId2 (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CchLszOfId2
api_type:
- DllExport
api_location:
- Msjint40.dll
ms.openlocfilehash: cba2d09f9865c43a5b64a34783c621c783c7aac3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331472"
---
# <a name="cchlszofid2-function"></a>CchLszOfId2 (funzione)

Decodifica e archivia una stringa.

## <a name="syntax"></a>Sintassi


```C++
UINT CchLszOfId2(
   UINT  id,
   WCHAR *lsz,
   UINT  cbmax
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*id* 
</dt> <dd>

Identificatore della stringa nel file di risorse da decodificare e archiviare. La validità della stringa non viene verificata.

</dd> <dt>

*LSZ* 
</dt> <dd>

Puntatore a un buffer con una lunghezza di *cbmax*. Le stringhe più lunghe di *cbmax* vengono troncate.

</dd> <dt>

*cbmax* 
</dt> <dd>

Lunghezza massima della stringa da archiviare nel parametro *LSZ* .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione restituisce la stringa decodificata.

## <a name="remarks"></a>Commenti

A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msjint40.dll</dt> </dl> |



 

 
