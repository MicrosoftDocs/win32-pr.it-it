---
description: Controlli di attivazione Low-Memory COM+
ms.assetid: 9805dc94-da38-4b2c-b18c-5f494b49691b
title: Controlli di attivazione Low-Memory COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad955cb1ed47008f52f1cf9b17edfc43b92aa674
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483093"
---
# <a name="com-low-memory-activation-gates"></a><span data-ttu-id="690b3-103">Controlli di attivazione Low-Memory COM+</span><span class="sxs-lookup"><span data-stu-id="690b3-103">COM+ Low-Memory Activation Gates</span></span>

<span data-ttu-id="690b3-104">Il servizio COM+ per l'attivazione della memoria insufficiente controlla automaticamente la memoria prima della creazione di un oggetto o di un server COM+.</span><span class="sxs-lookup"><span data-stu-id="690b3-104">The COM+ low-memory activation gates service automatically checks memory before a COM+ server or object is created.</span></span> <span data-ttu-id="690b3-105">Se la percentuale di memoria virtuale disponibile per l'applicazione scende al di sotto di una soglia fissa, l'attivazione avrà esito negativo prima della creazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="690b3-105">If the percentage of virtual memory available to the application falls below a fixed threshold, the activation fails before the object is created.</span></span> <span data-ttu-id="690b3-106">In questo modo, il servizio Gates per l'attivazione di memoria bassa migliora significativamente l'affidabilità del sistema.</span><span class="sxs-lookup"><span data-stu-id="690b3-106">In this way, the low-memory activation gates service greatly enhances system reliability.</span></span>

<span data-ttu-id="690b3-107">Negli argomenti seguenti vengono fornite informazioni di base e attività sul servizio COM+ per l'attivazione di memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="690b3-107">The following topics provide background and task information about the COM+ low-memory activation gates service.</span></span>



| <span data-ttu-id="690b3-108">Argomento</span><span class="sxs-lookup"><span data-stu-id="690b3-108">Topic</span></span>                                                                                                 | <span data-ttu-id="690b3-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="690b3-109">Description</span></span>                                                                            |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="690b3-110">Concetti di COM+ Low-Memory Activation Gates</span><span class="sxs-lookup"><span data-stu-id="690b3-110">COM+ Low-Memory Activation Gates Concepts</span></span>](com--low-memory-activation-gates-concepts.md)<br/> | <span data-ttu-id="690b3-111">Viene fornita una panoramica del servizio COM+ per l'attivazione a memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="690b3-111">Provides an overview of the COM+ low-memory activation gates service.</span></span><br/>       |
| [<span data-ttu-id="690b3-112">Attività di controllo di attivazione Low-Memory COM+</span><span class="sxs-lookup"><span data-stu-id="690b3-112">COM+ Low-Memory Activation Gates Tasks</span></span>](com--low-memory-activation-gates-tasks.md)<br/>       | <span data-ttu-id="690b3-113">Questa funzionalità non è configurabile, quindi non sono presenti attività associate.</span><span class="sxs-lookup"><span data-stu-id="690b3-113">This feature is not configurable, so there are no tasks associated with it.</span></span><br/> |



 

 

 




