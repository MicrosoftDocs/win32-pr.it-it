---
description: Avvia il processo di annullamento di una ricerca asincrona in sospeso.
title: Metodo IShellFolderSearchable::CancelAsyncSearch
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchable.CancelAsyncSearch
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 5c920dca-fbca-48e1-9dce-38713cf1fcef
ms.openlocfilehash: 3146fea4f6c8d8547c8c86096b434cbaea5b5926
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842992"
---
# <a name="ishellfoldersearchablecancelasyncsearch-method"></a>Metodo IShellFolderSearchable::CancelAsyncSearch

Avvia il processo di annullamento di una ricerca asincrona in sospeso.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CancelAsyncSearch(
  [in] LPCITEMIDLIST pidlSearch,
  [in] DWORD         *pdwFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pidlSearch* \[ Pollici\]
</dt> <dd>

Tipo: **LPCITEMIDLIST**

Puntatore a un [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) per la ricerca.

</dd> <dt>

*pdwFlags* \[ Pollici\]
</dt> <dd>

Tipo: **DWORD \***

Non è attualmente definito alcun flag. impostato su **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Restituisce S \_ OK in caso di annullamento oppure S FALSE se la ricerca non è in \_ esecuzione.

## <a name="remarks"></a>Commenti

Quando la ricerca viene effettivamente annullata, [**viene chiamato RunEnd.**](ishellfoldersearchablecallback-runend.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




