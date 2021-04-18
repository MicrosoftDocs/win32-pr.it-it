---
title: Funzione D2D1CreateFactory Factory (D2D1_FACTORY_TYPE, D2D1_FACTORY_OPTIONS, Factory) (D2d1. h)
description: Crea un oggetto factory che può essere utilizzato per creare risorse Direct2D. | Funzione D2D1CreateFactory Factory (D2D1_FACTORY_TYPE, D2D1_FACTORY_OPTIONS, Factory) (D2d1. h)
ms.assetid: 618d7fbc-3801-4507-8774-4e1f4f36af44
keywords:
- Funzione D2D1CreateFactory Factory (D2D1_FACTORY_TYPE, D2D1_FACTORY_OPTIONS, Factory) Direct2D
topic_type:
- apiref
api_name:
- D2D1CreateFactory Factory (D2D1_FACTORY_TYPE,D2D1_FACTORY_OPTIONS ,Factory ) Function
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b25e6588ef79b234402742d473982910255f4230
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106322004"
---
# <a name="d2d1createfactoryfactoryd2d1_factory_typed2d1_factory_optionsfactory-function"></a><span data-ttu-id="cdc05-105">D2D1CreateFactory <Factory> ( \_ \_ tipo di Factory d2d1, D2D1 \_ Factory \_ options&, factory \* \* )</span><span class="sxs-lookup"><span data-stu-id="cdc05-105">D2D1CreateFactory<Factory>(D2D1\_FACTORY\_TYPE,D2D1\_FACTORY\_OPTIONS&,Factory\*\*) Function</span></span>

<span data-ttu-id="cdc05-106">Crea un oggetto factory che può essere utilizzato per creare risorse Direct2D.</span><span class="sxs-lookup"><span data-stu-id="cdc05-106">Creates a factory object that can be used to create Direct2D resources.</span></span>

``` syntax
template<class Factory>
HRESULT D2D1CreateFactory(
    __in D2D1_FACTORY_TYPE factoryType,
    __in CONST D2D1_FACTORY_OPTIONS &factoryOptions,
    __out Factory **factory
);
```

## <a name="template-parameters"></a><span data-ttu-id="cdc05-107">Parametri di template</span><span class="sxs-lookup"><span data-stu-id="cdc05-107">Template Parameters</span></span>



| <span data-ttu-id="cdc05-108">Parametro</span><span class="sxs-lookup"><span data-stu-id="cdc05-108">Parameter</span></span> | <span data-ttu-id="cdc05-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cdc05-109">Description</span></span>                                                 |
|-----------|-------------------------------------------------------------|
| <span data-ttu-id="cdc05-110">*Fabbrica*</span><span class="sxs-lookup"><span data-stu-id="cdc05-110">*Factory*</span></span> | <span data-ttu-id="cdc05-111">Tipo di [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) da creare.</span><span class="sxs-lookup"><span data-stu-id="cdc05-111">The type of [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) to create.</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="cdc05-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="cdc05-112">Parameters</span></span>



| <span data-ttu-id="cdc05-113">Parametro</span><span class="sxs-lookup"><span data-stu-id="cdc05-113">Parameter</span></span>        | <span data-ttu-id="cdc05-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cdc05-114">Description</span></span>                                                                     |
|------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="cdc05-115">*factoryType*</span><span class="sxs-lookup"><span data-stu-id="cdc05-115">*factoryType*</span></span>    | <span data-ttu-id="cdc05-116">Il modello di threading della Factory e le risorse che crea.</span><span class="sxs-lookup"><span data-stu-id="cdc05-116">The threading model of the factory and the resources it creates.</span></span>                |
| <span data-ttu-id="cdc05-117">*factoryOptions*</span><span class="sxs-lookup"><span data-stu-id="cdc05-117">*factoryOptions*</span></span> | <span data-ttu-id="cdc05-118">Livello di dettaglio fornito al livello di debug.</span><span class="sxs-lookup"><span data-stu-id="cdc05-118">The level of detail provided to the debugging layer.</span></span>                            |
| <span data-ttu-id="cdc05-119">*factory*</span><span class="sxs-lookup"><span data-stu-id="cdc05-119">*factory*</span></span>        | <span data-ttu-id="cdc05-120">Quando termina, questo metodo contiene l'indirizzo di un puntatore alla nuova factory.</span><span class="sxs-lookup"><span data-stu-id="cdc05-120">When this method returns, contains the address of a pointer to the new factory.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="cdc05-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cdc05-121">Return Value</span></span>

<span data-ttu-id="cdc05-122">Se il metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="cdc05-122">If the method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="cdc05-123">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cdc05-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="cdc05-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cdc05-124">Requirements</span></span>



| <span data-ttu-id="cdc05-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="cdc05-125">Requirement</span></span> | <span data-ttu-id="cdc05-126">Valore</span><span class="sxs-lookup"><span data-stu-id="cdc05-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdc05-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cdc05-127">Minimum supported client</span></span><br/> | <span data-ttu-id="cdc05-128">Windows 7, Windows Vista con SP2 e aggiornamento della piattaforma per app desktop di Windows Vista \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="cdc05-128">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="cdc05-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cdc05-129">Minimum supported server</span></span><br/> | <span data-ttu-id="cdc05-130">Windows Server 2008 R2, Windows Server 2008 con SP2 e aggiornamento della piattaforma per app desktop di Windows Server 2008 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="cdc05-130">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="cdc05-131">Telefono minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cdc05-131">Minimum supported phone</span></span><br/>  | <span data-ttu-id="cdc05-132">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e app per Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="cdc05-132">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="cdc05-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cdc05-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="cdc05-134"><dt>D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="cdc05-134"><dt>D2d1.h</dt></span></span> </dl>                                                        |
| <span data-ttu-id="cdc05-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="cdc05-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="cdc05-136"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cdc05-136"><dt>D2d1.lib</dt></span></span> </dl>                                                      |
| <span data-ttu-id="cdc05-137">DLL</span><span class="sxs-lookup"><span data-stu-id="cdc05-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cdc05-138"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cdc05-138"><dt>D2d1.dll</dt></span></span> </dl>                                                      |



 

