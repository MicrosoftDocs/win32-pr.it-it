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
ms.openlocfilehash: cb5c6e324e657962a4a0bbbfa64cb45fefa7d37a3ca5ce21cd25e072fc1a6594
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119223371"
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

Puntatore a un [**ELEMENTO ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) per la ricerca.

</dd> <dt>

*pdwFlags* \[ Pollici\]
</dt> <dd>

Tipo: **DWORD \***

Nessun flag è attualmente definito. impostato su **NULL.**

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



 

 




