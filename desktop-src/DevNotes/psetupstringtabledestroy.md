---
description: Elimina una tabella di stringhe.
ms.assetid: a3ac1672-f898-44a0-bb7b-64ac24bdb9bf
title: Funzione pSetupStringTableDestroy
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
ms.openlocfilehash: adbde578b144aaa79993ede50ef5fbd480582c3354467a2d37b424a1897cae63
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119386411"
---
# <a name="psetupstringtabledestroy-function"></a>Funzione pSetupStringTableDestroy

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

*StringTable* \[ Pollici\]
</dt> <dd>

Puntatore alla tabella di stringhe.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

A questa funzione non è associata alcuna libreria di importazione o file di intestazione. è necessario chiamarlo usando le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



 

 
