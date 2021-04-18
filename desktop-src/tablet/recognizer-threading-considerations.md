---
description: Anche se non è possibile accedere a un&\# 160; contesto di riconoscimento&\# 160; su due thread contemporaneamente dalla piattaforma Tablet PC, la funzione AdviseInkChange può essere chiamata in qualsiasi momento in qualsiasi thread.
ms.assetid: 2cd19819-08d0-418d-830b-2288a66ca0d0
title: Considerazioni sul threading del riconoscimento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4297cc28e084bbb7c1c09593deb5babc2319ab43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315555"
---
# <a name="recognizer-threading-considerations"></a><span data-ttu-id="ae0a1-103">Considerazioni sul threading del riconoscimento</span><span class="sxs-lookup"><span data-stu-id="ae0a1-103">Recognizer Threading Considerations</span></span>

<span data-ttu-id="ae0a1-104">Sebbene non sia possibile accedere a un [contesto di riconoscimento](hrecocontext-handle.md) su due thread contemporaneamente dalla piattaforma Tablet PC, la funzione [**AdviseInkChange**](/windows/desktop/api/recapis/nf-recapis-adviseinkchange) può essere chiamata in qualsiasi momento in qualsiasi thread.</span><span class="sxs-lookup"><span data-stu-id="ae0a1-104">Although a [recognizer context](hrecocontext-handle.md) cannot be accessed on two threads simultaneously by the Tablet PC platform, the [**AdviseInkChange**](/windows/desktop/api/recapis/nf-recapis-adviseinkchange) function can be called at any time on any thread.</span></span> <span data-ttu-id="ae0a1-105">Poiché la piattaforma Tablet PC non garantisce la presenza di un solo contesto di riconoscimento alla volta, due contesti di riconoscimento distinti in thread distinti possono tentare contemporaneamente di accedere al [riconoscimento](hrecognizer-handle.md).</span><span class="sxs-lookup"><span data-stu-id="ae0a1-105">Because the Tablet PC platform does not ensure that there is only one recognizer context at a time, two separate recognizer contexts in separate threads may simultaneously attempt to access your [recognizer](hrecognizer-handle.md).</span></span> <span data-ttu-id="ae0a1-106">Pertanto, le variabili globali nel motore di riconoscimento devono essere thread-safe.</span><span class="sxs-lookup"><span data-stu-id="ae0a1-106">Therefore, global variables in your recognition engine must be thread-safe.</span></span>

<span data-ttu-id="ae0a1-107">Gli elenchi di parole sono un'implementazione facoltativa usata per aumentare la precisione.</span><span class="sxs-lookup"><span data-stu-id="ae0a1-107">Word lists are an optional implementation used to increase accuracy.</span></span> <span data-ttu-id="ae0a1-108">Se il riconoscimento implementa elenchi di parole, deve essere thread-safe.</span><span class="sxs-lookup"><span data-stu-id="ae0a1-108">If your recognizer implements word lists, it must be thread-safe.</span></span> <span data-ttu-id="ae0a1-109">Per ulteriori informazioni sull'utilizzo degli elenchi di parole, vedere [utilizzo dei dizionari delle applicazioni](using-application-dictionaries.md).</span><span class="sxs-lookup"><span data-stu-id="ae0a1-109">For more information about using word lists, see [Using Application Dictionaries](using-application-dictionaries.md).</span></span>

<span data-ttu-id="ae0a1-110">Per informazioni dettagliate sulle altre considerazioni relative al threading, vedere [considerazioni sul threading di Tablet PC](tablet-pc-threading-considerations.md).</span><span class="sxs-lookup"><span data-stu-id="ae0a1-110">For details about other threading considerations, see [Tablet PC Threading Considerations](tablet-pc-threading-considerations.md).</span></span>

 

 



