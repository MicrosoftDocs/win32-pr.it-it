---
description: Visualizza la finestra di dialogo Gestione chiavi nell'interfaccia utente.
ms.assetid: 65c2763f-42d5-4534-94f7-e753f6486014
title: KRShowKeyMgr (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KRShowKeyMgr
api_type:
- DllExport
api_location:
- Keymgr.dll
ms.openlocfilehash: 59b6b38cf7e78755c7d5c481a22a0a8b3854c8a6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324700"
---
# <a name="krshowkeymgr-function"></a>KRShowKeyMgr (funzione)

\[Questa funzione è inclusa solo in Windows XP. Non è attualmente incluso in nessun'altra versione di Windows, né dovrebbe essere incluso nelle versioni future di Windows.\]

Visualizza la finestra di dialogo Gestione chiavi nell'interfaccia utente.

## <a name="syntax"></a>Sintassi


```C++
void KRShowKeyMgr(
   HWND      hwParent,
   HINSTANCE hInstance,
   LPWSTR    pszCmdLine,
   int       CmdShow
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hwParent* 
</dt> <dd>

Handle per la finestra padre della finestra di dialogo. Questo parametro può essere **NULL**.

</dd> <dt>

*hInstance* 
</dt> <dd>

Questo parametro non viene utilizzato e deve essere impostato su **null**.

</dd> <dt>

*pszCmdLine* 
</dt> <dd>

Questo parametro non viene utilizzato e deve essere impostato su **null**.

</dd> <dt>

*CmdShow* 
</dt> <dd>

Questo parametro non viene utilizzato e deve essere impostato su **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Keymgr.dll</dt> </dl> |



 

 
