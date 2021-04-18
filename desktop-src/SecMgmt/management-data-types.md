---
description: Elenca i tipi di dati utilizzati dalle DLL allegati alla configurazione di sicurezza e dalle relative funzioni di supporto.
ms.assetid: 1d3bdf0d-320c-4b25-9e9b-fda134876979
title: Tipi di dati di gestione della sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae7efedb32ab545b903c61819042e32b7d83dbf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312767"
---
# <a name="security-management-data-types"></a><span data-ttu-id="fa683-103">Tipi di dati di gestione della sicurezza</span><span class="sxs-lookup"><span data-stu-id="fa683-103">Security Management Data Types</span></span>

<span data-ttu-id="fa683-104">I tipi di dati di gestione della sicurezza includono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="fa683-104">The security management data types include the following:</span></span>

-   [<span data-ttu-id="fa683-105">Tipi di dati allegati</span><span class="sxs-lookup"><span data-stu-id="fa683-105">Attachment Data Types</span></span>](#attachment-data-types)
-   [<span data-ttu-id="fa683-106">Tipi di dati dei criteri LSA</span><span class="sxs-lookup"><span data-stu-id="fa683-106">LSA Policy Data Types</span></span>](#lsa-policy-data-types)

## <a name="attachment-data-types"></a><span data-ttu-id="fa683-107">Tipi di dati allegati</span><span class="sxs-lookup"><span data-stu-id="fa683-107">Attachment Data Types</span></span>

<span data-ttu-id="fa683-108">I tipi di dati seguenti vengono utilizzati dalle DLL degli allegati di configurazione di sicurezza e dalle relative funzioni di supporto.</span><span class="sxs-lookup"><span data-stu-id="fa683-108">The following data types are used by the Security Configuration attachment DLLs and their supporting functions.</span></span>



| <span data-ttu-id="fa683-109">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="fa683-109">Data type</span></span>                                                    | <span data-ttu-id="fa683-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fa683-110">Description</span></span>                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fa683-111">**\_contesto di enumerazione SCE \_**</span><span class="sxs-lookup"><span data-stu-id="fa683-111">**SCE\_ENUMERATION\_CONTEXT**</span></span>](sce-enumeration-context.md) | <span data-ttu-id="fa683-112">Usato dalla funzione [**\_ \_ informazioni query PFSCE**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) per spostarsi nel database di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="fa683-112">Used by the [**PFSCE\_QUERY\_INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) function to navigate through the security database.</span></span>                                                                                                                                              |
| [<span data-ttu-id="fa683-113">**\_handle SCE**</span><span class="sxs-lookup"><span data-stu-id="fa683-113">**SCE\_HANDLE**</span></span>](sce-handle.md)                            | <span data-ttu-id="fa683-114">Usato dalle informazioni sulla [**\_ query PFSCE \_**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) e da [**PFSCE \_ set \_ info**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info) per passare le informazioni tra l'allegato e il database di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="fa683-114">Used by [**PFSCE\_QUERY\_INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) and [**PFSCE\_SET\_INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info) to pass information between the attachment and the security database.</span></span>                                                                                 |
| [<span data-ttu-id="fa683-115">**SCESTATUS**</span><span class="sxs-lookup"><span data-stu-id="fa683-115">**SCESTATUS**</span></span>](scestatus.md)                               | <span data-ttu-id="fa683-116">Il tipo di dati viene usato dall'API del set di strumenti di configurazione della sicurezza per restituire informazioni sui risultati di una chiamata di funzione.</span><span class="sxs-lookup"><span data-stu-id="fa683-116">Data type is used by the Security Configuration tool set API to return information about the results of a function call.</span></span>                                                                                                                                    |
| [<span data-ttu-id="fa683-117">**\_handle SCESVC**</span><span class="sxs-lookup"><span data-stu-id="fa683-117">**SCESVC\_HANDLE**</span></span>](scesvc-handle.md)                      | <span data-ttu-id="fa683-118">Utilizzato dai metodi delle interfacce [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata) e [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) per passare informazioni tra lo snap-in configurazione di sicurezza e l'estensione dello snap-in.</span><span class="sxs-lookup"><span data-stu-id="fa683-118">Used by methods of the [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata) and [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) interfaces to pass information between the Security Configuration snap-in and the snap-in extension.</span></span> |
| [<span data-ttu-id="fa683-119">**\_tipo di informazioni SCESVC \_**</span><span class="sxs-lookup"><span data-stu-id="fa683-119">**SCESVC\_INFO\_TYPE**</span></span>](/windows/desktop/api/Scesvc/ne-scesvc-scesvc_info_type)               | <span data-ttu-id="fa683-120">L'enumerazione viene utilizzata [**dalle \_ \_ informazioni di query PFSCE**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) e [**PFSCE \_ set \_ info**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info) per indicare il tipo di informazioni richieste da o passate al database di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="fa683-120">Enumeration is used by [**PFSCE\_QUERY\_INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) and [**PFSCE\_SET\_INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info) to indicate the type of information requested from or passed to the security database.</span></span>                                                 |



 

## <a name="lsa-policy-data-types"></a><span data-ttu-id="fa683-121">Tipi di dati dei criteri LSA</span><span class="sxs-lookup"><span data-stu-id="fa683-121">LSA Policy Data Types</span></span>

<span data-ttu-id="fa683-122">I tipi di dati seguenti vengono utilizzati dalle funzioni di gestione dei criteri LSA.</span><span class="sxs-lookup"><span data-stu-id="fa683-122">The following data types are used by the LSA policy management functions.</span></span>



| <span data-ttu-id="fa683-123">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="fa683-123">Data type</span></span>                                                  | <span data-ttu-id="fa683-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fa683-124">Description</span></span>                                                               |
|------------------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="fa683-125">**\_handle di enumerazione LSA \_**</span><span class="sxs-lookup"><span data-stu-id="fa683-125">**LSA\_ENUMERATION\_HANDLE**</span></span>](lsa-enumeration-handle.md) | <span data-ttu-id="fa683-126">Utilizzato per tenere traccia delle enumerazioni in cui sono richieste più chiamate di funzione.</span><span class="sxs-lookup"><span data-stu-id="fa683-126">Used to track enumerations in which multiple function calls are required.</span></span> |
| [<span data-ttu-id="fa683-127">**\_handle LSA**</span><span class="sxs-lookup"><span data-stu-id="fa683-127">**LSA\_HANDLE**</span></span>](lsa-handle.md)                          | <span data-ttu-id="fa683-128">Handle per un oggetto [**criteri**](policy-object.md) .</span><span class="sxs-lookup"><span data-stu-id="fa683-128">Handle to a [**Policy**](policy-object.md) object.</span></span>                       |



 

 

 
