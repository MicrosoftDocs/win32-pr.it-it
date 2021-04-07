---
description: Nella procedura riportata di seguito viene descritto uno scenario per generare una trasformazione che nasconde una funzionalità in modo permanente.
ms.assetid: 43f36866-a9df-4035-a8ae-5ccbcb628a90
title: Generazione di una trasformazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0543ae74f71155e6fcd504ebee677558f21bbfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057813"
---
# <a name="generating-a-transform"></a><span data-ttu-id="c0939-103">Generazione di una trasformazione</span><span class="sxs-lookup"><span data-stu-id="c0939-103">Generating a Transform</span></span>

<span data-ttu-id="c0939-104">Nella procedura riportata di seguito viene descritto uno scenario per generare una trasformazione che nasconde una funzionalità in modo permanente.</span><span class="sxs-lookup"><span data-stu-id="c0939-104">The following procedure describes a scenario to generate a transform that permanently hides a feature.</span></span>

<span data-ttu-id="c0939-105">**Per nascondere in modo permanente una funzionalità del prodotto**</span><span class="sxs-lookup"><span data-stu-id="c0939-105">**To permanently hide a product feature**</span></span>

1.  <span data-ttu-id="c0939-106">Copiare il pacchetto di installazione originale.</span><span class="sxs-lookup"><span data-stu-id="c0939-106">Copy the original installation package.</span></span>
2.  <span data-ttu-id="c0939-107">Modificare la copia impostando il valore della colonna di visualizzazione nella [tabella delle funzionalità](feature-table.md) su zero.</span><span class="sxs-lookup"><span data-stu-id="c0939-107">Alter the copy by setting the value of the Display column in the [Feature table](feature-table.md) to zero.</span></span> <span data-ttu-id="c0939-108">Consente di specificare di nascondere la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="c0939-108">This specifies hiding the feature.</span></span>
3.  <span data-ttu-id="c0939-109">Creare una trasformazione dal pacchetto di installazione originale nei nuovi pacchetti di installazione chiamando [**MsiDatabaseGenerateTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma).</span><span class="sxs-lookup"><span data-stu-id="c0939-109">Create a transform from the original installation package to the new installation packages by calling [**MsiDatabaseGenerateTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma).</span></span>
4.  <span data-ttu-id="c0939-110">Creare le informazioni di riepilogo nella trasformazione chiamando [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa).</span><span class="sxs-lookup"><span data-stu-id="c0939-110">Create the summary information in the transform by calling [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa).</span></span>

<span data-ttu-id="c0939-111">La trasformazione sarà quindi pronta per essere applicata durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="c0939-111">The transform is then ready to be applied during installation.</span></span> <span data-ttu-id="c0939-112">Per ulteriori informazioni, vedere [applicazione delle trasformazioni](applying-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="c0939-112">For more information, see [Applying Transforms](applying-transforms.md).</span></span>

 

 



