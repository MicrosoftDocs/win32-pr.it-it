---
description: Se le regole di selezione predefinita non soddisfano le esigenze dell'applicazione, l'applicazione ha la possibilità di selezionare il terminale manualmente.
ms.assetid: 12d7781e-a27d-4cbe-b7c4-6c0dfef11074
title: Selezione terminale manuale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95335402690c57cc3f564f5d238ca031df4b3549
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755114"
---
# <a name="manual-terminal-selection"></a><span data-ttu-id="57127-103">Selezione terminale manuale</span><span class="sxs-lookup"><span data-stu-id="57127-103">Manual Terminal Selection</span></span>

<span data-ttu-id="57127-104">Se le regole di selezione predefinita non soddisfano le esigenze dell'applicazione, l'applicazione è in grado di selezionare il terminale perché è sempre disponibile, ovvero può usare [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) per enumerare i flussi presenti nella chiamata e selezionare il terminale nei flussi appropriati (o, nel caso di terminali multitraccia, creare tracce per i flussi e selezionare le tracce create nei flussi).</span><span class="sxs-lookup"><span data-stu-id="57127-104">If the rules of Default selection do not meet the needs of the application, the application has the option of selecting the terminal as it always has: that is, it can use [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) to enumerate the streams present on the call and select the terminal on the appropriate streams (or, in case of multitrack terminals, create tracks for the streams and select created tracks on the streams).</span></span>

 

 
