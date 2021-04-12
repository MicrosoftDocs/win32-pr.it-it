---
description: Termina l'elaborazione per creare un'immagine decodificata.
ms.assetid: 4b47cd53-6ce0-47b0-83ed-84926e92430f
title: 'Metodo IDirect3DDXVADevice9:: EndFrame (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DDXVADevice9.EndFrame
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: a6a737fe6c4c3020b7ebfe7fee98281e6c83f168
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130343"
---
# <a name="idirect3ddxvadevice9endframe-method"></a><span data-ttu-id="d3d7d-103">Metodo IDirect3DDXVADevice9:: EndFrame</span><span class="sxs-lookup"><span data-stu-id="d3d7d-103">IDirect3DDXVADevice9::EndFrame method</span></span>

<span data-ttu-id="d3d7d-104">Termina l'elaborazione per creare un'immagine decodificata.</span><span class="sxs-lookup"><span data-stu-id="d3d7d-104">Ends the processing to create a decoded picture.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3d7d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d3d7d-105">Syntax</span></span>


```C++
HRESULT EndFrame(
   DWORD SizeMiscData,
   VOID  *pMiscData
);
```



## <a name="parameters"></a><span data-ttu-id="d3d7d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d3d7d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3d7d-107">*SizeMiscData*</span><span class="sxs-lookup"><span data-stu-id="d3d7d-107">*SizeMiscData*</span></span> 
</dt> <dd>

<span data-ttu-id="d3d7d-108">Dimensioni del buffer specificato da *pMiscData*, in byte.</span><span class="sxs-lookup"><span data-stu-id="d3d7d-108">The size of the buffer specified by *pMiscData*, in bytes.</span></span> <span data-ttu-id="d3d7d-109">Il valore deve essere 2.</span><span class="sxs-lookup"><span data-stu-id="d3d7d-109">The value must be 2.</span></span>

</dd> <dt>

<span data-ttu-id="d3d7d-110">*pMiscData*</span><span class="sxs-lookup"><span data-stu-id="d3d7d-110">*pMiscData*</span></span> 
</dt> <dd>

<span data-ttu-id="d3d7d-111">Puntatore a un buffer che contiene i dati per il tasto di scelta rapida del video.</span><span class="sxs-lookup"><span data-stu-id="d3d7d-111">Pointer to a buffer that contains data for the video accelerator.</span></span> <span data-ttu-id="d3d7d-112">Questo buffer deve contenere lo stesso indice frame passato al metodo [**IDirect3DDXVADevice9:: BeginFrame**](idirect3ddxvadevice9-beginframe.md) nel parametro *pInputData* .</span><span class="sxs-lookup"><span data-stu-id="d3d7d-112">This buffer must contain the same frame index that was passed to the [**IDirect3DDXVADevice9::BeginFrame**](idirect3ddxvadevice9-beginframe.md) method in the *pInputData* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3d7d-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d3d7d-113">Return value</span></span>

<span data-ttu-id="d3d7d-114">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d3d7d-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d3d7d-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d3d7d-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3d7d-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d3d7d-116">Requirements</span></span>



| <span data-ttu-id="d3d7d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3d7d-117">Requirement</span></span> | <span data-ttu-id="d3d7d-118">Valore</span><span class="sxs-lookup"><span data-stu-id="d3d7d-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="d3d7d-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d3d7d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d3d7d-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d3d7d-120">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d3d7d-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d3d7d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d3d7d-122">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d3d7d-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="d3d7d-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d3d7d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3d7d-124"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3d7d-124"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3d7d-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d3d7d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3d7d-126">**IDirect3DDXVADevice9**</span><span class="sxs-lookup"><span data-stu-id="d3d7d-126">**IDirect3DDXVADevice9**</span></span>](idirect3ddxvadevice9.md)
</dt> </dl>

 

 




