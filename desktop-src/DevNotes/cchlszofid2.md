---
description: Decodifica e archivia una stringa.
ms.assetid: 6ababd6e-57b7-49eb-98c9-a4bcb558a377
title: Funzione CchLszOfId2
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
ms.openlocfilehash: 0377b8507507b40c5b17c3d9bb6861e5077f8c7bb763b51c66289ab1819f9cc7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815471"
---
# <a name="cchlszofid2-function"></a>Funzione CchLszOfId2

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

*Lsz* 
</dt> <dd>

Puntatore a un buffer con lunghezza *cbmax*. Le stringhe più lunghe di *cbmax* vengono troncate.

</dd> <dt>

*cbmax* 
</dt> <dd>

Lunghezza massima della stringa da archiviare nel *parametro lsz.*

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione restituisce la stringa decodificata.

## <a name="remarks"></a>Commenti

A questa funzione non è associata alcuna libreria di importazione o file di intestazione. è necessario chiamarlo usando le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msjint40.dll</dt> </dl> |



 

 
