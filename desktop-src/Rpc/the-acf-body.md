---
title: Corpo ACF
description: Il corpo di ACF contiene gli attributi di configurazione che si applicano ai tipi e alle funzioni definiti nel corpo dell'interfaccia del file IDL.
ms.assetid: 7d6344d3-1117-40b9-be95-a400b81339d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b19422762c61dee63c4f502448197aefb432c80c
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "104047509"
---
# <a name="the-acf-body"></a><span data-ttu-id="0782a-103">Corpo ACF</span><span class="sxs-lookup"><span data-stu-id="0782a-103">The ACF Body</span></span>

<span data-ttu-id="0782a-104">Il corpo di ACF contiene gli attributi di configurazione che si applicano ai tipi e alle funzioni definiti nel corpo dell'interfaccia del file IDL.</span><span class="sxs-lookup"><span data-stu-id="0782a-104">The ACF body contains configuration attributes that apply to types and functions defined in the interface body of the IDL file.</span></span> <span data-ttu-id="0782a-105">Il corpo di ACF può essere vuoto o contenere gli attributi di [**inclusione**](/windows/desktop/Midl/include), [**typedef**](/windows/desktop/Midl/typedef), funzione e parametro di ACF.</span><span class="sxs-lookup"><span data-stu-id="0782a-105">The body of the ACF can be empty or it can contain ACF [**include**](/windows/desktop/Midl/include), [**typedef**](/windows/desktop/Midl/typedef), function, and parameter attributes.</span></span> <span data-ttu-id="0782a-106">Tutti questi elementi sono facoltativi.</span><span class="sxs-lookup"><span data-stu-id="0782a-106">All of these items are optional.</span></span> <span data-ttu-id="0782a-107">Attributi applicati a singoli tipi e funzioni nel corpo di ACF che eseguono l'override degli attributi nell'intestazione ACF.</span><span class="sxs-lookup"><span data-stu-id="0782a-107">Attributes applied to individual types and functions in the ACF body override attributes in the ACF header.</span></span>

<span data-ttu-id="0782a-108">L'ACF specifica il comportamento nel computer locale e non influisce sui dati trasmessi in rete.</span><span class="sxs-lookup"><span data-stu-id="0782a-108">The ACF specifies behavior on the local computer and does not affect the data transmitted over the network.</span></span> <span data-ttu-id="0782a-109">Viene utilizzato per specificare i dettagli di uno stub da generare.</span><span class="sxs-lookup"><span data-stu-id="0782a-109">It is used to specify details of a stub to be generated.</span></span> <span data-ttu-id="0782a-110">In modalità di compatibilità DCE ([**/OSF**](/windows/desktop/Midl/-osf)), ACF non influisce sull'interazione tra gli stub, ma tra lo stub e il codice dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0782a-110">In DCE-compatibility mode ([**/osf**](/windows/desktop/Midl/-osf)), the ACF does not affect interaction between stubs, but between the stub and application code.</span></span>

<span data-ttu-id="0782a-111">Un parametro specificato in ACF deve essere uno dei parametri specificati nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="0782a-111">A parameter specified in the ACF must be one of the parameters specified in the IDL file.</span></span> <span data-ttu-id="0782a-112">L'ordine di specifica del parametro nell'elemento ACF non è significativo perché la corrispondenza è in base al nome, non in base alla posizione.</span><span class="sxs-lookup"><span data-stu-id="0782a-112">The order of specification of the parameter in the ACF is not significant because the matching is by name, not by position.</span></span> <span data-ttu-id="0782a-113">L'elenco di parametri in ACF può essere vuoto, anche quando l'elenco dei parametri nella firma IDL corrispondente non è (ma questa operazione non è consigliata).</span><span class="sxs-lookup"><span data-stu-id="0782a-113">The parameter list in the ACF can be empty, even when the parameter list in the corresponding IDL signature is not (but this is not recommended).</span></span> <span data-ttu-id="0782a-114">I dichiaratori astratti (parametri senza nome) nel file IDL fanno sì che il compilatore MIDL segnali errori durante l'elaborazione di ACF perché il parametro non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="0782a-114">Abstract declarators (unnamed parameters) in the IDL file cause the MIDL compiler to report errors while processing the ACF because the parameter is not found.</span></span>

<span data-ttu-id="0782a-115">La direttiva di **inclusione** di ACF specifica i file di intestazione da visualizzare nell'intestazione generata come parte di un'istruzione di **\# inclusione** del preprocessore C standard.</span><span class="sxs-lookup"><span data-stu-id="0782a-115">The ACF **include** directive specifies the header files to appear in the generated header as part of a standard C-preprocessor **\#include** statement.</span></span> <span data-ttu-id="0782a-116">La parola chiave ACF **include** differisce da una direttiva **\# include** .</span><span class="sxs-lookup"><span data-stu-id="0782a-116">The ACF keyword **include** differs from an **\#include** directive.</span></span> <span data-ttu-id="0782a-117">La parola chiave ACF **include** fa in modo che la riga "**\# Includi** *filename*" venga visualizzata nel file di intestazione generato, mentre la direttiva del linguaggio C "**\# include** *filename*" fa sì che il contenuto del file venga inserito nell'ACF.</span><span class="sxs-lookup"><span data-stu-id="0782a-117">The ACF keyword **include** causes the line "**\#include** *filename*" to appear in the generated header file, while the C-language directive "**\#include** *filename*" causes the contents of that file to be placed in the ACF.</span></span>

