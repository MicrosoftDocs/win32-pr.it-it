---
description: Verifica che l'area multimediale nell'unità DVD corrisponda all'area dell'unità DVD.
ms.assetid: 864de493-94c2-4f32-96a8-14cfea13dbef
title: DvdLauncher (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DvdLauncher
api_type:
- DllExport
api_location:
- StorProp.dll
ms.openlocfilehash: ef49be579052e5a9fd493f5bf246a2efbd217c34
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127291"
---
# <a name="dvdlauncher-function"></a>DvdLauncher (funzione)

Verifica che l'area multimediale nell'unità DVD corrisponda all'area dell'unità DVD.

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI DvdLauncher(
  _In_ HWND HWnd,
  _In_ CHAR DriveLetter
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*HWND* \[ in\]
</dt> <dd>

Handle per la finestra di primo livello da utilizzare per qualsiasi interfaccia utente richiesta.

</dd> <dt>

*LetteraUnità* \[ in\]
</dt> <dd>

Lettera di unità.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo e le aree corrispondono, il valore restituito è diverso da zero. In caso contrario, il valore restituito è zero.

## <a name="remarks"></a>Commenti

A questa funzione non è associata alcuna libreria di importazione. È necessario utilizzare le funzioni [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegare dinamicamente a StorProp.dll.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP<br/>                                                                   |
| Server minimo supportato<br/> | Windows Server 2003<br/>                                                          |
| DLL<br/>                      | <dl> <dt>StorProp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di gestione dei dispositivi](device-management-functions.md)
</dt> </dl>

 

