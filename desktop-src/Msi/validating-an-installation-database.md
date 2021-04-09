---
description: Gli autori dei pacchetti di installazione devono sempre eseguire la convalida sui pacchetti prima di tentare di installare il pacchetto per la prima volta ed eseguire di nuovo la convalida ogni volta che vengono apportate modifiche al pacchetto.
ms.assetid: 1f16a349-4919-46d2-9b78-2533b8679a73
title: Convalida di un database di installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6db262a280afa1d9222696d40a6f5949d69ece0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878537"
---
# <a name="validating-an-installation-database"></a><span data-ttu-id="cf9ce-103">Convalida di un database di installazione</span><span class="sxs-lookup"><span data-stu-id="cf9ce-103">Validating an Installation Database</span></span>

<span data-ttu-id="cf9ce-104">Gli autori dei pacchetti di installazione devono sempre eseguire la convalida sui pacchetti prima di tentare di installare il pacchetto per la prima volta ed eseguire di nuovo la convalida ogni volta che vengono apportate modifiche al pacchetto.</span><span class="sxs-lookup"><span data-stu-id="cf9ce-104">Authors of installation packages should always run validation on their packages before attempting to install the package for the first time and rerun validation whenever making any changes to the package.</span></span> <span data-ttu-id="cf9ce-105">La convalida esegue l'analisi del database per individuare eventuali errori che possono apparire validi singolarmente, ma che provocano un comportamento non corretto nel contesto dell'intero database.</span><span class="sxs-lookup"><span data-stu-id="cf9ce-105">Validation scans the database for errors that may appear valid individually but that cause incorrect behavior in the context of the whole database.</span></span> <span data-ttu-id="cf9ce-106">Il tentativo di installare un pacchetto che non riesce a eseguire la convalida può danneggiare il sistema dell'utente.</span><span class="sxs-lookup"><span data-stu-id="cf9ce-106">Attempting to install a package that fails validation can damage the user's system.</span></span> <span data-ttu-id="cf9ce-107">Vedere le sezioni [convalida dei pacchetti](package-validation.md) e [analizzatori di coerenza interni-CIEM](internal-consistency-evaluators-ices.md).</span><span class="sxs-lookup"><span data-stu-id="cf9ce-107">See the sections [Package Validation](package-validation.md) and [Internal Consistency Evaluators - ICEs](internal-consistency-evaluators-ices.md).</span></span>

<span data-ttu-id="cf9ce-108">È possibile convalidare il pacchetto di esempio utilizzando [Orca.exe](orca-exe.md) o [Msival2.exe](msival2-exe.md).</span><span class="sxs-lookup"><span data-stu-id="cf9ce-108">You can validate the sample package using [Orca.exe](orca-exe.md) or [Msival2.exe](msival2-exe.md).</span></span> <span data-ttu-id="cf9ce-109">Per visualizzare la guida per Msival2.exe modificare le directory e immettere nella riga di comando.</span><span class="sxs-lookup"><span data-stu-id="cf9ce-109">To view the help for Msival2.exe change directories and enter on the command line.</span></span>

<span data-ttu-id="cf9ce-110">Msival2 -?</span><span class="sxs-lookup"><span data-stu-id="cf9ce-110">Msival2 -?</span></span>

<span data-ttu-id="cf9ce-111">Il file con estensione cub Darice. cub contiene le azioni personalizzate ICE richieste da Msival2.exe per eseguire la convalida.</span><span class="sxs-lookup"><span data-stu-id="cf9ce-111">The .cub file darice.cub contains the ICE custom actions needed by Msival2.exe to perform validation.</span></span> <span data-ttu-id="cf9ce-112">Per convalidare il MNP2000.msi immettere</span><span class="sxs-lookup"><span data-stu-id="cf9ce-112">To validate the MNP2000.msi enter</span></span>

<span data-ttu-id="cf9ce-113">MSIVal2 MNP2000.msi Darice. cub</span><span class="sxs-lookup"><span data-stu-id="cf9ce-113">msival2 MNP2000.msi Darice.cub</span></span>

<span data-ttu-id="cf9ce-114">Per una descrizione dei messaggi di errore e di avviso restituiti dalla convalida, vedere la Guida di [riferimento a Ice](ice-reference.md).</span><span class="sxs-lookup"><span data-stu-id="cf9ce-114">For a description of the error and warning messages returned by validation see the [ICE Reference](ice-reference.md).</span></span> <span data-ttu-id="cf9ce-115">Correggere tutti gli errori nel pacchetto ed eseguire di nuovo la convalida se necessario finché il pacchetto non supera la convalida senza errori.</span><span class="sxs-lookup"><span data-stu-id="cf9ce-115">Correct all the errors in the package and rerun validation as necessary until the package passes validation without errors.</span></span>

<span data-ttu-id="cf9ce-116">Una volta che il pacchetto ha superato la convalida, è possibile installare il pacchetto di esempio facendo clic sull'icona MNP2000.msi o dalla riga di comando usando le [Opzioni della riga di comando](command-line-options.md).</span><span class="sxs-lookup"><span data-stu-id="cf9ce-116">Once the package passes validation, you can install the sample package by clicking on the MNP2000.msi icon or from the command line using the [Command Line Options](command-line-options.md).</span></span>

<span data-ttu-id="cf9ce-117">Questa operazione completa l'installazione di esempio.</span><span class="sxs-lookup"><span data-stu-id="cf9ce-117">This completes the sample installation.</span></span>

## <a name="next-example"></a><span data-ttu-id="cf9ce-118">Esempio successivo</span><span class="sxs-lookup"><span data-stu-id="cf9ce-118">Next example</span></span>

[<span data-ttu-id="cf9ce-119">Esempio di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="cf9ce-119">An Upgrade Example</span></span>](an-upgrade-example.md)

 

 



