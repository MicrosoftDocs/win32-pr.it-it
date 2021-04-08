---
title: Interfaccia INapSoHProcessor (NapProtocol. h)
description: Vengono usati da SHAs per elaborare il contenuto di SoHResponses e SHV per elaborare il contenuto di SoHRequests.
ms.assetid: c2dd71ca-a4dd-44d2-81ab-b83e90599a2f
keywords:
- NAP interfaccia INapSoHProcessor
- Interfaccia NAP di INapSoHProcessor, descrizione
topic_type:
- apiref
api_name:
- INapSoHProcessor
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c43abf137bb267468deeb9d4bd47546275ba6c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047888"
---
# <a name="inapsohprocessor-interface"></a><span data-ttu-id="79f56-105">Interfaccia INapSoHProcessor</span><span class="sxs-lookup"><span data-stu-id="79f56-105">INapSoHProcessor interface</span></span>

> [!Note]  
> <span data-ttu-id="79f56-106">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="79f56-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="79f56-107">**INapSoHProcessor** fornisce i metodi usati da Shas per elaborare il contenuto di [**SoHResponses**](/windows/win32/api/naptypes/ns-naptypes-soh) e SHV per elaborare il contenuto di **SoHRequests**.</span><span class="sxs-lookup"><span data-stu-id="79f56-107">The **INapSoHProcessor** provides methods that are used by SHAs to process the contents of [**SoHResponses**](/windows/win32/api/naptypes/ns-naptypes-soh) and by SHVs to process the contents of **SoHRequests**.</span></span>

## <a name="members"></a><span data-ttu-id="79f56-108">Membri</span><span class="sxs-lookup"><span data-stu-id="79f56-108">Members</span></span>

<span data-ttu-id="79f56-109">L'interfaccia **INapSoHProcessor** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="79f56-109">The **INapSoHProcessor** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="79f56-110">**INapSoHProcessor** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="79f56-110">**INapSoHProcessor** also has these types of members:</span></span>

-   [<span data-ttu-id="79f56-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="79f56-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="79f56-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="79f56-112">Methods</span></span>

<span data-ttu-id="79f56-113">L'interfaccia **INapSoHProcessor** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="79f56-113">The **INapSoHProcessor** interface has these methods.</span></span>



| <span data-ttu-id="79f56-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="79f56-114">Method</span></span>                                                                                           | <span data-ttu-id="79f56-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="79f56-115">Description</span></span>                                                                           |
|:-------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [<span data-ttu-id="79f56-116">**INapSoHProcessor::FindNextAttribute**</span><span class="sxs-lookup"><span data-stu-id="79f56-116">**INapSoHProcessor::FindNextAttribute**</span></span>](inapsohprocessor-findnextattribute-method.md)         | <span data-ttu-id="79f56-117">Trova l'indice della posizione dell'attributo del pacchetto di rapporto di integrità successivo.</span><span class="sxs-lookup"><span data-stu-id="79f56-117">Finds the location index of the next SoH packet attribute.</span></span><br/>                 |
| [<span data-ttu-id="79f56-118">**INapSoHProcessor:: GetAttribute**</span><span class="sxs-lookup"><span data-stu-id="79f56-118">**INapSoHProcessor::GetAttribute**</span></span>](inapsohprocessor-getattribute-method.md)                   | <span data-ttu-id="79f56-119">Recupera il tipo e il valore dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="79f56-119">Retrieves the attribute type and value.</span></span><br/>                                    |
| [<span data-ttu-id="79f56-120">**INapSoHProcessor::GetNumberOfAttributes**</span><span class="sxs-lookup"><span data-stu-id="79f56-120">**INapSoHProcessor::GetNumberOfAttributes**</span></span>](inapsohprocessor-getnumberofattributes-method.md) | <span data-ttu-id="79f56-121">Recupera il numero di attributi contenuti nel rapporto di integrità.</span><span class="sxs-lookup"><span data-stu-id="79f56-121">Retrieves the number of attributes contained in the SoH.</span></span><br/>                   |
| [<span data-ttu-id="79f56-122">**INapSoHProcessor:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="79f56-122">**INapSoHProcessor::Initialize**</span></span>](inapsohprocessor-initialize-method.md)                       | <span data-ttu-id="79f56-123">Inizializza il pacchetto del protocollo di rapporto di integrità e il sistema NAP per l'elaborazione del contenuto.</span><span class="sxs-lookup"><span data-stu-id="79f56-123">Initializes the SoH protocol packet and NAP System for content processing.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="79f56-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="79f56-124">Requirements</span></span>



| <span data-ttu-id="79f56-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="79f56-125">Requirement</span></span> | <span data-ttu-id="79f56-126">Valore</span><span class="sxs-lookup"><span data-stu-id="79f56-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="79f56-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="79f56-127">Minimum supported client</span></span><br/> | <span data-ttu-id="79f56-128">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="79f56-128">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="79f56-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="79f56-129">Minimum supported server</span></span><br/> | <span data-ttu-id="79f56-130">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="79f56-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="79f56-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="79f56-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="79f56-132"><dt>NapProtocol. h</dt></span><span class="sxs-lookup"><span data-stu-id="79f56-132"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="79f56-133">IDL</span><span class="sxs-lookup"><span data-stu-id="79f56-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="79f56-134"><dt>NapProtocol. idl</dt></span><span class="sxs-lookup"><span data-stu-id="79f56-134"><dt>NapProtocol.idl</dt></span></span> </dl> |
| <span data-ttu-id="79f56-135">DLL</span><span class="sxs-lookup"><span data-stu-id="79f56-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="79f56-136"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="79f56-136"><dt>Qutil.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="79f56-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="79f56-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79f56-138">Interfacce NAP</span><span class="sxs-lookup"><span data-stu-id="79f56-138">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="79f56-139">Riferimento NAP</span><span class="sxs-lookup"><span data-stu-id="79f56-139">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

