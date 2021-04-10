---
title: File generati per un'interfaccia COM
description: Per le interfacce COM, il compilatore MIDL combina tutti i dati e le routine ausiliarie del client e del server oggetti in un singolo file proxy di interfaccia.
ms.assetid: 13063ee8-cb41-48a7-b90b-ea08c19c5230
keywords:
- MIDL Compiler MIDL, MIDL e COM
- MIDL COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9ea38ef85baa03890e323b4ba9d5eae4f295429
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103963007"
---
# <a name="files-generated-for-a-com-interface"></a><span data-ttu-id="cb5e9-105">File generati per un'interfaccia COM</span><span class="sxs-lookup"><span data-stu-id="cb5e9-105">Files Generated for a COM Interface</span></span>

<span data-ttu-id="cb5e9-106">Per le interfacce COM, il compilatore MIDL combina tutti i dati e le routine ausiliarie del client e del server oggetti in un singolo file proxy di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="cb5e9-106">For COM interfaces, the MIDL compiler combines all client and object server auxiliary routines and data into a single interface proxy file.</span></span> <span data-ttu-id="cb5e9-107">Questo file include i punti di ingresso surrogati per client e server.</span><span class="sxs-lookup"><span data-stu-id="cb5e9-107">This file includes the surrogate entry points for both clients and servers.</span></span> <span data-ttu-id="cb5e9-108">Il compilatore MIDL genera inoltre un file di intestazione di interfaccia, un file UUID dell'interfaccia e un file di registrazione dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="cb5e9-108">In addition, the MIDL compiler generates an interface header file, an interface UUID file and an interface registration file.</span></span> <span data-ttu-id="cb5e9-109">Si utilizzeranno tutti questi file quando si crea una DLL proxy che contiene il codice per supportare l'utilizzo dell'interfaccia da parte delle applicazioni client e dei server oggetti.</span><span class="sxs-lookup"><span data-stu-id="cb5e9-109">You will use all these files when creating a proxy DLL that contains the code to support the use of the interface by both client applications and object servers.</span></span> <span data-ttu-id="cb5e9-110">Si utilizzeranno anche il file di intestazione dell'interfaccia e il file UUID dell'interfaccia quando si crea il file eseguibile per un'applicazione client che utilizza l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="cb5e9-110">You will also use the interface header file and the interface UUID file when creating the executable file for a client application that uses the interface.</span></span>

<span data-ttu-id="cb5e9-111">Negli argomenti seguenti vengono descritti i file generati per un'interfaccia COM personalizzata, che è possibile identificare includendo l' **\[** attributo [**Object**](object.md) **\]** nell'elenco di attributi di interfaccia del file IDL:</span><span class="sxs-lookup"><span data-stu-id="cb5e9-111">The following topics describe each of the files generated for a custom COM interface, which you identify by including the **\[**[**object**](object.md)**\]** attribute in the interface attribute list of the IDL file:</span></span>

-   [<span data-ttu-id="cb5e9-112">File proxy di interfaccia</span><span class="sxs-lookup"><span data-stu-id="cb5e9-112">The Interface Proxy File</span></span>](the-interface-proxy-file.md)
-   [<span data-ttu-id="cb5e9-113">File di intestazione</span><span class="sxs-lookup"><span data-stu-id="cb5e9-113">The Header Files</span></span>](the-header-files.md)
-   [<span data-ttu-id="cb5e9-114">File UUID dell'interfaccia</span><span class="sxs-lookup"><span data-stu-id="cb5e9-114">The Interface UUID File</span></span>](the-interface-uuid-file.md)
-   [<span data-ttu-id="cb5e9-115">File di registrazione dell'interfaccia</span><span class="sxs-lookup"><span data-stu-id="cb5e9-115">The Interface Registration File</span></span>](the-interface-registration-file.md)

<span data-ttu-id="cb5e9-116">Per ulteriori informazioni, vedere il file di [configurazione dell'applicazione (ACF)](application-configuration-file-acf-.md), la [**\_ configurazione di/app**](-app-config.md), il [file di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)e [la compilazione e la registrazione di una DLL proxy](../com/building-and-registering-a-proxy-dll.md).</span><span class="sxs-lookup"><span data-stu-id="cb5e9-116">For more information, see [Application Configuration File (ACF)](application-configuration-file-acf-.md), [**/app\_config**](-app-config.md), [Interface Definition (IDL) File](interface-definition-idl-file.md), and [Building and Registering a Proxy DLL](../com/building-and-registering-a-proxy-dll.md).</span></span>

 

 