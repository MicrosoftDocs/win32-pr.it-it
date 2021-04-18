---
description: In ogni modulo merge è necessaria una tabella FeatureComponents vuota. Questa tabella vuota fornisce uno schema per lo strumento di merge se il file con estensione msi di destinazione non dispone di una propria tabella FeatureComponents.
ms.assetid: 19463fc7-8362-4943-8907-22c38f66fe25
title: Creazione di tabelle FeatureComponents del modulo merge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3522f32f91a66df93e9096bf9c528f8d00e11f6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311044"
---
# <a name="authoring-merge-module-featurecomponents-tables"></a><span data-ttu-id="f4e44-104">Creazione di tabelle FeatureComponents del modulo merge</span><span class="sxs-lookup"><span data-stu-id="f4e44-104">Authoring Merge Module FeatureComponents Tables</span></span>

<span data-ttu-id="f4e44-105">In ogni modulo merge è necessaria una [tabella FeatureComponents](featurecomponents-table.md) vuota.</span><span class="sxs-lookup"><span data-stu-id="f4e44-105">A blank [FeatureComponents table](featurecomponents-table.md) is required in every merge module.</span></span> <span data-ttu-id="f4e44-106">Questa tabella vuota fornisce uno schema per lo strumento di merge se il file con estensione msi di destinazione non dispone di una propria tabella FeatureComponents.</span><span class="sxs-lookup"><span data-stu-id="f4e44-106">This empty table provides a schema for the merge tool if the target .msi file does not have its own FeatureComponents table.</span></span>

<span data-ttu-id="f4e44-107">Se e solo se non è presente alcuna tabella FeatureComponents nel file con estensione msi di destinazione, lo strumento di merge usa la tabella vuota fornita nel modulo.</span><span class="sxs-lookup"><span data-stu-id="f4e44-107">If, and only if, there is no FeatureComponents table in the target .msi file does the merge tool use the blank table provided in the module.</span></span> <span data-ttu-id="f4e44-108">In questo caso, lo strumento di merge crea una tabella duplicata nel file con estensione msi di destinazione e aggiunge righe che associano i nuovi componenti del modulo merge alle funzionalità del pacchetto di installazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f4e44-108">In this case, the merge tool creates a duplicate table in the target .msi file and adds rows that associate the new components in the merge module to the features in the application's installation package.</span></span>

 

 



