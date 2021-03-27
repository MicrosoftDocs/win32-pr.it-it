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
# <a name="ishellfolderviewtype-interface"></a><span data-ttu-id="f572e-103">Interfaccia IShellFolderViewType</span><span class="sxs-lookup"><span data-stu-id="f572e-103">IShellFolderViewType interface</span></span>

<span data-ttu-id="f572e-104">Espone metodi che consentono a una cartella della shell di supportare visualizzazioni diverse sul contenuto (layout gerarchici diversi dei dati).</span><span class="sxs-lookup"><span data-stu-id="f572e-104">Exposes methods that enable a Shell folder to support different views on its content (different hierarchical layouts of its data).</span></span>

## <a name="members"></a><span data-ttu-id="f572e-105">Membri</span><span class="sxs-lookup"><span data-stu-id="f572e-105">Members</span></span>

<span data-ttu-id="f572e-106">L'interfaccia **IShellFolderViewType** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="f572e-106">The **IShellFolderViewType** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f572e-107">**IShellFolderViewType** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f572e-107">**IShellFolderViewType** also has these types of members:</span></span>

-   [<span data-ttu-id="f572e-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="f572e-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f572e-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="f572e-109">Methods</span></span>

<span data-ttu-id="f572e-110">L'interfaccia **IShellFolderViewType** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="f572e-110">The **IShellFolderViewType** interface has these methods.</span></span>



| <span data-ttu-id="f572e-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="f572e-111">Method</span></span>                                                                      | <span data-ttu-id="f572e-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f572e-112">Description</span></span>                                                                                                                                                          |
|:----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f572e-113">**EnumViews**</span><span class="sxs-lookup"><span data-stu-id="f572e-113">**EnumViews**</span></span>](ishellfolderviewtype-enumviews.md)                         | <span data-ttu-id="f572e-114">Recupera un enumeratore che restituirà un PIDL per ogni visualizzazione estesa.</span><span class="sxs-lookup"><span data-stu-id="f572e-114">Retrieves an enumerator that will return one PIDL for every extended view.</span></span><br/>                                                                                |
| [<span data-ttu-id="f572e-115">**GetDefaultViewName**</span><span class="sxs-lookup"><span data-stu-id="f572e-115">**GetDefaultViewName**</span></span>](ishellfolderviewtype-getdefaultviewname.md)       | <span data-ttu-id="f572e-116">Ottiene il nome della visualizzazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="f572e-116">Gets the name of the default view.</span></span> <span data-ttu-id="f572e-117">Chiamare [**IShellFolder:: GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) per recuperare i nomi delle altre visualizzazioni.</span><span class="sxs-lookup"><span data-stu-id="f572e-117">Call [**IShellFolder::GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) to retrieve the names of the other views.</span></span><br/> |
| [<span data-ttu-id="f572e-118">**GetViewTypeProperties**</span><span class="sxs-lookup"><span data-stu-id="f572e-118">**GetViewTypeProperties**</span></span>](ishellfolderviewtype-getviewtypeproperties.md) | <span data-ttu-id="f572e-119">Ottiene le proprietà della visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="f572e-119">Gets the properties of the view.</span></span><br/>                                                                                                                          |
| [<span data-ttu-id="f572e-120">**TranslateViewPidl**</span><span class="sxs-lookup"><span data-stu-id="f572e-120">**TranslateViewPidl**</span></span>](ishellfolderviewtype-translateviewpidl.md)         | <span data-ttu-id="f572e-121">Ricostruisce un PIDL da una rappresentazione gerarchica della cartella della shell in un'altra rappresentazione.</span><span class="sxs-lookup"><span data-stu-id="f572e-121">Reconstructs a PIDL from one hierarchical representation of the Shell folder into a different representation.</span></span><br/>                                             |



 

## <a name="remarks"></a><span data-ttu-id="f572e-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="f572e-122">Remarks</span></span>

<span data-ttu-id="f572e-123">Questo enumeratore restituisce PIDL che sono cartelle nascoste speciali nel primo livello della cartella della shell, che non sono altrimenti enumerate.</span><span class="sxs-lookup"><span data-stu-id="f572e-123">This enumerator returns PIDLs that are special hidden folders at the top level of the Shell folder, which are not otherwise enumerated.</span></span> <span data-ttu-id="f572e-124">La visualizzazione predefinita è quella visualizzata nella cartella della shell normalmente.</span><span class="sxs-lookup"><span data-stu-id="f572e-124">The default view is the one the Shell folder displays normally.</span></span>

<span data-ttu-id="f572e-125">Questa interfaccia non è definita in alcun file di intestazione pubblico.</span><span class="sxs-lookup"><span data-stu-id="f572e-125">This interface is not defined in any public header file.</span></span> <span data-ttu-id="f572e-126">Se si sceglie di implementare questa interfaccia, è possibile usare il codice C/C++ seguente per dichiararne i metodi.</span><span class="sxs-lookup"><span data-stu-id="f572e-126">Should you choose to implement this interface, you can use the following C/C++ code to declare its methods.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="f572e-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f572e-127">Requirements</span></span>



| <span data-ttu-id="f572e-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="f572e-128">Requirement</span></span> | <span data-ttu-id="f572e-129">Valore</span><span class="sxs-lookup"><span data-stu-id="f572e-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f572e-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f572e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="f572e-131">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f572e-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f572e-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f572e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="f572e-133">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f572e-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f572e-134">DLL</span><span class="sxs-lookup"><span data-stu-id="f572e-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f572e-135"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f572e-135"><dt>Shell32.dll</dt></span></span> </dl> |



 

 
