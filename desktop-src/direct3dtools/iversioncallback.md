---
description: Callback per restituire le versioni di tutte le interfacce supportate. Ciò consente al consumer di non essere sincronizzato con il motore di acquisizione.
MS-HAID: vspixengine.IVersionCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interfaccia IVersionCallback
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 7135E175-C537-4B0C-8F0A-CB77E3F2D945
api_name:
- IVersionCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5c53008e625d63e2e876bef9ab8cbdd376508c2f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304047"
---
# <a name="span-idvspixengineiversioncallbackspaniversioncallback-interface"></a><span data-ttu-id="e049e-104"><span id="vspixengine.iversioncallback"></span>Interfaccia IVersionCallback</span><span class="sxs-lookup"><span data-stu-id="e049e-104"><span id="vspixengine.iversioncallback"></span>IVersionCallback interface</span></span>

<span data-ttu-id="e049e-105">Callback per restituire le versioni di tutte le interfacce supportate.</span><span class="sxs-lookup"><span data-stu-id="e049e-105">Callback to return the versions of all the interfaces supported.</span></span> <span data-ttu-id="e049e-106">Ciò consente al consumer di non essere sincronizzato con il motore di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="e049e-106">This allows the consumer to be out of sync with the capture engine.</span></span>

## <a name="members"></a><span data-ttu-id="e049e-107">Membri</span><span class="sxs-lookup"><span data-stu-id="e049e-107">Members</span></span>

<span data-ttu-id="e049e-108">L'interfaccia **IVersionCallback** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="e049e-108">The **IVersionCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="e049e-109">**IVersionCallback** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e049e-109">**IVersionCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="e049e-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="e049e-110">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="e049e-111"><span id="methods"></span>Metodi</span><span class="sxs-lookup"><span data-stu-id="e049e-111"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="e049e-112">L'interfaccia **IVersionCallback** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="e049e-112">The **IVersionCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="e049e-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="e049e-113">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="e049e-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e049e-114">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="e049e-115"><a href="/windows/desktop/direct3dtools/iversioncallback-versiontableready-guid-arr-uint"><strong>VersionTableReady</strong></a></span><span class="sxs-lookup"><span data-stu-id="e049e-115"><a href="/windows/desktop/direct3dtools/iversioncallback-versiontableready-guid-arr-uint"><strong>VersionTableReady</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="e049e-116">Funzione di callback utilizzata per notificare all'host le interfacce supportate.</span><span class="sxs-lookup"><span data-stu-id="e049e-116">A callback function used to notify the host of which interfaces are supported.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="e049e-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e049e-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="e049e-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e049e-118">Header</span></span></p></td><td><span data-ttu-id="e049e-119">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="e049e-119">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
