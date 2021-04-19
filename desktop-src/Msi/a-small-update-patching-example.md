---
description: Questo esempio illustra come creare un pacchetto di patch che applica un piccolo aggiornamento al pacchetto di installazione di esempio descritto in un esempio di installazione.
ms.assetid: 17dadd64-6e81-444a-985e-1b340e4f2ee5
title: Un piccolo esempio di patch di aggiornamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36d4997a326e8fea33086a75c9cf40ecef8cb997
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311101"
---
# <a name="a-small-update-patching-example"></a><span data-ttu-id="8cdf2-103">Un piccolo esempio di patch di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="8cdf2-103">A Small Update Patching Example</span></span>

<span data-ttu-id="8cdf2-104">Questo esempio illustra come creare un pacchetto di [patch](patch-packages.md) che applica un [piccolo aggiornamento](small-updates.md) al pacchetto di installazione di esempio descritto in [un esempio di installazione](an-installation-example.md).</span><span class="sxs-lookup"><span data-stu-id="8cdf2-104">This example illustrates how to create a [patch package](patch-packages.md) that applies a [small update](small-updates.md) to the sample installation package discussed in [An Installation Example](an-installation-example.md).</span></span> <span data-ttu-id="8cdf2-105">Un piccolo aggiornamento apporta modifiche a uno o più file di applicazione giudicati troppo piccoli per garantire la modifica del codice del prodotto.</span><span class="sxs-lookup"><span data-stu-id="8cdf2-105">A small update makes changes to one or more application files that are judged to be too minor to warrant changing the product code.</span></span> <span data-ttu-id="8cdf2-106">Per ulteriori informazioni, vedere applicazione di [patch e aggiornamenti](patching-and-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="8cdf2-106">For more information see [Patching and Upgrades](patching-and-upgrades.md).</span></span>

<span data-ttu-id="8cdf2-107">Questo esempio illustra come creare un pacchetto di patch Windows Installer che aggiorna la funzionalità di concerto del prodotto ipotetico MNP2000 per correggere un errore nel prodotto originale.</span><span class="sxs-lookup"><span data-stu-id="8cdf2-107">This example illustrates how to create a Windows Installer patch package that updates the Concert feature of the hypothetical product MNP2000 to fix an error in the original product.</span></span> <span data-ttu-id="8cdf2-108">Il pacchetto di patch di esempio applica un piccolo aggiornamento al prodotto che non richiede la modifica del codice del prodotto.</span><span class="sxs-lookup"><span data-stu-id="8cdf2-108">The example patch package applies a small update to the product that does not require changing the product code.</span></span> <span data-ttu-id="8cdf2-109">Per ulteriori informazioni sugli aggiornamenti principali, vedere l'argomento relativo agli [aggiornamenti principali](major-upgrades.md) nella sezione applicazione di [patch e aggiornamenti](patching-and-upgrades.md) .</span><span class="sxs-lookup"><span data-stu-id="8cdf2-109">See the topic on [Major Upgrades](major-upgrades.md) in the [Patching and Upgrades](patching-and-upgrades.md) section for more information about major upgrades.</span></span>

<span data-ttu-id="8cdf2-110">Il pacchetto di aggiornamento di esempio presenta le specifiche seguenti:</span><span class="sxs-lookup"><span data-stu-id="8cdf2-110">The sample upgrade package has the following specifications:</span></span>

-   <span data-ttu-id="8cdf2-111">Corregge un errore secondario nella pianificazione del concerto visualizzata dalla funzionalità Concert.</span><span class="sxs-lookup"><span data-stu-id="8cdf2-111">It corrects a minor error in the Concert schedule displayed by the Concert feature.</span></span>
-   <span data-ttu-id="8cdf2-112">Aggiorna il codice del pacchetto in modo da riflettere che il pacchetto di installazione è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="8cdf2-112">It updates the package code to reflect the installation package has changed.</span></span>
-   <span data-ttu-id="8cdf2-113">Il piccolo aggiornamento può essere applicato applicando patch all'installazione locale del prodotto.</span><span class="sxs-lookup"><span data-stu-id="8cdf2-113">The small update can be applied by patching the local installation of the product.</span></span>

[<span data-ttu-id="8cdf2-114">Continua</span><span class="sxs-lookup"><span data-stu-id="8cdf2-114">Continue</span></span>](planning-a-small-update-patch.md)

 

 



