---
description: Rappresenta un tablet collegato al computer.
ms.assetid: 31e11f7d-5610-4c49-9203-2dc322fbef95
title: Interfaccia ITablet
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 76fa7baea2713e5a2e5eaae562b6dac29e002fff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314916"
---
# <a name="itablet-interface"></a><span data-ttu-id="b9305-103">Interfaccia ITablet</span><span class="sxs-lookup"><span data-stu-id="b9305-103">ITablet interface</span></span>

<span data-ttu-id="b9305-104">Rappresenta un tablet collegato al computer.</span><span class="sxs-lookup"><span data-stu-id="b9305-104">Represents a tablet attached to the computer.</span></span>

## <a name="members"></a><span data-ttu-id="b9305-105">Membri</span><span class="sxs-lookup"><span data-stu-id="b9305-105">Members</span></span>

<span data-ttu-id="b9305-106">L'interfaccia **ITablet** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="b9305-106">The **ITablet** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="b9305-107">**ITablet** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b9305-107">**ITablet** also has these types of members:</span></span>

-   [<span data-ttu-id="b9305-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="b9305-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b9305-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="b9305-109">Methods</span></span>

<span data-ttu-id="b9305-110">L'interfaccia **ITablet** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="b9305-110">The **ITablet** interface has these methods.</span></span>



| <span data-ttu-id="b9305-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="b9305-111">Method</span></span>                                                                 | <span data-ttu-id="b9305-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b9305-112">Description</span></span>                                                                           |
|:-----------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [<span data-ttu-id="b9305-113">**CreateContext**</span><span class="sxs-lookup"><span data-stu-id="b9305-113">**CreateContext**</span></span>](itablet-createcontext.md)                         | <span data-ttu-id="b9305-114">Crea un oggetto di contesto che descrive il dispositivo Tablet specificato.</span><span class="sxs-lookup"><span data-stu-id="b9305-114">Creates a context object that describes the specified tablet device.</span></span><br/>       |
| <span data-ttu-id="b9305-115">[**GetCursor**](/previous-versions/windows/desktop/legacy/aa373535(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b9305-115">[**GetCursor**](/previous-versions/windows/desktop/legacy/aa373535(v=vs.85))</span></span>                                 | <span data-ttu-id="b9305-116">Recupera l'oggetto [**ITabletCursor**](itabletcursor.md) specificato.</span><span class="sxs-lookup"><span data-stu-id="b9305-116">Retrieves the specified [**ITabletCursor**](itabletcursor.md) object.</span></span><br/>     |
| [<span data-ttu-id="b9305-117">**GetCursorCount**</span><span class="sxs-lookup"><span data-stu-id="b9305-117">**GetCursorCount**</span></span>](itablet-getcursorcount.md)                       | <span data-ttu-id="b9305-118">Recupera il numero di oggetti cursori associati al tablet.</span><span class="sxs-lookup"><span data-stu-id="b9305-118">Retrieves the number of cursor objects associated with the tablet.</span></span><br/>         |
| [<span data-ttu-id="b9305-119">**GetDefaultContextSettings**</span><span class="sxs-lookup"><span data-stu-id="b9305-119">**GetDefaultContextSettings**</span></span>](itablet-getdefaultcontextsettings.md) | <span data-ttu-id="b9305-120">Recupera le impostazioni di contesto predefinite per il tablet.</span><span class="sxs-lookup"><span data-stu-id="b9305-120">Retrieves the default context settings for the tablet.</span></span><br/>                     |
| [<span data-ttu-id="b9305-121">**GetHardwareCaps**</span><span class="sxs-lookup"><span data-stu-id="b9305-121">**GetHardwareCaps**</span></span>](itablet-gethardwarecaps.md)                     | <span data-ttu-id="b9305-122">Recupera un valore che rappresenta le funzionalità dell'hardware del tablet.</span><span class="sxs-lookup"><span data-stu-id="b9305-122">Retrieves a value that represents the capabilities of the tablet hardware.</span></span><br/> |
| [<span data-ttu-id="b9305-123">**GetMaxInputRect**</span><span class="sxs-lookup"><span data-stu-id="b9305-123">**GetMaxInputRect**</span></span>](itablet-getmaxinputrect.md)                     | <span data-ttu-id="b9305-124">Recupera un rettangolo che rappresenta l'area di input massima della tavoletta.</span><span class="sxs-lookup"><span data-stu-id="b9305-124">Retrieves a rectangle that represents maximum input area of the tablet.</span></span><br/>    |
| [<span data-ttu-id="b9305-125">**GetName**</span><span class="sxs-lookup"><span data-stu-id="b9305-125">**GetName**</span></span>](itablet-getname.md)                                     | <span data-ttu-id="b9305-126">Recupera una stringa contenente il nome del dispositivo tablet.</span><span class="sxs-lookup"><span data-stu-id="b9305-126">Retrieves a string containing the name of the tablet device.</span></span><br/>               |
| [<span data-ttu-id="b9305-127">**GetPlugAndPlayId**</span><span class="sxs-lookup"><span data-stu-id="b9305-127">**GetPlugAndPlayId**</span></span>](itablet-getplugandplayid.md)                   | <span data-ttu-id="b9305-128">Recupera una stringa contenente l'ID Plug and Play per la tavoletta.</span><span class="sxs-lookup"><span data-stu-id="b9305-128">Retrieves a string containing the Plug and Play ID for the tablet device.</span></span><br/>  |
| <span data-ttu-id="b9305-129">[**GetPropertyMetrics**](/previous-versions/windows/desktop/legacy/aa367722(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b9305-129">[**GetPropertyMetrics**](/previous-versions/windows/desktop/legacy/aa367722(v=vs.85))</span></span>               | <span data-ttu-id="b9305-130">Recupera i dati di metrica per una proprietà specificata.</span><span class="sxs-lookup"><span data-stu-id="b9305-130">Retrieves the metrics data for a specified property.</span></span><br/>                       |



 

## <a name="remarks"></a><span data-ttu-id="b9305-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="b9305-131">Remarks</span></span>

<span data-ttu-id="b9305-132">Gli sviluppatori non devono utilizzare questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="b9305-132">Developers should not use this interface.</span></span>

<span data-ttu-id="b9305-133">Il codice seguente descrive il modo in cui viene definita l'interfaccia **ITablet** .</span><span class="sxs-lookup"><span data-stu-id="b9305-133">The following code describes how the **ITablet** interface is defined.</span></span>

``` syntax
[
    object,
   uuid(1CB2EFC3-ABC7-4172-8FCB-3BC9CB93E29F),
    pointer_default(unique)
]
interface ITablet : IUnknown
{
    HRESULT GetDefaultContextSettings(
        [out] TABLET_CONTEXT_SETTINGS **ppTCS);

    HRESULT CreateContext(
        [in] HWND hWnd,
        [in, unique] RECT *prcInput,
        [in] DWORD dwOptions,
        [in, unique] TABLET_CONTEXT_SETTINGS *pTCS,
        [in] CONTEXT_ENABLE_TYPE cet,
        [out] ITabletContext **ppCtx,
        [in, out, unique] TABLET_CONTEXT_ID *pTcid,
        [in, out, unique] PACKET_DESCRIPTION **ppPD,
        [in, unique] ITabletEventSink *pSink);

    HRESULT GetName(
        [out] LPWSTR *ppwszName);

    HRESULT GetMaxInputRect(
        [out] RECT *prcInput);

    HRESULT GetHardwareCaps(
        [out] DWORD *pdwCaps);

    HRESULT GetPropertyMetrics(
        [in] REFGUID rguid,
        [out] PROPERTY_METRICS *pPM);

    HRESULT GetPlugAndPlayId(
        [out] LPWSTR *ppwszPPId);

    HRESULT GetCursorCount(
        [out] ULONG *pcCurs);

    HRESULT GetCursor(
        [in] ULONG iCur,
        [out] ITabletCursor **ppCur);
};   
```

## <a name="requirements"></a><span data-ttu-id="b9305-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b9305-134">Requirements</span></span>



| <span data-ttu-id="b9305-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9305-135">Requirement</span></span> | <span data-ttu-id="b9305-136">Valore</span><span class="sxs-lookup"><span data-stu-id="b9305-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b9305-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b9305-137">Minimum supported client</span></span><br/> | <span data-ttu-id="b9305-138">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="b9305-138">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="b9305-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b9305-139">Minimum supported server</span></span><br/> | <span data-ttu-id="b9305-140">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="b9305-140">None supported</span></span><br/>                                                              |
| <span data-ttu-id="b9305-141">Libreria</span><span class="sxs-lookup"><span data-stu-id="b9305-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="b9305-142"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b9305-142"><dt>Wisptis.exe</dt></span></span> </dl> |



 

