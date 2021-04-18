---
description: Esegue un'operazione di decodifica DXVA (DirectX Video Acceleration).
ms.assetid: cb87a087-ca53-470e-ab46-f4022cfd7869
title: 'Metodo IDirect3DDXVADevice9:: Execute (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DDXVADevice9.Execute
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: d624146c32b5f7eaeb4e680cf03878e8d065ee5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310838"
---
# <a name="idirect3ddxvadevice9execute-method"></a><span data-ttu-id="fa630-103">Metodo IDirect3DDXVADevice9:: Execute</span><span class="sxs-lookup"><span data-stu-id="fa630-103">IDirect3DDXVADevice9::Execute method</span></span>

<span data-ttu-id="fa630-104">Esegue un'operazione di decodifica DXVA (DirectX Video Acceleration).</span><span class="sxs-lookup"><span data-stu-id="fa630-104">Performs a DirectX Video Acceleration (DXVA) decoding operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa630-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fa630-105">Syntax</span></span>


```C++
HRESULT Execute(
   DWORD          FunctionNum,
   VOID           *pInputData,
   DWORD          InputSize,
   VOID           *OutputData,
   DWORD          OutputSize,
   DWORD          NumBuffers,
   DXVABufferInfo *pBufferInfo
);
```



## <a name="parameters"></a><span data-ttu-id="fa630-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="fa630-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa630-107">*FunctionNum*</span><span class="sxs-lookup"><span data-stu-id="fa630-107">*FunctionNum*</span></span> 
</dt> <dd>

<span data-ttu-id="fa630-108">**Valore DWORD** che contiene uno o più numeri di funzione DXVA.</span><span class="sxs-lookup"><span data-stu-id="fa630-108">A **DWORD** that contains one or more DXVA function numbers.</span></span> <span data-ttu-id="fa630-109">Per informazioni dettagliate, vedere la [specifica DXVA 1,0](/windows-hardware/drivers/display/directx-video-acceleration).</span><span class="sxs-lookup"><span data-stu-id="fa630-109">For details, refer to the [DXVA 1.0 specification](/windows-hardware/drivers/display/directx-video-acceleration).</span></span>

</dd> <dt>

<span data-ttu-id="fa630-110">*pInputData*</span><span class="sxs-lookup"><span data-stu-id="fa630-110">*pInputData*</span></span> 
</dt> <dd>

<span data-ttu-id="fa630-111">Puntatore a un buffer che contiene i dati di input per l'operazione di decodifica.</span><span class="sxs-lookup"><span data-stu-id="fa630-111">A pointer to a buffer that contains input data for the decoding operation.</span></span> <span data-ttu-id="fa630-112">Il significato di questi dati dipende dal tipo di superficie e dal numero di funzione.</span><span class="sxs-lookup"><span data-stu-id="fa630-112">The meaning of this data depends on the surface type and function number.</span></span>

</dd> <dt>

<span data-ttu-id="fa630-113">*InputSize*</span><span class="sxs-lookup"><span data-stu-id="fa630-113">*InputSize*</span></span> 
</dt> <dd>

<span data-ttu-id="fa630-114">Dimensioni in byte dei dati di input.</span><span class="sxs-lookup"><span data-stu-id="fa630-114">The size of the input data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="fa630-115">*OutputData*</span><span class="sxs-lookup"><span data-stu-id="fa630-115">*OutputData*</span></span> 
</dt> <dd>

<span data-ttu-id="fa630-116">Puntatore a un buffer in cui l'acceleratore video scrive i dati di output.</span><span class="sxs-lookup"><span data-stu-id="fa630-116">Pointer to a buffer where the video accelerator writes output data.</span></span>

</dd> <dt>

<span data-ttu-id="fa630-117">*OutputSize*</span><span class="sxs-lookup"><span data-stu-id="fa630-117">*OutputSize*</span></span> 
</dt> <dd>

<span data-ttu-id="fa630-118">Dimensioni in byte del buffer *outputData* .</span><span class="sxs-lookup"><span data-stu-id="fa630-118">The size of the *OutputData* buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="fa630-119">*NumBuffers*</span><span class="sxs-lookup"><span data-stu-id="fa630-119">*NumBuffers*</span></span> 
</dt> <dd>

<span data-ttu-id="fa630-120">Numero di elementi nella matrice *pBufferInfo* .</span><span class="sxs-lookup"><span data-stu-id="fa630-120">The number of elements in the *pBufferInfo* array.</span></span>

</dd> <dt>

<span data-ttu-id="fa630-121">*pBufferInfo*</span><span class="sxs-lookup"><span data-stu-id="fa630-121">*pBufferInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="fa630-122">Puntatore a una matrice di strutture [**DXVABufferInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvabufferinfo) .</span><span class="sxs-lookup"><span data-stu-id="fa630-122">A pointer to an array of [**DXVABufferInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvabufferinfo) structures.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa630-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fa630-123">Return value</span></span>

<span data-ttu-id="fa630-124">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="fa630-124">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fa630-125">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fa630-125">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa630-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fa630-126">Requirements</span></span>



| <span data-ttu-id="fa630-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa630-127">Requirement</span></span> | <span data-ttu-id="fa630-128">Valore</span><span class="sxs-lookup"><span data-stu-id="fa630-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="fa630-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fa630-129">Minimum supported client</span></span><br/> | <span data-ttu-id="fa630-130">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fa630-130">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fa630-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fa630-131">Minimum supported server</span></span><br/> | <span data-ttu-id="fa630-132">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fa630-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="fa630-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fa630-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa630-134"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa630-134"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa630-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fa630-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa630-136">**IDirect3DDXVADevice9**</span><span class="sxs-lookup"><span data-stu-id="fa630-136">**IDirect3DDXVADevice9**</span></span>](idirect3ddxvadevice9.md)
</dt> </dl>

 

 
