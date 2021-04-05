---
title: Individuazione di un oggetto remoto
description: Individuazione di un oggetto remoto
ms.assetid: b329de53-646b-42a2-afa3-06473c3483d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d0ce1b2280faaed7be3b5afb25a48438ff1a2b7
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103873034"
---
# <a name="locating-a-remote-object"></a><span data-ttu-id="a7d6c-103">Individuazione di un oggetto remoto</span><span class="sxs-lookup"><span data-stu-id="a7d6c-103">Locating a Remote Object</span></span>

<span data-ttu-id="a7d6c-104">Con l'avvento di COM per sistemi distribuiti, COM utilizza il modello di base per la creazione di oggetti descritti in [oggetti e CLSID della classe com](com-class-objects-and-clsids.md) e aggiunge più di un modo per individuare un oggetto che potrebbe trovarsi in un altro sistema in una rete, senza sovraccaricare l'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="a7d6c-104">With the advent of COM for distributed systems, COM uses the basic model for object creation described in [COM Class Objects and CLSIDs](com-class-objects-and-clsids.md) and adds more than one way to locate an object that might reside on another system in a network, without overburdening the client application.</span></span>

<span data-ttu-id="a7d6c-105">COM ha aggiunto chiavi del registro di sistema che consentono a un server di registrare il nome del computer in cui risiede o il computer in cui si trova una risorsa di archiviazione esistente.</span><span class="sxs-lookup"><span data-stu-id="a7d6c-105">COM has added registry keys that permit a server to register the name of the machine on which it resides or the machine where an existing storage is located.</span></span> <span data-ttu-id="a7d6c-106">Pertanto, le applicazioni client devono essere in grado di comprendere solo il CLSID del server.</span><span class="sxs-lookup"><span data-stu-id="a7d6c-106">Therefore, client applications need know only the CLSID of the server.</span></span>

<span data-ttu-id="a7d6c-107">Tuttavia, per i casi in cui si desidera, COM ha sostituito un parametro precedentemente riservato di [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) con una struttura [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) , che consente a un client di specificare il percorso di un server.</span><span class="sxs-lookup"><span data-stu-id="a7d6c-107">However, for cases where it is desired, COM has replaced a previously reserved parameter of [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) with a [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) structure, which allows a client to specify the location of a server.</span></span> <span data-ttu-id="a7d6c-108">Un altro importante valore nella funzione **CoGetClassObject** è l'enumerazione [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) , che specifica se l'oggetto previsto deve essere eseguito in-process, out-of-process locale o out-of-process remote.</span><span class="sxs-lookup"><span data-stu-id="a7d6c-108">Another important value in the **CoGetClassObject** function is the [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) enumeration, which specifies whether the expected object is to be run in-process, out-of-process local, or out-of-process remote.</span></span> <span data-ttu-id="a7d6c-109">Insieme, questi due valori e i valori nel registro di sistema determinano come e dove deve essere eseguito l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a7d6c-109">Taken together, these two values and the values in the registry determine how and where the object is to be run.</span></span>

> [!Note]  
> <span data-ttu-id="a7d6c-110">Per la creazione di istanze, quando specificano un percorso del server, può eseguire l'override di un'impostazione del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="a7d6c-110">Instance creation calls, when they specify a server location, can override a registry setting.</span></span> <span data-ttu-id="a7d6c-111">L'algoritmo COM utilizzato per eseguire questa operazione è descritto nel riferimento per l'enumerazione [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) .</span><span class="sxs-lookup"><span data-stu-id="a7d6c-111">The algorithm COM uses for doing this is described in the reference for the [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) enumeration.</span></span>

 

<span data-ttu-id="a7d6c-112">L'attivazione remota dipende dalla relazione di sicurezza tra client e server.</span><span class="sxs-lookup"><span data-stu-id="a7d6c-112">Remote activation depends on the security relationship between client and server.</span></span> <span data-ttu-id="a7d6c-113">Per ulteriori informazioni, vedere [sicurezza in com](security-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="a7d6c-113">For more information, see [Security in COM](security-in-com.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a7d6c-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a7d6c-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7d6c-115">Oggetti classe COM e CLSID</span><span class="sxs-lookup"><span data-stu-id="a7d6c-115">COM Class Objects and CLSIDs</span></span>](com-class-objects-and-clsids.md)
</dt> <dt>

[<span data-ttu-id="a7d6c-116">Creazione di un oggetto tramite un oggetto classe</span><span class="sxs-lookup"><span data-stu-id="a7d6c-116">Creating an Object Through a Class Object</span></span>](creating-an-object-through-a-class-object.md)
</dt> </dl>

 

 