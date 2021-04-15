---
title: LocalServer32
description: Specifica il percorso completo di un'applicazione server locale a 32 bit.
ms.assetid: 5d922230-f53d-4bf9-be50-c8c00f45b7a8
keywords:
- LocalServer32 chiave del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fd068f51f33b6c283384198c0206bc9c3b6357f
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104517164"
---
# <a name="localserver32"></a><span data-ttu-id="b68d5-104">LocalServer32</span><span class="sxs-lookup"><span data-stu-id="b68d5-104">LocalServer32</span></span>

<span data-ttu-id="b68d5-105">Specifica il percorso completo di un'applicazione server locale a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="b68d5-105">Specifies the full path to a 32-bit local server application.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="b68d5-106">Voce del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="b68d5-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      LocalServer32
         (Default) = path
         ServerExecutable = path
```

## <a name="remarks"></a><span data-ttu-id="b68d5-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="b68d5-107">Remarks</span></span>

<span data-ttu-id="b68d5-108">Il valore **ServerExecutable** , che è di tipo **reg \_ SZ** ed è supportato a partire da Windows Server 2003, funziona insieme alla sottochiave **LocalServer32** per evitare ambiguità quando si usa la funzione [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) .</span><span class="sxs-lookup"><span data-stu-id="b68d5-108">The **ServerExecutable** value, which is of type **REG\_SZ** and is supported starting with Windows Server 2003, works in conjunction with the **LocalServer32** subkey to prevent any ambiguity when using the [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) function.</span></span> <span data-ttu-id="b68d5-109">**LocalServer32** specifica il percorso dell'applicazione server COM da avviare e queste informazioni vengono passate come primo parametro *lpApplicationName* per **CreateProcess**.</span><span class="sxs-lookup"><span data-stu-id="b68d5-109">**LocalServer32** specifies the location of the COM server application to launch, and this information is passed as the first parameter *lpApplicationName* for **CreateProcess**.</span></span> <span data-ttu-id="b68d5-110">A seconda dell'implementazione di **CreateProcess**, le informazioni potrebbero essere ambigue.</span><span class="sxs-lookup"><span data-stu-id="b68d5-110">Depending on the implementation of **CreateProcess**, this information might be ambiguous.</span></span> <span data-ttu-id="b68d5-111">Per questo motivo, se si specifica **ServerExecutable** , com passa il valore **ServerExecutable** denominato al parametro *lpApplicationName* di **CreateProcess**.</span><span class="sxs-lookup"><span data-stu-id="b68d5-111">For this reason, if **ServerExecutable** is specified, COM passes the **ServerExecutable** named value to the *lpApplicationName* parameter of **CreateProcess**.</span></span> <span data-ttu-id="b68d5-112">Se **ServerExecutable** viene omesso, com passa **null** come valore per il primo parametro di **CreateProcess**.</span><span class="sxs-lookup"><span data-stu-id="b68d5-112">If **ServerExecutable** is not specified, COM passes **NULL** as the value for the first parameter of **CreateProcess**.</span></span>

<span data-ttu-id="b68d5-113">Per fornire la sicurezza del sistema, usare stringhe tra virgolette nel percorso per indicare dove termina il nome file eseguibile e gli argomenti iniziano.</span><span class="sxs-lookup"><span data-stu-id="b68d5-113">To help provide system security, use quoted strings in the path to indicate where the executable filename ends and the arguments begin.</span></span> <span data-ttu-id="b68d5-114">Ad esempio, anziché specificare il percorso seguente come voce **LocalServer32** :</span><span class="sxs-lookup"><span data-stu-id="b68d5-114">For example, instead of specifying the following path as the **LocalServer32** entry:</span></span>

<span data-ttu-id="b68d5-115">"C: \\ programmi \\ aziendali file \\Application.exe param1 param2"</span><span class="sxs-lookup"><span data-stu-id="b68d5-115">"C:\\Program Files\\Company Files\\Application.exe param1 param2"</span></span>

<span data-ttu-id="b68d5-116">specificare il percorso usando la sintassi seguente:</span><span class="sxs-lookup"><span data-stu-id="b68d5-116">specify the path using the following syntax:</span></span>

<span data-ttu-id="b68d5-117">" \\ " C: \\ programmi \\ aziendali file \\Application.exe\\ "param1 param2"</span><span class="sxs-lookup"><span data-stu-id="b68d5-117">"\\"C:\\Program Files\\Company Files\\Application.exe\\" param1 param2"</span></span>

<span data-ttu-id="b68d5-118">COM aggiunge il flag "-Embedding" alla stringa, quindi l'applicazione che usa i flag deve analizzare l'intera stringa e verificare la presenza del flag-Embedding.</span><span class="sxs-lookup"><span data-stu-id="b68d5-118">COM appends the "-Embedding" flag to the string, so the application that uses flags needs to parse the whole string and check for the -Embedding flag.</span></span>

<span data-ttu-id="b68d5-119">Quando COM avvia un server locale a 32 bit, il server deve registrare un oggetto classe entro un tempo trascorso impostato dall'utente.</span><span class="sxs-lookup"><span data-stu-id="b68d5-119">When COM starts a 32-bit local server, the server must register a class object within an elapsed time set by the user.</span></span> <span data-ttu-id="b68d5-120">Per impostazione predefinita, il valore del tempo trascorso deve essere almeno di 5 minuti, in millisecondi, ma non può superare il numero di millisecondi in 30 giorni.</span><span class="sxs-lookup"><span data-stu-id="b68d5-120">By default, the elapsed time value must be at least 5 minutes, in milliseconds, but cannot exceed the number of milliseconds in 30 days.</span></span> <span data-ttu-id="b68d5-121">Le applicazioni in genere non devono impostare questo valore, che si trova nella voce **HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ COM2 \\ ServerStartElapsedTime**</span><span class="sxs-lookup"><span data-stu-id="b68d5-121">Applications typically should not set this value, which is in the **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\COM2\\ServerStartElapsedTime** entry.</span></span>

<span data-ttu-id="b68d5-122">Le voci obbligatorie per i server locali a 32 bit sono [**InprocHandler32**](inprochandler32.md), [**LocalServer**](localserver.md), **LocalServer32** e [**Insertable**](insertable.md).</span><span class="sxs-lookup"><span data-stu-id="b68d5-122">The required entries for 32-bit local servers are [**InprocHandler32**](inprochandler32.md), [**LocalServer**](localserver.md), **LocalServer32**, and [**Insertable**](insertable.md).</span></span>

<span data-ttu-id="b68d5-123">Se un contenitore esegue la ricerca nel registro di sistema per un server locale, un server locale a 32 bit ha la priorità su un server locale a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="b68d5-123">If a container is searching the registry for a local server, a 32-bit local server has priority over a 16-bit local server.</span></span>

<span data-ttu-id="b68d5-124">Se si implementano classi come servizi, è necessario tenere presente che il valore denominato [**LocalService**](localservice.md) viene usato in preferenza con la chiave **LocalServer32** per l'attivazione locale e remota Requestsâ € "Se **LocalService** esiste e fa riferimento a un servizio valido, la chiave **LocalServer32** viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="b68d5-124">If you are implementing classes as services, you should be aware that the [**LocalService**](localservice.md) named value is used in preference to the **LocalServer32** key for local and remote activation requestsâ€”if **LocalService** exists and refers to a valid service, the **LocalServer32** key is ignored.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b68d5-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b68d5-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b68d5-126">**LocalServer**</span><span class="sxs-lookup"><span data-stu-id="b68d5-126">**LocalServer**</span></span>](localserver.md)
</dt> <dt>

[<span data-ttu-id="b68d5-127">**LocalService**</span><span class="sxs-lookup"><span data-stu-id="b68d5-127">**LocalService**</span></span>](localservice.md)
</dt> </dl>

 

 