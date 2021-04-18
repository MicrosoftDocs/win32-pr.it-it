---
title: Funzioni di NPS Extensions
description: Funzioni di NPS Extensions
ms.assetid: ca217314-00f9-4f9d-a9fe-ed928b3c3b3d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5a20b424b8ef5109cea7f4d00b97f1a545b89ff
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300155"
---
# <a name="nps-extensions-functions"></a><span data-ttu-id="6b7c6-103">Funzioni di NPS Extensions</span><span class="sxs-lookup"><span data-stu-id="6b7c6-103">NPS Extensions Functions</span></span>

> [!Note]  
> <span data-ttu-id="6b7c6-104">Il servizio di autenticazione Internet (IAS) è stato rinominato server dei criteri di rete (NPS) a partire da Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="6b7c6-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="6b7c6-105">Il contenuto di questo argomento si applica sia a IAS che a NPS.</span><span class="sxs-lookup"><span data-stu-id="6b7c6-105">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="6b7c6-106">In tutto il testo, NPS viene utilizzato per fare riferimento a tutte le versioni del servizio, incluse le versioni originariamente indicate come IAS.</span><span class="sxs-lookup"><span data-stu-id="6b7c6-106">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

## <a name="application-defined"></a><span data-ttu-id="6b7c6-107">Applicazione definita</span><span class="sxs-lookup"><span data-stu-id="6b7c6-107">Application Defined</span></span>

<span data-ttu-id="6b7c6-108">L'architettura per le DLL di estensione NPS supporta le funzioni esportate seguenti:</span><span class="sxs-lookup"><span data-stu-id="6b7c6-108">The architecture for NPS Extension DLLs supports the following exported functions:</span></span>

-   [<span data-ttu-id="6b7c6-109">**RadiusExtensionFreeAttributes**</span><span class="sxs-lookup"><span data-stu-id="6b7c6-109">**RadiusExtensionFreeAttributes**</span></span>](/windows/desktop/api/authif/nc-authif-pradius_extension_free_attributes)
-   [<span data-ttu-id="6b7c6-110">**RadiusExtensionInit**</span><span class="sxs-lookup"><span data-stu-id="6b7c6-110">**RadiusExtensionInit**</span></span>](/windows/desktop/api/authif/nc-authif-pradius_extension_init)
-   [<span data-ttu-id="6b7c6-111">**RadiusExtensionProcess**</span><span class="sxs-lookup"><span data-stu-id="6b7c6-111">**RadiusExtensionProcess**</span></span>](/windows/desktop/api/authif/nc-authif-pradius_extension_process)
-   [<span data-ttu-id="6b7c6-112">**RadiusExtensionProcessEx**</span><span class="sxs-lookup"><span data-stu-id="6b7c6-112">**RadiusExtensionProcessEx**</span></span>](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex)
-   [<span data-ttu-id="6b7c6-113">**RadiusExtensionProcess2**</span><span class="sxs-lookup"><span data-stu-id="6b7c6-113">**RadiusExtensionProcess2**</span></span>](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2)
-   [<span data-ttu-id="6b7c6-114">**RadiusExtensionTerm**</span><span class="sxs-lookup"><span data-stu-id="6b7c6-114">**RadiusExtensionTerm**</span></span>](/windows/desktop/api/authif/nc-authif-pradius_extension_term)

<span data-ttu-id="6b7c6-115">Le funzioni [**RadiusExtensionInit**](/windows/desktop/api/authif/nc-authif-pradius_extension_init) e [**RadiusExtensionTerm**](/windows/desktop/api/authif/nc-authif-pradius_extension_term) sono facoltative.</span><span class="sxs-lookup"><span data-stu-id="6b7c6-115">The [**RadiusExtensionInit**](/windows/desktop/api/authif/nc-authif-pradius_extension_init) and [**RadiusExtensionTerm**](/windows/desktop/api/authif/nc-authif-pradius_extension_term) functions are optional.</span></span>

<span data-ttu-id="6b7c6-116">La DLL di estensione può esportare [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2) invece di [**RadiusExtensionProcess**](/windows/desktop/api/authif/nc-authif-pradius_extension_process) o [**RadiusExtensionProcessEx**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex).</span><span class="sxs-lookup"><span data-stu-id="6b7c6-116">The Extension DLL may export [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2) instead of [**RadiusExtensionProcess**](/windows/desktop/api/authif/nc-authif-pradius_extension_process) or [**RadiusExtensionProcessEx**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex).</span></span>

<span data-ttu-id="6b7c6-117">Se la DLL di estensione Esporta [**RadiusExtensionProcessEx**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex), è necessario esportare anche [**RadiusExtensionFreeAttributes**](/windows/desktop/api/authif/nc-authif-pradius_extension_free_attributes).</span><span class="sxs-lookup"><span data-stu-id="6b7c6-117">If the Extension DLL exports [**RadiusExtensionProcessEx**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex), then it must also export [**RadiusExtensionFreeAttributes**](/windows/desktop/api/authif/nc-authif-pradius_extension_free_attributes).</span></span>

