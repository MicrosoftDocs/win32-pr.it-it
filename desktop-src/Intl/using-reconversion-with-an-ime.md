---
description: Un IME implementa una funzionalità denominata &\# 0034; riconversione&\# 0034;.
ms.assetid: 32b20872-7e5c-487e-99bb-9447ac3aebd4
title: Utilizzo della riconversione con un IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e28383a27fd7fd7827cbbf3c7ff97c895fb4a72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305632"
---
# <a name="using-reconversion-with-an-ime"></a><span data-ttu-id="2f06a-103">Utilizzo della riconversione con un IME</span><span class="sxs-lookup"><span data-stu-id="2f06a-103">Using Reconversion with an IME</span></span>

<span data-ttu-id="2f06a-104">Un IME implementa una funzionalità denominata "riconversione".</span><span class="sxs-lookup"><span data-stu-id="2f06a-104">An IME implements a feature called "reconversion".</span></span> <span data-ttu-id="2f06a-105">In genere l'IMM determina gli elenchi di candidati solo in base alle voci digitate dall'utente.</span><span class="sxs-lookup"><span data-stu-id="2f06a-105">Normally the IMM determines the lists of candidates based only on entries typed by the user.</span></span> <span data-ttu-id="2f06a-106">La riconversione consente a IMM di determinare uno o più candidati in base alla frase che lo contiene (contesto).</span><span class="sxs-lookup"><span data-stu-id="2f06a-106">Reconversion allows the IMM to determine one or more candidates based on the containing sentence (the context).</span></span> <span data-ttu-id="2f06a-107">I tipi di riconversione definiti sono semplici, normali e avanzati.</span><span class="sxs-lookup"><span data-stu-id="2f06a-107">The defined reconversion types are simple, normal, and enhanced.</span></span>

<span data-ttu-id="2f06a-108">La riconversione è utile quando un utente nota un errore di composizione in un documento.</span><span class="sxs-lookup"><span data-stu-id="2f06a-108">Reconversion is useful when a user notices a composition error in a document.</span></span> <span data-ttu-id="2f06a-109">L'utente può selezionare l'errore e scegliere riconversione da un menu.</span><span class="sxs-lookup"><span data-stu-id="2f06a-109">The user can select the error and choose reconversion from a menu.</span></span> <span data-ttu-id="2f06a-110">L'IME usa il contesto per determinare la sostituzione migliore.</span><span class="sxs-lookup"><span data-stu-id="2f06a-110">The IME uses the context to determine the best replacement.</span></span> <span data-ttu-id="2f06a-111">L'applicazione può usare [**ImmSetCompositionString**](/windows/desktop/api/Imm/nf-imm-immsetcompositionstringa) per supportare la riconversione.</span><span class="sxs-lookup"><span data-stu-id="2f06a-111">The application can use [**ImmSetCompositionString**](/windows/desktop/api/Imm/nf-imm-immsetcompositionstringa) to support reconversion.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2f06a-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2f06a-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f06a-113">Uso di gestione metodi di input</span><span class="sxs-lookup"><span data-stu-id="2f06a-113">Using Input Method Manager</span></span>](using-input-method-manager.md)
</dt> </dl>

 

 



