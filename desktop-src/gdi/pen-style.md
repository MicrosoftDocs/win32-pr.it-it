---
description: L'attributo di stile specifica il modello di linea visualizzato quando viene usata una particolare penna cosmetica o geometrica. Sono disponibili otto stili di penna predefiniti. Nella figura seguente sono illustrati i sette stili definiti dal sistema.
ms.assetid: a9aaa999-529c-46e1-9a3f-b6fdcbeb5b51
title: Stile penna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f447839627f97d7662fdef35bd7088ef7b0dcba5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967056"
---
# <a name="pen-style"></a><span data-ttu-id="3e553-105">Stile penna</span><span class="sxs-lookup"><span data-stu-id="3e553-105">Pen Style</span></span>

<span data-ttu-id="3e553-106">L'attributo di stile specifica il modello di linea visualizzato quando viene usata una particolare penna cosmetica o geometrica.</span><span class="sxs-lookup"><span data-stu-id="3e553-106">The style attribute specifies the line pattern that appears when a particular cosmetic or geometric pen is used.</span></span> <span data-ttu-id="3e553-107">Sono disponibili otto stili di penna predefiniti.</span><span class="sxs-lookup"><span data-stu-id="3e553-107">There are eight predefined pen styles.</span></span> <span data-ttu-id="3e553-108">Nella figura seguente sono illustrati i sette stili definiti dal sistema.</span><span class="sxs-lookup"><span data-stu-id="3e553-108">The following illustration shows the seven of these styles that are defined by the system.</span></span>

![illustrazione che mostra sette righe, ciascuna disegnata usando uno stile predefinito diverso](images/cspen-01.png)

<span data-ttu-id="3e553-110">Lo stile frame interno è identico allo stile solido per le penne cosmetiche.</span><span class="sxs-lookup"><span data-stu-id="3e553-110">The inside-frame style is identical to the solid style for cosmetic pens.</span></span> <span data-ttu-id="3e553-111">Tuttavia, funziona in modo diverso quando viene usato con una penna geometrica.</span><span class="sxs-lookup"><span data-stu-id="3e553-111">However, it operates differently when used with a geometric pen.</span></span> <span data-ttu-id="3e553-112">Se la penna geometrica è più ampia rispetto a un singolo pixel e una funzione di disegno usa la penna per disegnare un bordo intorno a un oggetto riempito, il sistema disegna il bordo all'interno del frame dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="3e553-112">If the geometric pen is wider than a single pixel and a drawing function uses the pen to draw a border around a filled object, the system draws the border inside the object's frame.</span></span> <span data-ttu-id="3e553-113">Utilizzando lo stile frame interno, un'applicazione può garantire che un oggetto venga visualizzato interamente all'interno delle dimensioni specificate, indipendentemente dalla larghezza della penna geometrica.</span><span class="sxs-lookup"><span data-stu-id="3e553-113">By using the inside-frame style, an application can ensure that an object appears entirely within the specified dimensions, regardless of the geometric pen width.</span></span>

<span data-ttu-id="3e553-114">Oltre ai sette stili definiti dal sistema, esiste un ottavo stile definito da utente (o applicazione).</span><span class="sxs-lookup"><span data-stu-id="3e553-114">In addition to the seven styles defined by the system, there is an eighth style that is user (or application) defined.</span></span> <span data-ttu-id="3e553-115">Uno stile definito dall'utente genera linee con una serie personalizzata di trattini e punti.</span><span class="sxs-lookup"><span data-stu-id="3e553-115">A user-defined style generates lines with a customized series of dashes and dots.</span></span>

<span data-ttu-id="3e553-116">Usare la funzione [**CreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-createpen), [**CreatePenIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect)o [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) per creare una penna con stili definiti dal sistema.</span><span class="sxs-lookup"><span data-stu-id="3e553-116">Use the [**CreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-createpen), [**CreatePenIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect), or [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) function to create a pen that has the system-defined styles.</span></span> <span data-ttu-id="3e553-117">Utilizzare la funzione **ExtCreatePen** per creare una penna con stile definito dall'utente.</span><span class="sxs-lookup"><span data-stu-id="3e553-117">Use the **ExtCreatePen** function to create a pen that has a user-defined style.</span></span>

 

 



