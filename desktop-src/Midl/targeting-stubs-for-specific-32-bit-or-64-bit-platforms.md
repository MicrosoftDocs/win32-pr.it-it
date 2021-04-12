---
title: Destinazione degli stub per piattaforme specifiche a 32 bit o a 64 bit
description: Alcune delle funzionalità di Microsoft RPC e i compilatori MIDL 3,0 e versioni successive sono specifici della piattaforma.
ms.assetid: bb1bee56-7f39-406c-bdbf-b73bda568247
keywords:
- piattaforme a 32 bit MIDL
- piattaforme a 64 bit MIDL
- Stub MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 526265a60f8b2ef2f31d19d0356d4ec3a3ae8c8f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331380"
---
# <a name="targeting-stubs-for-specific-32-bit-or-64-bit-platforms"></a><span data-ttu-id="611ba-106">Destinazione degli stub per piattaforme specifiche a 32 bit o a 64 bit</span><span class="sxs-lookup"><span data-stu-id="611ba-106">Targeting Stubs for Specific 32-bit or 64-bit Platforms</span></span>

<span data-ttu-id="611ba-107">Alcune delle funzionalità di Microsoft RPC e i compilatori MIDL 3,0 e versioni successive sono specifici della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="611ba-107">Some of the features of Microsoft RPC and the MIDL 3.0 and later compilers are platform-specific.</span></span>

<span data-ttu-id="611ba-108">Per precauzione, i compilatori MIDL 3,0 e versioni successive generano protezioni che facilitano il controllo della compatibilità durante la fase di compilazione C.</span><span class="sxs-lookup"><span data-stu-id="611ba-108">As a precaution, the MIDL 3.0 and later compilers generate guards that facilitate compatibility checking during the C-compilation phase.</span></span> <span data-ttu-id="611ba-109">MIDL genera due tipi di protezioni: un GUARD dipendente dalla piattaforma (32 bit rispetto a 64 bit) e un GUARD dipendente dalla versione (dipendenza dal set di funzionalità).</span><span class="sxs-lookup"><span data-stu-id="611ba-109">MIDL generates two types of guards: a platform-dependent guard (32-bit versus 64-bit) and a release-dependent guard (feature set dependency).</span></span> <span data-ttu-id="611ba-110">Ad esempio, MIDL genera la seguente protezione per impedire la compilazione C di uno stub a 32 bit per altre piattaforme:</span><span class="sxs-lookup"><span data-stu-id="611ba-110">For example, MIDL generates the following guard to prevent C-compiling of a 32-bit stub for other platforms:</span></span>

``` syntax
#if !defined(__RPC_WIN32__)
#error  Invalid build platform for this stub.
#endif
```

<span data-ttu-id="611ba-111">Il Guard dipendente dalla versione viene attivato da un set di funzionalità trovate nei file IDL elaborati e dall'opzione [**/target**](-target.md) .</span><span class="sxs-lookup"><span data-stu-id="611ba-111">The release-dependent guard is triggered by a set of features found in the processed IDL file(s) and by the [**/target**](-target.md) switch.</span></span> <span data-ttu-id="611ba-112">Se, ad esempio, l'interfaccia usa funzionalità supportate solo in Windows 2000 o versioni successive, MIDL genera una protezione con la destinazione \_ è \_ NT50 \_ o una \_ macro successiva.</span><span class="sxs-lookup"><span data-stu-id="611ba-112">For example, if the interface uses features supported only on WindowsÂ 2000 or later, MIDL generates a guard with the TARGET\_IS\_NT50\_OR\_LATER macro.</span></span>

<span data-ttu-id="611ba-113">Le macro Guard, definite in Rpcndr. h, dipendono dall'impostazione di WINVER e \_ Win32 \_ WinNT e vengono valutate dal compilatore C/C++.</span><span class="sxs-lookup"><span data-stu-id="611ba-113">The guard macros, defined in Rpcndr.h, depend on the setting of WINVER and \_WIN32\_WINNT and are evaluated by the C/C++ compiler.</span></span>

