---
description: Inizializza un oggetto servizio di sistema per installare un oggetto ActiveX quando l'utente corrente non dispone dell'autorizzazione per l'installazione dell'oggetto.
ms.assetid: 42f7cf83-789b-42ea-bb1a-4b79137188ea
title: Interfaccia IeAxiService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiService
api_type:
- COM
api_location: ''
ms.openlocfilehash: 34c4743327b2539616dee6b09c34d9f479aa3303
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315432"
---
# <a name="ieaxiservice-interface"></a><span data-ttu-id="97340-103">Interfaccia IeAxiService</span><span class="sxs-lookup"><span data-stu-id="97340-103">IeAxiService interface</span></span>

<span data-ttu-id="97340-104">L'interfaccia **IAxiService** Inizializza un oggetto servizio di sistema per installare un oggetto ActiveX quando l'utente corrente non dispone dell'autorizzazione per l'installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="97340-104">The **IAxiService** interface initializes a system service object to install an ActiveX object when the current user does not have permission to install the object.</span></span>

<span data-ttu-id="97340-105">La classe [**CIeAxiInstallerService**](cieaxiinstallerservice.md) implementa questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="97340-105">The [**CIeAxiInstallerService**](cieaxiinstallerservice.md) class implements this interface.</span></span>

<span data-ttu-id="97340-106">Questa interfaccia non è dichiarata in un'intestazione pubblica.</span><span class="sxs-lookup"><span data-stu-id="97340-106">This interface is not declared in a public header.</span></span> <span data-ttu-id="97340-107">Le applicazioni devono definirle autonomamente.</span><span class="sxs-lookup"><span data-stu-id="97340-107">Applications must define it themselves.</span></span> <span data-ttu-id="97340-108">Il frammento IDL (Interface Definition Language) seguente descrive questa interfaccia, incluso il relativo IID.</span><span class="sxs-lookup"><span data-stu-id="97340-108">The following Interface Definition Language (IDL) fragment describes this interface, including its IID.</span></span>

``` syntax
[
    object,
    uuid(E9E92380-9ECD-4982-A0EB-6815A56CCF27),
    pointer_default(unique)
]

interface IeAxiService : IUnknown{

    
    HRESULT Initialize(
            [in]        HWND            hwndParent,
            [in]        DWORD           dwClientPID,
            [in]        BSTR            bstrDesktop,
            [in]        BSTR            bstrClsID,              
            [in]        BSTR            bstrURL,                
            [out]       BSTR *          pbstrNonce,            
            [out]       IUnknown**      ppISyncBrokerInterface  
            );  
 
    HRESULT Cleanup();
};
```

## <a name="members"></a><span data-ttu-id="97340-109">Membri</span><span class="sxs-lookup"><span data-stu-id="97340-109">Members</span></span>

<span data-ttu-id="97340-110">L'interfaccia **IeAxiService** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="97340-110">The **IeAxiService** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="97340-111">**IeAxiService** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="97340-111">**IeAxiService** also has these types of members:</span></span>

-   [<span data-ttu-id="97340-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="97340-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="97340-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="97340-113">Methods</span></span>

<span data-ttu-id="97340-114">L'interfaccia **IeAxiService** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="97340-114">The **IeAxiService** interface has these methods.</span></span>



| <span data-ttu-id="97340-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="97340-115">Method</span></span>                                        | <span data-ttu-id="97340-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="97340-116">Description</span></span>                                                        |
|:----------------------------------------------|:-------------------------------------------------------------------|
| [<span data-ttu-id="97340-117">**Pulizia**</span><span class="sxs-lookup"><span data-stu-id="97340-117">**Cleanup**</span></span>](ieaxiservice-cleanup.md)       | <span data-ttu-id="97340-118">Libera le risorse usate dall'interfaccia **IeAxiService** .</span><span class="sxs-lookup"><span data-stu-id="97340-118">Frees resources used by the **IeAxiService** interface.</span></span><br/> |
| [<span data-ttu-id="97340-119">**Inizializzare**</span><span class="sxs-lookup"><span data-stu-id="97340-119">**Initialize**</span></span>](ieaxiservice-initialize.md) | <span data-ttu-id="97340-120">Verifica e Scarica un oggetto ActiveX.</span><span class="sxs-lookup"><span data-stu-id="97340-120">Checks and downloads an ActiveX object.</span></span><br/>                 |



 

## <a name="requirements"></a><span data-ttu-id="97340-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="97340-121">Requirements</span></span>



| <span data-ttu-id="97340-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="97340-122">Requirement</span></span> | <span data-ttu-id="97340-123">Valore</span><span class="sxs-lookup"><span data-stu-id="97340-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97340-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="97340-124">Minimum supported client</span></span><br/> | <span data-ttu-id="97340-125">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[ desktop apps\]</span><span class="sxs-lookup"><span data-stu-id="97340-125">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="97340-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="97340-126">Minimum supported server</span></span><br/> | <span data-ttu-id="97340-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="97340-127">None supported</span></span><br/>                                                                                 |
| <span data-ttu-id="97340-128">IID</span><span class="sxs-lookup"><span data-stu-id="97340-128">IID</span></span><br/>                      | <span data-ttu-id="97340-129">IID \_ IeAxiService è definito come E9E92380-9ECD-4982-A0EB-6815A56CCF27</span><span class="sxs-lookup"><span data-stu-id="97340-129">IID\_IeAxiService is defined as E9E92380-9ECD-4982-A0EB-6815A56CCF27</span></span><br/>                           |



 