<span data-ttu-id="0782a-118">L'istruzione ACF [**typedef**](/windows/desktop/Midl/typedef) consente di applicare gli attributi di tipo ACF ai tipi definiti in precedenza nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="0782a-118">The ACF [**typedef**](/windows/desktop/Midl/typedef) statement lets you apply ACF type attributes to types previously defined in the IDL file.</span></span> <span data-ttu-id="0782a-119">La sintassi di ACF **typedef** è diversa dalla sintassi del **typedef** C.</span><span class="sxs-lookup"><span data-stu-id="0782a-119">The ACF **typedef** syntax differs from the C **typedef** syntax.</span></span>

<span data-ttu-id="0782a-120">Gli attributi della funzione ACF consentono di specificare gli attributi che si applicano alla funzione nel suo complesso.</span><span class="sxs-lookup"><span data-stu-id="0782a-120">The ACF function attributes let you specify attributes that apply to the function as a whole.</span></span> <span data-ttu-id="0782a-121">Per ulteriori informazioni, vedere **\[** [**Code**](/windows/desktop/Midl/code) **\]** , **\[** [**optimize**](/windows/desktop/Midl/optimize) **\]** e **\[** [**NoCode**](/windows/desktop/Midl/nocode) **\]** .</span><span class="sxs-lookup"><span data-stu-id="0782a-121">For more information, see **\[**[**code**](/windows/desktop/Midl/code)**\]**, **\[**[**optimize**](/windows/desktop/Midl/optimize)**\]**, and **\[**[**nocode**](/windows/desktop/Midl/nocode)**\]**.</span></span>

<span data-ttu-id="0782a-122">Gli attributi del parametro ACF consentono di specificare gli attributi che si applicano ai singoli parametri della funzione.</span><span class="sxs-lookup"><span data-stu-id="0782a-122">The ACF parameter attributes let you specify attributes that apply to individual parameters of the function.</span></span> <span data-ttu-id="0782a-123">Per ulteriori informazioni, vedere **\[** [**\_ conteggio byte**](/windows/desktop/Midl/byte-count) **\]** .</span><span class="sxs-lookup"><span data-stu-id="0782a-123">For more information, see **\[**[**byte\_count**](/windows/desktop/Midl/byte-count)**\]**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0782a-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0782a-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0782a-125">**configurazione di/app \_**</span><span class="sxs-lookup"><span data-stu-id="0782a-125">**/app\_config**</span></span>](/windows/desktop/Midl/-app-config)
</dt> <dt>

[<span data-ttu-id="0782a-126">**/osf**</span><span class="sxs-lookup"><span data-stu-id="0782a-126">**/osf**</span></span>](/windows/desktop/Midl/-osf)
</dt> <dt>

<span data-ttu-id="0782a-127">[**\[\_handle automatico\]**](../midl/auto-handle.md)</span><span class="sxs-lookup"><span data-stu-id="0782a-127">[**\[auto\_handle\]**](../midl/auto-handle.md)</span></span>
</dt> <dt>

<span data-ttu-id="0782a-128">[**\[codice\]**](../midl/code.md)</span><span class="sxs-lookup"><span data-stu-id="0782a-128">[**\[code\]**](../midl/code.md)</span></span>
</dt> <dt>

<span data-ttu-id="0782a-129">[**\[handle esplicito \_\]**](../midl/explicit-handle.md)</span><span class="sxs-lookup"><span data-stu-id="0782a-129">[**\[explicit\_handle\]**](../midl/explicit-handle.md)</span></span>
</dt> <dt>

[<span data-ttu-id="0782a-130">File IDL (Interface Definition Language)</span><span class="sxs-lookup"><span data-stu-id="0782a-130">The Interface Definition Language (IDL) File</span></span>](the-interface-definition-language-idl-file.md)
</dt> <dt>

<span data-ttu-id="0782a-131">[**\[handle implicito \_\]**](../midl/implicit-handle.md)</span><span class="sxs-lookup"><span data-stu-id="0782a-131">[**\[implicit\_handle\]**](../midl/implicit-handle.md)</span></span>
</dt> <dt>

[<span data-ttu-id="0782a-132">**includere**</span><span class="sxs-lookup"><span data-stu-id="0782a-132">**include**</span></span>](/windows/desktop/Midl/include)
</dt> <dt>

[<span data-ttu-id="0782a-133">MIDL</span><span class="sxs-lookup"><span data-stu-id="0782a-133">midl</span></span>](/windows/desktop/Midl/midl-language-reference)
</dt> <dt>

<span data-ttu-id="0782a-134">[**\[NoCode\]**](../midl/nocode.md)</span><span class="sxs-lookup"><span data-stu-id="0782a-134">[**\[nocode\]**](../midl/nocode.md)</span></span>
</dt> <dt>

<span data-ttu-id="0782a-135">[**\[ottimizzare\]**](../midl/optimize.md)</span><span class="sxs-lookup"><span data-stu-id="0782a-135">[**\[optimize\]**](../midl/optimize.md)</span></span>
</dt> <dt>

<span data-ttu-id="0782a-136">[**\[rappresenta \_ come\]**](../midl/represent-as.md)</span><span class="sxs-lookup"><span data-stu-id="0782a-136">[**\[represent\_as\]**](../midl/represent-as.md)</span></span>
</dt> <dt>

[<span data-ttu-id="0782a-137">**typedef**</span><span class="sxs-lookup"><span data-stu-id="0782a-137">**typedef**</span></span>](/windows/desktop/Midl/typedef)
</dt> </dl>

 

 