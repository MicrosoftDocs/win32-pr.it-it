---
description: Espone metodi che consentono a una cartella della shell di supportare visualizzazioni diverse sul contenuto (layout gerarchici diversi dei dati).
title: Interfaccia IShellFolderViewType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderViewType
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 9b597f6b-ef27-4fa1-ad00-e131dbd979e7
ms.openlocfilehash: 1440b6d14950ad70d2c76168b28bb1077b19b5a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049998"
---
# <a name="ishellfolderviewtype-interface"></a>Interfaccia IShellFolderViewType

Espone metodi che consentono a una cartella della shell di supportare visualizzazioni diverse sul contenuto (layout gerarchici diversi dei dati).

## <a name="members"></a>Membri

L'interfaccia **IShellFolderViewType** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IShellFolderViewType** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IShellFolderViewType** dispone di questi metodi.



| Metodo                                                                      | Descrizione                                                                                                                                                          |
|:----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EnumViews**](ishellfolderviewtype-enumviews.md)                         | Recupera un enumeratore che restituirà un PIDL per ogni visualizzazione estesa.<br/>                                                                                |
| [**GetDefaultViewName**](ishellfolderviewtype-getdefaultviewname.md)       | Ottiene il nome della visualizzazione predefinita. Chiamare [**IShellFolder:: GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) per recuperare i nomi delle altre visualizzazioni.<br/> |
| [**GetViewTypeProperties**](ishellfolderviewtype-getviewtypeproperties.md) | Ottiene le proprietà della visualizzazione.<br/>                                                                                                                          |
| [**TranslateViewPidl**](ishellfolderviewtype-translateviewpidl.md)         | Ricostruisce un PIDL da una rappresentazione gerarchica della cartella della shell in un'altra rappresentazione.<br/>                                             |



 

## <a name="remarks"></a>Commenti

Questo enumeratore restituisce PIDL che sono cartelle nascoste speciali nel primo livello della cartella della shell, che non sono altrimenti enumerate. La visualizzazione predefinita è quella visualizzata nella cartella della shell normalmente.

Questa interfaccia non è definita in alcun file di intestazione pubblico. Se si sceglie di implementare questa interfaccia, è possibile usare il codice C/C++ seguente per dichiararne i metodi.


```
#undef  INTERFACE
#define INTERFACE   IShellFolderViewType
DECLARE_INTERFACE_IID_(IShellFolderViewType, IUnknown, "49422C1E-1C03-11d2-8DAB-0000F87A556C")
{
    // **_ IUnknown methods _*_
    STDMETHOD(QueryInterface) (THIS_ REFIID riid, __out void _*ppv) PURE;
    STDMETHOD_(ULONG,AddRef)  (THIS) PURE;
    STDMETHOD_(ULONG,Release) (THIS) PURE;

    // **_ IShellFolderViewType Methods _*_

    // EnumViews:
    //   Returns an enumerator which will give out one pidl for every extended view.
    STDMETHOD(EnumViews)(THIS_ ULONG grfFlags, __out IEnumIDList _*ppenum) PURE;

    // GetDefaultViewName:
    //   Returns the name of the default view.  The names of the other views
    //   can be retrieved by calling GetDisplayNameOf.
    STDMETHOD(GetDefaultViewName)(THIS_ DWORD  uFlags, __out LPWSTR *ppwszName) PURE;
    STDMETHOD(GetViewTypeProperties)(THIS_ PCUITEMID_CHILD pidl, __out DWORD *pdwFlags)  PURE;

    // TranslateViewPidl:
    //   Attempts to take a pidl represented in one hierarchical representation of
    //   the Shell folder, and find it in a different representation.
    //   pidl should be relative to the root folder.
    //   Remember to ILFree ppidlOut
    STDMETHOD(TranslateViewPidl)(THIS_ PCUIDLIST_RELATIVE pidl, PCUIDLIST_RELATIVE pidlView,
              __out PIDLIST_RELATIVE *ppidlOut) PURE;
};

#define SFVTFLAG_NOTIFY_CREATE  0x00000001
#define SFVTFLAG_NOTIFY_RESORT  0x00000002
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 