## <a name="system-defined"></a><span data-ttu-id="6b7c6-118">Definito dal sistema</span><span class="sxs-lookup"><span data-stu-id="6b7c6-118">System Defined</span></span>

<span data-ttu-id="6b7c6-119">Quando NPS chiama un'implementazione di [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2), NPS passa la funzione un puntatore a una struttura del [**\_ blocco di \_ controllo \_ dell'estensione RADIUS**](/windows/desktop/api/authif/ns-authif-radius_extension_control_block) .</span><span class="sxs-lookup"><span data-stu-id="6b7c6-119">When NPS calls an implementation of [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2), NPS passes the function a pointer to a [**RADIUS\_EXTENSION\_CONTROL\_BLOCK**](/windows/desktop/api/authif/ns-authif-radius_extension_control_block) structure.</span></span>

<span data-ttu-id="6b7c6-120">La struttura del [**\_ blocco di \_ controllo \_ dell'estensione RADIUS**](/windows/desktop/api/authif/ns-authif-radius_extension_control_block) contiene i puntatori a funzione delle funzioni seguenti fornite da NPS:</span><span class="sxs-lookup"><span data-stu-id="6b7c6-120">The [**RADIUS\_EXTENSION\_CONTROL\_BLOCK**](/windows/desktop/api/authif/ns-authif-radius_extension_control_block) structure contains function pointers to the following functions provided by NPS:</span></span>

-   <span data-ttu-id="6b7c6-121">[**GetRequest**](/previous-versions/ms688263(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6b7c6-121">[**GetRequest**](/previous-versions/ms688263(v=vs.85))</span></span>
-   <span data-ttu-id="6b7c6-122">[**GetResponse**](/previous-versions/ms688270(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6b7c6-122">[**GetResponse**](/previous-versions/ms688270(v=vs.85))</span></span>
-   <span data-ttu-id="6b7c6-123">[**SetResponseType**](/previous-versions/ms688462(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6b7c6-123">[**SetResponseType**](/previous-versions/ms688462(v=vs.85))</span></span>

<span data-ttu-id="6b7c6-124">Le funzioni [**GetRequest**](/previous-versions/ms688263(v=vs.85)) e [**GetResponse**](/previous-versions/ms688270(v=vs.85)) restituiscono puntatori a una struttura di tipo [**RADIUS \_ Attribute \_ Array**](/windows/desktop/api/authif/ns-authif-radius_attribute_array).</span><span class="sxs-lookup"><span data-stu-id="6b7c6-124">The functions [**GetRequest**](/previous-versions/ms688263(v=vs.85)) and [**GetResponse**](/previous-versions/ms688270(v=vs.85)) return pointers to a structure of type [**RADIUS\_ATTRIBUTE\_ARRAY**](/windows/desktop/api/authif/ns-authif-radius_attribute_array).</span></span>

<span data-ttu-id="6b7c6-125">La struttura della [**\_ \_ matrice di attributi RADIUS**](/windows/desktop/api/authif/ns-authif-radius_attribute_array) contiene i puntatori a funzione delle funzioni seguenti fornite da NPS:</span><span class="sxs-lookup"><span data-stu-id="6b7c6-125">The [**RADIUS\_ATTRIBUTE\_ARRAY**](/windows/desktop/api/authif/ns-authif-radius_attribute_array) structure contains function pointers to the following functions provided by NPS:</span></span>

-   <span data-ttu-id="6b7c6-126">[**Aggiungere**](/previous-versions/ms688246(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6b7c6-126">[**Add**](/previous-versions/ms688246(v=vs.85))</span></span>
-   <span data-ttu-id="6b7c6-127">[**AttributeAt**](/previous-versions/ms688253(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6b7c6-127">[**AttributeAt**](/previous-versions/ms688253(v=vs.85))</span></span>
-   <span data-ttu-id="6b7c6-128">[**GetSize**](/previous-versions/ms688277(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6b7c6-128">[**GetSize**](/previous-versions/ms688277(v=vs.85))</span></span>
-   <span data-ttu-id="6b7c6-129">[**InsertAt**](/previous-versions/ms688296(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6b7c6-129">[**InsertAt**](/previous-versions/ms688296(v=vs.85))</span></span>
-   <span data-ttu-id="6b7c6-130">[**RemoveAt**](/previous-versions/ms688452(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6b7c6-130">[**RemoveAt**](/previous-versions/ms688452(v=vs.85))</span></span>
-   <span data-ttu-id="6b7c6-131">[**SetAt**](/previous-versions/ms688456(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6b7c6-131">[**SetAt**](/previous-versions/ms688456(v=vs.85))</span></span>

 

 