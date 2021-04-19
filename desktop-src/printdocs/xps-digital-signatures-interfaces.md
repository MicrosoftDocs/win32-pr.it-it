---
description: Interfacce API per la firma digitale XPS
ms.assetid: 44244035-f7d5-47f1-b4d8-b895562be855
title: Interfacce API per la firma digitale XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 160fc532ed90cb41e4d0cb524daba87f72edefd8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317270"
---
# <a name="xps-digital-signature-api-interfaces"></a><span data-ttu-id="bf693-103">Interfacce API per la firma digitale XPS</span><span class="sxs-lookup"><span data-stu-id="bf693-103">XPS Digital Signature API Interfaces</span></span>

## <a name="contents"></a><span data-ttu-id="bf693-104">Contenuto</span><span class="sxs-lookup"><span data-stu-id="bf693-104">Contents</span></span>

## <a name="in-this-section"></a><span data-ttu-id="bf693-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="bf693-105">In this section</span></span>



| <span data-ttu-id="bf693-106">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="bf693-106">Interface</span></span>                                                                           | <span data-ttu-id="bf693-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bf693-107">Description</span></span>                                                                                         |
|-------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bf693-108">**IXpsSignature**</span><span class="sxs-lookup"><span data-stu-id="bf693-108">**IXpsSignature**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignature)<br/>                                   | <span data-ttu-id="bf693-109">Rappresenta una singola firma digitale.</span><span class="sxs-lookup"><span data-stu-id="bf693-109">Represents a single digital signature.</span></span><br/>                                                   |
| [<span data-ttu-id="bf693-110">**IXpsSignatureBlock**</span><span class="sxs-lookup"><span data-stu-id="bf693-110">**IXpsSignatureBlock**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock)<br/>                         | <span data-ttu-id="bf693-111">Rappresenta un blocco di richieste di firma archiviate in una parte SignatureDefinitions.</span><span class="sxs-lookup"><span data-stu-id="bf693-111">Represents a block of signature requests that are stored in a SignatureDefinitions part.</span></span><br/> |
| [<span data-ttu-id="bf693-112">**IXpsSignatureBlockCollection**</span><span class="sxs-lookup"><span data-stu-id="bf693-112">**IXpsSignatureBlockCollection**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblockcollection)<br/>     | <span data-ttu-id="bf693-113">Raccolta di interfacce [**IXpsSignatureBlock**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock) .</span><span class="sxs-lookup"><span data-stu-id="bf693-113">A collection of [**IXpsSignatureBlock**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock) interfaces.</span></span><br/>             |
| [<span data-ttu-id="bf693-114">**IXpsSignatureCollection**</span><span class="sxs-lookup"><span data-stu-id="bf693-114">**IXpsSignatureCollection**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturecollection)<br/>               | <span data-ttu-id="bf693-115">Raccolta di puntatori dell'interfaccia [**IXpsSignature**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignature) .</span><span class="sxs-lookup"><span data-stu-id="bf693-115">A collection of [**IXpsSignature**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignature) interface pointers.</span></span><br/>               |
| [<span data-ttu-id="bf693-116">**IXpsSignatureManager**</span><span class="sxs-lookup"><span data-stu-id="bf693-116">**IXpsSignatureManager**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager)<br/>                     | <span data-ttu-id="bf693-117">Gestisce le firme digitali e le richieste di firma digitale di un documento XPS.</span><span class="sxs-lookup"><span data-stu-id="bf693-117">Manages the digital signatures and digital signature requests of an XPS document.</span></span><br/>        |
| [<span data-ttu-id="bf693-118">**IXpsSignatureRequest**</span><span class="sxs-lookup"><span data-stu-id="bf693-118">**IXpsSignatureRequest**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequest)<br/>                     | <span data-ttu-id="bf693-119">Accede ai componenti di una richiesta di firma.</span><span class="sxs-lookup"><span data-stu-id="bf693-119">Accesses the components of a signature request.</span></span><br/>                                          |
| [<span data-ttu-id="bf693-120">**IXpsSignatureRequestCollection**</span><span class="sxs-lookup"><span data-stu-id="bf693-120">**IXpsSignatureRequestCollection**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequestcollection)<br/> | <span data-ttu-id="bf693-121">Raccolta di interfacce [**IXpsSignatureRequest**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequest) .</span><span class="sxs-lookup"><span data-stu-id="bf693-121">A collection of [**IXpsSignatureRequest**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequest) interfaces.</span></span><br/>         |
| [<span data-ttu-id="bf693-122">**IXpsSigningOptions**</span><span class="sxs-lookup"><span data-stu-id="bf693-122">**IXpsSigningOptions**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions)<br/>                         | <span data-ttu-id="bf693-123">Consente di accedere alle singole opzioni di firma utilizzate dalle nuove firme.</span><span class="sxs-lookup"><span data-stu-id="bf693-123">Provides access to the individual signing options that are used by new signatures.</span></span><br/>       |



 

 

 




