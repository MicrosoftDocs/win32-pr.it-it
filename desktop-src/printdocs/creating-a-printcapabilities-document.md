---
description: Dopo la convalida, un PrintTicket può essere usato per creare uno snapshot di PrintCapabilities.
ms.assetid: b49e20b7-bd9e-4b8f-bb4a-bb1e99b0c417
title: Creazione di un documento PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b96ea51cef9dfd0f351704b3b71a7f6163737736
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409514"
---
# <a name="creating-a-printcapabilities-document"></a><span data-ttu-id="07b44-103">Creazione di un documento PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="07b44-103">Creating a PrintCapabilities Document</span></span>

<span data-ttu-id="07b44-104">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="07b44-104">This topic is not current.</span></span> <span data-ttu-id="07b44-105">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="07b44-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="07b44-106">Dopo la convalida, un PrintTicket può essere usato per creare uno snapshot di PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="07b44-106">After a PrintTicket is validated, it can be used to create a snapshot of the PrintCapabilities.</span></span> <span data-ttu-id="07b44-107">Il provider deve avere una rappresentazione interna per qualsiasi property il cui valore dipende dalla configurazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="07b44-107">The provider must have an internal representation for any Property whose Value is dependent on the device configuration.</span></span> <span data-ttu-id="07b44-108">Ad esempio, se SpotDiameter è una proprietà dipendente dalle funzionalità Resolution e MediaType, una rappresentazione interna di SpotDiameter in relazione ai vari valori per Resolution e MediaType potrebbe essere visualizzata come nella tabella seguente:</span><span class="sxs-lookup"><span data-stu-id="07b44-108">For example, if SpotDiameter is a Property that is dependent on both the Resolution and MediaType Features, an internal representation of SpotDiameter as it relates to the various values for Resolution and MediaType might appear as in the following table:</span></span>



| <span data-ttu-id="07b44-109">Soluzione</span><span class="sxs-lookup"><span data-stu-id="07b44-109">Resolution</span></span>      | <span data-ttu-id="07b44-110">MediaType</span><span class="sxs-lookup"><span data-stu-id="07b44-110">MediaType</span></span>         | <span data-ttu-id="07b44-111">SpotDiameter</span><span class="sxs-lookup"><span data-stu-id="07b44-111">SpotDiameter</span></span>   |
|-----------------|-------------------|----------------|
| <span data-ttu-id="07b44-112">300</span><span class="sxs-lookup"><span data-stu-id="07b44-112">300</span></span><br/>  | <span data-ttu-id="07b44-113">Legame</span><span class="sxs-lookup"><span data-stu-id="07b44-113">Bond</span></span><br/>   | <span data-ttu-id="07b44-114">520</span><span class="sxs-lookup"><span data-stu-id="07b44-114">520</span></span><br/> |
| <span data-ttu-id="07b44-115">300</span><span class="sxs-lookup"><span data-stu-id="07b44-115">300</span></span><br/>  | <span data-ttu-id="07b44-116">Lucido</span><span class="sxs-lookup"><span data-stu-id="07b44-116">Glossy</span></span><br/> | <span data-ttu-id="07b44-117">350</span><span class="sxs-lookup"><span data-stu-id="07b44-117">350</span></span><br/> |
| <span data-ttu-id="07b44-118">600</span><span class="sxs-lookup"><span data-stu-id="07b44-118">600</span></span><br/>  | <span data-ttu-id="07b44-119">Legame</span><span class="sxs-lookup"><span data-stu-id="07b44-119">Bond</span></span><br/>   | <span data-ttu-id="07b44-120">330</span><span class="sxs-lookup"><span data-stu-id="07b44-120">330</span></span><br/> |
| <span data-ttu-id="07b44-121">600</span><span class="sxs-lookup"><span data-stu-id="07b44-121">600</span></span><br/>  | <span data-ttu-id="07b44-122">Lucido</span><span class="sxs-lookup"><span data-stu-id="07b44-122">Glossy</span></span><br/> | <span data-ttu-id="07b44-123">180</span><span class="sxs-lookup"><span data-stu-id="07b44-123">180</span></span><br/> |
| <span data-ttu-id="07b44-124">1200</span><span class="sxs-lookup"><span data-stu-id="07b44-124">1200</span></span><br/> | <span data-ttu-id="07b44-125">Legame</span><span class="sxs-lookup"><span data-stu-id="07b44-125">Bond</span></span><br/>   | <span data-ttu-id="07b44-126">250</span><span class="sxs-lookup"><span data-stu-id="07b44-126">250</span></span><br/> |
| <span data-ttu-id="07b44-127">1200</span><span class="sxs-lookup"><span data-stu-id="07b44-127">1200</span></span><br/> | <span data-ttu-id="07b44-128">Lucido</span><span class="sxs-lookup"><span data-stu-id="07b44-128">Glossy</span></span><br/> | <span data-ttu-id="07b44-129">100</span><span class="sxs-lookup"><span data-stu-id="07b44-129">100</span></span><br/> |



 

<span data-ttu-id="07b44-130">Per questo esempio, il provider PrintCapabilities deve usare il PrintTicket fornito per selezionare la voce appropriata dalla tabella interna e segnalare tale voce come Valore per la proprietà SpotDiameter.</span><span class="sxs-lookup"><span data-stu-id="07b44-130">For this example, the PrintCapabilities provider must use the provided PrintTicket to select the proper entry from the internal table and report that as the Value for the SpotDiameter Property.</span></span> <span data-ttu-id="07b44-131">Questo processo viene ripetuto per ogni proprietà multivalore (per ogni proprietà il cui valore dipende dalla configurazione).</span><span class="sxs-lookup"><span data-stu-id="07b44-131">This process is repeated for every multi-valued Property (for every Property whose Value is dependent on the configuration).</span></span> <span data-ttu-id="07b44-132">La [sezione Schema PrintCapabilities e Costruzione di](printcapabilities-schema-and-document-construction.md) documenti descrive gli altri passaggi necessari per creare uno snapshot di PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="07b44-132">The [PrintCapabilities Schema and Document Construction](printcapabilities-schema-and-document-construction.md) section describes the other steps involved in creating a snapshot of the PrintCapabilities.</span></span>

<span data-ttu-id="07b44-133">Per creare uno snapshot del documento PrintCapabilities predefinito, fornire un PrintTicket predefinito (anziché un PrintTicket arbitrario) al metodo che crea documenti PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="07b44-133">To create a snapshot of the default PrintCapabilities document, provide a default PrintTicket (rather than an arbitrary PrintTicket) to the method that creates PrintCapabilities documents.</span></span>

## <a name="related-topics"></a><span data-ttu-id="07b44-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="07b44-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07b44-135">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="07b44-135">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




