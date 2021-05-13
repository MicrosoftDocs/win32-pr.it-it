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
ms.openlocfilehash: cf1a3b03eed2a15e82e1313875a4ab8584243190
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842782"
---
# <a name="ishellfoldersearchablecallback-interface"></a><span data-ttu-id="4cf96-103">Interfaccia IShellFolderSearchableCallback</span><span class="sxs-lookup"><span data-stu-id="4cf96-103">IShellFolderSearchableCallback interface</span></span>

<span data-ttu-id="4cf96-104">Espone routine di callback per monitorare il processo di ricerca.</span><span class="sxs-lookup"><span data-stu-id="4cf96-104">Exposes callback routines to monitor the search process.</span></span>

## <a name="members"></a><span data-ttu-id="4cf96-105">Membri</span><span class="sxs-lookup"><span data-stu-id="4cf96-105">Members</span></span>

<span data-ttu-id="4cf96-106">**L'interfaccia IShellFolderSearchableCallback** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown)</span><span class="sxs-lookup"><span data-stu-id="4cf96-106">The **IShellFolderSearchableCallback** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="4cf96-107">**IShellFolderSearchableCallback** include anche questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="4cf96-107">**IShellFolderSearchableCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="4cf96-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="4cf96-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4cf96-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="4cf96-109">Methods</span></span>

<span data-ttu-id="4cf96-110">**L'interfaccia IShellFolderSearchableCallback** include questi metodi.</span><span class="sxs-lookup"><span data-stu-id="4cf96-110">The **IShellFolderSearchableCallback** interface has these methods.</span></span>



| <span data-ttu-id="4cf96-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="4cf96-111">Method</span></span>                                                      | <span data-ttu-id="4cf96-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4cf96-112">Description</span></span>                                      |
|:------------------------------------------------------------|:-------------------------------------------------|
| [<span data-ttu-id="4cf96-113">**RunBegin**</span><span class="sxs-lookup"><span data-stu-id="4cf96-113">**RunBegin**</span></span>](ishellfoldersearchablecallback-runbegin.md) | <span data-ttu-id="4cf96-114">Indica che è stata avviata una ricerca.</span><span class="sxs-lookup"><span data-stu-id="4cf96-114">Indicates that a search was started.</span></span><br/>  |
| [<span data-ttu-id="4cf96-115">**RunEnd**</span><span class="sxs-lookup"><span data-stu-id="4cf96-115">**RunEnd**</span></span>](ishellfoldersearchablecallback-runend.md)     | <span data-ttu-id="4cf96-116">Indica che una ricerca è stata completata.</span><span class="sxs-lookup"><span data-stu-id="4cf96-116">Indicates that a search has finished.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4cf96-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="4cf96-117">Remarks</span></span>

<span data-ttu-id="4cf96-118">Questa interfaccia non è definita in alcun file di intestazione pubblico.</span><span class="sxs-lookup"><span data-stu-id="4cf96-118">This interface is not defined in any public header files.</span></span> <span data-ttu-id="4cf96-119">Se si sceglie di implementare questa interfaccia, è possibile usare il codice C/C++ seguente per dichiararne i metodi.</span><span class="sxs-lookup"><span data-stu-id="4cf96-119">Should you choose to implement this interface, you can use the following C/C++ code to declare its methods.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="4cf96-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4cf96-120">Requirements</span></span>



| <span data-ttu-id="4cf96-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="4cf96-121">Requirement</span></span> | <span data-ttu-id="4cf96-122">Valore</span><span class="sxs-lookup"><span data-stu-id="4cf96-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4cf96-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4cf96-123">Minimum supported client</span></span><br/> | <span data-ttu-id="4cf96-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4cf96-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="4cf96-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4cf96-125">Minimum supported server</span></span><br/> | <span data-ttu-id="4cf96-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4cf96-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="4cf96-127">DLL</span><span class="sxs-lookup"><span data-stu-id="4cf96-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4cf96-128"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4cf96-128"><dt>Shell32.dll</dt></span></span> </dl> |



 

 
