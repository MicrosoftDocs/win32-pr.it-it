---
description: Un'applicazione abilitata per l'input penna comunica con il sistema di riconoscimento tramite le API della piattaforma Tablet PC.
ms.assetid: 0ea6881f-d2d7-4646-9c41-53d1c03ea55b
title: Architettura dell'API di riconoscimento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72838b77e11092cacd4adb998c669167940ecad2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104554533"
---
# <a name="recognition-api-architecture"></a><span data-ttu-id="8d449-103">Architettura dell'API di riconoscimento</span><span class="sxs-lookup"><span data-stu-id="8d449-103">Recognition API Architecture</span></span>

<span data-ttu-id="8d449-104">Un'applicazione abilitata per l'input penna comunica con il sistema di riconoscimento tramite le API della piattaforma Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="8d449-104">An ink-enabled application communicates with the recognition system through the Tablet PC Platform APIs.</span></span> <span data-ttu-id="8d449-105">Per eseguire questa operazione, le applicazioni utilizzano l'oggetto [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) .</span><span class="sxs-lookup"><span data-stu-id="8d449-105">Applications use the [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) object to accomplish this.</span></span> <span data-ttu-id="8d449-106">La piattaforma Tablet PC interagisce con il riconoscimento usando le interfacce di tipo C documentate in questa sezione.</span><span class="sxs-lookup"><span data-stu-id="8d449-106">The Tablet PC Platform interacts with your recognizer by using the C-style interfaces that are documented in this section.</span></span> <span data-ttu-id="8d449-107">Nell'illustrazione seguente, l'area all'interno della linea tratteggiata mostra quanto descritto in questa sezione.</span><span class="sxs-lookup"><span data-stu-id="8d449-107">In the following illustration, the area inside the dashed line shows what is documented in this section.</span></span>

![illustrazione dell'architettura di riconoscimento con il riconoscimento evidenziato](images/96ee7367-7b8a-4794-99c1-bcac9daed645.gif)

<span data-ttu-id="8d449-109">Un riconoscitore personalizzato deve includere il file recapit. h (installato per impostazione predefinita in C: \\ programmi \\ Microsoft Tablet PC Platform SDK \\ ).</span><span class="sxs-lookup"><span data-stu-id="8d449-109">A custom recognizer must include Recapis.h (installed by default in C:\\Program Files\\Microsoft Tablet PC Platform SDK\\Include).</span></span> <span data-ttu-id="8d449-110">Ad eccezione di quanto indicato, la libreria di collegamento dinamico (DLL) deve esportare tutte le funzioni API, anche se si sceglie di fare in modo che vengano restituite E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="8d449-110">Except where noted, your dynamic-link library (DLL) must export all of the API functions, even if you choose to have some of them return E\_NOTIMPL.</span></span>

<span data-ttu-id="8d449-111">In nessuna circostanza il riconoscimento verrà chiamato direttamente da un'applicazione abilitata per l'input penna.</span><span class="sxs-lookup"><span data-stu-id="8d449-111">Under no circumstances will your recognizer be called directly by an ink-enabled application.</span></span> <span data-ttu-id="8d449-112">Al contrario, le applicazioni chiamano le API di automazione o le API gestite per ottenere risultati dal riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="8d449-112">Instead, applications will call either the Automation APIs or the Managed APIs to get results from your recognizer.</span></span>

 

 



