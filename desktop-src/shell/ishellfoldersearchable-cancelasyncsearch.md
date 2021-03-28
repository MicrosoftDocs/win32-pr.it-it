---
description: Inizia il processo di annullamento di una ricerca asincrona in sospeso.
title: 'Metodo IShellFolderSearchable:: CancelAsyncSearch'
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
ms.openlocfilehash: e9e3231e8cc602a4e00b6ee79a25392717b6e68b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977954"
---
# <a name="ishellfoldersearchablecancelasyncsearch-method"></a>Metodo IShellFolderSearchable:: CancelAsyncSearch

Inizia il processo di annullamento di una ricerca asincrona in sospeso.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CancelAsyncSearch(
  [in] LPCITEMIDLIST pidlSearch,
  [in] DWORD         *pdwFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pidlSearch* \[ in\]
</dt> <dd>

Tipo: **LPCITEMIDLIST**

Puntatore a un oggetto [**ItemId**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) per la ricerca.

</dd> <dt>

*pdwFlags* \[ in\]
</dt> <dd>

Tipo: **DWORD \** _

Nessun flag attualmente definito. impostare su _ * NULL * *.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Restituisce \_ OK se viene annullata o \_ è false se la ricerca non è in esecuzione.

## <a name="remarks"></a>Commenti

Quando la ricerca viene effettivamente annullata, verrà chiamato [**RunEnd**](ishellfoldersearchablecallback-runend.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




