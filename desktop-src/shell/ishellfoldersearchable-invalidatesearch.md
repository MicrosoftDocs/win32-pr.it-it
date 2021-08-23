---
description: Rende questo puntatore a un elenco di identificatori di elemento (PIDL) una parte non valida della cartella Shell.
title: Metodo IShellFolderSearchable::InvalidateSearch
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchable.InvalidateSearch
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 6985a299-8547-4db4-99f9-d46dafe4789b
ms.openlocfilehash: 5f443f3abd4a5cf2c1d0fc473c9267660d05c183a02c7f7705c1fabcbc9a8918
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119596571"
---
# <a name="ishellfoldersearchableinvalidatesearch-method"></a>Metodo IShellFolderSearchable::InvalidateSearch

Rende questo puntatore a un elenco di identificatori di elemento (PIDL) una parte non valida della cartella Shell.

## <a name="syntax"></a>Sintassi


```C++
HRESULT InvalidateSearch(
  [in] LPCITEMIDLIST pidlSearch,
  [in] DWORD         *pdwFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pidlSearch* \[ Pollici\]
</dt> <dd>

Tipo: **LPCITEMIDLIST**

Puntatore alla [**struttura ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) per la cartella di ricerca.

</dd> <dt>

*pdwFlags* \[ Pollici\]
</dt> <dd>

Tipo: **DWORD \***

Nessun flag è attualmente definito. impostato su **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Quando una cartella di ricerca viene invalidata, può eseguire la pulizia di tutte le risorse usate. Il **metodo IShellFolderSearchable::InvalidateSearch** può causare l'annullamento di una ricerca asincrona e comporterà la versione finale dell'oggetto interfaccia [**IShellFolderSearchableCallback.**](ishellfoldersearchablecallback.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




