---
description: L'interfaccia IProvidePropertyBuilder, quando implementata, consente agli oggetti di specificare oggetti generatore di proprietà per le proprietà.
ms.assetid: 26557622-4a97-4db0-85ed-3f77fcb769a0
title: Interfaccia IProvidePropertyBuilder
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IProvidePropertyBuilder:IUnknown
api_type:
- COM
api_location:
- Vsp.dll
ms.openlocfilehash: b93d05c3c64686b21f19ffe6262ddfd68812dd80
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325213"
---
# <a name="iprovidepropertybuilder-interface"></a><span data-ttu-id="4d2b4-103">Interfaccia IProvidePropertyBuilder</span><span class="sxs-lookup"><span data-stu-id="4d2b4-103">IProvidePropertyBuilder interface</span></span>

<span data-ttu-id="4d2b4-104">L'interfaccia **IProvidePropertyBuilder** , quando implementata, consente agli oggetti di specificare oggetti generatore di proprietà per le proprietà.</span><span class="sxs-lookup"><span data-stu-id="4d2b4-104">The **IProvidePropertyBuilder** interface, when implemented, allows objects to specify property builder objects for properties.</span></span> <span data-ttu-id="4d2b4-105">I generatori vengono richiamati da un pulsante con i puntini di sospensione ( \[ ... \] ) nel Visualizzatore proprietà Microsoft Visual Studio e vengono richiamati tramite [**ExecuteBuilder**](iprovidepropertybuilder-executebuilder.md) quando viene premuto il pulsante.</span><span class="sxs-lookup"><span data-stu-id="4d2b4-105">Builders are invoked by an ellipsis button (\[...\]) on the Microsoft Visual Studio property browser and is invoked through [**ExecuteBuilder**](iprovidepropertybuilder-executebuilder.md) when the button is pressed.</span></span> <span data-ttu-id="4d2b4-106">Per fornire un generatore per una determinata proprietà, restituire un GUID per il generatore di proprietà che deve essere richiamato per la proprietà corrente da [**MapPropertyToBuilder**](iprovidepropertybuilder-mappropertytobuilder.md).</span><span class="sxs-lookup"><span data-stu-id="4d2b4-106">To supply a builder for a given property, return a GUID for the property builder that should be invoked for the current property from [**MapPropertyToBuilder**](iprovidepropertybuilder-mappropertytobuilder.md).</span></span> <span data-ttu-id="4d2b4-107">I generatori vengono in genere implementati tramite le finestre di dialogo modali.</span><span class="sxs-lookup"><span data-stu-id="4d2b4-107">Builders are generally implemented through modal dialog boxes.</span></span>

<span data-ttu-id="4d2b4-108">La versione per questa interfaccia è 1,0.</span><span class="sxs-lookup"><span data-stu-id="4d2b4-108">The version for this interface is 1.0.</span></span> <span data-ttu-id="4d2b4-109">Le chiamate al metodo vengono ricevute in un endpoint assegnato dinamicamente (come descritto nella documentazione binaria MSMQ sul mapping degli endpoint) e usano l'UUID (Universally Unique Identifier) "33C0C1D8-33CF-11d3-BFF2-00C04F990235".</span><span class="sxs-lookup"><span data-stu-id="4d2b4-109">Method calls are received at a dynamically assigned endpoint (as described in the MSMQ binary documentation on endpoint mapping) and use the UUID (universally unique identifier) "33C0C1D8-33CF-11d3-BFF2-00C04F990235".</span></span>

## <a name="members"></a><span data-ttu-id="4d2b4-110">Membri</span><span class="sxs-lookup"><span data-stu-id="4d2b4-110">Members</span></span>

<span data-ttu-id="4d2b4-111">L'interfaccia **IProvidePropertyBuilder: IUnknown** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="4d2b4-111">The **IProvidePropertyBuilder:IUnknown** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="4d2b4-112">**IProvidePropertyBuilder** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="4d2b4-112">**IProvidePropertyBuilder** also has these types of members:</span></span>

-   [<span data-ttu-id="4d2b4-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="4d2b4-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4d2b4-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="4d2b4-114">Methods</span></span>

<span data-ttu-id="4d2b4-115">L'interfaccia **IProvidePropertyBuilder: IUnknown** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="4d2b4-115">The **IProvidePropertyBuilder:IUnknown** interface has these methods.</span></span>



| <span data-ttu-id="4d2b4-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="4d2b4-116">Method</span></span>                                                                       | <span data-ttu-id="4d2b4-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4d2b4-117">Description</span></span>                                                                                  |
|:-----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4d2b4-118">**ExecuteBuilder**</span><span class="sxs-lookup"><span data-stu-id="4d2b4-118">**ExecuteBuilder**</span></span>](iprovidepropertybuilder-executebuilder.md)             | <span data-ttu-id="4d2b4-119">Notifica a un oggetto che deve visualizzare il relativo generatore per la proprietà specificata.</span><span class="sxs-lookup"><span data-stu-id="4d2b4-119">Notifies an object that it should display its builder for the specified property.</span></span><br/> |
| [<span data-ttu-id="4d2b4-120">**MapPropertyToBuilder**</span><span class="sxs-lookup"><span data-stu-id="4d2b4-120">**MapPropertyToBuilder**</span></span>](iprovidepropertybuilder-mappropertytobuilder.md) | <span data-ttu-id="4d2b4-121">Verifica se un generatore deve essere associato a una particolare proprietà.</span><span class="sxs-lookup"><span data-stu-id="4d2b4-121">Checks whether a builder should be associated with a particular property.</span></span><br/>         |



 

## <a name="requirements"></a><span data-ttu-id="4d2b4-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4d2b4-122">Requirements</span></span>



| <span data-ttu-id="4d2b4-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d2b4-123">Requirement</span></span> | <span data-ttu-id="4d2b4-124">Valore</span><span class="sxs-lookup"><span data-stu-id="4d2b4-124">Value</span></span> |
|----------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4d2b4-125">DLL</span><span class="sxs-lookup"><span data-stu-id="4d2b4-125">DLL</span></span><br/> | <dl> <span data-ttu-id="4d2b4-126"><dt>Vsp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d2b4-126"><dt>Vsp.dll</dt></span></span> </dl> |



 

 
