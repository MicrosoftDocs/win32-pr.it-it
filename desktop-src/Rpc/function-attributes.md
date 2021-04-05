---
title: Attributi di funzioni
description: Gli attributi \ callback \ e \ Local \ possono essere applicati come attributi di funzione.
ms.assetid: 05e19164-072c-4a5a-878d-845273975854
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75ef199b937d5a3e9a8444be9ed65749da007ced
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729642"
---
# <a name="function-attributes"></a><span data-ttu-id="33ac2-103">Attributi di funzioni</span><span class="sxs-lookup"><span data-stu-id="33ac2-103">Function Attributes</span></span>

<span data-ttu-id="33ac2-104">Gli **\[** [](/windows/desktop/Midl/callback) **\]** attributi locali e di callback **\[** [](/windows/desktop/Midl/local) **\]** possono essere applicati come attributi di funzione.</span><span class="sxs-lookup"><span data-stu-id="33ac2-104">The **\[**[**callback**](/windows/desktop/Midl/callback)**\]** and **\[**[**local**](/windows/desktop/Midl/local)**\]** attributes can be applied as function attributes.</span></span>

<span data-ttu-id="33ac2-105">Un callback è una chiamata remota da server a client eseguita come parte di un thread di esecuzione singola concettuale.</span><span class="sxs-lookup"><span data-stu-id="33ac2-105">A callback is a remote call from server to client that executes as part of a conceptual single-execution thread.</span></span> <span data-ttu-id="33ac2-106">Un callback viene sempre emesso nel contesto di una chiamata remota (o callback) e viene eseguito dal thread che ha emesso la chiamata remota originale (o callback).</span><span class="sxs-lookup"><span data-stu-id="33ac2-106">A callback is always issued in the context of a remote call (or callback) and is executed by the thread that issued the original remote call (or callback).</span></span>

<span data-ttu-id="33ac2-107">Spesso è consigliabile inserire una dichiarazione di routine locale nel file IDL, perché si tratta della posizione logica per descrivere le interfacce a un pacchetto.</span><span class="sxs-lookup"><span data-stu-id="33ac2-107">It is often desirable to place a local procedure declaration in the IDL file, since this is the logical place to describe interfaces to a package.</span></span> <span data-ttu-id="33ac2-108">L' **\[** [](/windows/desktop/Midl/local) **\]** attributo local indica che una dichiarazione di routine non è in realtà una funzione remota, ma una procedura locale.</span><span class="sxs-lookup"><span data-stu-id="33ac2-108">The **\[**[**local**](/windows/desktop/Midl/local)**\]** attribute indicates that a procedure declaration is not actually a remote function, but a local procedure.</span></span> <span data-ttu-id="33ac2-109">Il compilatore MIDL non genera stub per le funzioni con l'attributo **\[ Local \]** .</span><span class="sxs-lookup"><span data-stu-id="33ac2-109">The MIDL compiler does not generate any stubs for functions with the **\[local\]** attribute.</span></span>

<span data-ttu-id="33ac2-110">È importante notare che l'uso del **\[** [**callback**](/windows/desktop/Midl/callback) **\]** non è consigliato nella programmazione multithread.</span><span class="sxs-lookup"><span data-stu-id="33ac2-110">It is important to note that the use of **\[**[**callback**](/windows/desktop/Midl/callback)**\]** is not recommended in multi-thread programming.</span></span> <span data-ttu-id="33ac2-111">Come funzione di programmazione a thread singolo, non è disponibile per supportare le richieste di sicurezza offerte da un ambiente multithread.</span><span class="sxs-lookup"><span data-stu-id="33ac2-111">As a single-thread programming function, it is not equipped to support the security demands a multi-thread environment provides.</span></span>

 

 