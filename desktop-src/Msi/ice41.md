---
description: ICE41 verifica che le voci della classe e le tabelle di estensioni facciano riferimento alle voci della tabella dei componenti che implementano l'oggetto o l'estensione della classe del componente.
ms.assetid: 43572322-ba23-4f99-be34-e572d4c6e3eb
title: ICE41
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4bc6c0a8bb634706750810484963e56b6d6e0ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314216"
---
# <a name="ice41"></a><span data-ttu-id="27394-103">ICE41</span><span class="sxs-lookup"><span data-stu-id="27394-103">ICE41</span></span>

<span data-ttu-id="27394-104">ICE41 verifica che le voci della [classe](class-table.md) e le tabelle di [estensioni](extension-table.md) facciano riferimento alle voci della [tabella dei componenti](component-table.md) che implementano l'oggetto o l'estensione della classe del componente.</span><span class="sxs-lookup"><span data-stu-id="27394-104">ICE41 validates that the entries in the [Class](class-table.md) and [Extension](extension-table.md) tables refer to entries in the [Component table](component-table.md) that implement the class object or extension of the component.</span></span>

## <a name="result"></a><span data-ttu-id="27394-105">Risultato</span><span class="sxs-lookup"><span data-stu-id="27394-105">Result</span></span>

<span data-ttu-id="27394-106">ICE41 Invia un errore se esiste una funzionalità che non contiene il componente che implementa l'estensione o l'oggetto della classe.</span><span class="sxs-lookup"><span data-stu-id="27394-106">ICE41 posts an error if there is a feature that does not contain the component implementing the class object or extension.</span></span>

## <a name="example"></a><span data-ttu-id="27394-107">Esempio</span><span class="sxs-lookup"><span data-stu-id="27394-107">Example</span></span>

<span data-ttu-id="27394-108">ICE41 segnala gli errori seguenti per l'esempio illustrato.</span><span class="sxs-lookup"><span data-stu-id="27394-108">ICE41 reports the following errors for the example shown.</span></span>



| <span data-ttu-id="27394-109">Errore ICE41</span><span class="sxs-lookup"><span data-stu-id="27394-109">ICE41 error</span></span>                                                                                                                                                                                    | <span data-ttu-id="27394-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="27394-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27394-111">La classe {00000000-0000-0000-0000-0000000000000} fa riferimento alla funzionalità Funzionalità2 e al componente Component1, ma il componente non è associato a tale funzionalità nella tabella FeatureComponents.</span><span class="sxs-lookup"><span data-stu-id="27394-111">Class {00000000-0000-0000-0000-0000000000000} references feature Feature2 and component Component1, but the that Component is not associated with that Feature in the FeatureComponents table.</span></span> | <span data-ttu-id="27394-112">Esiste una funzionalità che non contiene il componente che implementa l'oggetto classe.</span><span class="sxs-lookup"><span data-stu-id="27394-112">There is a feature that does not contain the component implementing the class object.</span></span> <span data-ttu-id="27394-113">Ciò significa che il programma di installazione non installa il componente con la funzionalità e che la pubblicità potrebbe non funzionare come previsto.</span><span class="sxs-lookup"><span data-stu-id="27394-113">This means that the installer does not install the component with the feature and that advertising may not work as expected.</span></span> <span data-ttu-id="27394-114">Per correggere l'errore, modificare la voce nella colonna funzionalità \_ della voce [tabella classi](class-table.md) per fare riferimento a una funzionalità che installa il componente elencato nella \_ colonna componente o modificare la funzionalità e il componente associati nella [tabella FeatureComponents](featurecomponents-table.md).</span><span class="sxs-lookup"><span data-stu-id="27394-114">To fix this error, change the entry in the Feature\_ column of the [Class table](class-table.md) entry to reference a feature that installs component listed in the Component\_ column or change the feature and component associated in the [FeatureComponents table](featurecomponents-table.md).</span></span><br/>          |
| <span data-ttu-id="27394-115">Extension. Feature1 fa riferimento a feature Component2 e Component, ma il componente non è associato a tale funzionalità nella tabella FeatureComponents.</span><span class="sxs-lookup"><span data-stu-id="27394-115">Extension .yip references feature Feature1 and component Component2, but the that Component is not associated with that Feature in the FeatureComponents table.</span></span>                                | <span data-ttu-id="27394-116">Esiste una funzionalità che non contiene il componente che implementa l'estensione.</span><span class="sxs-lookup"><span data-stu-id="27394-116">There is a feature that does not contain the component implementing the extension.</span></span> <span data-ttu-id="27394-117">Ciò significa che il programma di installazione non installa il componente con la funzionalità e che la pubblicità potrebbe non funzionare come previsto.</span><span class="sxs-lookup"><span data-stu-id="27394-117">This means that the installer does not install the component with the feature and that advertising may not work as expected.</span></span> <span data-ttu-id="27394-118">Per correggere l'errore, modificare la voce nella colonna funzionalità \_ della voce della [tabella di estensione](extension-table.md) in modo che faccia riferimento a una funzionalità che installa il componente elencato nella \_ colonna componente o modificare la funzionalità e il componente associati nella [tabella FeatureComponents](featurecomponents-table.md).</span><span class="sxs-lookup"><span data-stu-id="27394-118">To fix this error, change the entry in the Feature\_ column of the [Extension table](extension-table.md) entry to reference a feature that installs the component listed in the Component\_ column or change the feature and component associated in the [FeatureComponents table](featurecomponents-table.md).</span></span><br/> |



 

