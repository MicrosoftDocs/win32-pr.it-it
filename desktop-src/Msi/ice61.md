---
description: ICE61 convalida la tabella di aggiornamento di un database di Windows Installer.
ms.assetid: 9f6834c6-74eb-4219-8111-7b722ea41a3a
title: ICE61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89f5a685d5b0a4f2bd5ce8dac70a738cbe2e0b9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314792"
---
# <a name="ice61"></a><span data-ttu-id="81692-103">ICE61</span><span class="sxs-lookup"><span data-stu-id="81692-103">ICE61</span></span>

<span data-ttu-id="81692-104">ICE61 controlla la tabella di aggiornamento per verificare che siano soddisfatte le condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="81692-104">ICE61 checks the upgrade table to ensure that the following conditions are true:</span></span>

-   <span data-ttu-id="81692-105">Tutte le proprietà di ActionProperty non sono già state create nella tabella delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="81692-105">All ActionProperty properties are not pre-authored in the Property table.</span></span>
-   <span data-ttu-id="81692-106">Tutte le proprietà di ActionProperty sono proprietà pubbliche.</span><span class="sxs-lookup"><span data-stu-id="81692-106">All ActionProperty properties are Public Properties.</span></span>
-   <span data-ttu-id="81692-107">Tutte le proprietà di ActionProperty sono incluse nella proprietà [**SecureCustomProperties**](securecustomproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="81692-107">All ActionProperty properties are included in the [**SecureCustomProperties**](securecustomproperties.md) property.</span></span>
-   <span data-ttu-id="81692-108">Tutte le proprietà di ActionProperty sono univoche per ogni record della tabella di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="81692-108">All ActionProperty properties are unique to each record in the Upgrade table.</span></span>
-   <span data-ttu-id="81692-109">Tutti i valori di VersionMax non sono minori dei valori VersionMin corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="81692-109">All VersionMax values are not less than the corresponding VersionMin values.</span></span>
-   <span data-ttu-id="81692-110">I valori VersionMin e VersionMax sono versioni di prodotti valide.</span><span class="sxs-lookup"><span data-stu-id="81692-110">VersionMin and VersionMax values are valid product versions.</span></span> <span data-ttu-id="81692-111">Per il formato della versione del prodotto valido, vedere la proprietà [**ProductVersion**](productversion.md) .</span><span class="sxs-lookup"><span data-stu-id="81692-111">See the [**ProductVersion**](productversion.md) property for the valid product version format.</span></span>
-   <span data-ttu-id="81692-112">Non viene effettuato alcun tentativo di rimuovere una versione più recente o uguale del prodotto corrente.</span><span class="sxs-lookup"><span data-stu-id="81692-112">No attempt is made to remove a newer or equal version of the current product.</span></span>

<span data-ttu-id="81692-113">La mancata correzione di un avviso o di un errore segnalato da ICE61 in genere comporta problemi nell'aggiornamento dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="81692-113">Failure to fix a warning or error reported by ICE61 generally leads to problems in upgrading your application.</span></span> <span data-ttu-id="81692-114">A seconda dell'errore esatto, potrebbe essere necessario lasciare i file dalla versione precedente, eliminare i file dalla versione precedente anche se sono necessari per la nuova applicazione o completare l'errore dell'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="81692-114">Depending on the exact error, this could be anything from leaving files from the older version behind, deleting files from the older version even though they are needed by the new application, or complete failure of the upgrade.</span></span>

## <a name="result"></a><span data-ttu-id="81692-115">Risultato</span><span class="sxs-lookup"><span data-stu-id="81692-115">Result</span></span>

<span data-ttu-id="81692-116">ICE61 Invia un avviso o un errore se una qualsiasi delle condizioni precedenti non è vera.</span><span class="sxs-lookup"><span data-stu-id="81692-116">ICE61 posts a warning or error if any of the above conditions are not true.</span></span>

## <a name="example"></a><span data-ttu-id="81692-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="81692-117">Example</span></span>

<span data-ttu-id="81692-118">ICE61 segnala gli errori e gli avvisi seguenti per gli esempi mostrati.</span><span class="sxs-lookup"><span data-stu-id="81692-118">ICE61 reports the following errors and warning for the examples shown.</span></span>

``` syntax
This product should remove only older versions of itself. The Maximum version is not less than the current product. (2.01.0000 2.01.0000)
```

<span data-ttu-id="81692-119">In questo caso, la prima riga tenterà di rimuovere un prodotto della stessa versione.</span><span class="sxs-lookup"><span data-stu-id="81692-119">In this case, the first row would try to remove a product of the same version.</span></span> <span data-ttu-id="81692-120">La colonna VersionMax è uguale alla versione del prodotto nella tabella delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="81692-120">(VersionMax column is equal to the product version in the Property table).</span></span>

<span data-ttu-id="81692-121">Per correggere l'errore, utilizzare una versione nella colonna VersionMax inferiore alla versione corrente specificata nella tabella delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="81692-121">To fix this error, use a version in the VersionMax column lower than the current version specified in the Property table.</span></span> <span data-ttu-id="81692-122">Rimuovere il bit **msidbUpgradeAttributesVersionMaxInclusive** dalla colonna Attributes se VersionMax è uguale alla versione corrente.</span><span class="sxs-lookup"><span data-stu-id="81692-122">Remove the **msidbUpgradeAttributesVersionMaxInclusive** bit from the Attributes column if the VersionMax is equal to the current version.</span></span> <span data-ttu-id="81692-123">Se lo scopo è quello di rilevare il prodotto e non rimuoverlo, l'errore verrà risolto anche aggiungendo il bit **msidbUpgradeAttributesOnlyDetect** alla colonna Attributes.</span><span class="sxs-lookup"><span data-stu-id="81692-123">If the intent is only to detect the product and not remove it, adding the **msidbUpgradeAttributesOnlyDetect** bit to the Attributes column will also fix this error.</span></span>

``` syntax
Upgrade.ActionProperty EnglishAPPFOUND must be added to the SecureCustomProperties property.
```

<span data-ttu-id="81692-124">A meno che la proprietà non sia elencata nella proprietà [**SecureCustomProperties**](securecustomproperties.md) , la proprietà non viene passata al lato server dell'installazione quando viene trovata la proprietà.</span><span class="sxs-lookup"><span data-stu-id="81692-124">Unless the property is listed in the [**SecureCustomProperties**](securecustomproperties.md) property, the property is not passed to the server side of the install when the property is found.</span></span>

<span data-ttu-id="81692-125">Per correggere l'errore, aggiungere la proprietà a [**SecureCustomProperties**](securecustomproperties.md).</span><span class="sxs-lookup"><span data-stu-id="81692-125">To fix this error, add the property to [**SecureCustomProperties**](securecustomproperties.md).</span></span>

``` syntax
Upgrade.ActionProperty EnglishAPPFOUND must not contain lowercase letters.
```

<span data-ttu-id="81692-126">Le proprietà di aggiornamento devono essere proprietà pubbliche affinché il risultato venga passato al lato server dell'installazione.</span><span class="sxs-lookup"><span data-stu-id="81692-126">Upgrade properties must be public properties for the result to be passed to the server side of the installation.</span></span>

<span data-ttu-id="81692-127">Per correggere l'errore, utilizzare tutte le lettere maiuscole nel nome della proprietà.</span><span class="sxs-lookup"><span data-stu-id="81692-127">To fix this error, use all uppercase letters in the property name.</span></span>

``` syntax
Upgrade.ActionProperty OLDAPPFOUND may be used in only one record of the Upgrade table.
```

<span data-ttu-id="81692-128">Una proprietà può essere utilizzata solo in una riga della tabella di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="81692-128">A property can only be used in one row of the Upgrade table.</span></span>

<span data-ttu-id="81692-129">Per correggere l'errore, utilizzare una proprietà diversa per la seconda riga.</span><span class="sxs-lookup"><span data-stu-id="81692-129">To fix this error, use a different property for the second row.</span></span>

``` syntax
Upgrade.VersionMax cannot be less than Upgrade.VersionMin. (OLDAPPFOUND)
```

<span data-ttu-id="81692-130">La versione minima deve essere minore della versione massima.</span><span class="sxs-lookup"><span data-stu-id="81692-130">The minimum version must be less than the maximum version.</span></span>

<span data-ttu-id="81692-131">Per correggere l'errore, controllare i numeri di versione per gli errori di digitazione.</span><span class="sxs-lookup"><span data-stu-id="81692-131">To fix this error, check your version numbers for typos.</span></span> <span data-ttu-id="81692-132">Se sono corretti e si vuole usare l'intervallo tra le due versioni, cambiarle in modo che VersionMin sia minore di VersionMax.</span><span class="sxs-lookup"><span data-stu-id="81692-132">If they are correct and you want to use the range between the two versions, switch them so that VersionMin is less than VersionMax.</span></span>

[<span data-ttu-id="81692-133">Tabella delle proprietà</span><span class="sxs-lookup"><span data-stu-id="81692-133">Property Table</span></span>](property-table.md)



| <span data-ttu-id="81692-134">Proprietà</span><span class="sxs-lookup"><span data-stu-id="81692-134">Property</span></span>                                                 | <span data-ttu-id="81692-135">Valore</span><span class="sxs-lookup"><span data-stu-id="81692-135">Value</span></span>                                  |
|----------------------------------------------------------|----------------------------------------|
| [<span data-ttu-id="81692-136">**UpgradeCode**</span><span class="sxs-lookup"><span data-stu-id="81692-136">**UpgradeCode**</span></span>](upgradecode.md)                       | <span data-ttu-id="81692-137">{61AA4C55-E17F-11D2-93BB-0060089A76DB}</span><span class="sxs-lookup"><span data-stu-id="81692-137">{61AA4C55-E17F-11D2-93BB-0060089A76DB}</span></span> |
| [<span data-ttu-id="81692-138">**ProductVersion**</span><span class="sxs-lookup"><span data-stu-id="81692-138">**ProductVersion**</span></span>](productversion.md)                 | <span data-ttu-id="81692-139">2.01.0000</span><span class="sxs-lookup"><span data-stu-id="81692-139">2.01.0000</span></span>                              |
| [<span data-ttu-id="81692-140">**SecureCustomProperties**</span><span class="sxs-lookup"><span data-stu-id="81692-140">**SecureCustomProperties**</span></span>](securecustomproperties.md) | <span data-ttu-id="81692-141">OLDAPPFOUND</span><span class="sxs-lookup"><span data-stu-id="81692-141">OLDAPPFOUND</span></span>                            |



 

[<span data-ttu-id="81692-142">Aggiorna tabella</span><span class="sxs-lookup"><span data-stu-id="81692-142">Upgrade Table</span></span>](upgrade-table.md)



| <span data-ttu-id="81692-143">UpgradeCode</span><span class="sxs-lookup"><span data-stu-id="81692-143">UpgradeCode</span></span>                            | <span data-ttu-id="81692-144">VersionMin</span><span class="sxs-lookup"><span data-stu-id="81692-144">VersionMin</span></span> | <span data-ttu-id="81692-145">VersionMax</span><span class="sxs-lookup"><span data-stu-id="81692-145">VersionMax</span></span> | <span data-ttu-id="81692-146">Linguaggio</span><span class="sxs-lookup"><span data-stu-id="81692-146">Language</span></span> | <span data-ttu-id="81692-147">Attributi</span><span class="sxs-lookup"><span data-stu-id="81692-147">Attributes</span></span> | <span data-ttu-id="81692-148">Rimuovi</span><span class="sxs-lookup"><span data-stu-id="81692-148">Remove</span></span>                | <span data-ttu-id="81692-149">ActionProperty</span><span class="sxs-lookup"><span data-stu-id="81692-149">ActionProperty</span></span>  |
|----------------------------------------|------------|------------|----------|------------|-----------------------|-----------------|
| <span data-ttu-id="81692-150">{61AA4C55-E17F-11D2-93BB-0060089A76DB}</span><span class="sxs-lookup"><span data-stu-id="81692-150">{61AA4C55-E17F-11D2-93BB-0060089A76DB}</span></span> |            | <span data-ttu-id="81692-151">2.01.0000</span><span class="sxs-lookup"><span data-stu-id="81692-151">2.01.0000</span></span>  |          | <span data-ttu-id="81692-152">513</span><span class="sxs-lookup"><span data-stu-id="81692-152">513</span></span>        |                       | <span data-ttu-id="81692-153">OLDAPPFOUND</span><span class="sxs-lookup"><span data-stu-id="81692-153">OLDAPPFOUND</span></span>     |
| <span data-ttu-id="81692-154">{61AA4C55-E17F-11D2-93BB-0060089A76DB}</span><span class="sxs-lookup"><span data-stu-id="81692-154">{61AA4C55-E17F-11D2-93BB-0060089A76DB}</span></span> | <span data-ttu-id="81692-155">2.01.0001</span><span class="sxs-lookup"><span data-stu-id="81692-155">2.01.0001</span></span>  | <span data-ttu-id="81692-156">2.01.0000</span><span class="sxs-lookup"><span data-stu-id="81692-156">2.01.0000</span></span>  |          |            |                       | <span data-ttu-id="81692-157">OLDAPPFOUND</span><span class="sxs-lookup"><span data-stu-id="81692-157">OLDAPPFOUND</span></span>     |
| <span data-ttu-id="81692-158">{C6CB4596-D8E8-D5A4-635F-9FE456D682EB}</span><span class="sxs-lookup"><span data-stu-id="81692-158">{C6CB4596-D8E8-D5A4-635F-9FE456D682EB}</span></span> | <span data-ttu-id="81692-159">1.00.0000</span><span class="sxs-lookup"><span data-stu-id="81692-159">1.00.0000</span></span>  | <span data-ttu-id="81692-160">2.00.0000</span><span class="sxs-lookup"><span data-stu-id="81692-160">2.00.0000</span></span>  | <span data-ttu-id="81692-161">1033</span><span class="sxs-lookup"><span data-stu-id="81692-161">1033</span></span>     |            | <span data-ttu-id="81692-162">\[AppFeatureEnglish\]</span><span class="sxs-lookup"><span data-stu-id="81692-162">\[AppFeatureEnglish\]</span></span> | <span data-ttu-id="81692-163">EnglishAPPFOUND</span><span class="sxs-lookup"><span data-stu-id="81692-163">EnglishAPPFOUND</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="81692-164">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="81692-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81692-165">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="81692-165">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



