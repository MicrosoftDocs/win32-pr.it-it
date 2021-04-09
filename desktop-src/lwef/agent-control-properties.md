---
title: Proprietà del controllo agente
description: Proprietà del controllo agente
ms.assetid: e6a5b2db-9abf-4988-be41-fc7f4530507f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f5e80b10469e7e256b1b2bf3bcf55fb5a8a08b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044273"
---
# <a name="agent-control-properties"></a><span data-ttu-id="b6ed3-103">Proprietà del controllo agente</span><span class="sxs-lookup"><span data-stu-id="b6ed3-103">Agent Control Properties</span></span>

<span data-ttu-id="b6ed3-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b6ed3-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="b6ed3-105">Le proprietà seguenti sono accessibili direttamente dal controllo agente:</span><span class="sxs-lookup"><span data-stu-id="b6ed3-105">The following properties are directly accessed from the Agent control:</span></span>

-   [<span data-ttu-id="b6ed3-106">**Connesso**</span><span class="sxs-lookup"><span data-stu-id="b6ed3-106">**Connected**</span></span>](connected-property.md)
-   [<span data-ttu-id="b6ed3-107">**Nome**</span><span class="sxs-lookup"><span data-stu-id="b6ed3-107">**Name**</span></span>](name-property-a.md)
-   [<span data-ttu-id="b6ed3-108">**RaiseRequestErrors**</span><span class="sxs-lookup"><span data-stu-id="b6ed3-108">**RaiseRequestErrors**</span></span>](raiserequesterrors-property.md)

<span data-ttu-id="b6ed3-109">Inoltre, alcuni ambienti di programmazione possono assegnare proprietà aggiuntive in fase di progettazione o in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="b6ed3-109">In addition, some programming environments may assign additional design-time or run-time properties.</span></span> <span data-ttu-id="b6ed3-110">Ad esempio, Visual Basic aggiunge le proprietà Left, index, tag e top che definiscono la posizione del controllo in un form anche se il controllo non viene visualizzato nella pagina del form in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="b6ed3-110">For example, Visual Basic adds Left, Index, Tag, and Top properties that define the location of the control on a form even though the control does not appear on the form's page at run time.</span></span>

<span data-ttu-id="b6ed3-111">La proprietà Suspended è ancora supportata per la compatibilità con le versioni precedenti, ma restituisce sempre **false** perché il server non supporta più lo stato Suspended.</span><span class="sxs-lookup"><span data-stu-id="b6ed3-111">The Suspended property is still supported for backward compatibility, but always returns **False** because the server no longer supports a suspended state.</span></span>

 

 




