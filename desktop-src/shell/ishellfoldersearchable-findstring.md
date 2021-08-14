---
description: Avvia una ricerca per una stringa di ricerca specificata.
ms.assetid: 6ecad03c-e8e0-45ba-8def-b55a029992f2
title: Metodo IShellFolderSearchable::FindString (Mmc.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchable.FindString
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 947cda4094491702fa0f847e6a8abd4fed7bcbe9bd3504c5f8aec2097b0d6b8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118220937"
---
# <a name="ishellfoldersearchablefindstring-method"></a>Metodo IShellFolderSearchable::FindString

Avvia una ricerca per una stringa di ricerca specificata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT FindString(
  [in]  LPCWSTR      pwszTarget,
  [in]  DWORD        *pdwFlags,
  [in]  IUnknown     *punkOnAsyncSearch,
  [out] LPITEMIDLIST ppidlOut
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pwszTarget* \[ Pollici\]
</dt> <dd>

Tipo: **LPCWSTR**

Puntatore a una stringa che specifica la parola chiave di ricerca.

</dd> <dt>

*pdwFlags* \[ Pollici\]
</dt> <dd>

Tipo: **DWORD \***

Nessun flag è attualmente definito. impostato su **NULL.**

</dd> <dt>

*punkOnAsyncSearch* \[ Pollici\]
</dt> <dd>

Tipo: **[ **IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***

Puntatore a un oggetto di tipo [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) Questo oggetto deve supportare [**l'interfaccia IShellFolderSearchableCallback.**](ishellfoldersearchablecallback.md) Impostare su **NULL se** non è necessario alcun callback.

</dd> <dt>

*ppidlOut* \[ Cambio\]
</dt> <dd>

Tipo: **LPITEMIDLIST**

Puntatore a una [**struttura ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) per la cartella di ricerca.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Mmc.h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 
