---
description: ICE11 viene usato con le installazioni simultanee. Le installazioni simultanee non sono consigliate per l'installazione di applicazioni destinate al rilascio al pubblico. Per informazioni sulle installazioni simultanee, vedere installazioni simultanee.
ms.assetid: fbcc94fa-be94-4ad1-a3f0-ea7d50ee0a15
title: ICE11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d3f85a4dc4d736acfbd4385324aa35565f399bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967793"
---
# <a name="ice11"></a><span data-ttu-id="02705-105">ICE11</span><span class="sxs-lookup"><span data-stu-id="02705-105">ICE11</span></span>

<span data-ttu-id="02705-106">ICE11 viene usato con le installazioni simultanee.</span><span class="sxs-lookup"><span data-stu-id="02705-106">The ICE11 is used with concurrent installations.</span></span> <span data-ttu-id="02705-107">Le installazioni simultanee non sono consigliate per l'installazione di applicazioni destinate al rilascio al pubblico.</span><span class="sxs-lookup"><span data-stu-id="02705-107">Concurrent installations are not recommended for the installation of applications intended for release to the public.</span></span> <span data-ttu-id="02705-108">Per informazioni sulle installazioni simultanee, vedere [installazioni simultanee](concurrent-installations.md).</span><span class="sxs-lookup"><span data-stu-id="02705-108">For information about concurrent installations please see [Concurrent Installations](concurrent-installations.md).</span></span>

## <a name="result"></a><span data-ttu-id="02705-109">Risultato</span><span class="sxs-lookup"><span data-stu-id="02705-109">Result</span></span>

<span data-ttu-id="02705-110">ICE11 convalida la colonna di origine della [tabella CustomAction](customaction-table.md) delle azioni personalizzate di installazione simultanea.</span><span class="sxs-lookup"><span data-stu-id="02705-110">ICE11 validates the Source column of the [CustomAction table](customaction-table.md) of concurrent installation custom actions.</span></span> <span data-ttu-id="02705-111">La colonna di origine deve contenere un [GUID](guid.md) valido (Codice prodotto MSI).</span><span class="sxs-lookup"><span data-stu-id="02705-111">The Source column must contain a valid [GUID](guid.md) (MSI product code).</span></span>

<span data-ttu-id="02705-112">ICE11 Invia un errore se la colonna di origine della tabella CustomAction non è stata creata correttamente per le azioni personalizzate di installazione simultanea.</span><span class="sxs-lookup"><span data-stu-id="02705-112">ICE11 posts an error if the Source column of the CustomAction table is authored incorrectly for concurrent installation custom actions.</span></span>

## <a name="example"></a><span data-ttu-id="02705-113">Esempio</span><span class="sxs-lookup"><span data-stu-id="02705-113">Example</span></span>

<span data-ttu-id="02705-114">ICE inserisce i messaggi di errore seguenti per l'esempio illustrato.</span><span class="sxs-lookup"><span data-stu-id="02705-114">ICE posts the following error messages for the example shown.</span></span>

``` syntax
CustomAction: CA4 is a nested install of an advertised MSI.  The 'Source' must contain a valid MSI product code.  Current: ProductCode.
CustomAction: CA1 is a nested install of an advertised MSI.  It duplicates the ProductCode of the base MSI package.  Current: {BFB69273-F0AE-45C4-9853-0AF946714768}.
CustomAction: CA2 is a nested install of an advertised MSI.  The GUID must be all upper-case.  Current: {BFB69273-F0AE-55c5-9853-0AF946714768}.
```

