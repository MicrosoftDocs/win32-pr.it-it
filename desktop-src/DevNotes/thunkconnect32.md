---
description: La funzione ThunkConnect32 viene usata dai driver di dispositivo a 16 bit (per MS-DOS) che chiamano nel kernel a 32 bit.
ms.assetid: 3376ca67-04ea-4765-a2f4-15a84d5c84d4
title: Funzione ThunkConnect32
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
ms.openlocfilehash: 3f754d4c0e88ee860d112a6fb99d15c2690af0014951e77425d425b65ad16e39
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119929111"
---
# <a name="thunkconnect32-function"></a>Funzione ThunkConnect32

\[Questa funzione è supportata per la compatibilità con le versioni precedenti, ma non è presente nelle versioni correnti di Windows. I nuovi driver di dispositivo devono essere a 32 o 64 bit e non necessitano di questa funzione.\]

La **funzione ThunkConnect32** viene usata dai driver di dispositivo a 16 bit (per MS-DOS) che chiamano nel kernel a 32 bit.

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

Restituisce sempre **FALSE.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Kernel32.dll</dt> </dl> |



 

 




