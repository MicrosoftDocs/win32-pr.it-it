---
description: Un profilo 802.1 X contiene i seguenti elementi dello schema.
ms.assetid: be3f1986-d0c2-47f6-b4dd-8defb89bd03a
title: Elementi dello schema OneX
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7b7f3e7bac256b915d0e134720fc63b3519b21e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756458"
---
# <a name="onex-schema-elements"></a><span data-ttu-id="ff10f-103">Elementi dello schema OneX</span><span class="sxs-lookup"><span data-stu-id="ff10f-103">OneX Schema Elements</span></span>

<span data-ttu-id="ff10f-104">Un profilo 802.1 X contiene i seguenti elementi dello schema.</span><span class="sxs-lookup"><span data-stu-id="ff10f-104">An 802.1X profile contains the following schema elements.</span></span> <span data-ttu-id="ff10f-105">Tutti gli elementi dello schema OneX si applicano ai profili cablati e wireless.</span><span class="sxs-lookup"><span data-stu-id="ff10f-105">All OneX schema elements apply to both wired and wireless profiles.</span></span> <span data-ttu-id="ff10f-106">La maggior parte degli elementi denominati si trova nello spazio dei nomi `https://www.microsoft.com/networking/OneX/v1` , ad eccezione di [**EAPConfig (Onex)**](onexschema-eapconfig-onex-element.md) , che si trova nello spazio dei nomi `https://www.microsoft.com/provisioning/EapHostConfig` .</span><span class="sxs-lookup"><span data-stu-id="ff10f-106">Most of the named elements are in the namespace `https://www.microsoft.com/networking/OneX/v1`, except for [**EAPConfig (OneX)**](onexschema-eapconfig-onex-element.md) which is in the namespace `https://www.microsoft.com/provisioning/EapHostConfig`.</span></span>

<span data-ttu-id="ff10f-107">Nell'elenco seguente vengono illustrati gli elementi definiti nell'ordine in cui gli elementi vengono visualizzati in un profilo.</span><span class="sxs-lookup"><span data-stu-id="ff10f-107">The following list shows the defined elements in the order in which the elements appear in a profile.</span></span> <span data-ttu-id="ff10f-108">Viene applicato l'ordinamento degli elementi.</span><span class="sxs-lookup"><span data-stu-id="ff10f-108">The ordering of elements is enforced.</span></span> <span data-ttu-id="ff10f-109">Non tutti gli elementi sono in tutti i profili, perché alcuni elementi sono facoltativi.</span><span class="sxs-lookup"><span data-stu-id="ff10f-109">Not all elements are in every profile, as some elements are optional.</span></span>

<span data-ttu-id="ff10f-110">Questo elenco non Mostra tutti i possibili elementi che possono essere visualizzati in un profilo, perché è possibile aggiungere elementi in **xs: qualsiasi** punto di inserimento.</span><span class="sxs-lookup"><span data-stu-id="ff10f-110">This list does not show all possible elements that can appear in a profile, as elements can be added in **xs:any** insertion points.</span></span>

-   [<span data-ttu-id="ff10f-111">**OneX**</span><span class="sxs-lookup"><span data-stu-id="ff10f-111">**OneX**</span></span>](onexschema-onex-element.md)
    -   [<span data-ttu-id="ff10f-112">**cacheUserData (OneX)**</span><span class="sxs-lookup"><span data-stu-id="ff10f-112">**cacheUserData (OneX)**</span></span>](onexschema-cacheuserdata-onex-element.md)
    -   [<span data-ttu-id="ff10f-113">**heldPeriod (OneX)**</span><span class="sxs-lookup"><span data-stu-id="ff10f-113">**heldPeriod (OneX)**</span></span>](onexschema-heldperiod-onex-element.md)
    -   [<span data-ttu-id="ff10f-114">**authPeriod (OneX)**</span><span class="sxs-lookup"><span data-stu-id="ff10f-114">**authPeriod (OneX)**</span></span>](onexschema-authperiod-onex-element.md)
    -   [<span data-ttu-id="ff10f-115">**startPeriod (OneX)**</span><span class="sxs-lookup"><span data-stu-id="ff10f-115">**startPeriod (OneX)**</span></span>](onexschema-startperiod-onex-element.md)
    -   [<span data-ttu-id="ff10f-116">**maxStart (OneX)**</span><span class="sxs-lookup"><span data-stu-id="ff10f-116">**maxStart (OneX)**</span></span>](onexschema-maxstart-onex-element.md)
    -   [<span data-ttu-id="ff10f-117">**maxAuthFailures (OneX)**</span><span class="sxs-lookup"><span data-stu-id="ff10f-117">**maxAuthFailures (OneX)**</span></span>](onexschema-maxauthfailures-onex-element.md)
    -   [<span data-ttu-id="ff10f-118">**supplicantMode (OneX)**</span><span class="sxs-lookup"><span data-stu-id="ff10f-118">**supplicantMode (OneX)**</span></span>](onexschema-supplicantmode-onex-element.md)
    -   [<span data-ttu-id="ff10f-119">**authMode (OneX)**</span><span class="sxs-lookup"><span data-stu-id="ff10f-119">**authMode (OneX)**</span></span>](onexschema-authmode-onex-element.md)
    -   [<span data-ttu-id="ff10f-120">**singleSignOn (OneX)**</span><span class="sxs-lookup"><span data-stu-id="ff10f-120">**singleSignOn (OneX)**</span></span>](onexschema-singlesignon-onex-element.md)
        -   [<span data-ttu-id="ff10f-121">**tipo (singleSignOn)**</span><span class="sxs-lookup"><span data-stu-id="ff10f-121">**type (singleSignOn)**</span></span>](onexschema-type-singlesignon-element.md)
        -   [<span data-ttu-id="ff10f-122">**maxDelay (singleSignOn)**</span><span class="sxs-lookup"><span data-stu-id="ff10f-122">**maxDelay (singleSignOn)**</span></span>](onexschema-maxdelay-singlesignon-element.md)
        -   [<span data-ttu-id="ff10f-123">**userBasedVirtualLan (singleSignOn)**</span><span class="sxs-lookup"><span data-stu-id="ff10f-123">**userBasedVirtualLan (singleSignOn)**</span></span>](onexschema-userbasedvirtuallan-singlesignon-element.md)
    -   [<span data-ttu-id="ff10f-124">**EAPConfig (OneX)**</span><span class="sxs-lookup"><span data-stu-id="ff10f-124">**EAPConfig (OneX)**</span></span>](onexschema-eapconfig-onex-element.md)

 

 



