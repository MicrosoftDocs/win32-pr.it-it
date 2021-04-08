---
title: Interfaccia IWMDRMLicenseQuery
description: L'interfaccia IWMDRMLicenseQuery consente alle applicazioni di eseguire query sui diritti e sullo stato delle licenze per un file protetto.
ms.assetid: 4ec8ff9f-0acb-4389-8995-65f24736491b
keywords:
- Formato Windows Media Interface IWMDRMLicenseQuery
- Interfaccia IWMDRMLicenseQuery-formato Windows Media, descritto
topic_type:
- apiref
api_name:
- IWMDRMLicenseQuery
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6463f405bf50d4d4ecb037dc542e3af0e5b7df46
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728714"
---
# <a name="iwmdrmlicensequery-interface"></a><span data-ttu-id="e4f43-105">Interfaccia IWMDRMLicenseQuery</span><span class="sxs-lookup"><span data-stu-id="e4f43-105">IWMDRMLicenseQuery interface</span></span>

<span data-ttu-id="e4f43-106">L'interfaccia **IWMDRMLicenseQuery** consente alle applicazioni di eseguire query sui diritti e sullo stato delle licenze per un file protetto.</span><span class="sxs-lookup"><span data-stu-id="e4f43-106">The **IWMDRMLicenseQuery** interface enables applications to query the rights and license state for a protected file.</span></span> <span data-ttu-id="e4f43-107">Questa interfaccia usa l'ID chiave per eseguire query sull'archivio licenze locale.</span><span class="sxs-lookup"><span data-stu-id="e4f43-107">This interface uses the Key ID to perform queries on the local license store.</span></span>

<span data-ttu-id="e4f43-108">Per ottenere un'istanza di questa interfaccia, chiamare [**IWMDRMProvider:: CreateObject**](iwmdrmprovider-createobject.md).</span><span class="sxs-lookup"><span data-stu-id="e4f43-108">To obtain an instance of this interface, call [**IWMDRMProvider::CreateObject**](iwmdrmprovider-createobject.md).</span></span> <span data-ttu-id="e4f43-109">Passare **IID \_ IWMDRMLicenseQuery** come parametro *riid* .</span><span class="sxs-lookup"><span data-stu-id="e4f43-109">Pass **IID\_IWMDRMLicenseQuery** as the *riid* parameter.</span></span>

## <a name="members"></a><span data-ttu-id="e4f43-110">Membri</span><span class="sxs-lookup"><span data-stu-id="e4f43-110">Members</span></span>

<span data-ttu-id="e4f43-111">L'interfaccia **IWMDRMLicenseQuery** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="e4f43-111">The **IWMDRMLicenseQuery** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="e4f43-112">**IWMDRMLicenseQuery** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e4f43-112">**IWMDRMLicenseQuery** also has these types of members:</span></span>

-   [<span data-ttu-id="e4f43-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="e4f43-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e4f43-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="e4f43-114">Methods</span></span>

<span data-ttu-id="e4f43-115">L'interfaccia **IWMDRMLicenseQuery** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="e4f43-115">The **IWMDRMLicenseQuery** interface has these methods.</span></span>



| <span data-ttu-id="e4f43-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="e4f43-116">Method</span></span>                                                                                | <span data-ttu-id="e4f43-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e4f43-117">Description</span></span>                                                                                      |
|:--------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e4f43-118">**QueryActionAllowed**</span><span class="sxs-lookup"><span data-stu-id="e4f43-118">**QueryActionAllowed**</span></span>](iwmdrmlicensequery-queryactionallowed.md)                   | <span data-ttu-id="e4f43-119">Esegue una query sull'archivio licenze locale per le autorizzazioni per l'esecuzione di azioni in base all'ID chiave.</span><span class="sxs-lookup"><span data-stu-id="e4f43-119">Queries the local license store for permissions to perform actions by Key ID.</span></span><br/>         |
| [<span data-ttu-id="e4f43-120">**QueryLicenseState**</span><span class="sxs-lookup"><span data-stu-id="e4f43-120">**QueryLicenseState**</span></span>](iwmdrmlicensequery-querylicensestate.md)                     | <span data-ttu-id="e4f43-121">Esegue una query nell'archivio licenze locale per i dati relativi allo stato della licenza in base all'ID chiave e diritti specifici.</span><span class="sxs-lookup"><span data-stu-id="e4f43-121">Queries the local license store for license state data by Key ID and specific rights.</span></span><br/> |
| [<span data-ttu-id="e4f43-122">**SetActionAllowedQueryParams**</span><span class="sxs-lookup"><span data-stu-id="e4f43-122">**SetActionAllowedQueryParams**</span></span>](iwmdrmlicensequery-setactionallowedqueryparams.md) | <span data-ttu-id="e4f43-123">Imposta i parametri ambientali per migliorare l'accuratezza delle query sulle licenze.</span><span class="sxs-lookup"><span data-stu-id="e4f43-123">Sets environmental parameters to improve the accuracy of license queries.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="e4f43-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="e4f43-124">Remarks</span></span>

<span data-ttu-id="e4f43-125">I metodi di **IWMDRMLicenseQuery** non forniscono informazioni sulle singole licenze.</span><span class="sxs-lookup"><span data-stu-id="e4f43-125">The methods of **IWMDRMLicenseQuery** do not provide information about individual licenses.</span></span> <span data-ttu-id="e4f43-126">I dati di licenza vengono invece aggregati dal sottosistema DRM prima che vengano restituiti i risultati della query.</span><span class="sxs-lookup"><span data-stu-id="e4f43-126">Instead, the license data is aggregated by the DRM subsystem before the query results are returned.</span></span>

## <a name="see-also"></a><span data-ttu-id="e4f43-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e4f43-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4f43-128">**Interfacce**</span><span class="sxs-lookup"><span data-stu-id="e4f43-128">**Interfaces**</span></span>](drm-interfaces.md)
</dt> </dl>

 

