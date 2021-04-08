---
description: Indica che è in corso l'avvio del processo di sospensione e che è necessario portare le risorse in uno stato coerente.
ms.assetid: 5cf3d249-3d8b-4596-9d8b-e7b95a270eff
title: 'Metodo IMFCdmSuspendNotify:: Begin'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFCdmSuspendNotify.Begin
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 84453a6c846e88a9d6e6c32c5253d97d36e89c7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749663"
---
# <a name="imfcdmsuspendnotifybegin-method"></a><span data-ttu-id="db3f3-103">Metodo IMFCdmSuspendNotify:: Begin</span><span class="sxs-lookup"><span data-stu-id="db3f3-103">IMFCdmSuspendNotify::Begin method</span></span>

<span data-ttu-id="db3f3-104">Indica che è in corso l'avvio del processo di sospensione e che è necessario portare le risorse in uno stato coerente.</span><span class="sxs-lookup"><span data-stu-id="db3f3-104">Indicates that the suspend process is starting and resources should be brought into a consistent state.</span></span>

## <a name="syntax"></a><span data-ttu-id="db3f3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="db3f3-105">Syntax</span></span>


```C++
HRESULT Begin();
```



## <a name="parameters"></a><span data-ttu-id="db3f3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="db3f3-106">Parameters</span></span>

<span data-ttu-id="db3f3-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="db3f3-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="db3f3-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="db3f3-108">Return value</span></span>

<span data-ttu-id="db3f3-109">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="db3f3-109">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="db3f3-110">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="db3f3-110">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="db3f3-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="db3f3-111">Requirements</span></span>



| <span data-ttu-id="db3f3-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="db3f3-112">Requirement</span></span> | <span data-ttu-id="db3f3-113">Valore</span><span class="sxs-lookup"><span data-stu-id="db3f3-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="db3f3-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="db3f3-114">Minimum supported client</span></span><br/> | <span data-ttu-id="db3f3-115">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="db3f3-115">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="db3f3-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="db3f3-116">Minimum supported server</span></span><br/> | <span data-ttu-id="db3f3-117">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="db3f3-117">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="db3f3-118">IDL</span><span class="sxs-lookup"><span data-stu-id="db3f3-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="db3f3-119"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="db3f3-119"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db3f3-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="db3f3-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db3f3-121">**IMFCdmSuspendNotify**</span><span class="sxs-lookup"><span data-stu-id="db3f3-121">**IMFCdmSuspendNotify**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfcdmsuspendnotify)
</dt> </dl>

 

 




