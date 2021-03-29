---
description: Consente di visualizzare la scheda condivisione cartelle nella finestra delle proprietà per la cartella specificata.
ms.assetid: e622e4bb-eaf7-494f-b2a2-78ba1311a496
title: ShowShareFolderUI (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShowShareFolderUI
- ShowShareFolderUIW
api_type:
- DllExport
api_location:
- Ntshrui.dll
ms.openlocfilehash: e6270f72d1574a21b98ac9ee3151af1f34f08a72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346426"
---
# <a name="showsharefolderui-function"></a>ShowShareFolderUI (funzione)

Consente di visualizzare la scheda **condivisione cartelle** nella finestra delle proprietà per la cartella specificata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ShowShareFolderUI(
  _In_ HWND    hwndParent,
  _In_ LPCWSTR pszPath
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hwndParent* \[ in\]
</dt> <dd>

Tipo: **HWND**

Handle per la finestra padre della finestra delle proprietà.

</dd> <dt>

*pszPath* \[ in\]
</dt> <dd>

Tipo: **LPCWSTR**

Puntatore a una stringa che specifica il percorso alla cartella che visualizza la scheda **condivisione cartelle** .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Questa funzione restituisce sempre S \_ OK.

## <a name="remarks"></a>Commenti

A questa funzione non è associato alcun file con estensione LIB. Per usarlo, è necessario usare [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Ntshrui.dll</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **ShowShareFolderUIW** (Unicode)<br/>                                            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CanShareFolderW**](cansharefolderw.md)
</dt> </dl>

 

 
