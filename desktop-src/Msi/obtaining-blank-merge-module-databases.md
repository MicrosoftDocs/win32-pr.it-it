---
description: Ottenere un database del modulo merge vuoto. È possibile usare il file schema. msm fornito con Windows Installer SDK come database iniziale per il modulo merge. Per ulteriori informazioni, vedere Windows SDK Components for Windows Installer Developers.
ms.assetid: 8408e892-adc6-4ef5-ad36-4d04c021c899
title: Recupero di database del modulo merge vuoti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba75d55763d30b0ab545d2dbddbc19c1b0c279d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309993"
---
# <a name="obtaining-blank-merge-module-databases"></a><span data-ttu-id="c9d99-105">Recupero di database del modulo merge vuoti</span><span class="sxs-lookup"><span data-stu-id="c9d99-105">Obtaining Blank Merge Module Databases</span></span>

<span data-ttu-id="c9d99-106">Ottenere un database del modulo merge vuoto.</span><span class="sxs-lookup"><span data-stu-id="c9d99-106">Obtain a blank merge module database.</span></span> <span data-ttu-id="c9d99-107">È possibile usare il file schema. msm fornito con Windows Installer SDK come database iniziale per il modulo merge.</span><span class="sxs-lookup"><span data-stu-id="c9d99-107">You can use the file Schema.msm provided with the Windows Installer SDK as a starting database for your merge module.</span></span> <span data-ttu-id="c9d99-108">Per ulteriori informazioni, vedere [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="c9d99-108">For more information, see [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

<span data-ttu-id="c9d99-109">Gli sviluppatori devono creare moduli unione usando lo schema di database più semplice che installa i componenti.</span><span class="sxs-lookup"><span data-stu-id="c9d99-109">Developers should author merge modules using the simplest database schema that installs their components.</span></span> <span data-ttu-id="c9d99-110">L'utilizzo di uno schema semplice garantisce la massima compatibilità per il modulo merge.</span><span class="sxs-lookup"><span data-stu-id="c9d99-110">The use of a simple schema ensures the greatest compatibility for the merge module.</span></span> <span data-ttu-id="c9d99-111">L'Unione di un modulo merge in un pacchetto di installazione con uno schema di database diverso in genere comporta conflitti di merge.</span><span class="sxs-lookup"><span data-stu-id="c9d99-111">Merging a merge module into an installation package with a different database schema usually results in merge conflicts.</span></span>

<span data-ttu-id="c9d99-112">Per un elenco completo di tutte le tabelle obbligatorie e facoltative nei moduli merge, vedere [Merge Module Database Tables](merge-module-database-tables.md).</span><span class="sxs-lookup"><span data-stu-id="c9d99-112">For a complete list of all the required and optional tables in merge modules, see [Merge Module Database Tables](merge-module-database-tables.md).</span></span>

 

 



