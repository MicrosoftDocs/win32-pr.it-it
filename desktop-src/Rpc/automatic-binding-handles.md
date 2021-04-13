---
title: Handle di binding automatici
description: Gli handle di binding automatici sono utili quando l'applicazione non richiede un server specifico e quando non è necessario mantenere le informazioni sullo stato tra il client e il server.
ms.assetid: ba049369-6c8b-4313-a266-e0364a30056e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fe83d3f9029e0384c87e5e409583ff70f1e91ac
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338782"
---
# <a name="automatic-binding-handles"></a><span data-ttu-id="26729-103">Handle di binding automatici</span><span class="sxs-lookup"><span data-stu-id="26729-103">Automatic Binding Handles</span></span>

<span data-ttu-id="26729-104">Gli handle di binding automatici sono utili quando l'applicazione non richiede un server specifico e quando non è necessario mantenere le informazioni sullo stato tra il client e il server.</span><span class="sxs-lookup"><span data-stu-id="26729-104">Automatic binding handles are useful when the application does not require a specific server and when it does not need to maintain any state information between the client and server.</span></span> <span data-ttu-id="26729-105">Quando si usa un handle di binding automatico, non è necessario scrivere codice dell'applicazione client per gestire l'associazione e gli handle. è sufficiente specificare l'uso dell'handle di binding automatico nel file di configurazione dell'applicazione (ACF).</span><span class="sxs-lookup"><span data-stu-id="26729-105">When you use an automatic binding handle, you do not have to write any client application code to deal with binding and handles—you simply specify the use of the automatic binding handle in the application configuration file (ACF).</span></span> <span data-ttu-id="26729-106">Lo stub definisce quindi l'handle e gestisce l'associazione.</span><span class="sxs-lookup"><span data-stu-id="26729-106">The stub then defines the handle and manages the binding.</span></span>

<span data-ttu-id="26729-107">Ad esempio, un'operazione timestamp può essere implementata usando un handle automatico.</span><span class="sxs-lookup"><span data-stu-id="26729-107">For example, a time-stamp operation can be implemented using an auto handle.</span></span> <span data-ttu-id="26729-108">Non fa alcuna differenza per l'applicazione client che il server fornisce al timestamp perché può accettare l'ora da qualsiasi server disponibile.</span><span class="sxs-lookup"><span data-stu-id="26729-108">It makes no difference to the client application which server provides it with the time stamp because it can accept the time from any available server.</span></span>

> [!Note]  
> <span data-ttu-id="26729-109">Gli handle automatici non sono supportati per la piattaforma Macintosh.</span><span class="sxs-lookup"><span data-stu-id="26729-109">Auto handles are not supported for the Macintosh platform.</span></span>

 

<span data-ttu-id="26729-110">È possibile specificare l'uso di handle automatici includendo l' \[ attributo [**\_ handle automatico**](/windows/desktop/Midl/auto-handle) \] in ACF.</span><span class="sxs-lookup"><span data-stu-id="26729-110">You specify the use of auto handles by including the \[[**auto\_handle**](/windows/desktop/Midl/auto-handle)\] attribute in the ACF.</span></span> <span data-ttu-id="26729-111">Nell'esempio relativo al timestamp viene usato il seguente ACF:</span><span class="sxs-lookup"><span data-stu-id="26729-111">The time-stamp example uses the following ACF:</span></span>

``` syntax
/* ACF file */
[
  auto_handle
]
interface autoh
{
}
```

<span data-ttu-id="26729-112">Quando ACF non include altri attributi di handle e quando le procedure remote non usano handle espliciti, il compilatore MIDL usa gli handle automatici per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="26729-112">When the ACF does not include any other handle attribute, and when the remote procedures do not use explicit handles, the MIDL compiler uses automatic handles by default.</span></span> <span data-ttu-id="26729-113">USA anche handle automatici come impostazione predefinita quando l'ACF non è presente.</span><span class="sxs-lookup"><span data-stu-id="26729-113">It also uses automatic handles as the default when the ACF is not present.</span></span>

<span data-ttu-id="26729-114">Le procedure remote vengono specificate nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="26729-114">The remote procedures are specified in the IDL file.</span></span> <span data-ttu-id="26729-115">L'handle automatico non deve essere visualizzato come argomento della procedura remota.</span><span class="sxs-lookup"><span data-stu-id="26729-115">The auto handle must not appear as an argument to the remote procedure.</span></span> <span data-ttu-id="26729-116">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="26729-116">For example:</span></span>

``` syntax
/* IDL file */
[ 
  uuid (6B29FC40-CA47-1067-B31D-00DD010662DA),
  version(1.0),
  pointer_default(unique)
]
interface autoh
{
  void GetTime([out] long * time);
  void Shutdown(void);
}
```

<span data-ttu-id="26729-117">Il vantaggio dell'handle automatico è che lo sviluppatore non deve scrivere codice per gestire l'handle; gli stub gestiscono automaticamente l'associazione.</span><span class="sxs-lookup"><span data-stu-id="26729-117">The benefit of the auto handle is that the developer does not have to write any code to manage the handle; the stubs manage the binding automatically.</span></span> <span data-ttu-id="26729-118">Questo è significativamente diverso dall' [esempio Hello, World](tutorial.md), in cui il client gestisce l'handle primitivo implicito definito in ACF e deve chiamare diverse funzioni di run-time per stabilire l'handle di associazione.</span><span class="sxs-lookup"><span data-stu-id="26729-118">This is significantly different from the [Hello, World example](tutorial.md), where the client manages the implicit primitive handle defined in the ACF and must call several run-time functions to establish the binding handle.</span></span>

 

 