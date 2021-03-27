---
description: Rende questo puntatore a un elenco di identificatori di elemento (PIDL) una parte non valida della cartella della shell.
title: 'Metodo IShellFolderSearchable:: InvalidateSearch'
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
ms.openlocfilehash: 36c1de0a606fdfddbe8eb74b5cc6c20cdda8e983
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226364"
---
# <a name="ishellfoldersearchableinvalidatesearch-method"></a>Metodo IShellFolderSearchable:: InvalidateSearch

Rende questo puntatore a un elenco di identificatori di elemento (PIDL) una parte non valida della cartella della shell.

## <a name="syntax"></a>Sintassi


```C++
HRESULT InvalidateSearch(
  [in] LPCITEMIDLIST pidlSearch,
  [in] DWORD         *pdwFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pidlSearch* \[ in\]
</dt> <dd>

Tipo: **LPCITEMIDLIST**

Puntatore alla struttura [**ItemId**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) per la cartella di ricerca.

</dd> <dt>

*pdwFlags* \[ in\]
</dt> <dd>

Tipo: **DWORD \** _

Nessun flag attualmente definito. impostare su _ * NULL * *.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Quando una cartella di ricerca viene invalidata, può eseguire la pulizia delle risorse usate. Il metodo **IShellFolderSearchable:: InvalidateSearch** può causare l'annullamento di una ricerca asincrona e comporterà la versione finale dell'oggetto interfaccia [**IShellFolderSearchableCallback**](ishellfoldersearchablecallback.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




