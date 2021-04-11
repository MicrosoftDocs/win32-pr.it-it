---
description: Il carattere di escape della stampante fornito da Windows a 16 bit ha consentito l'accesso alle funzionalità speciali del dispositivo.
ms.assetid: 4bdd1d47-8cf4-4088-aec8-88193e71a828
title: Caratteri di escape della stampante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59463c4201e97c5ac1ec689a772581fab28314b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232135"
---
# <a name="printer-escapes"></a><span data-ttu-id="a4e08-103">Caratteri di escape della stampante</span><span class="sxs-lookup"><span data-stu-id="a4e08-103">Printer Escapes</span></span>

<span data-ttu-id="a4e08-104">Il carattere di escape della stampante fornito da Windows a 16 bit ha consentito l'accesso alle funzionalità speciali del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a4e08-104">The printer escapes provided by 16-bit Windows allowed access special device features.</span></span> <span data-ttu-id="a4e08-105">La maggior parte di questi caratteri di escape è obsoleta, ma ne sono stati forniti alcuni per semplificare il porting delle applicazioni basate su Windows a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="a4e08-105">Most of these escapes are obsolete, but a few are provided to simplify the porting of 16-bit Windows-based applications.</span></span> <span data-ttu-id="a4e08-106">GDI supporta un set completo di funzioni di percorso che le applicazioni possono usare al posto degli escape per tracciare i percorsi su qualsiasi dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a4e08-106">GDI supports a complete set of path functions that applications can use instead of the escapes to draw paths on any device.</span></span> <span data-ttu-id="a4e08-107">Per un elenco di funzioni che sostituiscono alcuni caratteri di escape, vedere la funzione [**escape**](/windows/desktop/api/Wingdi/nf-wingdi-escape) .</span><span class="sxs-lookup"><span data-stu-id="a4e08-107">For a list of functions that replace some of the escapes, see the [**Escape**](/windows/desktop/api/Wingdi/nf-wingdi-escape) function.</span></span>

<span data-ttu-id="a4e08-108">Delle 64 di escape della stampante originale, è possibile usare solo **QUERYESCSUPPORT** e **PassThrough** .</span><span class="sxs-lookup"><span data-stu-id="a4e08-108">Of the 64 original printer escapes, only **QUERYESCSUPPORT** and **PASSTHROUGH** can be used.</span></span>

<span data-ttu-id="a4e08-109">È disponibile anche una funzione di escape estesa denominata [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).</span><span class="sxs-lookup"><span data-stu-id="a4e08-109">There is also an extended escape function called [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).</span></span> <span data-ttu-id="a4e08-110">Questa funzione consente alle applicazioni di accedere alle funzionalità di un dispositivo specifico non direttamente disponibili tramite GDI.</span><span class="sxs-lookup"><span data-stu-id="a4e08-110">This function allows applications to access capabilities of a particular device not directly available through GDI.</span></span>

 

 



