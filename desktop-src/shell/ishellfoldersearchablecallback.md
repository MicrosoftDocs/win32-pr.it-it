---
description: Espone routine di callback per monitorare il processo di ricerca.
title: Interfaccia IShellFolderSearchableCallback
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchableCallback
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 3412a01b-d5ea-44e1-819c-f10f81fac391
ms.openlocfilehash: 620acb5d5a3486b721cac3818c57b8392174436f68a304a8788ef62bccae28b2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119443291"
---
# <a name="ishellfoldersearchablecallback-interface"></a>Interfaccia IShellFolderSearchableCallback

Espone routine di callback per monitorare il processo di ricerca.

## <a name="members"></a>Membri

**L'interfaccia IShellFolderSearchableCallback** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IShellFolderSearchableCallback** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IShellFolderSearchableCallback** include questi metodi.



| Metodo                                                      | Descrizione                                      |
|:------------------------------------------------------------|:-------------------------------------------------|
| [**RunBegin**](ishellfoldersearchablecallback-runbegin.md) | Indica che è stata avviata una ricerca.<br/>  |
| [**RunEnd**](ishellfoldersearchablecallback-runend.md)     | Indica che una ricerca è stata completata.<br/> |



 

## <a name="remarks"></a>Commenti

Questa interfaccia non è definita in alcun file di intestazione pubblico. Se si sceglie di implementare questa interfaccia, è possibile usare il codice C/C++ seguente per dichiararne i metodi.


```
#undef  INTERFACE
#define INTERFACE IShellFolderSearchableCallback
DECLARE_INTERFACE_IID_(IShellFolderSearchableCallback, IUnknown, "F98D8294-2BBC-11d2-8DBD-0000F87A556C")
{
    // *** IUnknown methods ***
    STDMETHOD(QueryInterface) (THIS_ REFIID riid, __out void **ppv) PURE;
    STDMETHOD_(ULONG,AddRef)  (THIS) PURE;
    STDMETHOD_(ULONG,Release) (THIS) PURE;

    // *** IShellFolderSearchableCallback Methods ***

    STDMETHOD(RunBegin)(THIS_ DWORD dwReserved) PURE;
    STDMETHOD(RunEnd)(THIS_ DWORD dwReserved) PURE;
};
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 
