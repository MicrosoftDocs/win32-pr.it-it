---
description: Ogni funzionalità Windows Installer utilizza uno o più componenti di Windows Installer e le funzionalità possono condividere i componenti.
ms.assetid: 7ab4b359-e729-4ca5-8ef3-fa8e988be6da
title: Specifica di relazioni Feature-Component
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a05ff15f4c735ac7d081c16f49f1aafe555a96db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307837"
---
# <a name="specifying-feature-component-relationships"></a><span data-ttu-id="cdd23-103">Specifica di relazioni Feature-Component</span><span class="sxs-lookup"><span data-stu-id="cdd23-103">Specifying Feature-Component Relationships</span></span>

<span data-ttu-id="cdd23-104">Ogni [funzionalità Windows Installer](windows-installer-features.md) utilizza uno o più [componenti di Windows Installer](windows-installer-components.md)e le funzionalità possono condividere i componenti.</span><span class="sxs-lookup"><span data-stu-id="cdd23-104">Each [Windows Installer Feature](windows-installer-features.md) uses one or more [Windows Installer Components](windows-installer-components.md), and features may share components.</span></span> <span data-ttu-id="cdd23-105">La [tabella FeatureComponents](featurecomponents-table.md) definisce la relazione tra le funzionalità e i componenti.</span><span class="sxs-lookup"><span data-stu-id="cdd23-105">The [FeatureComponents table](featurecomponents-table.md) defines the relationship between features and components.</span></span> <span data-ttu-id="cdd23-106">Vedere il [gruppo di tabelle](core-tables-group.md) e i [componenti e le funzionalità](components-and-features.md) principali nella Panoramica di Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="cdd23-106">See the [Core Tables Group](core-tables-group.md) and [Components and Features](components-and-features.md) in the Windows Installer overview.</span></span> <span data-ttu-id="cdd23-107">In questa sezione si aggiungono informazioni alla tabella FeatureComponents dell'esempio del blocco note.</span><span class="sxs-lookup"><span data-stu-id="cdd23-107">In this section you add information to the FeatureComponents table of the Notepad sample.</span></span>

<span data-ttu-id="cdd23-108">Utilizzare l'editor di database per aprire MNP2000.msi e immettere i dati seguenti nella tabella FeatureComponents vuota.</span><span class="sxs-lookup"><span data-stu-id="cdd23-108">Use your database editor to open MNP2000.msi and enter the following data into the empty FeatureComponents table.</span></span>

[<span data-ttu-id="cdd23-109">Tabella FeatureComponents</span><span class="sxs-lookup"><span data-stu-id="cdd23-109">FeatureComponents Table</span></span>](featurecomponents-table.md)



| <span data-ttu-id="cdd23-110">Funzionalità\_</span><span class="sxs-lookup"><span data-stu-id="cdd23-110">Feature\_</span></span> | <span data-ttu-id="cdd23-111">Componente\_</span><span class="sxs-lookup"><span data-stu-id="cdd23-111">Component\_</span></span> |
|-----------|-------------|
| <span data-ttu-id="cdd23-112">Baseball</span><span class="sxs-lookup"><span data-stu-id="cdd23-112">Baseball</span></span>  | <span data-ttu-id="cdd23-113">Baseball</span><span class="sxs-lookup"><span data-stu-id="cdd23-113">Baseball</span></span>    |
| <span data-ttu-id="cdd23-114">Concerto</span><span class="sxs-lookup"><span data-stu-id="cdd23-114">Concert</span></span>   | <span data-ttu-id="cdd23-115">Concerto</span><span class="sxs-lookup"><span data-stu-id="cdd23-115">Concert</span></span>     |
| <span data-ttu-id="cdd23-116">Danza</span><span class="sxs-lookup"><span data-stu-id="cdd23-116">Dance</span></span>     | <span data-ttu-id="cdd23-117">Danza</span><span class="sxs-lookup"><span data-stu-id="cdd23-117">Dance</span></span>       |
| <span data-ttu-id="cdd23-118">Calcio</span><span class="sxs-lookup"><span data-stu-id="cdd23-118">Football</span></span>  | <span data-ttu-id="cdd23-119">Calcio</span><span class="sxs-lookup"><span data-stu-id="cdd23-119">Football</span></span>    |
| <span data-ttu-id="cdd23-120">Help</span><span class="sxs-lookup"><span data-stu-id="cdd23-120">Help</span></span>      | <span data-ttu-id="cdd23-121">Help</span><span class="sxs-lookup"><span data-stu-id="cdd23-121">Help</span></span>        |
| <span data-ttu-id="cdd23-122">January</span><span class="sxs-lookup"><span data-stu-id="cdd23-122">January</span></span>   | <span data-ttu-id="cdd23-123">January</span><span class="sxs-lookup"><span data-stu-id="cdd23-123">January</span></span>     |
| <span data-ttu-id="cdd23-124">NewYears</span><span class="sxs-lookup"><span data-stu-id="cdd23-124">NewYears</span></span>  | <span data-ttu-id="cdd23-125">NewYears</span><span class="sxs-lookup"><span data-stu-id="cdd23-125">NewYears</span></span>    |
| <span data-ttu-id="cdd23-126">Blocco note</span><span class="sxs-lookup"><span data-stu-id="cdd23-126">Notepad</span></span>   | <span data-ttu-id="cdd23-127">Blocco note</span><span class="sxs-lookup"><span data-stu-id="cdd23-127">Notepad</span></span>     |
| <span data-ttu-id="cdd23-128">File Leggimi</span><span class="sxs-lookup"><span data-stu-id="cdd23-128">Readme</span></span>    | <span data-ttu-id="cdd23-129">Blocco note</span><span class="sxs-lookup"><span data-stu-id="cdd23-129">Notepad</span></span>     |



 

[<span data-ttu-id="cdd23-130">Continua</span><span class="sxs-lookup"><span data-stu-id="cdd23-130">Continue</span></span>](adding-registry-information.md)

 

 



