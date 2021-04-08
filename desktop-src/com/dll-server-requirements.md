---
title: Requisiti del server DLL
description: Sebbene la maggior parte delle dll possa essere eseguita in un surrogato, alcune dll non possono.
ms.assetid: f89dabe6-f65f-4d90-ad0e-c680d4b08ba5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae82aa44771d398d80169c56976df7b0e209ea6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045368"
---
# <a name="dll-server-requirements"></a><span data-ttu-id="5df37-103">Requisiti del server DLL</span><span class="sxs-lookup"><span data-stu-id="5df37-103">DLL Server Requirements</span></span>

<span data-ttu-id="5df37-104">Sebbene la maggior parte delle dll possa essere eseguita in un surrogato, alcune dll non possono.</span><span class="sxs-lookup"><span data-stu-id="5df37-104">While most DLLs can run in a surrogate, some DLLs cannot.</span></span>

<span data-ttu-id="5df37-105">Se si desidera utilizzare il surrogato fornito dal sistema, la DLL deve essere ben compensata.</span><span class="sxs-lookup"><span data-stu-id="5df37-105">The DLL must be well-behaved if you want to use the system-supplied surrogate.</span></span> <span data-ttu-id="5df37-106">Ad esempio, una DLL che chiama i metodi che registrano i callback dal client tenterà di richiamare tali callback come se i puntatori a funzione ricevuti fossero per istruzioni nello spazio degli indirizzi, che non è il caso.</span><span class="sxs-lookup"><span data-stu-id="5df37-106">For example, a DLL that calls methods that register callbacks from the client would try to invoke those callbacks as if the function pointers it received were for instructions in its address space, which is not the case.</span></span> <span data-ttu-id="5df37-107">Analogamente, una DLL che usa una variabile globale a cui si aspetta che il client acceda non funzionerà.</span><span class="sxs-lookup"><span data-stu-id="5df37-107">Similarly, a DLL that uses a global variable that it expects the client to access would not work.</span></span> <span data-ttu-id="5df37-108">In generale, i parametri per i quali non è possibile effettuare il marshalling in modo corretto impediscono l'esecuzione del server DLL all'esterno del processo client.</span><span class="sxs-lookup"><span data-stu-id="5df37-108">In general, parameters that cannot be properly marshaled will prevent the DLL server from running outside the client process.</span></span> <span data-ttu-id="5df37-109">In molti casi, è possibile scrivere un surrogato personalizzato progettato appositamente per compensare il comportamento "errato".</span><span class="sxs-lookup"><span data-stu-id="5df37-109">In many cases, you can write a custom surrogate specifically designed to compensate for "bad" behavior.</span></span> <span data-ttu-id="5df37-110">Per ulteriori informazioni, vedere [scrittura di un surrogato personalizzato](writing-a-custom-surrogate.md).</span><span class="sxs-lookup"><span data-stu-id="5df37-110">(For more information, see [Writing a Custom Surrogate](writing-a-custom-surrogate.md).)</span></span>

<span data-ttu-id="5df37-111">Se il server DLL utilizza interfacce personalizzate, è necessario assicurarsi che il codice di marshalling sia disponibile per tali interfacce.</span><span class="sxs-lookup"><span data-stu-id="5df37-111">If the DLL server uses custom interfaces, you would have to ensure that marshaling code is available for those interfaces.</span></span> <span data-ttu-id="5df37-112">Ad esempio, è possibile compilare e registrare una DLL proxy oppure fornire e registrare una libreria dei tipi che consenta al server di funzionare correttamente durante l'esecuzione in un surrogato.</span><span class="sxs-lookup"><span data-stu-id="5df37-112">For example, you could build and register a proxy DLL or provide and register a type library that would allow the server to function correctly while running in a surrogate.</span></span>

<span data-ttu-id="5df37-113">I server DLL verranno caricati solo in un processo surrogato in esecuzione nel contesto di sicurezza appropriato.</span><span class="sxs-lookup"><span data-stu-id="5df37-113">DLL servers will be loaded only into a surrogate process running in the proper security context.</span></span> <span data-ttu-id="5df37-114">Il contesto di sicurezza per il surrogato del server DLL viene determinato in modo analogo ai server EXE.</span><span class="sxs-lookup"><span data-stu-id="5df37-114">The security context for the DLL server surrogate is determined in the same way as for EXE servers.</span></span> <span data-ttu-id="5df37-115">Il surrogato del server DLL viene eseguito nello stesso contesto di sicurezza del client, a meno che non sia impostato un valore **RunAs** , che determina il contesto di sicurezza, nella sezione del registro di sistema [AppID](appid-clsid.md) per il server.</span><span class="sxs-lookup"><span data-stu-id="5df37-115">The DLL server surrogate runs in the same security context as the client, unless a **RunAs** value, which determines the security context, is set in the [AppID](appid-clsid.md) registry section for the server.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5df37-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5df37-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5df37-117">Surrogati DLL</span><span class="sxs-lookup"><span data-stu-id="5df37-117">DLL Surrogates</span></span>](dll-surrogates.md)
</dt> </dl>

 

 




