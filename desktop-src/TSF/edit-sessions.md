---
title: Sessioni di modifica
description: Quando un servizio di testo deve ottenere, modificare o impostare il testo in un contesto, deve richiedere una sessione di modifica.
ms.assetid: e4115227-1036-4892-986d-dc4cef5b178e
keywords:
- Framework servizi di testo (TSF), modifica sessione
- TSF (Framework di servizi di testo), modifica sessione
- Servizi di testo, modifica sessione
- sessione di modifica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81897c3c63539626776b693a22be9096f973d02e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104516051"
---
# <a name="edit-sessions"></a><span data-ttu-id="85f0a-107">Sessioni di modifica</span><span class="sxs-lookup"><span data-stu-id="85f0a-107">Edit Sessions</span></span>

<span data-ttu-id="85f0a-108">Quando un servizio di testo deve ottenere, modificare o impostare il testo in un contesto, deve richiedere una *sessione di modifica*.</span><span class="sxs-lookup"><span data-stu-id="85f0a-108">When a text service must obtain, modify, or set text in a context, it must request an *edit session*.</span></span> <span data-ttu-id="85f0a-109">Quando viene richiesta una sessione di modifica, il gestore TSF negozia con il proprietario del contesto di destinazione per un blocco del documento del tipo richiesto.</span><span class="sxs-lookup"><span data-stu-id="85f0a-109">When an edit session is requested, the TSF manager negotiates with the owner of the target context for a document lock of the requested type.</span></span> <span data-ttu-id="85f0a-110">Quando viene concesso il blocco del documento, gestione TSF consente al servizio di testo di leggere e/o scrivere testo da o verso il contesto.</span><span class="sxs-lookup"><span data-stu-id="85f0a-110">When the document lock is granted, the TSF manager enables the text service to read and/or write text to or from the context.</span></span>

 

 




