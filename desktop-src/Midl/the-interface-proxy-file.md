---
title: File proxy di interfaccia
description: Il file proxy di interfaccia (U \_ p. c) è un file c che contiene routine equivalenti a quelle negli stub client e nei file stub del server di un'interfaccia di oggetto (com).
ms.assetid: f85f7384-a590-4146-9705-2e87f1a0a87a
keywords:
- MIDL e COM MIDL, interfacce, file proxy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7be52b3561af03df0375212d729f64f41e3cdd7b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955657"
---
# <a name="the-interface-proxy-file"></a><span data-ttu-id="6c160-104">File proxy di interfaccia</span><span class="sxs-lookup"><span data-stu-id="6c160-104">The Interface Proxy File</span></span>

<span data-ttu-id="6c160-105">Il file proxy di interfaccia (U \_ p. c) è un file c che contiene routine equivalenti a quelle negli stub client e nei file stub del server di un'interfaccia di oggetto (com).</span><span class="sxs-lookup"><span data-stu-id="6c160-105">The interface proxy file (U\_p.c) is a C file that contains routines equivalent to those in the client stub and server stub files of an object (COM) interface.</span></span> <span data-ttu-id="6c160-106">Questo file contiene le implementazioni delle routine surrogate per il client e il server in modalità inline del compilatore, i dati e i thunk equivalenti nelle modalità interpretate, nonché altri dati di Glue COM appropriati, ad esempio il proxy e lo stub vtable.</span><span class="sxs-lookup"><span data-stu-id="6c160-106">This file contains implementations of the surrogate routines for client and server in the inline mode of the compiler or equivalent data and thunks in the interpreted modes, as well as other appropriate COM glue data, such as the proxy and stub Vtables.</span></span>

<span data-ttu-id="6c160-107">Il file proxy di interfaccia include le routine e i dati di supporto solo per i metodi delle interfacce definite nel file IDL corrente.</span><span class="sxs-lookup"><span data-stu-id="6c160-107">The interface proxy file includes the supporting routines and data only for methods of the interfaces defined in the current IDL file.</span></span> <span data-ttu-id="6c160-108">Per chiarire questo comportamento, in questa sezione viene usato un esempio esteso.</span><span class="sxs-lookup"><span data-stu-id="6c160-108">To clarify this behavior, an extended example is used throughout this section.</span></span> <span data-ttu-id="6c160-109">Quando si compila un file IDL con un'interfaccia come IFaceB che eredita da IFaceA, vengono generati i dati e le routine ausiliari correlati a IFaceB per il file proxy corrente, mentre l'interfaccia di base IFaceA i dati e le routine ausiliari correlati. si trovano nel proxy generato dal file IDL contenente la definizione IFaceA.</span><span class="sxs-lookup"><span data-stu-id="6c160-109">When compiling an IDL file with an interface such as IFaceB that inherits from IFaceA, IFaceB related auxiliary data and routines are generated to the current proxy file, while the base interface IFaceA related auxiliary data and routines are found in the proxy generated from the IDL file containing the IFaceA definition.</span></span> <span data-ttu-id="6c160-110">Il compilatore genera tutti i dati necessari per identificare i surrogati dell'interfaccia di base e per delegarli quando necessario per supportare i metodi IFaceA usati tramite l'interfaccia IFaceB.</span><span class="sxs-lookup"><span data-stu-id="6c160-110">The compiler generates all data necessary to identify the surrogates of the base interface, and to delegate to them when needed to support the IFaceA methods used through IFaceB interface.</span></span>

<span data-ttu-id="6c160-111">Per ogni metodo in un'interfaccia del file IDL corrente, il file proxy contiene i due metodi surrogati seguenti se compilati in modalità mista ([/OS](-os.md)) e dati dell'interprete equivalenti quando vengono compilati in modalità interprete ([/OI](-oi.md)).</span><span class="sxs-lookup"><span data-stu-id="6c160-111">For every method in an interface in the current IDL file, the proxy file contains the following two surrogate methods when compiled in the mixed mode ([/Os](-os.md)), and equivalent interpreter data when compiled in the interpreter mode ([/Oi](-oi.md)).</span></span>

-   <span data-ttu-id="6c160-112">Surrogato del lato client, ad esempio il \_ proxy del metodo IFaceB \_ in questo esempio.</span><span class="sxs-lookup"><span data-stu-id="6c160-112">The client-side surrogate, such as IFaceB\_Method\_Proxy in this example.</span></span>

    <span data-ttu-id="6c160-113">Questo surrogato sul lato client è il punto di ingresso virtuale a cui viene inviato il client, ad esempio IFaceB:: Method.</span><span class="sxs-lookup"><span data-stu-id="6c160-113">This client-side surrogate is the virtual entry point to which the client, for example IFaceB::Method, dispatches.</span></span> <span data-ttu-id="6c160-114">Esegue il marshalling degli argomenti di input in un form transmittable, trasmette gli argomenti di marshalling insieme alle informazioni che identificano l'interfaccia e l'operazione, quindi esegue l'unmarshalling del valore restituito e degli eventuali argomenti di output quando l'operazione richiamata restituisce.</span><span class="sxs-lookup"><span data-stu-id="6c160-114">It marshals the input arguments into a transmittable form, transmits the marshaled arguments along with information that identifies the interface and the operation, and then unmarshals the return value and any output arguments when the invoked operation returns.</span></span>

-   <span data-ttu-id="6c160-115">Surrogato lato server, ad esempio, \_ Stub metodo IFaceB \_ .</span><span class="sxs-lookup"><span data-stu-id="6c160-115">The server-side surrogate, for example, IFaceB\_Method\_Stub .</span></span>

    <span data-ttu-id="6c160-116">Questo surrogato sul lato server è il punto di ingresso virtuale che il runtime sottostante invia al server per emulare il client.</span><span class="sxs-lookup"><span data-stu-id="6c160-116">This server-side surrogate is the virtual entry point that the underlying runtime dispatches to at the server to emulate the client.</span></span> <span data-ttu-id="6c160-117">Esegue l'unmarshalling degli argomenti di input per replicare i dati del client, richiama l'implementazione del server della funzione di interfaccia, quindi esegue il marshalling e trasmette il valore restituito e gli eventuali argomenti di output al lato client.</span><span class="sxs-lookup"><span data-stu-id="6c160-117">It unmarshals the input arguments to replicate the client data, invokes the server's implementation of the interface function, and then marshals and transmits the return value and any output arguments back to the client side.</span></span>

<span data-ttu-id="6c160-118">Il nome predefinito per un file proxy generato da un file. idl è il file \_ p. c. utilizzare l'opzione del compilatore MIDL [**/proxy**](-proxy.md) per eseguire l'override del nome predefinito del file proxy di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="6c160-118">The default name for a proxy file generated from a file.idl is file\_p.c.Use the [**/proxy**](-proxy.md) MIDL compiler switch to override the default name of the interface proxy file.</span></span> <span data-ttu-id="6c160-119">Le opzioni [**/ENV**](-env.md) e [**/out**](-out.md) influiscono sul file.</span><span class="sxs-lookup"><span data-stu-id="6c160-119">The [**/env**](-env.md) and [**/out**](-out.md) switches affect this file.</span></span>

 

 




