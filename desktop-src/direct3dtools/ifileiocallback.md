---
description: Callback per salvare o terminare l'esperimento. Indica che il salvataggio del file è stato eseguito.
MS-HAID: vspixengine.IFileIOCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interfaccia IFileIOCallback
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F9C5E117-310C-4769-B78D-9A779A52EAE7
api_name:
- IFileIOCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: cccb7895a862b91250101fe2dd9e4b4ca43b0650
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104225415"
---
# <a name="span-idvspixengineifileiocallbackspanifileiocallback-interface"></a><span data-ttu-id="38b5c-104"><span id="vspixengine.ifileiocallback"></span>Interfaccia IFileIOCallback</span><span class="sxs-lookup"><span data-stu-id="38b5c-104"><span id="vspixengine.ifileiocallback"></span>IFileIOCallback interface</span></span>

<span data-ttu-id="38b5c-105">Callback per salvare o terminare l'esperimento.</span><span class="sxs-lookup"><span data-stu-id="38b5c-105">Callback to save or end the experiment.</span></span> <span data-ttu-id="38b5c-106">Indica che il salvataggio del file è stato eseguito.</span><span class="sxs-lookup"><span data-stu-id="38b5c-106">Indicates file save is done.</span></span>

## <a name="members"></a><span data-ttu-id="38b5c-107">Membri</span><span class="sxs-lookup"><span data-stu-id="38b5c-107">Members</span></span>

<span data-ttu-id="38b5c-108">L'interfaccia **IFileIOCallback** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="38b5c-108">The **IFileIOCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="38b5c-109">**IFileIOCallback** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="38b5c-109">**IFileIOCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="38b5c-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="38b5c-110">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="38b5c-111"><span id="methods"></span>Metodi</span><span class="sxs-lookup"><span data-stu-id="38b5c-111"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="38b5c-112">L'interfaccia **IFileIOCallback** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="38b5c-112">The **IFileIOCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="38b5c-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="38b5c-113">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="38b5c-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="38b5c-114">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="38b5c-115"><a href="/windows/desktop/direct3dtools/ifileiocallback-resultcallback-dword"><strong>ResultCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="38b5c-115"><a href="/windows/desktop/direct3dtools/ifileiocallback-resultcallback-dword"><strong>ResultCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="38b5c-116">Funzione di callback utilizzata per notificare l'host degli errori durante l'acquisizione o la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="38b5c-116">A callback function used to notify the host of errors while during capture or playback.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="38b5c-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="38b5c-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="38b5c-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="38b5c-118">Header</span></span></p></td><td><span data-ttu-id="38b5c-119">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="38b5c-119">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
