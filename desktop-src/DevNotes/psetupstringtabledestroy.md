---
description: Elimina una tabella di stringhe.
ms.assetid: a3ac1672-f898-44a0-bb7b-64ac24bdb9bf
title: pSetupStringTableDestroy (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupStringTableDestroy
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 472ee152d98c064edb8bac5d4de849b505b634da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325206"
---
# <a name="psetupstringtabledestroy-function"></a>pSetupStringTableDestroy (funzione)

\[Questa funzione non è disponibile in Windows Vista o Windows Server 2008.\]

Elimina una tabella di stringhe.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI pSetupStringTableDestroy(
  _In_ PVOID StringTable
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Un'STRINGTABLE* \[ in\]
</dt> <dd>

Puntatore alla tabella delle stringhe.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



 

 
