---
description: Quando si crea una patch per un aggiornamento Windows Installer Small, attenersi alle linee guida seguenti.
ms.assetid: 0e57c2aa-e86a-4161-9749-c7963182a6d5
title: Creazione di una patch di aggiornamento di piccole dimensioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d948c871baed7fbc15545ed9669c9864ce954799
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318288"
---
# <a name="creating-a-small-update-patch"></a><span data-ttu-id="02de2-103">Creazione di una patch di aggiornamento di piccole dimensioni</span><span class="sxs-lookup"><span data-stu-id="02de2-103">Creating a Small Update Patch</span></span>

<span data-ttu-id="02de2-104">Quando si crea una patch per [piccoli aggiornamenti](small-updates.md), gli autori devono rispettare le linee guida seguenti:</span><span class="sxs-lookup"><span data-stu-id="02de2-104">When creating a patch for [small updates](small-updates.md), authors should adhere to the following guidelines:</span></span>

-   <span data-ttu-id="02de2-105">Le patch di aggiornamento di piccole dimensioni devono essere progettate per una singola installazione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="02de2-105">Small update patches must be designed for a single, target installation.</span></span>
-   <span data-ttu-id="02de2-106">Le patch di aggiornamento di piccole dimensioni devono usare la versione più recente dell'installazione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="02de2-106">Small update patches should use the earliest version as the target installation.</span></span>
-   <span data-ttu-id="02de2-107">Una patch di aggiornamento di piccole dimensioni dovrebbe sostituire e rendere obsolete le patch di aggiornamento di piccole dimensioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="02de2-107">A small update patch should replace and make obsolete any earlier small update patches.</span></span>

<span data-ttu-id="02de2-108">Lo scenario seguente illustra quando è preferibile una patch di aggiornamento di dimensioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="02de2-108">The following scenario illustrates when a small update patch is best.</span></span>

<span data-ttu-id="02de2-109">La società viene fornita dalla versione 1,0 del Myproduct.msi.</span><span class="sxs-lookup"><span data-stu-id="02de2-109">Your company ships version 1.0 of Myproduct.msi.</span></span> <span data-ttu-id="02de2-110">Poco dopo, viene fornita una patch di [aggiornamento di piccole dimensioni](small-updates.md) per Myproduct.msi denominata QFE1.</span><span class="sxs-lookup"><span data-stu-id="02de2-110">Shortly thereafter, you ship a [small update](small-updates.md) patch for Myproduct.msi called QFE1.</span></span> <span data-ttu-id="02de2-111">Questa operazione non comporta la modifica della proprietà [**ProductCode**](productcode.md) o della proprietà [**ProductVersion**](productversion.md) .</span><span class="sxs-lookup"><span data-stu-id="02de2-111">This does not change the [**ProductCode**](productcode.md) property or the [**ProductVersion**](productversion.md) property.</span></span>

<span data-ttu-id="02de2-112">Successivamente, è possibile creare una seconda patch di [aggiornamento di piccole dimensioni](small-updates.md) per Myproduct.msi denominata QFE2.</span><span class="sxs-lookup"><span data-stu-id="02de2-112">Later, you author a second [small update](small-updates.md) patch for Myproduct.msi called QFE2.</span></span> <span data-ttu-id="02de2-113">Questa seconda patch deve avere come destinazione Myproduct.msi versione 1,0.</span><span class="sxs-lookup"><span data-stu-id="02de2-113">This second patch must target Myproduct.msi version 1.0.</span></span> <span data-ttu-id="02de2-114">Questa seconda patch non deve essere destinata a Myproduct.msi versione 1,0 e Myproduct.msi versione 1,0 + QFE1.</span><span class="sxs-lookup"><span data-stu-id="02de2-114">This second patch must not target both Myproduct.msi version 1.0 and Myproduct.msi version 1.0 + QFE1.</span></span> <span data-ttu-id="02de2-115">Quando QFE2 viene applicato, deve rimuovere QFE1.</span><span class="sxs-lookup"><span data-stu-id="02de2-115">When QFE2 is applied it should remove QFE1.</span></span>

 

 



