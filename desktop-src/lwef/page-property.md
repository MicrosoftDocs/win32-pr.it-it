---
title: Proprietà Page
description: Proprietà Page
ms.assetid: c3cf07e9-a324-443b-a0c0-2fb80463548f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c51f55e4d1e9c7d2d23713810412060d915c7af
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395947"
---
# <a name="page-property"></a><span data-ttu-id="3d8a7-103">Proprietà Page</span><span class="sxs-lookup"><span data-stu-id="3d8a7-103">Page Property</span></span>

<span data-ttu-id="3d8a7-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3d8a7-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="3d8a7-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="3d8a7-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="3d8a7-106">Restituisce o imposta la pagina visualizzata nella finestra delle proprietà di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="3d8a7-106">Returns or sets the page displayed in the Microsoft Agent property sheet window.</span></span>

</dd> <dt>

<span data-ttu-id="3d8a7-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="3d8a7-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span></span> 
</dt> <dd>

<span data-ttu-id="3d8a7-108">\*agente \* \* *.* \*  \[  =  *Stringa* PropertySheet.Page\]</span><span class="sxs-lookup"><span data-stu-id="3d8a7-108">*agent\*\*\*.PropertySheet.Page*\* \[ = *string*\]</span></span>



| <span data-ttu-id="3d8a7-109">Parte</span><span class="sxs-lookup"><span data-stu-id="3d8a7-109">Part</span></span>     | <span data-ttu-id="3d8a7-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3d8a7-110">Description</span></span>                                                                                                                                                                                                             |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d8a7-111">*string*</span><span class="sxs-lookup"><span data-stu-id="3d8a7-111">*string*</span></span> | <span data-ttu-id="3d8a7-112">Espressione stringa con uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="3d8a7-112">A string expression with one of the following values.</span></span> <span data-ttu-id="3d8a7-113">**"Sintesi vocale"** Visualizza la pagina di input vocale.</span><span class="sxs-lookup"><span data-stu-id="3d8a7-113">**"Speech"** Displays the Speech Input page.</span></span><br/> <span data-ttu-id="3d8a7-114">**"Output"** Consente di visualizzare la pagina di output.</span><span class="sxs-lookup"><span data-stu-id="3d8a7-114">**"Output"** Displays the Output page.</span></span><br/> <span data-ttu-id="3d8a7-115">**"Copyright"** Visualizza la pagina copyright.</span><span class="sxs-lookup"><span data-stu-id="3d8a7-115">**"Copyright"** Displays the Copyright page.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3d8a7-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="3d8a7-116">Remarks</span></span>

<span data-ttu-id="3d8a7-117">Se non è installato alcun motore vocale, l'impostazione della **pagina** su **"speech"** non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="3d8a7-117">If no speech engine is installed, setting **Page** to **"Speech"** has no effect.</span></span> <span data-ttu-id="3d8a7-118">Inoltre, la proprietà **Visible** della finestra deve essere impostata su **true** in modo che l'utente visualizzi la pagina.</span><span class="sxs-lookup"><span data-stu-id="3d8a7-118">Also, the window's **Visible** property must be set to **True** for the user to see the page.</span></span>

> [!Note]  
> <span data-ttu-id="3d8a7-119">L'utente può eseguire l'override di questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="3d8a7-119">The user can override this property.</span></span>

 

 

 





