---
description: Chiamato dall'interfaccia IeAxiSystemInstaller per verificare che sia possibile installare un oggetto ActiveX.
ms.assetid: d5cd6263-d07e-4261-9463-b9a06e883f16
title: Interfaccia IeAxiServiceCallback
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiServiceCallback
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3ad276126548ac6d5fdc2c828f722c90b43ad679
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885669"
---
# <a name="ieaxiservicecallback-interface"></a><span data-ttu-id="77b23-103">Interfaccia IeAxiServiceCallback</span><span class="sxs-lookup"><span data-stu-id="77b23-103">IeAxiServiceCallback interface</span></span>

<span data-ttu-id="77b23-104">L'interfaccia **IeAxiServiceCallback** viene chiamata dall'interfaccia [**IeAxiSystemInstaller**](ieaxisysteminstaller.md) per verificare che sia possibile installare un oggetto ActiveX.</span><span class="sxs-lookup"><span data-stu-id="77b23-104">The **IeAxiServiceCallback** interface is called by the [**IeAxiSystemInstaller**](ieaxisysteminstaller.md) interface to verify that an ActiveX object can be installed.</span></span>

<span data-ttu-id="77b23-105">La classe [**CIeAxiInstallerService**](cieaxiinstallerservice.md) implementa questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="77b23-105">The [**CIeAxiInstallerService**](cieaxiinstallerservice.md) class implements this interface.</span></span>

<span data-ttu-id="77b23-106">Questa interfaccia non è dichiarata in un'intestazione pubblica.</span><span class="sxs-lookup"><span data-stu-id="77b23-106">This interface is not declared in a public header.</span></span> <span data-ttu-id="77b23-107">Le applicazioni devono definirle autonomamente.</span><span class="sxs-lookup"><span data-stu-id="77b23-107">Applications must define it themselves.</span></span> <span data-ttu-id="77b23-108">Il frammento IDL (Interface Definition Language) seguente descrive questa interfaccia, incluso il relativo IID.</span><span class="sxs-lookup"><span data-stu-id="77b23-108">The following Interface Definition Language (IDL) fragment describes this interface, including its IID.</span></span>

``` syntax
[
    object,
    uuid(1823E7BA-EC36-447a-9B2E-B4912E15AFE7),
    dual,
    nonextensible,
    pointer_default(unique)
]

interface IeAxiServiceCallback : IUnknown
{
    HRESULT VerifyFile(
                       [in] BSTR bstrFileUrl,
                       [out] BSTR * bstrApprovedFileName);
}

```

## <a name="members"></a><span data-ttu-id="77b23-109">Membri</span><span class="sxs-lookup"><span data-stu-id="77b23-109">Members</span></span>

<span data-ttu-id="77b23-110">L'interfaccia **IeAxiServiceCallback** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="77b23-110">The **IeAxiServiceCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="77b23-111">**IeAxiServiceCallback** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="77b23-111">**IeAxiServiceCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="77b23-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="77b23-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="77b23-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="77b23-113">Methods</span></span>

<span data-ttu-id="77b23-114">L'interfaccia **IeAxiServiceCallback** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="77b23-114">The **IeAxiServiceCallback** interface has these methods.</span></span>



| <span data-ttu-id="77b23-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="77b23-115">Method</span></span>                                                | <span data-ttu-id="77b23-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="77b23-116">Description</span></span>                                                                                                                                    |
|:------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="77b23-117">**VerifyFile**</span><span class="sxs-lookup"><span data-stu-id="77b23-117">**VerifyFile**</span></span>](ieaxiservicecallback-verifyfile.md) | <span data-ttu-id="77b23-118">Esegue i controlli di sicurezza sull'oggetto ActiveX specificato e restituisce il percorso in cui è stato scaricato il file con estensione CAB corrispondente.</span><span class="sxs-lookup"><span data-stu-id="77b23-118">Performs security checks on the specified ActiveX object and returns the location where the corresponding .cab file was downloaded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="77b23-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="77b23-119">Requirements</span></span>



| <span data-ttu-id="77b23-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="77b23-120">Requirement</span></span> | <span data-ttu-id="77b23-121">Valore</span><span class="sxs-lookup"><span data-stu-id="77b23-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77b23-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="77b23-122">Minimum supported client</span></span><br/> | <span data-ttu-id="77b23-123">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[ desktop apps\]</span><span class="sxs-lookup"><span data-stu-id="77b23-123">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="77b23-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="77b23-124">Minimum supported server</span></span><br/> | <span data-ttu-id="77b23-125">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="77b23-125">None supported</span></span><br/>                                                                                 |
| <span data-ttu-id="77b23-126">IID</span><span class="sxs-lookup"><span data-stu-id="77b23-126">IID</span></span><br/>                      | <span data-ttu-id="77b23-127">IID \_ IeAxiServiceCallback è definito come 1823E7BA-EC36-447A-9B2E-B4912E15AFE7</span><span class="sxs-lookup"><span data-stu-id="77b23-127">IID\_IeAxiServiceCallback is defined as 1823E7BA-EC36-447a-9B2E-B4912E15AFE7</span></span><br/>                   |



 

