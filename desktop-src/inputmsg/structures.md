---
title: Strutture (messaggi di input del puntatore e notifiche)
description: Negli argomenti di questa sezione vengono fornite le specifiche di riferimento per le strutture di notifiche e messaggi di input del puntatore.
ms.assetid: 2224DCD0-DAE1-4AC2-AB36-23D114801138
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: bc796c3924df9a1a349ea2180123f88f56d6a96c
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/26/2021
ms.locfileid: "106334017"
---
# <a name="pointer-input-messages-and-notifications-structures"></a><span data-ttu-id="0fd27-103">Strutture di notifiche e messaggi di input del puntatore</span><span class="sxs-lookup"><span data-stu-id="0fd27-103">Pointer Input Messages and Notifications structures</span></span>

<span data-ttu-id="0fd27-104">Negli argomenti di questa sezione vengono fornite le specifiche di riferimento per le strutture di [notifiche e messaggi di input del puntatore](messages-and-notifications-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="0fd27-104">The topics in this section provide the reference specifications for [Pointer Input Messages and Notifications](messages-and-notifications-portal.md) structures.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="0fd27-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="0fd27-105">In this section</span></span>



| <span data-ttu-id="0fd27-106">Argomento</span><span class="sxs-lookup"><span data-stu-id="0fd27-106">Topic</span></span>                                                                            | <span data-ttu-id="0fd27-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0fd27-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0fd27-108">**INPUT_TRANSFORM**</span><span class="sxs-lookup"><span data-stu-id="0fd27-108">**INPUT_TRANSFORM**</span></span>](/previous-versions/windows/desktop/api)<br/>                           | <span data-ttu-id="0fd27-109">Definisce la matrice che rappresenta una trasformazione in un consumer di messaggi.</span><span class="sxs-lookup"><span data-stu-id="0fd27-109">Defines the matrix that represents a transform on a message consumer.</span></span> <span data-ttu-id="0fd27-110">Questa matrice può essere utilizzata per trasformare i dati di input del puntatore da coordinate client a coordinate dello schermo, mentre l'inverso può essere utilizzato per trasformare i dati di input del puntatore dalle coordinate dello schermo alle coordinate del client.</span><span class="sxs-lookup"><span data-stu-id="0fd27-110">This matrix can be used to transform pointer input data from client coordinates to screen coordinates, while the inverse can be used to transform pointer input data from screen coordinates to client coordinates.</span></span> <br/>                                                                 |
| [<span data-ttu-id="0fd27-111">**POINTER_INFO**</span><span class="sxs-lookup"><span data-stu-id="0fd27-111">**POINTER_INFO**</span></span>](/previous-versions/windows/desktop/api)<br/>                          | <span data-ttu-id="0fd27-112">Contiene informazioni di base sul puntatore comuni a tutti i tipi di puntatore.</span><span class="sxs-lookup"><span data-stu-id="0fd27-112">Contains basic pointer information common to all pointer types.</span></span> <span data-ttu-id="0fd27-113">Le applicazioni possono recuperare queste informazioni usando le funzioni [**GetPointerInfo**](/previous-versions/windows/desktop/api), [**GetPointerFrameInfo**](/previous-versions/windows/desktop/api), [**GetPointerInfoHistory**](/previous-versions/windows/desktop/api) e [**GetPointerFrameInfoHistory**](/previous-versions/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="0fd27-113">Applications can retrieve this information using the [**GetPointerInfo**](/previous-versions/windows/desktop/api), [**GetPointerFrameInfo**](/previous-versions/windows/desktop/api), [**GetPointerInfoHistory**](/previous-versions/windows/desktop/api) and [**GetPointerFrameInfoHistory**](/previous-versions/windows/desktop/api) functions.</span></span> <br/> |
| [<span data-ttu-id="0fd27-114">**POINTER_PEN_INFO**</span><span class="sxs-lookup"><span data-stu-id="0fd27-114">**POINTER_PEN_INFO**</span></span>](/previous-versions/windows/desktop/api)<br/>                 | <span data-ttu-id="0fd27-115">Definisce informazioni di base sulla penna comuni a tutti i tipi di puntatore.</span><span class="sxs-lookup"><span data-stu-id="0fd27-115">Defines basic pen information common to all pointer types.</span></span> <br/>                                                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="0fd27-116">**POINTER_TOUCH_INFO**</span><span class="sxs-lookup"><span data-stu-id="0fd27-116">**POINTER_TOUCH_INFO**</span></span>](/previous-versions/windows/desktop/api)<br/>             | <span data-ttu-id="0fd27-117">Definisce le informazioni di base sul tocco comuni a tutti i tipi di puntatore.</span><span class="sxs-lookup"><span data-stu-id="0fd27-117">Defines basic touch information common to all pointer types.</span></span><br/>                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="0fd27-118">**TOUCHPREDICTIONPARAMETERS**</span><span class="sxs-lookup"><span data-stu-id="0fd27-118">**TOUCHPREDICTIONPARAMETERS**</span></span>](/previous-versions/windows/desktop/api)<br/> | <span data-ttu-id="0fd27-119">Contiene i dettagli di input dell'hardware che possono essere usati per stimare le destinazioni tocco e per compensare la latenza hardware durante l'elaborazione dell'input tocco e movimento che contiene i dati relativi alla distanza e alla velocità.</span><span class="sxs-lookup"><span data-stu-id="0fd27-119">Contains hardware input details that can be used to predict touch targets and help compensate for hardware latency when processing touch and gesture input that contains distance and velocity data.</span></span><br/>                                                                                                                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="0fd27-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0fd27-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0fd27-121">Riferimento al messaggio di input del puntatore</span><span class="sxs-lookup"><span data-stu-id="0fd27-121">Pointer Input Message Reference</span></span>](wmpointer-reference.md)
</dt> </dl>

 

 





