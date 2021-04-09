---
description: Il Windows Installer fornisce molte azioni predefinite per l'esecuzione del processo di installazione. Per un elenco di queste azioni, vedere le informazioni di riferimento sulle azioni standard.
ms.assetid: 4a1f3ccc-4904-47d0-bfc6-013e404de47e
title: Azioni personalizzate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9623351bdcd4cd109d2112724d13e0f9ccaa6b2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050152"
---
# <a name="custom-actions"></a><span data-ttu-id="5ab96-104">Azioni personalizzate</span><span class="sxs-lookup"><span data-stu-id="5ab96-104">Custom Actions</span></span>

<span data-ttu-id="5ab96-105">Il Windows Installer fornisce molte azioni predefinite per l'esecuzione del processo di installazione.</span><span class="sxs-lookup"><span data-stu-id="5ab96-105">The Windows Installer provides many built-in actions for performing the installation process.</span></span> <span data-ttu-id="5ab96-106">Per un elenco di queste azioni, vedere le informazioni di [riferimento sulle azioni standard](standard-actions-reference.md).</span><span class="sxs-lookup"><span data-stu-id="5ab96-106">For a list of these actions, see the [Standard Actions Reference](standard-actions-reference.md).</span></span>

<span data-ttu-id="5ab96-107">Le azioni standard sono sufficienti per eseguire un'installazione nella maggior parte dei casi.</span><span class="sxs-lookup"><span data-stu-id="5ab96-107">Standard actions are sufficient to execute an installation in most cases.</span></span> <span data-ttu-id="5ab96-108">Tuttavia, esistono situazioni in cui lo sviluppatore di un pacchetto di installazione rileva che è necessario scrivere un'azione personalizzata.</span><span class="sxs-lookup"><span data-stu-id="5ab96-108">However, there are situations where the developer of an installation package finds it necessary to write a custom action.</span></span> <span data-ttu-id="5ab96-109">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="5ab96-109">For example:</span></span>

-   <span data-ttu-id="5ab96-110">Si vuole avviare un file eseguibile durante l'installazione installato nel computer dell'utente o installato con l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5ab96-110">You want to launch an executable during installation that is installed on the user's machine or that is being installed with the application.</span></span>
-   <span data-ttu-id="5ab96-111">Si desidera chiamare funzioni speciali durante un'installazione definita in una libreria a collegamento dinamico (DLL).</span><span class="sxs-lookup"><span data-stu-id="5ab96-111">You want to call special functions during an installation that are defined in a dynamic-link library (DLL).</span></span>
-   <span data-ttu-id="5ab96-112">Si desidera utilizzare le funzioni scritte nei linguaggi di sviluppo Microsoft Visual Basic Scripting Edition o testo script letterale di Microsoft JScript durante un'installazione.</span><span class="sxs-lookup"><span data-stu-id="5ab96-112">You want to use functions written in the development languages Microsoft Visual Basic Scripting Edition or Microsoft JScript literal script text during an installation.</span></span>
-   <span data-ttu-id="5ab96-113">Si desidera rinviare l'esecuzione di alcune azioni fino al momento in cui viene eseguito lo script di installazione.</span><span class="sxs-lookup"><span data-stu-id="5ab96-113">You want to defer the execution of some actions until the time when the installation script is being executed.</span></span>
-   <span data-ttu-id="5ab96-114">Si desidera aggiungere informazioni sull'ora e sullo stato di avanzamento a un controllo ProgressBar e a un controllo di testo TimeRemaining.</span><span class="sxs-lookup"><span data-stu-id="5ab96-114">You want to add time and progress information to a ProgressBar control and a TimeRemaining Text control.</span></span>

<span data-ttu-id="5ab96-115">Nelle sezioni seguenti vengono descritte le azioni personalizzate e le modalità di incorporamento in un pacchetto di installazione:</span><span class="sxs-lookup"><span data-stu-id="5ab96-115">The following sections describe custom actions and how to incorporate them into an installation package:</span></span>

-   [<span data-ttu-id="5ab96-116">Informazioni sulle azioni personalizzate</span><span class="sxs-lookup"><span data-stu-id="5ab96-116">About Custom Actions</span></span>](about-custom-actions.md)
-   [<span data-ttu-id="5ab96-117">Uso di azioni personalizzate</span><span class="sxs-lookup"><span data-stu-id="5ab96-117">Using Custom Actions</span></span>](using-custom-actions.md)
-   [<span data-ttu-id="5ab96-118">Riferimento all'azione personalizzata</span><span class="sxs-lookup"><span data-stu-id="5ab96-118">Custom Action Reference</span></span>](custom-action-reference.md)
-   [<span data-ttu-id="5ab96-119">Elenco riepilogativo di tutti i tipi di azione personalizzati</span><span class="sxs-lookup"><span data-stu-id="5ab96-119">Summary List of All Custom Action Types</span></span>](summary-list-of-all-custom-action-types.md)

 

 



