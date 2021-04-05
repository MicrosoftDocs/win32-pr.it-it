---
description: Un gestore dell'interfaccia utente esterno può restituire un numero qualsiasi di valori da Windows Installer a seconda del tipo di pulsante fornito nel parametro di tipo del messaggio passato dal programma di installazione al gestore.
ms.assetid: a918082d-709d-4b4f-ae3b-5f16ed0ca910
title: Restituzione di valori da un gestore di interfaccia utente esterno
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b466f6bc3cc034551a01bd2b87caa7292824e0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754202"
---
# <a name="returning-values-from-an-external-user-interface-handler"></a><span data-ttu-id="4e38a-103">Restituzione di valori da un gestore di interfaccia utente esterno</span><span class="sxs-lookup"><span data-stu-id="4e38a-103">Returning Values from an External User Interface Handler</span></span>

<span data-ttu-id="4e38a-104">Un gestore dell'interfaccia utente esterno può restituire un numero qualsiasi di valori da Windows Installer a seconda del tipo di pulsante fornito nel parametro di tipo del messaggio passato dal programma di installazione al gestore.</span><span class="sxs-lookup"><span data-stu-id="4e38a-104">An external user interface (UI) handler can return any number of values to Windows Installer depending on the button type provided in the message type parameter the installer passes to the handler.</span></span>

<span data-ttu-id="4e38a-105">Il gestore dell'interfaccia utente esterno può restituire i valori – 1 e 0 in qualsiasi momento, perché non sono correlati ai tipi di pulsanti.</span><span class="sxs-lookup"><span data-stu-id="4e38a-105">The external UI handler can return the values –1 and 0 at any time because these are not related to the button types.</span></span> <span data-ttu-id="4e38a-106">Un valore restituito di – 1 indica che si è verificato un errore interno nel gestore dell'interfaccia utente esterno.</span><span class="sxs-lookup"><span data-stu-id="4e38a-106">A return value of –1 indicates that an internal error occurred in the external UI handler.</span></span> <span data-ttu-id="4e38a-107">Un valore restituito pari a 0 indica che il gestore dell'interfaccia utente esterno non ha gestito il messaggio del programma di installazione e che il programma di installazione deve gestire il messaggio.</span><span class="sxs-lookup"><span data-stu-id="4e38a-107">A return value of 0 indicates that the external UI handler has not handled the installer message and the installer must handle the message instead.</span></span>

<span data-ttu-id="4e38a-108">Per i messaggi che non includono un tipo di pulsante, ad esempio INSTALLMESSAGE \_ ACTIONDATA e INSTALLMESSAGE \_ Progress, la restituzione di IDCANCEL Annulla l'installazione.</span><span class="sxs-lookup"><span data-stu-id="4e38a-108">For messages that do not include a button type, such as INSTALLMESSAGE\_ACTIONDATA and INSTALLMESSAGE\_PROGRESS, returning IDCANCEL cancels the installation.</span></span> <span data-ttu-id="4e38a-109">La restituzione di IDOK notifica al programma di installazione che il messaggio è stato gestito dal gestore dell'interfaccia utente esterno.</span><span class="sxs-lookup"><span data-stu-id="4e38a-109">Returning IDOK notifies the installer that the message was handled by the external UI handler.</span></span>

<span data-ttu-id="4e38a-110">I valori restituiti rimanenti, come descritto di seguito, sono direttamente correlati ai tipi di pulsanti inclusi nel tipo di messaggio.</span><span class="sxs-lookup"><span data-stu-id="4e38a-110">The remaining return values, as described below, are directly related to the button types that are included with the message type.</span></span>



