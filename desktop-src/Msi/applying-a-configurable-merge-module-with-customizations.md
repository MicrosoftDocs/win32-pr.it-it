---
description: Seguire le linee guida generali per l'applicazione dei moduli di merge descritti in applicazione di moduli di Unione.
ms.assetid: 6035b1a9-d452-4020-9fe3-c20ba874a2ed
title: Applicazione di un modulo merge configurabile con personalizzazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4f1e3da426ba5ca13e149814ab9bb927e83d4e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311057"
---
# <a name="applying-a-configurable-merge-module-with-customizations"></a><span data-ttu-id="dbaa9-103">Applicazione di un modulo merge configurabile con personalizzazioni</span><span class="sxs-lookup"><span data-stu-id="dbaa9-103">Applying a Configurable Merge Module with Customizations</span></span>

<span data-ttu-id="dbaa9-104">Seguire le linee guida generali per l'applicazione dei moduli di merge descritti in [applicazione di moduli di Unione](applying-merge-modules.md).</span><span class="sxs-lookup"><span data-stu-id="dbaa9-104">Follow the general guidelines for applying merge modules described in [Applying Merge Modules](applying-merge-modules.md).</span></span> <span data-ttu-id="dbaa9-105">Per configurare un modulo merge al momento dell'installazione, inoltre, gli utenti del modulo merge devono eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="dbaa9-105">In addition, merge module consumers must do the following to configure a merge module at the time of installation:</span></span>

-   <span data-ttu-id="dbaa9-106">Utilizzare un modulo merge creato per avere impostazioni configurabili.</span><span class="sxs-lookup"><span data-stu-id="dbaa9-106">Use a merge module that is authored to have configurable settings.</span></span> <span data-ttu-id="dbaa9-107">Per ulteriori informazioni, vedere [creazione di un modulo merge che può essere configurato dall'utente finale](creating-a-merge-module-that-can-be-configured-by-the-end-user.md)</span><span class="sxs-lookup"><span data-stu-id="dbaa9-107">For more information, see [Creating a Merge Module that Can Be Configured by the End-User](creating-a-merge-module-that-can-be-configured-by-the-end-user.md)</span></span>
-   <span data-ttu-id="dbaa9-108">Usare uno strumento di merge e configurazione che chiama Mergemod.dll versione 2,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="dbaa9-108">Use a merge and configuration tool that calls Mergemod.dll version 2.0 or later.</span></span> <span data-ttu-id="dbaa9-109">Nelle versioni precedenti di Mergmod.dll non è possibile configurare le impostazioni del modulo merge.</span><span class="sxs-lookup"><span data-stu-id="dbaa9-109">Earlier versions of Mergmod.dll cannot configure merge module settings.</span></span> <span data-ttu-id="dbaa9-110">Gli autori devono creare moduli unione che forniscano valori predefiniti e siano compatibili con le versioni precedenti di Mergmod.dll.</span><span class="sxs-lookup"><span data-stu-id="dbaa9-110">Authors should create merge modules that provide default values and are compatible with earlier versions of Mergmod.dll.</span></span>
-   <span data-ttu-id="dbaa9-111">Fornire le informazioni di personalizzazione quando richiesto dallo strumento client di configurazione.</span><span class="sxs-lookup"><span data-stu-id="dbaa9-111">Provide customization information when prompted by the configuration client tool.</span></span> <span data-ttu-id="dbaa9-112">Gli autori devono creare moduli merge che utilizzano valori predefiniti quando un utente rifiuta di fornire informazioni.</span><span class="sxs-lookup"><span data-stu-id="dbaa9-112">Authors should create merge modules that use default values when a user declines to provide information.</span></span>

 

 



