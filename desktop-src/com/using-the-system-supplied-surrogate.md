---
title: Uso del surrogato System-Supplied
description: Uso del surrogato System-Supplied
ms.assetid: 6709e5e2-50e0-470f-b618-3d3043f6e180
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 444cb94c5564a78ec5580ae8e7f781e91a8a9c15
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332479"
---
# <a name="using-the-system-supplied-surrogate"></a><span data-ttu-id="b0b89-103">Uso del surrogato System-Supplied</span><span class="sxs-lookup"><span data-stu-id="b0b89-103">Using the System-Supplied Surrogate</span></span>

<span data-ttu-id="b0b89-104">Per utilizzare il surrogato fornito dal sistema per il server DLL, registrare la DLL specificando una stringa vuota o **null** per il valore [DllSurrogate](dllsurrogate.md) nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="b0b89-104">To use the system-supplied surrogate for your DLL server, register the DLL specifying an empty string or **NULL** for the [DllSurrogate](dllsurrogate.md) value in the registry.</span></span> <span data-ttu-id="b0b89-105">Quando una richiesta di attivazione per un server DLL designato si avvicina a COM, COM avvia il processo surrogato predefinito e la DLL richiesta (specificando il CLSID nella riga di comando Launch internamente) allo stesso tempo per evitare una chiamata separata.</span><span class="sxs-lookup"><span data-stu-id="b0b89-105">When an activation request for a DLL server so designated comes to COM, COM launches the default surrogate process and the requested DLL (by specifying the CLSID on the launch command line internally) at the same time to avoid a separate call.</span></span> <span data-ttu-id="b0b89-106">Per informazioni sull'esecuzione di più di un server DLL in un processo surrogato, vedere la pagina relativa alla [condivisione dei surrogati](surrogate-sharing.md).</span><span class="sxs-lookup"><span data-stu-id="b0b89-106">(For information on running more than one DLL server in a surrogate process, see [Surrogate Sharing](surrogate-sharing.md).)</span></span>

<span data-ttu-id="b0b89-107">L'implementazione predefinita del processo surrogato è un server pseudo-COM di tipo modello a thread misto.</span><span class="sxs-lookup"><span data-stu-id="b0b89-107">The default implementation of the surrogate process is a mixed-threading model style pseudo-COM server.</span></span> <span data-ttu-id="b0b89-108">Quando più server DLL vengono caricati in un singolo processo surrogato, questo processo assicura che venga creata un'istanza di ogni server DLL utilizzando il modello di threading specificato nel registro di sistema per tale server.</span><span class="sxs-lookup"><span data-stu-id="b0b89-108">When multiple DLL servers are loaded into a single surrogate process, this process ensures that each DLL server is instantiated using the threading model specified in the registry for that server.</span></span> <span data-ttu-id="b0b89-109">Tutti i server a thread libero caricati si troveranno insieme nell'apartment multithread, mentre ogni server con threading Apartment si troverà in un Apartment a thread singolo.</span><span class="sxs-lookup"><span data-stu-id="b0b89-109">All loaded free-threaded servers will live together in the multithreaded apartment, while each apartment-threaded server will reside in a single-threaded apartment.</span></span> <span data-ttu-id="b0b89-110">Se un server DLL supporta entrambi i modelli di threading, COM sceglierà il multithreading.</span><span class="sxs-lookup"><span data-stu-id="b0b89-110">If a DLL server supports both threading models, COM will choose multithreading.</span></span>

<span data-ttu-id="b0b89-111">Questo processo surrogato viene scritto in modo che COM gestisca lo scaricamento dei server DLL e la terminazione del processo surrogato.</span><span class="sxs-lookup"><span data-stu-id="b0b89-111">This surrogate process is written so that COM handles both the unloading of DLL servers and the terminating of the surrogate process.</span></span>

<span data-ttu-id="b0b89-112">Il surrogato fornito dal sistema funziona molto bene per la maggior parte degli sviluppatori, oltre a essere molto facile da usare.</span><span class="sxs-lookup"><span data-stu-id="b0b89-112">The system-provided surrogate will work very well for most developers, as well as being very easy to use.</span></span> <span data-ttu-id="b0b89-113">Tuttavia, gli sviluppatori con considerazioni speciali possono decidere che è necessario un surrogato personalizzato.</span><span class="sxs-lookup"><span data-stu-id="b0b89-113">However, those developers with special considerations may decide that a custom surrogate is necessary.</span></span> <span data-ttu-id="b0b89-114">Per ulteriori informazioni, vedere [scrittura di un surrogato personalizzato](writing-a-custom-surrogate.md).</span><span class="sxs-lookup"><span data-stu-id="b0b89-114">For more information, see [Writing a Custom Surrogate](writing-a-custom-surrogate.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b0b89-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b0b89-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0b89-116">Surrogati DLL</span><span class="sxs-lookup"><span data-stu-id="b0b89-116">DLL Surrogates</span></span>](dll-surrogates.md)
</dt> </dl>

 

 




