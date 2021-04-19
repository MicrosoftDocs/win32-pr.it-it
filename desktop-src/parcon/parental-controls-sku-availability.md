---
description: Controllo parentale disponibilità SKU
ms.assetid: 5fbf6c4a-3897-4a12-bef6-19478fdb48aa
title: Controllo parentale disponibilità SKU
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b858bc62e8f10a3b06313befd99d67e497b8d442
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311581"
---
# <a name="parental-controls-sku-availability"></a><span data-ttu-id="7f037-103">Controllo parentale disponibilità SKU</span><span class="sxs-lookup"><span data-stu-id="7f037-103">Parental Controls SKU Availability</span></span>

<span data-ttu-id="7f037-104">Le interfacce utente, le funzionalità e le API dei controlli padre descritti in questa sezione sono attualmente pianificate per essere disponibili solo per gli SKU incentrati sul cliente, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="7f037-104">The Parental Controls user interfaces, features, and APIs described in this section are currently planned to be available only on consumer-focused SKUs such as:</span></span>

-   <span data-ttu-id="7f037-105">Windows Vista Starter</span><span class="sxs-lookup"><span data-stu-id="7f037-105">Windows Vista Starter</span></span>
-   <span data-ttu-id="7f037-106">Windows Vista Home Basic</span><span class="sxs-lookup"><span data-stu-id="7f037-106">Windows Vista Home Basic</span></span>
-   <span data-ttu-id="7f037-107">Windows Vista Home Premium</span><span class="sxs-lookup"><span data-stu-id="7f037-107">Windows Vista Home Premium</span></span>
-   <span data-ttu-id="7f037-108">Windows Vista Ultimate</span><span class="sxs-lookup"><span data-stu-id="7f037-108">Windows Vista Ultimate</span></span>

<span data-ttu-id="7f037-109">I controlli padre vengono installati solo in questi SKU.</span><span class="sxs-lookup"><span data-stu-id="7f037-109">Parental Controls only installs on these SKUs.</span></span> <span data-ttu-id="7f037-110">Le soluzioni che hanno un requisito per la distribuzione negli SKU aziendali dovranno:</span><span class="sxs-lookup"><span data-stu-id="7f037-110">Solutions having a requirement to deploy onto business SKUs will need to either:</span></span>

-   <span data-ttu-id="7f037-111">Rilevare e non fornire funzionalità di controllo parentale negli SKU aziendali.</span><span class="sxs-lookup"><span data-stu-id="7f037-111">Detect and not provide parental controls functionality on business SKUs.</span></span>
-   <span data-ttu-id="7f037-112">Rilevare e fornire un metodo alternativo di configurazione, registrazione e restrizioni.</span><span class="sxs-lookup"><span data-stu-id="7f037-112">Detect and provide an alternative means of configuration, logging, and restrictions.</span></span>

<span data-ttu-id="7f037-113">È consigliabile che le soluzioni rilevino la disponibilità dell'infrastruttura dei controlli padre controllando la riuscita di COM CoCreateInstance nell'API di conformità.</span><span class="sxs-lookup"><span data-stu-id="7f037-113">It is recommended that solutions detect availability of the Parental Controls Infrastructure by checking for success of COM CoCreateInstance on the Compliance API.</span></span>

<span data-ttu-id="7f037-114">Le applicazioni in grado di riconoscere i controlli padre, a seconda dell'infrastruttura di Windows Vista, possono anche voler evitare di visualizzare le impostazioni dell'interfaccia utente o altre funzionalità quando l'interfaccia utente dei controlli padre viene disattivata in uno SKU supportato.</span><span class="sxs-lookup"><span data-stu-id="7f037-114">Parental Controls-aware applications depending on the Windows Vista infrastructure may also want to suppress any of their own UI exposing settings or other functionality when Parental Controls UI is suppressed on a supported SKU.</span></span> <span data-ttu-id="7f037-115">Viene fornita una funzione per la determinazione della visibilità che copre casi come l'eliminazione aggiunta a un dominio.</span><span class="sxs-lookup"><span data-stu-id="7f037-115">A function is provided for visibility determination that covers cases such as domain-joined suppression.</span></span>

 

 



