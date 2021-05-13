---
description: Espone metodi che consentono a un'estensione shell di fornire uno spazio dei nomi ricercabile.
title: Interfaccia IShellFolderSearchable
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchable
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 359def5c-d7ad-46bd-bdda-30a7b3eea56c
ms.openlocfilehash: 6daa00e6821833d783aefa95be23b7b8de769907
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842832"
---
# <a name="ishellfoldersearchable-interface"></a>Interfaccia IShellFolderSearchable

Espone metodi che consentono a un'estensione shell di fornire uno spazio dei nomi ricercabile.

## <a name="members"></a>Membri

**L'interfaccia IShellFolderSearchable** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IShellFolderSearchable** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IShellFolderSearchable** include questi metodi.



| Metodo                                                                | Descrizione                                                               |
|:----------------------------------------------------------------------|:--------------------------------------------------------------------------|
| [**CancelAsyncSearch**](ishellfoldersearchable-cancelasyncsearch.md) | Avvia il processo di annullamento di una ricerca asincrona in sospeso.<br/> |
| [**Findstring**](ishellfoldersearchable-findstring.md)               | Avvia una ricerca per una stringa di ricerca specificata.<br/>                 |
| [**InvalidateSearch**](ishellfoldersearchable-invalidatesearch.md)   | Rende questo PIDL una parte non valida della cartella Shell.<br/>        |



 

## <a name="remarks"></a>Commenti

Questa interfaccia non è definita in alcun file di intestazione pubblico. Se si sceglie di implementare questa interfaccia, è possibile usare il codice C/C++ seguente per dichiarare i relativi metodi.


```
#undef  INTERFACE
#define INTERFACE IShellFolderSearchable
DECLARE_INTERFACE_IID_(IShellFolderSearchable, IUnknown, "4E1AE66C-204B-11d2-8DB3-0000F87A556C")
{
    // *** IUnknown methods ***
    STDMETHOD(QueryInterface) (THIS_ REFIID riid, __out void **ppv) PURE;
    STDMETHOD_(ULONG,AddRef)  (THIS) PURE;
    STDMETHOD_(ULONG,Release) (THIS) PURE;

    // *** IShellFolderSearchable methods ***

    // FindString -
    //  The returned Shell folder's enumerator will have any
    //   search hits for the given search string.
    //  punkOnAsyncSearch will be QI'd for IShellFolderSearchableCallback
    STDMETHOD(FindString)(THIS_ LPCWSTR pwszTarget, __inout_opt DWORD *pdwFlags,
                          __in_opt IUnknown *punkOnAsyncSearch, __out LPITEMIDLIST *ppidlOut)   PURE;
    // CancelAsyncSearch -
    //   Begins the process of canceling any pending
    //    asynchronous search from this pidl.
    //    When the search is actually canceled, RunEnd will be called
    //   Returns: S_OK => cancelling, S_FALSE => not running
    STDMETHOD(CancelAsyncSearch) (THIS_ LPCITEMIDLIST pidlSearch, __inout_opt DWORD *pdwFlags) PURE;

    // InvalidateSearch -
    //   Makes this pidl no longer a valid portion of the Shell folder
    //    Also does some cleanup of any databases used in the search and
    //    will cause the eventual release of the callback
    //   May cause async search to be canceled
    STDMETHOD(InvalidateSearch)  (THIS_ LPCITEMIDLIST pidlSearch, __inout_opt DWORD *pdwFlags) PURE;
};
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 