| <span data-ttu-id="4e38a-111">Valore restituito dall'interfaccia utente esterna</span><span class="sxs-lookup"><span data-stu-id="4e38a-111">External UI return value</span></span> | <span data-ttu-id="4e38a-112">Significato</span><span class="sxs-lookup"><span data-stu-id="4e38a-112">Meaning</span></span>                                                                                                |
|--------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e38a-113">IDOK</span><span class="sxs-lookup"><span data-stu-id="4e38a-113">IDOK</span></span>                     | <span data-ttu-id="4e38a-114">Il pulsante **OK** è stato premuto dall'utente.</span><span class="sxs-lookup"><span data-stu-id="4e38a-114">The **OK** button was pressed by the user.</span></span> <span data-ttu-id="4e38a-115">Informazioni sul messaggio riconosciute.</span><span class="sxs-lookup"><span data-stu-id="4e38a-115">The message information was understood.</span></span>                     |
| <span data-ttu-id="4e38a-116">IDCANCEL</span><span class="sxs-lookup"><span data-stu-id="4e38a-116">IDCANCEL</span></span>                 | <span data-ttu-id="4e38a-117">È stato premuto il pulsante **Annulla** .</span><span class="sxs-lookup"><span data-stu-id="4e38a-117">The **CANCEL** button was pressed.</span></span> <span data-ttu-id="4e38a-118">Annulla l'installazione.</span><span class="sxs-lookup"><span data-stu-id="4e38a-118">Cancel the installation.</span></span>                                            |
| <span data-ttu-id="4e38a-119">IDABORT</span><span class="sxs-lookup"><span data-stu-id="4e38a-119">IDABORT</span></span>                  | <span data-ttu-id="4e38a-120">È stato premuto il pulsante **Interrompi** .</span><span class="sxs-lookup"><span data-stu-id="4e38a-120">The **ABORT** button was pressed.</span></span> <span data-ttu-id="4e38a-121">Interrompere l'installazione.</span><span class="sxs-lookup"><span data-stu-id="4e38a-121">Abort the installation.</span></span>                                              |
| <span data-ttu-id="4e38a-122">IDRETRY</span><span class="sxs-lookup"><span data-stu-id="4e38a-122">IDRETRY</span></span>                  | <span data-ttu-id="4e38a-123">È stato premuto il pulsante **Riprova** .</span><span class="sxs-lookup"><span data-stu-id="4e38a-123">The **RETRY** button was pressed.</span></span> <span data-ttu-id="4e38a-124">Ripetere l'azione.</span><span class="sxs-lookup"><span data-stu-id="4e38a-124">Try the action again.</span></span>                                                |
| <span data-ttu-id="4e38a-125">IDIGNORE</span><span class="sxs-lookup"><span data-stu-id="4e38a-125">IDIGNORE</span></span>                 | <span data-ttu-id="4e38a-126">È stato premuto il pulsante **Ignora** .</span><span class="sxs-lookup"><span data-stu-id="4e38a-126">The **IGNORE** button was pressed.</span></span> <span data-ttu-id="4e38a-127">Ignorare l'errore e continuare.</span><span class="sxs-lookup"><span data-stu-id="4e38a-127">Ignore the error and continue.</span></span>                                      |
| <span data-ttu-id="4e38a-128">IDYES</span><span class="sxs-lookup"><span data-stu-id="4e38a-128">IDYES</span></span>                    | <span data-ttu-id="4e38a-129">È stato premuto il pulsante **Sì** .</span><span class="sxs-lookup"><span data-stu-id="4e38a-129">The **YES** button was pressed.</span></span> <span data-ttu-id="4e38a-130">La risposta affermativa continua con la sequenza di eventi corrente.</span><span class="sxs-lookup"><span data-stu-id="4e38a-130">The affirmative response, continue with current sequence of events..</span></span>   |
| <span data-ttu-id="4e38a-131">IDNO</span><span class="sxs-lookup"><span data-stu-id="4e38a-131">IDNO</span></span>                     | <span data-ttu-id="4e38a-132">È stato premuto il pulsante **No** .</span><span class="sxs-lookup"><span data-stu-id="4e38a-132">The **NO** button was pressed.</span></span> <span data-ttu-id="4e38a-133">La risposta negativa non continua con la sequenza di eventi corrente.</span><span class="sxs-lookup"><span data-stu-id="4e38a-133">The negative response, do not continue with current sequence of events.</span></span> |



 

<span data-ttu-id="4e38a-134">Se, ad esempio, al gestore dell'interfaccia utente esterno viene inviato un messaggio con il \_ flag di stili della finestra di messaggio MB AbortRetryIgnore (, il gestore dell'interfaccia utente esterno può restituire uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="4e38a-134">For example, if the external UI handler is sent a message with the MB\_ABORTRETRYIGNORE message box styles flag, the external UI handler can return one of the following values:</span></span>

-   <span data-ttu-id="4e38a-135">-1 (errore nel gestore dell'interfaccia utente esterno)</span><span class="sxs-lookup"><span data-stu-id="4e38a-135">–1 (error in external UI handler)</span></span>
-   <span data-ttu-id="4e38a-136">0 (nessuna azione eseguita nel gestore dell'interfaccia utente esterno, consente di Windows Installer gestirla)</span><span class="sxs-lookup"><span data-stu-id="4e38a-136">0 (no action taken in external UI handler, let Windows Installer handle it)</span></span>
-   <span data-ttu-id="4e38a-137">IDABORT (pulsante **Interrompi** premuto)</span><span class="sxs-lookup"><span data-stu-id="4e38a-137">IDABORT (**ABORT** button pressed)</span></span>
-   <span data-ttu-id="4e38a-138">IDRETRY (pulsante **Riprova** premuto)</span><span class="sxs-lookup"><span data-stu-id="4e38a-138">IDRETRY (**RETRY** button pressed)</span></span>
-   <span data-ttu-id="4e38a-139">IDIGNORE (pulsante **Ignora** premuto)</span><span class="sxs-lookup"><span data-stu-id="4e38a-139">IDIGNORE (**IGNORE** button pressed)</span></span>

 

 



