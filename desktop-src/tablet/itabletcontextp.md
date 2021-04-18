---
description: Rappresenta il contesto della tavoletta.
ms.assetid: d518c42d-c2f6-4776-bea5-fecdfe48e260
title: Interfaccia ITabletContextP
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletContextP
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 5b3b6a69deeaa30c3fa0e16b1b36094dceaff304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319166"
---
# <a name="itabletcontextp-interface"></a><span data-ttu-id="6700e-103">Interfaccia ITabletContextP</span><span class="sxs-lookup"><span data-stu-id="6700e-103">ITabletContextP interface</span></span>

<span data-ttu-id="6700e-104">Rappresenta il contesto della tavoletta.</span><span class="sxs-lookup"><span data-stu-id="6700e-104">Represents the tablet context.</span></span>

## <a name="members"></a><span data-ttu-id="6700e-105">Membri</span><span class="sxs-lookup"><span data-stu-id="6700e-105">Members</span></span>

<span data-ttu-id="6700e-106">L'interfaccia **ITabletContextP** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="6700e-106">The **ITabletContextP** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="6700e-107">**ITabletContextP** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="6700e-107">**ITabletContextP** also has these types of members:</span></span>

-   [<span data-ttu-id="6700e-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="6700e-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6700e-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="6700e-109">Methods</span></span>

<span data-ttu-id="6700e-110">L'interfaccia **ITabletContextP** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="6700e-110">The **ITabletContextP** interface has these methods.</span></span>



| <span data-ttu-id="6700e-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="6700e-111">Method</span></span>                                                                                           | <span data-ttu-id="6700e-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6700e-112">Description</span></span>                                                                     |
|:-------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------|
| [<span data-ttu-id="6700e-113">**IsTopMostHook**</span><span class="sxs-lookup"><span data-stu-id="6700e-113">**IsTopMostHook**</span></span>](itabletcontextp-istopmosthook.md)                                           | <span data-ttu-id="6700e-114">Indica se il contesto del tablet è nell'hook superiore.</span><span class="sxs-lookup"><span data-stu-id="6700e-114">Indicates if the tablet context is in the top most hook.</span></span><br/>             |
| [<span data-ttu-id="6700e-115">**Overlap**</span><span class="sxs-lookup"><span data-stu-id="6700e-115">**Overlap**</span></span>](itabletcontextp-overlap.md)                                                       | <span data-ttu-id="6700e-116">Sposta un contesto del tablet nella parte anteriore o posteriore della coda di input.</span><span class="sxs-lookup"><span data-stu-id="6700e-116">Moves a tablet context to the front or back of the input queue.</span></span><br/>      |
| [<span data-ttu-id="6700e-117">**TrackInputRect**</span><span class="sxs-lookup"><span data-stu-id="6700e-117">**TrackInputRect**</span></span>](itabletcontextp-trackinputrect.md)                                         | <span data-ttu-id="6700e-118">Aggiorna il digitalizzatore del Tablet alle coordinate del mapping della posizione della finestra.</span><span class="sxs-lookup"><span data-stu-id="6700e-118">Updates the tablet digitizer to window location mapping coordinates.</span></span><br/> |
| [<span data-ttu-id="6700e-119">**UseNamedSharedMemoryCommunications**</span><span class="sxs-lookup"><span data-stu-id="6700e-119">**UseNamedSharedMemoryCommunications**</span></span>](itabletcontextp-usenamedsharedmemorycommunications.md) | <span data-ttu-id="6700e-120">Consente di accedere alla memoria condivisa tra i thread del tablet.</span><span class="sxs-lookup"><span data-stu-id="6700e-120">Provides access to memory shared between tablet threads.</span></span><br/>             |
| [<span data-ttu-id="6700e-121">**UseSharedMemoryCommunications**</span><span class="sxs-lookup"><span data-stu-id="6700e-121">**UseSharedMemoryCommunications**</span></span>](itabletcontextp-usesharedmemorycommunications.md)           | <span data-ttu-id="6700e-122">Consente di accedere alla memoria condivisa tra i thread del tablet.</span><span class="sxs-lookup"><span data-stu-id="6700e-122">Provides access to memory shared between tablet threads.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="6700e-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="6700e-123">Remarks</span></span>

<span data-ttu-id="6700e-124">Gli sviluppatori non devono utilizzare questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="6700e-124">Developers should not use this interface.</span></span>

<span data-ttu-id="6700e-125">[**UseNamedSharedMemoryCommunications**](itabletcontextp-usenamedsharedmemorycommunications.md) è disponibile solo in Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="6700e-125">[**UseNamedSharedMemoryCommunications**](itabletcontextp-usenamedsharedmemorycommunications.md) is only available on Windows Vista and later.</span></span>

<span data-ttu-id="6700e-126">Il codice seguente descrive il modo in cui viene definita l'interfaccia **ITabletContextP** .</span><span class="sxs-lookup"><span data-stu-id="6700e-126">The following code describes how the **ITabletContextP** interface is defined.</span></span>

``` syntax
[
    object,
    uuid(22F74D0A-694F-4f47-A5CE-AE08A6409AC8),
    pointer_default(unique)
]
interface ITabletContextP : ITabletContext
{

    HRESULT Overlap([in] BOOL bTop, [out] DWORD *pdwtcid);

    HRESULT GetType([out] CONTEXT_TYPE *pct);

    HRESULT TrackInputRect([out] RECT *prcInput);

    HRESULT IsTopMostHook();

    HRESULT GetEventSink(
        [out] ITabletEventSink **ppSink);

    HRESULT UseSharedMemoryCommunications(
        [in]  DWORD pid,
        [out] DWORD *phEventMoreData,
        [out] DWORD *phEventClientReady,
        [out] DWORD *phMutexAccess,
        [out] DWORD *phFileMapping);

    HRESULT UseNamedSharedMemoryCommunications(
        [in] DWORD pid,
        [in, string] LPCTSTR szSid,
        [in, string] LPCTSTR sdIlSid,
        [out] DWORD *pdwEventMoreDataId,
        [out] DWORD *pdwEventClientReadyId,
        [out] DWORD *pdwMutexAccessId,
        [out] DWORD *pdwFileMappingId);
};
```

## <a name="requirements"></a><span data-ttu-id="6700e-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6700e-127">Requirements</span></span>



| <span data-ttu-id="6700e-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="6700e-128">Requirement</span></span> | <span data-ttu-id="6700e-129">Valore</span><span class="sxs-lookup"><span data-stu-id="6700e-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6700e-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6700e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="6700e-131">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="6700e-131">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="6700e-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6700e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="6700e-133">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="6700e-133">None supported</span></span><br/>                                                              |
| <span data-ttu-id="6700e-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="6700e-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="6700e-135"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6700e-135"><dt>Wisptis.exe</dt></span></span> </dl> |



 