<span data-ttu-id="02705-115">[Tabella delle proprietà](property-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="02705-115">[Property Table](property-table.md) (partial)</span></span>



| <span data-ttu-id="02705-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="02705-116">Property</span></span>        | <span data-ttu-id="02705-117">Valore</span><span class="sxs-lookup"><span data-stu-id="02705-117">Value</span></span>                                  |
|-----------------|----------------------------------------|
| <span data-ttu-id="02705-118">**ProductCode**</span><span class="sxs-lookup"><span data-stu-id="02705-118">**ProductCode**</span></span> | <span data-ttu-id="02705-119">{BFB69273-F0AE-45C4-9853-0AF946714768}</span><span class="sxs-lookup"><span data-stu-id="02705-119">{BFB69273-F0AE-45C4-9853-0AF946714768}</span></span> |



 

<span data-ttu-id="02705-120">[Tabella CustomAction](customaction-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="02705-120">[CustomAction Table](customaction-table.md) (partial)</span></span>



| <span data-ttu-id="02705-121">CustomAction</span><span class="sxs-lookup"><span data-stu-id="02705-121">CustomAction</span></span> | <span data-ttu-id="02705-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="02705-122">Type</span></span> | <span data-ttu-id="02705-123">Source (Sorgente)</span><span class="sxs-lookup"><span data-stu-id="02705-123">Source</span></span>                                 |
|--------------|------|----------------------------------------|
| <span data-ttu-id="02705-124">CA1</span><span class="sxs-lookup"><span data-stu-id="02705-124">CA1</span></span>          | <span data-ttu-id="02705-125">39</span><span class="sxs-lookup"><span data-stu-id="02705-125">39</span></span>   | <span data-ttu-id="02705-126">{BFB69273-F0AE-45C4-9853-0AF946714768}</span><span class="sxs-lookup"><span data-stu-id="02705-126">{BFB69273-F0AE-45C4-9853-0AF946714768}</span></span> |
| <span data-ttu-id="02705-127">CA2</span><span class="sxs-lookup"><span data-stu-id="02705-127">CA2</span></span>          | <span data-ttu-id="02705-128">39</span><span class="sxs-lookup"><span data-stu-id="02705-128">39</span></span>   | <span data-ttu-id="02705-129">{BFB69273-F0AE-55c5-9853-0AF946714768}</span><span class="sxs-lookup"><span data-stu-id="02705-129">{BFB69273-F0AE-55c5-9853-0AF946714768}</span></span> |
| <span data-ttu-id="02705-130">CA3</span><span class="sxs-lookup"><span data-stu-id="02705-130">CA3</span></span>          | <span data-ttu-id="02705-131">39</span><span class="sxs-lookup"><span data-stu-id="02705-131">39</span></span>   | <span data-ttu-id="02705-132">{BFB69273-F0AE-66C6-9853-0AF946714768}</span><span class="sxs-lookup"><span data-stu-id="02705-132">{BFB69273-F0AE-66C6-9853-0AF946714768}</span></span> |
| <span data-ttu-id="02705-133">CA4</span><span class="sxs-lookup"><span data-stu-id="02705-133">CA4</span></span>          | <span data-ttu-id="02705-134">39</span><span class="sxs-lookup"><span data-stu-id="02705-134">39</span></span>   | <span data-ttu-id="02705-135">ProductCode</span><span class="sxs-lookup"><span data-stu-id="02705-135">ProductCode</span></span>                            |



 

<span data-ttu-id="02705-136">Per correggere gli errori, per CA1 non è possibile eseguire un'installazione simultanea del "pacchetto di base".</span><span class="sxs-lookup"><span data-stu-id="02705-136">To fix the errors, for CA1, you cannot do a concurrent installation of the "base package".</span></span> <span data-ttu-id="02705-137">Ciò comporta un'installazione ricorsiva.</span><span class="sxs-lookup"><span data-stu-id="02705-137">This would result in a recursive installation.</span></span> <span data-ttu-id="02705-138">Questa voce deve essere rimossa o la colonna di origine deve essere modificata in un GUID per un file MSI annunciato che differisce dal GUID del pacchetto di base.</span><span class="sxs-lookup"><span data-stu-id="02705-138">This entry should be removed or the Source column should be changed to a GUID for an advertised MSI that differs from the base package's GUID.</span></span> <span data-ttu-id="02705-139">Per il CA2, fare in modo che tutti i caratteri del GUID siano maiuscoli.</span><span class="sxs-lookup"><span data-stu-id="02705-139">For CA2, make all characters of the GUID uppercase.</span></span> <span data-ttu-id="02705-140">Infine, modificare la colonna di origine CA4's per fare riferimento a un GUID valido di un file MSI annunciato.</span><span class="sxs-lookup"><span data-stu-id="02705-140">Lastly, change CA4's Source column to reference a valid GUID of an advertised MSI.</span></span>

## <a name="related-topics"></a><span data-ttu-id="02705-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="02705-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02705-142">Installazioni simultanee</span><span class="sxs-lookup"><span data-stu-id="02705-142">Concurrent Installations</span></span>](concurrent-installations.md)
</dt> <dt>

[<span data-ttu-id="02705-143">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="02705-143">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



