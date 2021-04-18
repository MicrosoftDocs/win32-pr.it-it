---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: b49e20b7-bd9e-4b8f-bb4a-bb1e99b0c417
title: Creazione di un documento PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ccb1adf4626254ba9f71c706ad7d4556a23aeb6
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320870"
---
# <a name="creating-a-printcapabilities-document"></a><span data-ttu-id="c4646-104">Creazione di un documento PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="c4646-104">Creating a PrintCapabilities Document</span></span>

<span data-ttu-id="c4646-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="c4646-105">This topic is not current.</span></span> <span data-ttu-id="c4646-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="c4646-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c4646-107">Una volta convalidata, un oggetto PrintTicket può essere utilizzato per creare uno snapshot dell'oggetto PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="c4646-107">After a PrintTicket is validated, it can be used to create a snapshot of the PrintCapabilities.</span></span> <span data-ttu-id="c4646-108">Il provider deve avere una rappresentazione interna per qualsiasi proprietà il cui valore dipende dalla configurazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c4646-108">The provider must have an internal representation for any Property whose Value is dependent on the device configuration.</span></span> <span data-ttu-id="c4646-109">Se, ad esempio, SpotDiameter è una proprietà che dipende dalle funzionalità di risoluzione e di MediaType, una rappresentazione interna di SpotDiameter in relazione ai vari valori per la risoluzione e MediaType potrebbe apparire come indicato nella tabella seguente:</span><span class="sxs-lookup"><span data-stu-id="c4646-109">For example, if SpotDiameter is a Property that is dependent on both the Resolution and MediaType Features, an internal representation of SpotDiameter as it relates to the various values for Resolution and MediaType might appear as in the following table:</span></span>



| <span data-ttu-id="c4646-110">Soluzione</span><span class="sxs-lookup"><span data-stu-id="c4646-110">Resolution</span></span>      | <span data-ttu-id="c4646-111">MediaType</span><span class="sxs-lookup"><span data-stu-id="c4646-111">MediaType</span></span>         | <span data-ttu-id="c4646-112">SpotDiameter</span><span class="sxs-lookup"><span data-stu-id="c4646-112">SpotDiameter</span></span>   |
|-----------------|-------------------|----------------|
| <span data-ttu-id="c4646-113">300</span><span class="sxs-lookup"><span data-stu-id="c4646-113">300</span></span><br/>  | <span data-ttu-id="c4646-114">Legame</span><span class="sxs-lookup"><span data-stu-id="c4646-114">Bond</span></span><br/>   | <span data-ttu-id="c4646-115">520</span><span class="sxs-lookup"><span data-stu-id="c4646-115">520</span></span><br/> |
| <span data-ttu-id="c4646-116">300</span><span class="sxs-lookup"><span data-stu-id="c4646-116">300</span></span><br/>  | <span data-ttu-id="c4646-117">Lucido</span><span class="sxs-lookup"><span data-stu-id="c4646-117">Glossy</span></span><br/> | <span data-ttu-id="c4646-118">350</span><span class="sxs-lookup"><span data-stu-id="c4646-118">350</span></span><br/> |
| <span data-ttu-id="c4646-119">600</span><span class="sxs-lookup"><span data-stu-id="c4646-119">600</span></span><br/>  | <span data-ttu-id="c4646-120">Legame</span><span class="sxs-lookup"><span data-stu-id="c4646-120">Bond</span></span><br/>   | <span data-ttu-id="c4646-121">330</span><span class="sxs-lookup"><span data-stu-id="c4646-121">330</span></span><br/> |
| <span data-ttu-id="c4646-122">600</span><span class="sxs-lookup"><span data-stu-id="c4646-122">600</span></span><br/>  | <span data-ttu-id="c4646-123">Lucido</span><span class="sxs-lookup"><span data-stu-id="c4646-123">Glossy</span></span><br/> | <span data-ttu-id="c4646-124">180</span><span class="sxs-lookup"><span data-stu-id="c4646-124">180</span></span><br/> |
| <span data-ttu-id="c4646-125">1200</span><span class="sxs-lookup"><span data-stu-id="c4646-125">1200</span></span><br/> | <span data-ttu-id="c4646-126">Legame</span><span class="sxs-lookup"><span data-stu-id="c4646-126">Bond</span></span><br/>   | <span data-ttu-id="c4646-127">250</span><span class="sxs-lookup"><span data-stu-id="c4646-127">250</span></span><br/> |
| <span data-ttu-id="c4646-128">1200</span><span class="sxs-lookup"><span data-stu-id="c4646-128">1200</span></span><br/> | <span data-ttu-id="c4646-129">Lucido</span><span class="sxs-lookup"><span data-stu-id="c4646-129">Glossy</span></span><br/> | <span data-ttu-id="c4646-130">100</span><span class="sxs-lookup"><span data-stu-id="c4646-130">100</span></span><br/> |



 

<span data-ttu-id="c4646-131">Per questo esempio, il provider PrintCapabilities deve usare l'oggetto PrintTicket fornito per selezionare la voce appropriata della tabella interna e segnalarla come valore per la proprietà SpotDiameter.</span><span class="sxs-lookup"><span data-stu-id="c4646-131">For this example, the PrintCapabilities provider must use the provided PrintTicket to select the proper entry from the internal table and report that as the Value for the SpotDiameter Property.</span></span> <span data-ttu-id="c4646-132">Questo processo viene ripetuto per ogni proprietà multivalore (per ogni proprietà il cui valore dipende dalla configurazione).</span><span class="sxs-lookup"><span data-stu-id="c4646-132">This process is repeated for every multi-valued Property (for every Property whose Value is dependent on the configuration).</span></span> <span data-ttu-id="c4646-133">Nella sezione relativa alla creazione di [schemi e documenti di PrintCapabilities](printcapabilities-schema-and-document-construction.md) vengono descritti gli altri passaggi necessari per la creazione di uno snapshot dell'oggetto PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="c4646-133">The [PrintCapabilities Schema and Document Construction](printcapabilities-schema-and-document-construction.md) section describes the other steps involved in creating a snapshot of the PrintCapabilities.</span></span>

<span data-ttu-id="c4646-134">Per creare uno snapshot del documento PrintCapabilities predefinito, fornire un oggetto PrintTicket predefinito (anziché un oggetto PrintTicket arbitrario) al metodo che crea documenti PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="c4646-134">To create a snapshot of the default PrintCapabilities document, provide a default PrintTicket (rather than an arbitrary PrintTicket) to the method that creates PrintCapabilities documents.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c4646-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c4646-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4646-136">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="c4646-136">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




