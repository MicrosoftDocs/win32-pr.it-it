---
description: ELS supporta le funzioni definite nella tabella seguente.
ms.assetid: d62ab664-a75a-4d06-aefb-a3311ea7d4a7
title: Funzioni di servizi linguistici estesi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a5b8acff7601955f8ed6e37f430caa0a52aa880
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313833"
---
# <a name="extended-linguistic-services-functions"></a><span data-ttu-id="79a66-103">Funzioni di servizi linguistici estesi</span><span class="sxs-lookup"><span data-stu-id="79a66-103">Extended Linguistic Services Functions</span></span>

<span data-ttu-id="79a66-104">ELS supporta le funzioni definite nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="79a66-104">ELS supports the functions defined in the following table.</span></span>



| <span data-ttu-id="79a66-105">Funzione</span><span class="sxs-lookup"><span data-stu-id="79a66-105">Function</span></span>                                                 | <span data-ttu-id="79a66-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="79a66-106">Description</span></span>                                                                                                                                    |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="79a66-107">**MappingCallbackProc**</span><span class="sxs-lookup"><span data-stu-id="79a66-107">**MappingCallbackProc**</span></span>](/windows/desktop/api/Elscore/nc-elscore-pfn_mappingcallbackproc)       | <span data-ttu-id="79a66-108">Funzione di callback definita dall'applicazione che elabora in modo asincrono i dati prodotti dalla funzione **MappingRecognizeText** .</span><span class="sxs-lookup"><span data-stu-id="79a66-108">An application-defined callback function that asynchronously processes data produced by the **MappingRecognizeText** function.</span></span>                 |
| [<span data-ttu-id="79a66-109">**MappingDoAction**</span><span class="sxs-lookup"><span data-stu-id="79a66-109">**MappingDoAction**</span></span>](/windows/desktop/api/Elscore/nf-elscore-mappingdoaction)               | <span data-ttu-id="79a66-110">Consente a un servizio ELS di eseguire un'azione dopo il riconoscimento del testo.</span><span class="sxs-lookup"><span data-stu-id="79a66-110">Causes an ELS service to perform an action after text recognition has occurred.</span></span>                                                                |
| [<span data-ttu-id="79a66-111">**MappingFreePropertyBag**</span><span class="sxs-lookup"><span data-stu-id="79a66-111">**MappingFreePropertyBag**</span></span>](/windows/desktop/api/Elscore/nf-elscore-mappingfreepropertybag) | <span data-ttu-id="79a66-112">Libera memoria e risorse allocate durante un'operazione di riconoscimento del testo ELS.</span><span class="sxs-lookup"><span data-stu-id="79a66-112">Frees memory and resources allocated during an ELS text recognition operation.</span></span>                                                                 |
| [<span data-ttu-id="79a66-113">**MappingFreeServices**</span><span class="sxs-lookup"><span data-stu-id="79a66-113">**MappingFreeServices**</span></span>](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices)       | <span data-ttu-id="79a66-114">Libera la memoria e le risorse allocate per l'applicazione per interagire con uno o più servizi ELS.</span><span class="sxs-lookup"><span data-stu-id="79a66-114">Frees memory and resources allocated for the application to interact with one or more ELS services.</span></span>                                            |
| [<span data-ttu-id="79a66-115">**MappingGetServices**</span><span class="sxs-lookup"><span data-stu-id="79a66-115">**MappingGetServices**</span></span>](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices)         | <span data-ttu-id="79a66-116">Recupera un elenco di servizi di supporto della piattaforma ELS disponibili, insieme alle informazioni associate, in base ai criteri specificati dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="79a66-116">Retrieves a list of available ELS platform-supported services, along with associated information, according to application-specified criteria.</span></span> |
| [<span data-ttu-id="79a66-117">**MappingRecognizeText**</span><span class="sxs-lookup"><span data-stu-id="79a66-117">**MappingRecognizeText**</span></span>](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext)     | <span data-ttu-id="79a66-118">Chiama un servizio ELS per riconoscere il testo.</span><span class="sxs-lookup"><span data-stu-id="79a66-118">Calls upon an ELS service to recognize text.</span></span>                                                                                                   |



 

 

 



