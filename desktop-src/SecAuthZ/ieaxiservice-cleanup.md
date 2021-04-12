---
description: Libera le risorse usate dall'interfaccia IeAxiService.
ms.assetid: 11f5cfdc-dcdd-4b41-b02c-b19b9452509e
title: 'Metodo IeAxiService:: Cleanup'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiService.Cleanup
api_type:
- COM
api_location: ''
ms.openlocfilehash: b29784ae360ec78b9f7e01d2045617615333a5c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232668"
---
# <a name="ieaxiservicecleanup-method"></a><span data-ttu-id="599ae-103">Metodo IeAxiService:: Cleanup</span><span class="sxs-lookup"><span data-stu-id="599ae-103">IeAxiService::Cleanup method</span></span>

<span data-ttu-id="599ae-104">Il metodo **Cleanup** libera le risorse usate dall'interfaccia [**IeAxiService**](ieaxiservice.md) .</span><span class="sxs-lookup"><span data-stu-id="599ae-104">The **Cleanup** method frees resources used by the [**IeAxiService**](ieaxiservice.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="599ae-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="599ae-105">Syntax</span></span>


```C++
HRESULT Cleanup();
```



## <a name="parameters"></a><span data-ttu-id="599ae-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="599ae-106">Parameters</span></span>

<span data-ttu-id="599ae-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="599ae-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="599ae-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="599ae-108">Return value</span></span>

<span data-ttu-id="599ae-109">Se il metodo ha esito positivo, il metodo restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="599ae-109">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="599ae-110">Se il metodo ha esito negativo, restituisce un valore **HRESULT** che indica l'errore.</span><span class="sxs-lookup"><span data-stu-id="599ae-110">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="599ae-111">Per un elenco di codici di errore comuni, vedere [valori HRESULT comuni](/windows/desktop/SecCrypto/common-hresult-values).</span><span class="sxs-lookup"><span data-stu-id="599ae-111">For a list of common error codes, see [Common HRESULT Values](/windows/desktop/SecCrypto/common-hresult-values).</span></span>

## <a name="requirements"></a><span data-ttu-id="599ae-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="599ae-112">Requirements</span></span>



| <span data-ttu-id="599ae-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="599ae-113">Requirement</span></span> | <span data-ttu-id="599ae-114">Valore</span><span class="sxs-lookup"><span data-stu-id="599ae-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="599ae-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="599ae-115">Minimum supported client</span></span><br/> | <span data-ttu-id="599ae-116">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[ desktop apps\]</span><span class="sxs-lookup"><span data-stu-id="599ae-116">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="599ae-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="599ae-117">Minimum supported server</span></span><br/> | <span data-ttu-id="599ae-118">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="599ae-118">None supported</span></span><br/>                                                                                 |
| <span data-ttu-id="599ae-119">IID</span><span class="sxs-lookup"><span data-stu-id="599ae-119">IID</span></span><br/>                      | <span data-ttu-id="599ae-120">IID \_ IeAxiService è definito come E9E92380-9ECD-4982-A0EB-6815A56CCF27</span><span class="sxs-lookup"><span data-stu-id="599ae-120">IID\_IeAxiService is defined as E9E92380-9ECD-4982-A0EB-6815A56CCF27</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="599ae-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="599ae-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="599ae-122">**IeAxiService**</span><span class="sxs-lookup"><span data-stu-id="599ae-122">**IeAxiService**</span></span>](ieaxiservice.md)
</dt> </dl>

 

