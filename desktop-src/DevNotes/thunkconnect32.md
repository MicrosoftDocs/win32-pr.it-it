---
description: La funzione ThunkConnect32 viene usata dai driver di dispositivo a 16 bit (per MS-DOS) che effettuano chiamate nel kernel a 32 bit.
ms.assetid: 3376ca67-04ea-4765-a2f4-15a84d5c84d4
title: ThunkConnect32 (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ThunkConnect32
api_type:
- DllExport
api_location:
- Kernel32.dll
ms.openlocfilehash: 7f22d7ceb59732e986c23c873133b11f358364cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324859"
---
# <a name="thunkconnect32-function"></a>ThunkConnect32 (funzione)

\[Questa funzione è supportata per compatibilità con le versioni precedenti, ma non è presente nelle versioni correnti di Windows. I nuovi driver di dispositivo dovrebbero essere 32 o 64 bit e non richiedono questa funzione.\]

La funzione **ThunkConnect32** viene usata dai driver di dispositivo a 16 bit (per MS-DOS) che effettuano chiamate nel kernel a 32 bit.

## <a name="syntax"></a>Sintassi


```C++
BOOL ThunkConnect32(
   LPVOID lpThunkData32,
   LPSTR  pszThunkData16Name,
   LPSTR  pszDll16,
   LPSTR  pszDll32,
   HANDLE hInstance,
   DWORD  dwReason
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpThunkData32* 
</dt> <dd>

Ignorato.

</dd> <dt>

*pszThunkData16Name* 
</dt> <dd>

Ignorato.

</dd> <dt>

*pszDll16* 
</dt> <dd>

Ignorato.

</dd> <dt>

*pszDll32* 
</dt> <dd>

Ignorato.

</dd> <dt>

*hInstance* 
</dt> <dd>

Ignorato.

</dd> <dt>

*dwReason* 
</dt> <dd>

Ignorato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce sempre **false**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Kernel32.dll</dt> </dl> |



 

 




