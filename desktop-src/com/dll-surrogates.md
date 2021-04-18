---
title: Surrogati DLL
description: Surrogati DLL
ms.assetid: fe30c0ae-1d19-4a5f-8ee3-8a5337c79c44
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 313c3fcbd07b4c6317dfb6ac8ede772fc62035f0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298938"
---
# <a name="dll-surrogates"></a><span data-ttu-id="7cf68-103">Surrogati DLL</span><span class="sxs-lookup"><span data-stu-id="7cf68-103">DLL Surrogates</span></span>

<span data-ttu-id="7cf68-104">COM rende possibile la creazione di server DLL che possono essere caricati in un processo EXE surrogato.</span><span class="sxs-lookup"><span data-stu-id="7cf68-104">COM makes it possible to create DLL servers that can be loaded into a surrogate EXE process.</span></span> <span data-ttu-id="7cf68-105">Questa operazione combina la facilità di scrittura dei server DLL con i vantaggi dell'implementazione eseguibile.</span><span class="sxs-lookup"><span data-stu-id="7cf68-105">This combines the ease of writing DLL servers with the benefits of executable implementation.</span></span> <span data-ttu-id="7cf68-106">Gli strumenti di sviluppo come Microsoft Visual Studio facilitano la scrittura dei server DLL, ma un server DLL ha limiti.</span><span class="sxs-lookup"><span data-stu-id="7cf68-106">Development tools like Microsoft Visual Studio facilitate the writing of DLL servers, but a DLL server in itself has limits.</span></span> <span data-ttu-id="7cf68-107">L'esecuzione del server DLL in un processo surrogato offre diversi vantaggi:</span><span class="sxs-lookup"><span data-stu-id="7cf68-107">Running the DLL server in a surrogate process offers several possible benefits:</span></span>

-   <span data-ttu-id="7cf68-108">Isolamento degli errori e possibilità di servire contemporaneamente più client.</span><span class="sxs-lookup"><span data-stu-id="7cf68-108">Fault isolation and the ability to service multiple clients simultaneously.</span></span>
-   <span data-ttu-id="7cf68-109">In un ambiente distribuito, è possibile usare un'implementazione del server DLL per servire i client remoti.</span><span class="sxs-lookup"><span data-stu-id="7cf68-109">In a distributed environment, a DLL server implementation could be used to service remote clients.</span></span>
-   <span data-ttu-id="7cf68-110">Potrebbe consentire ai client di proteggersi da codice server non attendibile consentendo loro di accedere ai servizi forniti dal server DLL.</span><span class="sxs-lookup"><span data-stu-id="7cf68-110">It could permit clients to help protect themselves from untrusted server code while allowing them access to the services the DLL server provides.</span></span>
-   <span data-ttu-id="7cf68-111">L'esecuzione di un server DLL in un surrogato fornisce la DLL con la sicurezza del surrogato.</span><span class="sxs-lookup"><span data-stu-id="7cf68-111">Running a DLL server in a surrogate provides the DLL with the surrogate's security.</span></span>

<span data-ttu-id="7cf68-112">COM fornisce un processo surrogato predefinito oppure è possibile scrivere un surrogato personalizzato se si hanno esigenze particolari.</span><span class="sxs-lookup"><span data-stu-id="7cf68-112">COM provides a default surrogate process, or you can write a custom surrogate if you have special needs.</span></span>

<span data-ttu-id="7cf68-113">Negli argomenti seguenti vengono fornite ulteriori informazioni sui surrogati della DLL:</span><span class="sxs-lookup"><span data-stu-id="7cf68-113">The following topics provide more information on DLL surrogates:</span></span>

-   [<span data-ttu-id="7cf68-114">Requisiti del server DLL</span><span class="sxs-lookup"><span data-stu-id="7cf68-114">DLL Server Requirements</span></span>](dll-server-requirements.md)
-   [<span data-ttu-id="7cf68-115">Uso del surrogato System-Supplied</span><span class="sxs-lookup"><span data-stu-id="7cf68-115">Using the System-Supplied Surrogate</span></span>](using-the-system-supplied-surrogate.md)
-   [<span data-ttu-id="7cf68-116">Scrittura di un surrogato personalizzato</span><span class="sxs-lookup"><span data-stu-id="7cf68-116">Writing a Custom Surrogate</span></span>](writing-a-custom-surrogate.md)

 

 




