---
description: Richiesta di scrittura di una trama affiancata come file DDS.
MS-HAID: vspixengine.ITileRequest
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interfaccia ITileRequest
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: DBA493E7-EBB6-490D-BDC6-946265A474D6
api_name:
- ITileRequest
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: ceb630661cfe67bc8beb28b2d1de2480726ec594
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746802"
---
# <a name="span-idvspixengineitilerequestspanitilerequest-interface"></a><span data-ttu-id="1a8e6-103"><span id="vspixengine.itilerequest"></span>Interfaccia ITileRequest</span><span class="sxs-lookup"><span data-stu-id="1a8e6-103"><span id="vspixengine.itilerequest"></span>ITileRequest interface</span></span>

<span data-ttu-id="1a8e6-104">Richiesta di scrittura di una trama affiancata come file DDS.</span><span class="sxs-lookup"><span data-stu-id="1a8e6-104">Request for a tiled texture to be written as a DDS file.</span></span>

## <a name="members"></a><span data-ttu-id="1a8e6-105">Membri</span><span class="sxs-lookup"><span data-stu-id="1a8e6-105">Members</span></span>

<span data-ttu-id="1a8e6-106">L'interfaccia **ITileRequest** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="1a8e6-106">The **ITileRequest** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="1a8e6-107">**ITileRequest** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="1a8e6-107">**ITileRequest** also has these types of members:</span></span>

-   [<span data-ttu-id="1a8e6-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="1a8e6-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="1a8e6-109"><span id="methods"></span>Metodi</span><span class="sxs-lookup"><span data-stu-id="1a8e6-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="1a8e6-110">L'interfaccia **ITileRequest** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="1a8e6-110">The **ITileRequest** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="1a8e6-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="1a8e6-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="1a8e6-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1a8e6-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="1a8e6-113"><a href="/windows/desktop/direct3dtools/itilerequest-requestbuffertileasync-eventid-dword-bstr-uint-ibufferobjectdatacallback-ptr-dword-dword"><strong>RequestBufferTileAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a8e6-113"><a href="/windows/desktop/direct3dtools/itilerequest-requestbuffertileasync-eventid-dword-bstr-uint-ibufferobjectdatacallback-ptr-dword-dword"><strong>RequestBufferTileAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="1a8e6-114">Richiede di ottenere il contenuto non elaborato di un riquadro.</span><span class="sxs-lookup"><span data-stu-id="1a8e6-114">Requests to get the raw contents of a tile.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="1a8e6-115"><a href="/windows/desktop/direct3dtools/itilerequest-requesttexturetileasync-eventid-dword-uint-uint-uint-uint-bstr-itexturecallback-ptr-dword-dword"><strong>RequestTextureTileAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a8e6-115"><a href="/windows/desktop/direct3dtools/itilerequest-requesttexturetileasync-eventid-dword-uint-uint-uint-uint-bstr-itexturecallback-ptr-dword-dword"><strong>RequestTextureTileAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="1a8e6-116">Richiede di ottenere il contenuto di una trama affiancata come. File DDS (superficie DirectDraw).</span><span class="sxs-lookup"><span data-stu-id="1a8e6-116">Requests to get the contents of a tiled texture as a .DDS (DirectDraw Surface) file.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="1a8e6-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1a8e6-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="1a8e6-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1a8e6-118">Header</span></span></p></td><td><span data-ttu-id="1a8e6-119">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="1a8e6-119">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
