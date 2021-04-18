---
title: Metodo Controls. Step
description: Il metodo Step fa in modo che l'elemento multimediale del video corrente blocchi la riproduzione nel frame successivo o nel frame precedente.
ms.assetid: f717c583-4073-45a9-b05d-7134d02724a4
keywords:
- Metodo Step Media Player Windows
- Metodo Step Media Player Windows, classe Controls
- Classe Controls Media Player Windows, Metodo Step
topic_type:
- apiref
api_name:
- Controls.step
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43fc50ea28bde95efef6e6261788fdcc62df6089
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327390"
---
# <a name="controlsstep-method"></a><span data-ttu-id="23769-106">Metodo Controls. Step</span><span class="sxs-lookup"><span data-stu-id="23769-106">Controls.step method</span></span>

<span data-ttu-id="23769-107">Il metodo **Step** fa in modo che l'elemento multimediale del video corrente blocchi la riproduzione nel frame successivo o nel frame precedente.</span><span class="sxs-lookup"><span data-stu-id="23769-107">The **step** method causes the current video media item to freeze playback on the next frame or the previous frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="23769-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="23769-108">Syntax</span></span>


```JScript
Controls.step(
  frameCount
)
```



## <a name="parameters"></a><span data-ttu-id="23769-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="23769-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23769-110">*frameCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="23769-110">*frameCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23769-111">**Numero** (**Long**) che indica il numero di frame da scorrere prima del blocco.</span><span class="sxs-lookup"><span data-stu-id="23769-111">**Number** (**long**) indicating how many frames to step before freezing.</span></span> <span data-ttu-id="23769-112">Attualmente deve essere impostato su 1 o-1.</span><span class="sxs-lookup"><span data-stu-id="23769-112">Must currently be set to 1 or -1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23769-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="23769-113">Return value</span></span>

<span data-ttu-id="23769-114">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="23769-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="23769-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="23769-115">Remarks</span></span>

<span data-ttu-id="23769-116">Questo metodo supporta attualmente solo i parametri 1 o-1, pertanto è possibile eseguire un solo passaggio di un frame alla volta.</span><span class="sxs-lookup"><span data-stu-id="23769-116">This method currently only supports the parameters 1 or -1, so you can only step one frame at a time.</span></span>

<span data-ttu-id="23769-117">**Windows Media Player 10 Mobile:** Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="23769-117">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="23769-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="23769-118">Requirements</span></span>



| <span data-ttu-id="23769-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="23769-119">Requirement</span></span> | <span data-ttu-id="23769-120">Valore</span><span class="sxs-lookup"><span data-stu-id="23769-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="23769-121">Versione</span><span class="sxs-lookup"><span data-stu-id="23769-121">Version</span></span><br/> | <span data-ttu-id="23769-122">Windows Media Player per Windows XP o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="23769-122">Windows Media Player for Windows XP or later.</span></span><br/>                           |
| <span data-ttu-id="23769-123">DLL</span><span class="sxs-lookup"><span data-stu-id="23769-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="23769-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23769-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23769-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="23769-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23769-126">**Oggetto Controls**</span><span class="sxs-lookup"><span data-stu-id="23769-126">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="23769-127">**Oggetto DVD**</span><span class="sxs-lookup"><span data-stu-id="23769-127">**DVD Object**</span></span>](dvd-object.md)
</dt> </dl>

 

 





