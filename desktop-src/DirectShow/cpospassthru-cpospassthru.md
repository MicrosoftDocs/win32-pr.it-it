---
description: 'Costruttore CPosPassThru.CPosPassThru : metodo costruttore.'
ms.assetid: b258401c-158b-4eb8-8736-1e1ad9a8403a
title: Costruttore CPosPassThru.CPosPassThru
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.CPosPassThru
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2a6c49b305b3c6638aeaaee1480d0b561fd8c99a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085599"
---
# <a name="cpospassthrucpospassthru-constructor"></a><span data-ttu-id="fd588-103">Costruttore CPosPassThru.CPosPassThru</span><span class="sxs-lookup"><span data-stu-id="fd588-103">CPosPassThru.CPosPassThru constructor</span></span>

<span data-ttu-id="fd588-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="fd588-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd588-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fd588-105">Syntax</span></span>


```C++
CPosPassThru(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr,
         IPin      *pPin,
                   
);
```



## <a name="parameters"></a><span data-ttu-id="fd588-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="fd588-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd588-107">*Pname*</span><span class="sxs-lookup"><span data-stu-id="fd588-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="fd588-108">Puntatore al nome dell'oggetto, a scopo di debug.</span><span class="sxs-lookup"><span data-stu-id="fd588-108">Pointer to the name of the object, for debugging purposes.</span></span> <span data-ttu-id="fd588-109">Allocare questo parametro nella memoria statica.</span><span class="sxs-lookup"><span data-stu-id="fd588-109">Allocate this parameter in static memory.</span></span>

</dd> <dt>

<span data-ttu-id="fd588-110">*Punk*</span><span class="sxs-lookup"><span data-stu-id="fd588-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="fd588-111">Puntatore al proprietario dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="fd588-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="fd588-112">Se l'oggetto è aggregato, passare un puntatore all'interfaccia **IUnknown dell'oggetto** di aggregazione.</span><span class="sxs-lookup"><span data-stu-id="fd588-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="fd588-113">In caso contrario, impostare questo parametro su **NULL.**</span><span class="sxs-lookup"><span data-stu-id="fd588-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="fd588-114">*Phr*</span><span class="sxs-lookup"><span data-stu-id="fd588-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="fd588-115">Puntatore a un **valore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="fd588-115">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="fd588-116">Ignorato.</span><span class="sxs-lookup"><span data-stu-id="fd588-116">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="fd588-117">*pPin*</span><span class="sxs-lookup"><span data-stu-id="fd588-117">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="fd588-118">Puntatore [**all'interfaccia IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del pin di input del filtro.</span><span class="sxs-lookup"><span data-stu-id="fd588-118">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the filter's input pin.</span></span>

</dd> <dt>

 
</dt> <dd></dd> </dl>

 

 



