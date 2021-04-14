---
description: 'Altre informazioni su: Metodo IMFMediaKeys:: Shutdown'
ms.assetid: 464b598c-5fa7-40af-83ba-8619fbd84b04
title: 'Metodo IMFMediaKeys:: Shutdown'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeys.Shutdown
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 9fcee861b53aaf0c9fda2c6265f50fcee60f674c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351566"
---
# <a name="imfmediakeysshutdown-method"></a><span data-ttu-id="76ab6-103">Metodo IMFMediaKeys:: Shutdown</span><span class="sxs-lookup"><span data-stu-id="76ab6-103">IMFMediaKeys::Shutdown method</span></span>

## <a name="syntax"></a><span data-ttu-id="76ab6-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="76ab6-104">Syntax</span></span>


```C++
HRESULT Shutdown();
```



## <a name="parameters"></a><span data-ttu-id="76ab6-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="76ab6-105">Parameters</span></span>

<span data-ttu-id="76ab6-106">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="76ab6-106">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="76ab6-107">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="76ab6-107">Return value</span></span>

<span data-ttu-id="76ab6-108">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="76ab6-108">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="76ab6-109">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="76ab6-109">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="76ab6-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="76ab6-110">Remarks</span></span>

<span data-ttu-id="76ab6-111">L' **arresto** deve essere chiamato dall'applicazione prima della versione finale.</span><span class="sxs-lookup"><span data-stu-id="76ab6-111">**Shutdown** should be called by the application before final release.</span></span> <span data-ttu-id="76ab6-112">A questo punto vengono rilasciati il riferimento del modulo di decrittografia del contenuto (CDM) e altre risorse.</span><span class="sxs-lookup"><span data-stu-id="76ab6-112">The Content Decryption Module (CDM) reference and any other resources is released at this point.</span></span> <span data-ttu-id="76ab6-113">Tuttavia, le sessioni correlate non vengono liberate o chiuse.</span><span class="sxs-lookup"><span data-stu-id="76ab6-113">However, related sessions are not freed or closed.</span></span>

## <a name="requirements"></a><span data-ttu-id="76ab6-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="76ab6-114">Requirements</span></span>



| <span data-ttu-id="76ab6-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="76ab6-115">Requirement</span></span> | <span data-ttu-id="76ab6-116">Valore</span><span class="sxs-lookup"><span data-stu-id="76ab6-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="76ab6-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="76ab6-117">Minimum supported client</span></span><br/> | <span data-ttu-id="76ab6-118">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="76ab6-118">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="76ab6-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="76ab6-119">Minimum supported server</span></span><br/> | <span data-ttu-id="76ab6-120">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="76ab6-120">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="76ab6-121">IDL</span><span class="sxs-lookup"><span data-stu-id="76ab6-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="76ab6-122"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="76ab6-122"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76ab6-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="76ab6-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76ab6-124">**IMFMediaKeys**</span><span class="sxs-lookup"><span data-stu-id="76ab6-124">**IMFMediaKeys**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeys)
</dt> </dl>

 

 




