---
description: Richiede l'avvio del debug dell'elenco di istruzioni specificato.
MS-HAID: vspixengine.IDebugShaderRequest2\_BeginDebugShader\_IPixErrorCallback\_ptr\_DWORD\_BYTE\_arr\_DWORD\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IDebugShaderRequest2:: BeginDebugShader'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: B454D673-C14F-4A8F-9DA7-2C47510BE5DA
api_name:
- IDebugShaderRequest2.BeginDebugShader
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 39f6749a233140b745097bc1270963e50d0f11fb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124629"
---
# <a name="span-idvspixengineidebugshaderrequest2_begindebugshader_ipixerrorcallback_ptr_dword_byte_arr_dword_ptrspanidebugshaderrequest2begindebugshader-method"></a><span data-ttu-id="a0f01-103"><span id="vspixengine.idebugshaderrequest2_begindebugshader_ipixerrorcallback_ptr_dword_byte_arr_dword_ptr"></span>Metodo IDebugShaderRequest2:: BeginDebugShader</span><span class="sxs-lookup"><span data-stu-id="a0f01-103"><span id="vspixengine.idebugshaderrequest2_begindebugshader_ipixerrorcallback_ptr_dword_byte_arr_dword_ptr"></span>IDebugShaderRequest2::BeginDebugShader method</span></span>

<span data-ttu-id="a0f01-104">Richiede l'avvio del debug dell'elenco di istruzioni specificato.</span><span class="sxs-lookup"><span data-stu-id="a0f01-104">Requests to start debugging the specified list of instructions.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0f01-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a0f01-105">Syntax</span></span>


```C++
HRESULT BeginDebugShader(
   IPixErrorCallback * errorCallback,
   DWORD               instructionStreamSize,
   BYTE []             count1_instructionStream,
   DWORD *             pDevice
);
```

## <a name="parameters"></a><span data-ttu-id="a0f01-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a0f01-106">Parameters</span></span>

<span data-ttu-id="a0f01-107">*errorCallback* </span><span class="sxs-lookup"><span data-stu-id="a0f01-107">*errorCallback* </span></span>  
<span data-ttu-id="a0f01-108">Indirizzo di un callback per gli errori che potrebbero verificarsi durante il debug.</span><span class="sxs-lookup"><span data-stu-id="a0f01-108">The address of a callback for errors that might occur during debugging.</span></span>

<span data-ttu-id="a0f01-109">*instructionStreamSize* </span><span class="sxs-lookup"><span data-stu-id="a0f01-109">*instructionStreamSize* </span></span>  
<span data-ttu-id="a0f01-110">Il numero di istruzioni nel flusso di istruzioni.</span><span class="sxs-lookup"><span data-stu-id="a0f01-110">The number of instructions in the instruction stream.</span></span>

<span data-ttu-id="a0f01-111">*\_instructionStream count1* </span><span class="sxs-lookup"><span data-stu-id="a0f01-111">*count1\_instructionStream* </span></span>  
<span data-ttu-id="a0f01-112">Flusso di istruzioni specificato.</span><span class="sxs-lookup"><span data-stu-id="a0f01-112">The specified instruction stream.</span></span>

<span data-ttu-id="a0f01-113">*pDevice* </span><span class="sxs-lookup"><span data-stu-id="a0f01-113">*pDevice* </span></span>  
<span data-ttu-id="a0f01-114">Indirizzo da passare al motore di debug per la comunicazione con questa sessione di debug (motore di debug ReadProcessMemory su questo indirizzo).</span><span class="sxs-lookup"><span data-stu-id="a0f01-114">The address to pass to the debug engine for communicating with this debug session (debug engine readprocessmemory on this address).</span></span>

## <a name="return-value"></a><span data-ttu-id="a0f01-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a0f01-115">Return value</span></span>

<span data-ttu-id="a0f01-116">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="a0f01-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a0f01-117">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a0f01-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0f01-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a0f01-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="a0f01-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a0f01-119">Header</span></span></p></td><td><span data-ttu-id="a0f01-120">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="a0f01-120">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="a0f01-121"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="a0f01-121"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="a0f01-122">**IDebugShaderRequest2**</span><span class="sxs-lookup"><span data-stu-id="a0f01-122">**IDebugShaderRequest2**</span></span>](/windows/desktop/direct3dtools/idebugshaderrequest2)

 

 
