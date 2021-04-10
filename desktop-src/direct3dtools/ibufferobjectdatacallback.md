---
description: Callback per restituire il contenuto di un oggetto in formato buffer per quelli che lo supportano (buffer, trame).
MS-HAID: vspixengine.IBufferObjectDataCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interfaccia IBufferObjectDataCallback
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: AAE4CE9A-B8EB-4ED6-9F48-D00C19B27A2E
api_name:
- IBufferObjectDataCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6e5fb7deebd7d1b16d333ae59edab9372b54ad8c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124167"
---
# <a name="span-idvspixengineibufferobjectdatacallbackspanibufferobjectdatacallback-interface"></a><span data-ttu-id="23c73-103"><span id="vspixengine.ibufferobjectdatacallback"></span>Interfaccia IBufferObjectDataCallback</span><span class="sxs-lookup"><span data-stu-id="23c73-103"><span id="vspixengine.ibufferobjectdatacallback"></span>IBufferObjectDataCallback interface</span></span>

<span data-ttu-id="23c73-104">Callback per restituire il contenuto di un oggetto in formato buffer per quelli che lo supportano (buffer, trame).</span><span class="sxs-lookup"><span data-stu-id="23c73-104">Callback to return the contents of an object in buffer form for those that support it (buffers, textures).</span></span>

## <a name="members"></a><span data-ttu-id="23c73-105">Membri</span><span class="sxs-lookup"><span data-stu-id="23c73-105">Members</span></span>

<span data-ttu-id="23c73-106">L'interfaccia **IBufferObjectDataCallback** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="23c73-106">The **IBufferObjectDataCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="23c73-107">**IBufferObjectDataCallback** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="23c73-107">**IBufferObjectDataCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="23c73-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="23c73-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="23c73-109"><span id="methods"></span>Metodi</span><span class="sxs-lookup"><span data-stu-id="23c73-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="23c73-110">L'interfaccia **IBufferObjectDataCallback** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="23c73-110">The **IBufferObjectDataCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="23c73-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="23c73-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="23c73-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="23c73-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="23c73-113"><a href="/windows/desktop/direct3dtools/ibufferobjectdatacallback-resultcallback-bstr"><strong>ResultCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="23c73-113"><a href="/windows/desktop/direct3dtools/ibufferobjectdatacallback-resultcallback-bstr"><strong>ResultCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="23c73-114">Callback che notifica all'host le informazioni del buffer scritte in un file dalla richiesta associata.</span><span class="sxs-lookup"><span data-stu-id="23c73-114">A callback that notifies the host of buffer information written to a file by the assocaited request.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="23c73-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="23c73-115">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="23c73-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="23c73-116">Header</span></span></p></td><td><span data-ttu-id="23c73-117">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="23c73-117">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