<span data-ttu-id="27394-119">[Tabella FeatureComponents](featurecomponents-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="27394-119">[FeatureComponents Table](featurecomponents-table.md) (partial)</span></span>



| <span data-ttu-id="27394-120">Funzionalità\_</span><span class="sxs-lookup"><span data-stu-id="27394-120">Feature\_</span></span> |
|-----------|
| <span data-ttu-id="27394-121">Feature1</span><span class="sxs-lookup"><span data-stu-id="27394-121">Feature1</span></span>  |
| <span data-ttu-id="27394-122">Funzionalità2</span><span class="sxs-lookup"><span data-stu-id="27394-122">Feature2</span></span>  |



 

<span data-ttu-id="27394-123">[Tabella classi](class-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="27394-123">[Class Table](class-table.md) (partial)</span></span>



| <span data-ttu-id="27394-124">CLSID</span><span class="sxs-lookup"><span data-stu-id="27394-124">CLSID</span></span>                                  | <span data-ttu-id="27394-125">Componente\_</span><span class="sxs-lookup"><span data-stu-id="27394-125">Component\_</span></span> | <span data-ttu-id="27394-126">Funzionalità\_</span><span class="sxs-lookup"><span data-stu-id="27394-126">Feature\_</span></span> |
|----------------------------------------|-------------|-----------|
| {00000000-0000-0000-0000-000000000000} | <span data-ttu-id="27394-127">Component1</span><span class="sxs-lookup"><span data-stu-id="27394-127">Component1</span></span>  | <span data-ttu-id="27394-128">Funzionalità2</span><span class="sxs-lookup"><span data-stu-id="27394-128">Feature2</span></span>  |



 

<span data-ttu-id="27394-129">[Tabella classi](class-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="27394-129">[Class Table](class-table.md) (partial)</span></span>



| <span data-ttu-id="27394-130">Estensione</span><span class="sxs-lookup"><span data-stu-id="27394-130">Extension</span></span> | <span data-ttu-id="27394-131">Componente\_</span><span class="sxs-lookup"><span data-stu-id="27394-131">Component\_</span></span> | <span data-ttu-id="27394-132">Funzionalità\_</span><span class="sxs-lookup"><span data-stu-id="27394-132">Feature\_</span></span> |
|-----------|-------------|-----------|
| <span data-ttu-id="27394-133">.</span><span class="sxs-lookup"><span data-stu-id="27394-133">.yip</span></span>      | <span data-ttu-id="27394-134">Component2</span><span class="sxs-lookup"><span data-stu-id="27394-134">Component2</span></span>  | <span data-ttu-id="27394-135">Feature1</span><span class="sxs-lookup"><span data-stu-id="27394-135">Feature1</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="27394-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="27394-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27394-137">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="27394-137">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




