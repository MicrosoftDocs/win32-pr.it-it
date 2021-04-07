---
description: Installa un oggetto ActiveX.
ms.assetid: 0eb725a9-ceb8-40e5-808d-ac2b286a48b6
title: Interfaccia IeAxiSystemInstaller
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiSystemInstaller
api_type:
- COM
api_location: ''
ms.openlocfilehash: 391088a70aa845cd685511f10e4eb6e809dc7fcf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058135"
---
# <a name="ieaxisysteminstaller-interface"></a><span data-ttu-id="af72b-103">Interfaccia IeAxiSystemInstaller</span><span class="sxs-lookup"><span data-stu-id="af72b-103">IeAxiSystemInstaller interface</span></span>

<span data-ttu-id="af72b-104">L'interfaccia **IeAxiSystemInstaller** installa un oggetto ActiveX.</span><span class="sxs-lookup"><span data-stu-id="af72b-104">The **IeAxiSystemInstaller** interface installs an ActiveX object.</span></span>

<span data-ttu-id="af72b-105">Questa interfaccia non è dichiarata in un'intestazione pubblica.</span><span class="sxs-lookup"><span data-stu-id="af72b-105">This interface is not declared in a public header.</span></span> <span data-ttu-id="af72b-106">Le applicazioni devono definirle autonomamente.</span><span class="sxs-lookup"><span data-stu-id="af72b-106">Applications must define it themselves.</span></span> <span data-ttu-id="af72b-107">Il frammento IDL (Interface Definition Language) seguente descrive questa interfaccia, incluso il relativo IID.</span><span class="sxs-lookup"><span data-stu-id="af72b-107">The following Interface Definition Language (IDL) fragment describes this interface, including its IID.</span></span>

``` syntax
[
    object,
    uuid(a50ea6f8-4764-4299-b309-022b2a8b4d8d),
    
]
interface IeAxiSystemInstaller : IUnknown
{
    
    HRESULT InitializeSystemInstaller(  [in] BSTR bstrUrl,
                                  [in] DWORD dwClientPID,
                                  [in] IUnknown* pCallback,
                                  [out] BSTR * pbstrNonce);
}

```

## <a name="members"></a><span data-ttu-id="af72b-108">Membri</span><span class="sxs-lookup"><span data-stu-id="af72b-108">Members</span></span>

<span data-ttu-id="af72b-109">L'interfaccia **IeAxiSystemInstaller** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="af72b-109">The **IeAxiSystemInstaller** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="af72b-110">**IeAxiSystemInstaller** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="af72b-110">**IeAxiSystemInstaller** also has these types of members:</span></span>

-   [<span data-ttu-id="af72b-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="af72b-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="af72b-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="af72b-112">Methods</span></span>

<span data-ttu-id="af72b-113">L'interfaccia **IeAxiSystemInstaller** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="af72b-113">The **IeAxiSystemInstaller** interface has these methods.</span></span>



| <span data-ttu-id="af72b-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="af72b-114">Method</span></span>                                                                              | <span data-ttu-id="af72b-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="af72b-115">Description</span></span>                                       |
|:------------------------------------------------------------------------------------|:--------------------------------------------------|
| [<span data-ttu-id="af72b-116">**InitializeSystemInstaller**</span><span class="sxs-lookup"><span data-stu-id="af72b-116">**InitializeSystemInstaller**</span></span>](ieaxisysteminstaller-initializesysteminstaller.md) | <span data-ttu-id="af72b-117">Installa l'oggetto ActiveX specificato.</span><span class="sxs-lookup"><span data-stu-id="af72b-117">Installs the specified ActiveX object.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="af72b-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="af72b-118">Requirements</span></span>



| <span data-ttu-id="af72b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="af72b-119">Requirement</span></span> | <span data-ttu-id="af72b-120">Valore</span><span class="sxs-lookup"><span data-stu-id="af72b-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af72b-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="af72b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="af72b-122">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[ desktop apps\]</span><span class="sxs-lookup"><span data-stu-id="af72b-122">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="af72b-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="af72b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="af72b-124">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="af72b-124">None supported</span></span><br/>                                                                                 |
| <span data-ttu-id="af72b-125">IID</span><span class="sxs-lookup"><span data-stu-id="af72b-125">IID</span></span><br/>                      | <span data-ttu-id="af72b-126">IID \_ IeAxiSystemInstaller è definito come a50ea6f8-4764-4299-B309-022b2a8b4d8d</span><span class="sxs-lookup"><span data-stu-id="af72b-126">IID\_IeAxiSystemInstaller is defined as a50ea6f8-4764-4299-b309-022b2a8b4d8d</span></span><br/>                   |



 

