---
title: Macro
description: Negli argomenti di questa sezione vengono fornite le specifiche di riferimento per i messaggi di input del puntatore e le macro di notifiche per il recupero di informazioni dai parametri dei messaggi di input del puntatore.
ms.assetid: 2324DCD0-DAE1-4AC2-AB36-23D114803138
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 07b099a9d0595278e7eb53960da42714763a7f90
ms.sourcegitcommit: f2fe9d9bd65333b74f2af8e30eddbb1643b40c8f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2020
ms.locfileid: "104398457"
---
# <a name="macros"></a><span data-ttu-id="7494f-103">Macro</span><span class="sxs-lookup"><span data-stu-id="7494f-103">Macros</span></span>

<span data-ttu-id="7494f-104">Negli argomenti di questa sezione vengono fornite le specifiche di riferimento per [i messaggi di input del puntatore e](messages-and-notifications-portal.md) le macro di notifiche per il recupero di informazioni dai parametri dei messaggi di input del puntatore.</span><span class="sxs-lookup"><span data-stu-id="7494f-104">The topics in this section provide the reference specifications for [Pointer Input Messages and Notifications](messages-and-notifications-portal.md) macros for retrieving information from pointer input message parameters.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="7494f-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="7494f-105">In this section</span></span>



| <span data-ttu-id="7494f-106">Argomento</span><span class="sxs-lookup"><span data-stu-id="7494f-106">Topic</span></span>                                                                                  | <span data-ttu-id="7494f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7494f-107">Description</span></span>                                                                                                                         |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7494f-108">**GET_POINTERID_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="7494f-108">**GET_POINTERID_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>                      | <span data-ttu-id="7494f-109">Recupera l'ID del puntatore usando il valore specificato.</span><span class="sxs-lookup"><span data-stu-id="7494f-109">Retrieves the pointer ID using the specified value.</span></span> <br/>                                                                     |
| [<span data-ttu-id="7494f-110">**HAS_POINTER_CONFIDENCE_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="7494f-110">**HAS_POINTER_CONFIDENCE_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>   | <span data-ttu-id="7494f-111">Controlla se il messaggio del puntatore specificato è considerato intenzionale anziché accidentale.</span><span class="sxs-lookup"><span data-stu-id="7494f-111">Checks whether the specified pointer message is considered intentional rather than accidental.</span></span><br/>                           |
| [<span data-ttu-id="7494f-112">**IS_POINTER_CANCELED_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="7494f-112">**IS_POINTER_CANCELED_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>         | <span data-ttu-id="7494f-113">Verifica se l'input del puntatore specificato è stato interrotto bruscamente oppure non è valido, a indicare che l'interazione non è stata completata.</span><span class="sxs-lookup"><span data-stu-id="7494f-113">Checks whether the specified pointer input ended abruptly, or was invalid, indicating the interaction was not completed.</span></span><br/> |
| [<span data-ttu-id="7494f-114">**IS_POINTER_FIFTHBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="7494f-114">**IS_POINTER_FIFTHBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>   | <span data-ttu-id="7494f-115">Controlla se il puntatore specificato ha avuto una quinta azione.</span><span class="sxs-lookup"><span data-stu-id="7494f-115">Checks whether the specified pointer took fifth action.</span></span> <br/>                                                                 |
| [<span data-ttu-id="7494f-116">**IS_POINTER_FIRSTBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="7494f-116">**IS_POINTER_FIRSTBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>   | <span data-ttu-id="7494f-117">Verifica se il puntatore specificato ha avuto la prima azione.</span><span class="sxs-lookup"><span data-stu-id="7494f-117">Checks whether the specified pointer took first action.</span></span><br/>                                                                  |
| [<span data-ttu-id="7494f-118">**IS_POINTER_FLAG_SET_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="7494f-118">**IS_POINTER_FLAG_SET_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>        | <span data-ttu-id="7494f-119">Verifica se una macro del puntatore imposta il flag specificato.</span><span class="sxs-lookup"><span data-stu-id="7494f-119">Checks whether a pointer macro sets the specified flag.</span></span> <br/>                                                                 |
| [<span data-ttu-id="7494f-120">**IS_POINTER_FOURTHBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="7494f-120">**IS_POINTER_FOURTHBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/> | <span data-ttu-id="7494f-121">Verifica se il puntatore specificato ha avuto una quarta azione.</span><span class="sxs-lookup"><span data-stu-id="7494f-121">Checks whether the specified pointer took fourth action.</span></span> <br/>                                                                |
| [<span data-ttu-id="7494f-122">**IS_POINTER_INCONTACT_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="7494f-122">**IS_POINTER_INCONTACT_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>       | <span data-ttu-id="7494f-123">Controlla se il puntatore specificato è in contatto.</span><span class="sxs-lookup"><span data-stu-id="7494f-123">Checks whether the specified pointer is in contact.</span></span> <br/>                                                                     |
| [<span data-ttu-id="7494f-124">**IS_POINTER_INRANGE_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="7494f-124">**IS_POINTER_INRANGE_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>           | <span data-ttu-id="7494f-125">Controlla se il puntatore specificato è compreso nell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="7494f-125">Checks whether the specified pointer is in range.</span></span> <br/>                                                                       |
| [<span data-ttu-id="7494f-126">**IS_POINTER_NEW_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="7494f-126">**IS_POINTER_NEW_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>                   | <span data-ttu-id="7494f-127">Controlla se il puntatore specificato è un nuovo puntatore.</span><span class="sxs-lookup"><span data-stu-id="7494f-127">Checks whether the specified pointer is a new pointer.</span></span> <br/>                                                                  |
| [<span data-ttu-id="7494f-128">**IS_POINTER_PRIMARY_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="7494f-128">**IS_POINTER_PRIMARY_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>           | <span data-ttu-id="7494f-129">Controlla se il puntatore specificato è il puntatore primario.</span><span class="sxs-lookup"><span data-stu-id="7494f-129">Checks whether the specified pointer is the primary pointer.</span></span> <br/>                                                            |
| [<span data-ttu-id="7494f-130">**IS_POINTER_SECONDBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="7494f-130">**IS_POINTER_SECONDBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/> | <span data-ttu-id="7494f-131">Verifica se il puntatore specificato ha impiegato una seconda azione.</span><span class="sxs-lookup"><span data-stu-id="7494f-131">Checks whether the specified pointer took second action.</span></span> <br/>                                                                |
| [<span data-ttu-id="7494f-132">**IS_POINTER_THIRDBUTTON_WPARAM**</span><span class="sxs-lookup"><span data-stu-id="7494f-132">**IS_POINTER_THIRDBUTTON_WPARAM**</span></span>](/previous-versions/windows/desktop/api)<br/>   | <span data-ttu-id="7494f-133">Verifica se il puntatore specificato ha intrapreso la terza azione.</span><span class="sxs-lookup"><span data-stu-id="7494f-133">Checks whether the specified pointer took third action.</span></span> <br/>                                                                 |



 

## <a name="related-topics"></a><span data-ttu-id="7494f-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7494f-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7494f-135">Riferimento al messaggio di input del puntatore</span><span class="sxs-lookup"><span data-stu-id="7494f-135">Pointer Input Message Reference</span></span>](wmpointer-reference.md)
</dt> </dl>

 

 





