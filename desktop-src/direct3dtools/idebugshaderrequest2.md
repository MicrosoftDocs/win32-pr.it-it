---
description: 'Richiesta di avvio del debug di uno shader. Questa richiesta contiene due parti: generare una traccia ed eseguire il debug di una traccia.'
MS-HAID: vspixengine.IDebugShaderRequest2
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interfaccia IDebugShaderRequest2
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 80F95900-F2E6-4B5C-B902-573280956E94
api_name:
- IDebugShaderRequest2
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7b7c183cc04422d47b8d6599c67f2e7c1f5e58cd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124623"
---
# <a name="span-idvspixengineidebugshaderrequest2spanidebugshaderrequest2-interface"></a><span data-ttu-id="0094a-104"><span id="vspixengine.idebugshaderrequest2"></span>Interfaccia IDebugShaderRequest2</span><span class="sxs-lookup"><span data-stu-id="0094a-104"><span id="vspixengine.idebugshaderrequest2"></span>IDebugShaderRequest2 interface</span></span>

<span data-ttu-id="0094a-105">Richiesta di avvio del debug di uno shader.</span><span class="sxs-lookup"><span data-stu-id="0094a-105">Request to start debugging a shader.</span></span> <span data-ttu-id="0094a-106">Questa richiesta contiene due parti: generare una traccia ed eseguire il debug di una traccia.</span><span class="sxs-lookup"><span data-stu-id="0094a-106">This request contains two parts: generate a trace, and debug a trace.</span></span>

## <a name="members"></a><span data-ttu-id="0094a-107">Membri</span><span class="sxs-lookup"><span data-stu-id="0094a-107">Members</span></span>

<span data-ttu-id="0094a-108">L'interfaccia **IDebugShaderRequest2** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="0094a-108">The **IDebugShaderRequest2** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="0094a-109">**IDebugShaderRequest2** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="0094a-109">**IDebugShaderRequest2** also has these types of members:</span></span>

-   [<span data-ttu-id="0094a-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="0094a-110">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="0094a-111"><span id="methods"></span>Metodi</span><span class="sxs-lookup"><span data-stu-id="0094a-111"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="0094a-112">L'interfaccia **IDebugShaderRequest2** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="0094a-112">The **IDebugShaderRequest2** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="0094a-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="0094a-113">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="0094a-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0094a-114">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="0094a-115"><a href="/windows/desktop/direct3dtools/idebugshaderrequest2-begindebugshader-ipixerrorcallback-ptr-dword-byte-arr-dword-ptr"><strong>BeginDebugShader</strong></a></span><span class="sxs-lookup"><span data-stu-id="0094a-115"><a href="/windows/desktop/direct3dtools/idebugshaderrequest2-begindebugshader-ipixerrorcallback-ptr-dword-byte-arr-dword-ptr"><strong>BeginDebugShader</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="0094a-116">Richiede l'avvio del debug dell'elenco di istruzioni specificato.</span><span class="sxs-lookup"><span data-stu-id="0094a-116">Requests to start debugging the specified list of instructions.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="0094a-117"><a href="/windows/desktop/direct3dtools/idebugshaderrequest2-generateinstructions-ipixerrorcallback-ptr-debugshaderrequestinfo-ptr-pixelhistoryoperation-ptr-idebugshadercallback-ptr"><strong>GenerateInstructions</strong></a></span><span class="sxs-lookup"><span data-stu-id="0094a-117"><a href="/windows/desktop/direct3dtools/idebugshaderrequest2-generateinstructions-ipixerrorcallback-ptr-debugshaderrequestinfo-ptr-pixelhistoryoperation-ptr-idebugshadercallback-ptr"><strong>GenerateInstructions</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="0094a-118">Richiede la generazione di istruzioni di traccia dello shader in una richiesta di debug.</span><span class="sxs-lookup"><span data-stu-id="0094a-118">Requests to generate shader trace instructions in a debug request.</span></span> <span data-ttu-id="0094a-119">Il debug basato su traccia si verifica sulla CPU (Warp) invece che sulla GPU.</span><span class="sxs-lookup"><span data-stu-id="0094a-119">Trace-based debugging occurs on the CPU (warp) instead of the GPU.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="0094a-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0094a-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="0094a-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0094a-121">Header</span></span></p></td><td><span data-ttu-id="0094a-122">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="0094a-122">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
