---
description: ICE74 verifica che la proprietà FASTOEM non sia stata creata nella tabella delle proprietà.
ms.assetid: 2af132f0-0ffa-405f-9d05-7cb5d5f826b8
title: ICE74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fe2762710e061f2c88f55893294a40fbac8700f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308323"
---
# <a name="ice74"></a><span data-ttu-id="1d731-103">ICE74</span><span class="sxs-lookup"><span data-stu-id="1d731-103">ICE74</span></span>

<span data-ttu-id="1d731-104">ICE74 verifica che la proprietà [**FASTOEM**](fastoem.md) non sia stata creata nella [tabella delle proprietà](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="1d731-104">ICE74 verifies that the [**FASTOEM**](fastoem.md) property has not been authored into the [Property table](property-table.md).</span></span>

<span data-ttu-id="1d731-105">La proprietà [**FASTOEM**](fastoem.md) consente agli OEM di ridurre il tempo necessario per installare le applicazioni Windows Installer per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="1d731-105">The [**FASTOEM**](fastoem.md) property enables OEMs to reduce the time required to install Windows Installer applications for the first time.</span></span> <span data-ttu-id="1d731-106">Non può essere utilizzata dopo la prima installazione.</span><span class="sxs-lookup"><span data-stu-id="1d731-106">It cannot be used after the first install.</span></span> <span data-ttu-id="1d731-107">La proprietà **FASTOEM** non deve essere creata nella tabella delle proprietà perché questa operazione interferisce con le installazioni successive per la manutenzione, la rimozione o il ripristino dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1d731-107">The **FASTOEM** property must not be authored in the Property table because this interferes with subsequent installations for the maintenance, removal, or repair of the application.</span></span>

<span data-ttu-id="1d731-108">ICE74 verifica inoltre che la proprietà [**UpgradeCode**](upgradecode.md) sia stata creata nella tabella delle [Proprietà](property-table.md)e che il relativo valore non sia un GUID null, {00000000-0000-0000-0000-000000000000} .</span><span class="sxs-lookup"><span data-stu-id="1d731-108">ICE74 also verifies that the [**UpgradeCode**](upgradecode.md) property is authored into the [Property table](property-table.md), and that its value is not a null GUID, {00000000-0000-0000-0000-000000000000}.</span></span>

## <a name="result"></a><span data-ttu-id="1d731-109">Risultato</span><span class="sxs-lookup"><span data-stu-id="1d731-109">Result</span></span>

<span data-ttu-id="1d731-110">ICE74 può inserire i seguenti errori.</span><span class="sxs-lookup"><span data-stu-id="1d731-110">ICE74 can post the following errors.</span></span>



| <span data-ttu-id="1d731-111">Errore ICE74</span><span class="sxs-lookup"><span data-stu-id="1d731-111">ICE74 error</span></span>                                                                       | <span data-ttu-id="1d731-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1d731-112">Description</span></span>                                                                                             |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d731-113">Impossibile creare la proprietà [**FASTOEM**](fastoem.md) nella tabella delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="1d731-113">The [**FASTOEM**](fastoem.md) property cannot be authored in the Property table.</span></span> | <span data-ttu-id="1d731-114">La proprietà [**FASTOEM**](fastoem.md) è stata impostata nella tabella delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="1d731-114">The [**FASTOEM**](fastoem.md) property has been set in the Property table.</span></span>                             |
| <span data-ttu-id="1d731-115">' \[ 2 \] ' non è un [**UpgradeCode**](upgradecode.md)valido.</span><span class="sxs-lookup"><span data-stu-id="1d731-115">'\[2\]' is not a valid [**UpgradeCode**](upgradecode.md).</span></span>                        | <span data-ttu-id="1d731-116">È stato immesso un GUID null per la proprietà [**UpgradeCode**](upgradecode.md) nella tabella delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="1d731-116">A null GUID has been entered for the [**UpgradeCode**](upgradecode.md) property in the Property table.</span></span> |



 

<span data-ttu-id="1d731-117">ICE74 può inviare il seguente avviso.</span><span class="sxs-lookup"><span data-stu-id="1d731-117">ICE74 can post the following warning.</span></span>



| <span data-ttu-id="1d731-118">Avviso di ICE74</span><span class="sxs-lookup"><span data-stu-id="1d731-118">ICE74 warning</span></span>                                                                                                                                                                                             | <span data-ttu-id="1d731-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1d731-119">Description</span></span>                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1d731-120">La proprietà [**UpgradeCode**](upgradecode.md) non è stata creata nella tabella delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="1d731-120">The [**UpgradeCode**](upgradecode.md) property is not authored in the Property table.</span></span> <span data-ttu-id="1d731-121">Si consiglia vivamente agli autori dei pacchetti di installazione di specificare un **UpgradeCode** per la propria applicazione.</span><span class="sxs-lookup"><span data-stu-id="1d731-121">It is strongly recommended that authors of installation packages specify an **UpgradeCode** for their application.</span></span> | <span data-ttu-id="1d731-122">La proprietà [**UpgradeCode**](upgradecode.md) non è stata creata nella tabella delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="1d731-122">The [**UpgradeCode**](upgradecode.md) property is not authored in the Property table.</span></span> |



 

## <a name="example"></a><span data-ttu-id="1d731-123">Esempio</span><span class="sxs-lookup"><span data-stu-id="1d731-123">Example</span></span>

<span data-ttu-id="1d731-124">ICE74 segnala l'errore seguente se la proprietà [**FASTOEM**](fastoem.md) è impostata: FASTOEM</span><span class="sxs-lookup"><span data-stu-id="1d731-124">ICE74 reports the following error if the [**FASTOEM**](fastoem.md) property is set: The FASTOEM</span></span>

``` syntax
 property cannot be authored in the Property table.
```

<span data-ttu-id="1d731-125">[Tabella delle proprietà](property-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="1d731-125">[Property Table](property-table.md) (partial)</span></span>



| <span data-ttu-id="1d731-126">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1d731-126">Property</span></span>                   | <span data-ttu-id="1d731-127">Valore</span><span class="sxs-lookup"><span data-stu-id="1d731-127">Value</span></span> |
|----------------------------|-------|
| [<span data-ttu-id="1d731-128">**FASTOEM**</span><span class="sxs-lookup"><span data-stu-id="1d731-128">**FASTOEM**</span></span>](fastoem.md) | <span data-ttu-id="1d731-129">1</span><span class="sxs-lookup"><span data-stu-id="1d731-129">1</span></span>     |



 

<span data-ttu-id="1d731-130">Per correggere l'errore, rimuovere la proprietà [**FASTOEM**](fastoem.md) dalla tabella delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="1d731-130">To fix this error remove the [**FASTOEM**](fastoem.md) property from the Property Table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1d731-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1d731-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d731-132">**Proprietà FASTOEM**</span><span class="sxs-lookup"><span data-stu-id="1d731-132">**FASTOEM property**</span></span>](fastoem.md)
</dt> <dt>

[<span data-ttu-id="1d731-133">Tabella delle proprietà</span><span class="sxs-lookup"><span data-stu-id="1d731-133">Property table</span></span>](property-table.md)
</dt> <dt>

[<span data-ttu-id="1d731-134">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="1d731-134">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



