---
description: Espone metodi che consentono a un'estensione della shell di fornire uno spazio dei nomi in cui è possibile eseguire ricerche.
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
ms.openlocfilehash: 1f42b3af012361bfd24c93e03c38e6954eb5326e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977943"
---
# <a name="ishellfoldersearchable-interface"></a><span data-ttu-id="d305b-103">Interfaccia IShellFolderSearchable</span><span class="sxs-lookup"><span data-stu-id="d305b-103">IShellFolderSearchable interface</span></span>

<span data-ttu-id="d305b-104">Espone metodi che consentono a un'estensione della shell di fornire uno spazio dei nomi in cui è possibile eseguire ricerche.</span><span class="sxs-lookup"><span data-stu-id="d305b-104">Exposes methods that allow a Shell extension to provide a searchable namespace.</span></span>

## <a name="members"></a><span data-ttu-id="d305b-105">Membri</span><span class="sxs-lookup"><span data-stu-id="d305b-105">Members</span></span>

<span data-ttu-id="d305b-106">L'interfaccia **IShellFolderSearchable** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="d305b-106">The **IShellFolderSearchable** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="d305b-107">**IShellFolderSearchable** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="d305b-107">**IShellFolderSearchable** also has these types of members:</span></span>

-   [<span data-ttu-id="d305b-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="d305b-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d305b-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="d305b-109">Methods</span></span>

<span data-ttu-id="d305b-110">L'interfaccia **IShellFolderSearchable** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="d305b-110">The **IShellFolderSearchable** interface has these methods.</span></span>



| <span data-ttu-id="d305b-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="d305b-111">Method</span></span>                                                                | <span data-ttu-id="d305b-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d305b-112">Description</span></span>                                                               |
|:----------------------------------------------------------------------|:--------------------------------------------------------------------------|
| [<span data-ttu-id="d305b-113">**CancelAsyncSearch**</span><span class="sxs-lookup"><span data-stu-id="d305b-113">**CancelAsyncSearch**</span></span>](ishellfoldersearchable-cancelasyncsearch.md) | <span data-ttu-id="d305b-114">Inizia il processo di annullamento di una ricerca asincrona in sospeso.</span><span class="sxs-lookup"><span data-stu-id="d305b-114">Begins the process of canceling a pending asynchronous search.</span></span><br/> |
| [<span data-ttu-id="d305b-115">**FindString**</span><span class="sxs-lookup"><span data-stu-id="d305b-115">**FindString**</span></span>](ishellfoldersearchable-findstring.md)               | <span data-ttu-id="d305b-116">Inizia una ricerca di una stringa di ricerca specificata.</span><span class="sxs-lookup"><span data-stu-id="d305b-116">Begins a search for a specified search string.</span></span><br/>                 |
| [<span data-ttu-id="d305b-117">**InvalidateSearch**</span><span class="sxs-lookup"><span data-stu-id="d305b-117">**InvalidateSearch**</span></span>](ishellfoldersearchable-invalidatesearch.md)   | <span data-ttu-id="d305b-118">Rende PIDL una parte non valida della cartella della shell.</span><span class="sxs-lookup"><span data-stu-id="d305b-118">Makes this PIDL an invalid portion of the Shell folder.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="d305b-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="d305b-119">Remarks</span></span>

<span data-ttu-id="d305b-120">Questa interfaccia non è definita in alcun file di intestazione pubblica.</span><span class="sxs-lookup"><span data-stu-id="d305b-120">This interface is not defined in any public header files.</span></span> <span data-ttu-id="d305b-121">Se si sceglie di implementare questa interfaccia, è possibile usare il codice C/C++ seguente per dichiararne i metodi.</span><span class="sxs-lookup"><span data-stu-id="d305b-121">Should you choose to implement this interface, you can use the following C/C++ code to declare its methods.</span></span>


```
#undef  INTERFACE
#define INTERFACE IShellFolderSearchable
DECLARE_INTERFACE_IID_(IShellFolderSearchable, IUnknown, "4E1AE66C-204B-11d2-8DB3-0000F87A556C")
{
    // **_ IUnknown methods _*_
    STDMETHOD(QueryInterface) (THIS_ REFIID riid, __out void _*ppv) PURE;
    STDMETHOD_(ULONG,AddRef)  (THIS) PURE;
    STDMETHOD_(ULONG,Release) (THIS) PURE;

    // **_ IShellFolderSearchable methods _*_

    // FindString -
    //  The returned Shell folder's enumerator will have any
    //   search hits for the given search string.
    //  punkOnAsyncSearch will be QI'd for IShellFolderSearchableCallback
    STDMETHOD(FindString)(THIS_ LPCWSTR pwszTarget, __inout_opt DWORD _pdwFlags,
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



## <a name="requirements"></a><span data-ttu-id="d305b-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d305b-122">Requirements</span></span>



| <span data-ttu-id="d305b-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="d305b-123">Requirement</span></span> | <span data-ttu-id="d305b-124">Valore</span><span class="sxs-lookup"><span data-stu-id="d305b-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d305b-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d305b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d305b-126">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d305b-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d305b-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d305b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d305b-128">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d305b-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d305b-129">DLL</span><span class="sxs-lookup"><span data-stu-id="d305b-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d305b-130"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d305b-130"><dt>Shell32.dll</dt></span></span> </dl> |



 

 
