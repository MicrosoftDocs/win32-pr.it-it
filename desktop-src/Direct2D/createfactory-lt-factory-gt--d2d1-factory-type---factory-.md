---
title: Funzione Factory (D2D1_FACTORY_TYPE, Factory) D2D1CreateFactory (D2d1. h)
description: Crea un oggetto factory che può essere utilizzato per creare risorse Direct2D. | Funzione Factory (D2D1_FACTORY_TYPE, Factory) D2D1CreateFactory (D2d1. h)
ms.assetid: c1c25d51-15ea-4075-a896-bd6501bf68c1
keywords:
- D2D1CreateFactory Factory (D2D1_FACTORY_TYPE, Factory) funzione Direct2D
topic_type:
- apiref
api_name:
- D2D1CreateFactory Factory (D2D1_FACTORY_TYPE,Factory ) Function
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c03400cec8c838ba561a7eb504674e074d7b3199
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106322006"
---
# <a name="d2d1createfactoryfactoryd2d1_factory_typefactory-function"></a><span data-ttu-id="07a78-105"><Factory>Funzione D2D1CreateFactory ( \_ tipo Factory d2d1 \_ , factory \* \* )</span><span class="sxs-lookup"><span data-stu-id="07a78-105">D2D1CreateFactory<Factory>(D2D1\_FACTORY\_TYPE,Factory\*\*) Function</span></span>

<span data-ttu-id="07a78-106">Crea un oggetto factory che può essere utilizzato per creare risorse Direct2D.</span><span class="sxs-lookup"><span data-stu-id="07a78-106">Creates a factory object that can be used to create Direct2D resources.</span></span>

``` syntax
template<class Factory>
HRESULT D2D1CreateFactory(
    __in D2D1_FACTORY_TYPE factoryType,
    __out Factory **factory
);
```

## <a name="template-parameters"></a><span data-ttu-id="07a78-107">Parametri di template</span><span class="sxs-lookup"><span data-stu-id="07a78-107">Template Parameters</span></span>



| <span data-ttu-id="07a78-108">Parametro</span><span class="sxs-lookup"><span data-stu-id="07a78-108">Parameter</span></span> | <span data-ttu-id="07a78-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="07a78-109">Description</span></span>                                                 |
|-----------|-------------------------------------------------------------|
| <span data-ttu-id="07a78-110">*Fabbrica*</span><span class="sxs-lookup"><span data-stu-id="07a78-110">*Factory*</span></span> | <span data-ttu-id="07a78-111">Tipo di [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) da creare.</span><span class="sxs-lookup"><span data-stu-id="07a78-111">The type of [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) to create.</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="07a78-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="07a78-112">Parameters</span></span>



| <span data-ttu-id="07a78-113">Parametro</span><span class="sxs-lookup"><span data-stu-id="07a78-113">Parameter</span></span>     | <span data-ttu-id="07a78-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="07a78-114">Description</span></span>                                                                     |
|---------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="07a78-115">*factoryType*</span><span class="sxs-lookup"><span data-stu-id="07a78-115">*factoryType*</span></span> | <span data-ttu-id="07a78-116">Il modello di threading della Factory e le risorse che crea.</span><span class="sxs-lookup"><span data-stu-id="07a78-116">The threading model of the factory and the resources it creates.</span></span>                |
| <span data-ttu-id="07a78-117">*factory*</span><span class="sxs-lookup"><span data-stu-id="07a78-117">*factory*</span></span>     | <span data-ttu-id="07a78-118">Quando termina, questo metodo contiene l'indirizzo di un puntatore alla nuova factory.</span><span class="sxs-lookup"><span data-stu-id="07a78-118">When this method returns, contains the address of a pointer to the new factory.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="07a78-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="07a78-119">Return Value</span></span>

<span data-ttu-id="07a78-120">Se il metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="07a78-120">If the method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="07a78-121">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="07a78-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="examples"></a><span data-ttu-id="07a78-122">Esempio</span><span class="sxs-lookup"><span data-stu-id="07a78-122">Examples</span></span>

<span data-ttu-id="07a78-123">Nell'esempio seguente viene creata una factory.</span><span class="sxs-lookup"><span data-stu-id="07a78-123">The following example creates a factory.</span></span>


```C++
HRESULT DemoApp::CreateDeviceIndependentResources()
{
    HRESULT hr = S_OK;

    // Create a Direct2D factory.
    hr = D2D1CreateFactory(D2D1_FACTORY_TYPE_SINGLE_THREADED, &m_pDirect2dFactory);

    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="07a78-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="07a78-124">Requirements</span></span>



| <span data-ttu-id="07a78-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="07a78-125">Requirement</span></span> | <span data-ttu-id="07a78-126">Valore</span><span class="sxs-lookup"><span data-stu-id="07a78-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07a78-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="07a78-127">Minimum supported client</span></span><br/> | <span data-ttu-id="07a78-128">Windows 7, Windows Vista con SP2 e aggiornamento della piattaforma per app desktop di Windows Vista \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="07a78-128">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="07a78-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="07a78-129">Minimum supported server</span></span><br/> | <span data-ttu-id="07a78-130">Windows Server 2008 R2, Windows Server 2008 con SP2 e aggiornamento della piattaforma per app desktop di Windows Server 2008 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="07a78-130">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="07a78-131">Telefono minimo supportato</span><span class="sxs-lookup"><span data-stu-id="07a78-131">Minimum supported phone</span></span><br/>  | <span data-ttu-id="07a78-132">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e app per Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="07a78-132">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="07a78-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="07a78-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="07a78-134"><dt>D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="07a78-134"><dt>D2d1.h</dt></span></span> </dl>                                                        |
| <span data-ttu-id="07a78-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="07a78-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="07a78-136"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="07a78-136"><dt>D2d1.lib</dt></span></span> </dl>                                                      |
| <span data-ttu-id="07a78-137">DLL</span><span class="sxs-lookup"><span data-stu-id="07a78-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07a78-138"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07a78-138"><dt>D2d1.dll</dt></span></span> </dl>                                                      |



 