<span data-ttu-id="611ba-114">Se, in fase di compilazione C, viene ricevuto un messaggio di errore che indica che è necessaria una piattaforma specifica per eseguire uno stub, verificare prima di tutto che non sia stata usata una funzionalità non disponibile in questa piattaforma.</span><span class="sxs-lookup"><span data-stu-id="611ba-114">If, at C-compile time, you get an error message indicating that you need a specific platform to run a stub, first check to make sure you have not used a feature that is not available on this platform.</span></span> <span data-ttu-id="611ba-115">Le funzionalità che attivano una particolare protezione sono elencate nel corpo della protezione.</span><span class="sxs-lookup"><span data-stu-id="611ba-115">The features triggering a particular guard are listed in the body of the guard.</span></span> <span data-ttu-id="611ba-116">Nell'esempio precedente, l'opzione del compilatore-Oicf ha attivato la protezione.</span><span class="sxs-lookup"><span data-stu-id="611ba-116">In the previous example, the -Oicf compiler switch triggered the guard.</span></span> <span data-ttu-id="611ba-117">Le funzionalità rilevanti di questo tipo includono l'opzione [**/robust**](-robust.md) e l' \[ [](async.md) \] attributo asincrono disponibile in Windows 2000 e versioni successive, il costruttore del tipo di [**pipe**](pipe.md) , l'opzione del compilatore/OIF e gli attributi di \[ [**\_ marshalling degli utenti**](user-marshal.md) \] e del \[ [**\_ marshalling di rete**](wire-marshal.md) \] .</span><span class="sxs-lookup"><span data-stu-id="611ba-117">Notable features of this kind include the [**/robust**](-robust.md) switch and the \[[**async**](async.md)\] attribute available on WindowsÂ 2000 and later, the [**pipe**](pipe.md) type constructor, the /Oif compiler option, and the \[[**user\_marshal**](user-marshal.md)\] and \[[**wire\_marshal**](wire-marshal.md)\] attributes.</span></span> <span data-ttu-id="611ba-118">Gli stub che usano queste funzionalità non vengono eseguiti nei sistemi precedenti.</span><span class="sxs-lookup"><span data-stu-id="611ba-118">Stubs using these features will not run on earlier systems.</span></span>

<span data-ttu-id="611ba-119">Se si è certi che la piattaforma di destinazione è corretta per le funzionalità in uso e viene comunque visualizzato un errore, potrebbe essere necessario impostare le variabili di ambiente in modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="611ba-119">If you know that your target platform is correct for the features you are using and still receive an error, you may need to set the environment variables appropriately.</span></span>

<span data-ttu-id="611ba-120">**Per compilare per Windows 2000 o versioni successive**</span><span class="sxs-lookup"><span data-stu-id="611ba-120">**To build for WindowsÂ 2000 or later releases**</span></span>

-   <span data-ttu-id="611ba-121">Aggiungere questa riga al Makefile:</span><span class="sxs-lookup"><span data-stu-id="611ba-121">Add this line to your makefile:</span></span>

    ``` syntax
    CFLAGS = $(CFLAGS) -D_WIN32_WINNT=0x500
    ```

## <a name="related-topics"></a><span data-ttu-id="611ba-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="611ba-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="611ba-123">**/target**</span><span class="sxs-lookup"><span data-stu-id="611ba-123">**/target**</span></span>](-target.md)
</dt> <dt>

[<span data-ttu-id="611ba-124">**/Robust**</span><span class="sxs-lookup"><span data-stu-id="611ba-124">**/robust**</span></span>](-robust.md)
</dt> <dt>

[<span data-ttu-id="611ba-125">**async**</span><span class="sxs-lookup"><span data-stu-id="611ba-125">**async**</span></span>](async.md)
</dt> <dt>

[<span data-ttu-id="611ba-126">**\_UUID asincrono**</span><span class="sxs-lookup"><span data-stu-id="611ba-126">**async\_uuid**</span></span>](async-uuid.md)
</dt> <dt>

[<span data-ttu-id="611ba-127">**/OI**</span><span class="sxs-lookup"><span data-stu-id="611ba-127">**/Oi**</span></span>](-oi.md)
</dt> <dt>

[<span data-ttu-id="611ba-128">**inviare tramite pipe**</span><span class="sxs-lookup"><span data-stu-id="611ba-128">**pipe**</span></span>](pipe.md)
</dt> <dt>

[<span data-ttu-id="611ba-129">**\_marshalling di rete**</span><span class="sxs-lookup"><span data-stu-id="611ba-129">**wire\_marshal**</span></span>](wire-marshal.md)
</dt> <dt>

[<span data-ttu-id="611ba-130">**\_marshalling utente**</span><span class="sxs-lookup"><span data-stu-id="611ba-130">**user\_marshal**</span></span>](user-marshal.md)
</dt> <dt>

[<span data-ttu-id="611ba-131">Marshalling di tipi di dati OLE</span><span class="sxs-lookup"><span data-stu-id="611ba-131">Marshaling OLE Data Types</span></span>](marshaling-ole-data-types.md)
</dt> </dl>

 

 




