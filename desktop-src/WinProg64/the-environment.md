---
title: Ambiente
description: Gli sviluppatori che lavorano sulle applicazioni per Windows a 64 bit troveranno l'ambiente di sviluppo praticamente identico all'ambiente di sviluppo per Windows a 32 bit.
ms.assetid: 49b2b952-f771-4721-a9b0-01eb67a98007
keywords:
- ambiente di sviluppo programmazione Windows a 64 bit
- ambiente a 64 bit programmazione Windows
- Guida alla programmazione di Windows a 64 bit Guida alla programmazione Windows a 64 bit, ambiente di sviluppo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 104ea1bdacbb478eaa0abcf46d04c3d772540f26
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044383"
---
# <a name="the-environment"></a><span data-ttu-id="ba2c4-106">Ambiente</span><span class="sxs-lookup"><span data-stu-id="ba2c4-106">The Environment</span></span>

<span data-ttu-id="ba2c4-107">Gli sviluppatori che lavorano sulle applicazioni per Windows a 64 bit troveranno l'ambiente di sviluppo praticamente identico all'ambiente di sviluppo per Windows a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="ba2c4-107">Developers working on applications for 64-bit Windows will find the development environment virtually identical to the development environment for 32-bit Windows.</span></span> <span data-ttu-id="ba2c4-108">Le API esistenti sono state modificate laddove necessario per consentire loro di riflettere la precisione della piattaforma in cui sono in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="ba2c4-108">The existing APIs have been modified where necessary to allow them to reflect the precision of the platform on which they are running.</span></span> <span data-ttu-id="ba2c4-109">Il risultato è la semplicità e una breve curva di apprendimento per lo sviluppatore: la scrittura di codice per Windows a 64 bit è esattamente come la scrittura di codice per Windows a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="ba2c4-109">The result is simplicity and a short learning curve for the developer—writing code for 64-bit Windows is just like writing code for 32-bit Windows.</span></span>

<span data-ttu-id="ba2c4-110">I file di intestazione di Windows supportano i nuovi tipi di dati che consentono a puntatori e variabili associate a puntatore di riflettere la precisione della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="ba2c4-110">The Windows header files support new data types that allow pointers and pointer-associated variables to reflect the precision of the platform.</span></span> <span data-ttu-id="ba2c4-111">Ciò significa che gli sviluppatori possono compilare una singola base di origine per l'esecuzione a livello nativo in Windows a 32 bit o a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="ba2c4-111">This means that developers can compile a single source base to run natively on either 32-bit Windows or 64-bit Windows.</span></span> <span data-ttu-id="ba2c4-112">Questa strategia consente di ridurre i costi di sviluppo di applicazioni che sfruttano l'hardware a 64 bit, ad esempio processori AMD Opteron o Athlon64 o processori Intel Itanium.</span><span class="sxs-lookup"><span data-stu-id="ba2c4-112">This strategy reduces the cost of developing applications that leverage 64-bit hardware such as AMD Opteron or Athlon64 processors or Intel Itanium processors.</span></span>

<span data-ttu-id="ba2c4-113">Se si adottano le nuove convenzioni del tipo di dati appena possibile, sarà necessario più tempo per rendere le applicazioni disponibili a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="ba2c4-113">You will have more time to make your applications 64-bit ready if you adopt the new data-type conventions as soon as possible.</span></span> <span data-ttu-id="ba2c4-114">Se si modifica il codice, è necessario modificare le definizioni dei dati nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="ba2c4-114">If you are changing your code, you should change the data definitions at the same time.</span></span> <span data-ttu-id="ba2c4-115">Testare l'applicazione in Windows a 32 bit, eseguirla tramite il compilatore a 64 bit (descritto negli [strumenti](the-tools.md)) e l'applicazione sarà pronta per essere testata quando si dispone dell'hardware a 64 bit appropriato.</span><span class="sxs-lookup"><span data-stu-id="ba2c4-115">Test the application on 32-bit Windows, run it through the 64-bit compiler (described in [The Tools](the-tools.md)), and the application will be ready to test when you have the appropriate 64-bit hardware.</span></span>

 

 




