---
title: File IDL
description: Il file IDL è costituito da una o più definizioni di interfaccia, ognuna delle quali dispone di un'intestazione e di un corpo.
ms.assetid: 64a30a12-a53e-4c53-b8cf-7af85ffd0a94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 862adfad2a43f10dac3598279554fd6e1f00a302
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473294"
---
# <a name="the-idl-file"></a><span data-ttu-id="dadb4-103">File IDL</span><span class="sxs-lookup"><span data-stu-id="dadb4-103">The IDL File</span></span>

<span data-ttu-id="dadb4-104">Il file IDL è costituito da una o più definizioni di interfaccia, ognuna delle quali dispone di un'intestazione e di un corpo.</span><span class="sxs-lookup"><span data-stu-id="dadb4-104">The IDL file consists of one or more interface definitions, each of which has a header and a body.</span></span> <span data-ttu-id="dadb4-105">L'intestazione contiene informazioni che si applicano all'intera interfaccia, ad esempio l'UUID.</span><span class="sxs-lookup"><span data-stu-id="dadb4-105">The header contains information that applies to the entire interface, such as the UUID.</span></span> <span data-ttu-id="dadb4-106">Queste informazioni sono racchiuse tra parentesi quadre ed è seguita dall' **interfaccia** della parola chiave e dal nome dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="dadb4-106">This information is enclosed in square brackets and is followed by the keyword **interface** and the interface name.</span></span> <span data-ttu-id="dadb4-107">Il corpo contiene le definizioni del tipo di dati C e i prototipi di funzione, integrati con attributi che descrivono in che modo i dati vengono trasmessi in rete.</span><span class="sxs-lookup"><span data-stu-id="dadb4-107">The body contains C-style data type definitions and function prototypes, augmented with attributes that describe how the data is transmitted over the network.</span></span>

<span data-ttu-id="dadb4-108">In questo esempio, l'intestazione dell'interfaccia contiene solo l'UUID e il numero di versione.</span><span class="sxs-lookup"><span data-stu-id="dadb4-108">In this example, the interface header contains only the UUID and the version number.</span></span> <span data-ttu-id="dadb4-109">Il numero di versione garantisce che, in presenza di più versioni di un'interfaccia RPC, verranno connesse solo le versioni compatibili del client e del server.</span><span class="sxs-lookup"><span data-stu-id="dadb4-109">The version number ensures that when there are multiple versions of an RPC interface, only compatible versions of the client and server will be connected.</span></span>

<span data-ttu-id="dadb4-110">Il corpo dell'interfaccia contiene il prototipo di funzione per **HelloProc**.</span><span class="sxs-lookup"><span data-stu-id="dadb4-110">The interface body contains the function prototype for **HelloProc**.</span></span> <span data-ttu-id="dadb4-111">In questo prototipo, il parametro della funzione pszString ha gli attributi **\[** [**in**](/windows/desktop/Midl/in) **\]** e **\[** [**String**](/windows/desktop/Midl/string) **\]** .</span><span class="sxs-lookup"><span data-stu-id="dadb4-111">In this prototype, the function parameter pszString has the attributes **\[**[**in**](/windows/desktop/Midl/in)**\]** and **\[**[**string**](/windows/desktop/Midl/string)**\]**.</span></span> <span data-ttu-id="dadb4-112">L'attributo **\[ in \]** indica alla libreria di runtime che il parametro viene passato solo dal client al server.</span><span class="sxs-lookup"><span data-stu-id="dadb4-112">The **\[in\]** attribute tells the run-time library that the parameter is passed only from the client to the server.</span></span> <span data-ttu-id="dadb4-113">L'attributo **\[ String \]** specifica che lo stub deve considerare il parametro come una stringa di caratteri di tipo C.</span><span class="sxs-lookup"><span data-stu-id="dadb4-113">The **\[string\]** attribute specifies that the stub should treat the parameter as a C-style character string.</span></span>

<span data-ttu-id="dadb4-114">L'applicazione client deve essere in grado di arrestare l'applicazione server, quindi l'interfaccia contiene un prototipo per un'altra funzione remota,**Shutdown** , che verrà implementata più avanti in questa esercitazione.</span><span class="sxs-lookup"><span data-stu-id="dadb4-114">The client application should be able to shut down the server application, so the interface contains a prototype for another remote function,**Shutdown** , that will be implemented later in this tutorial.</span></span>

``` syntax
//file hello.idl
[
    uuid(7a98c250-6808-11cf-b73b-00aa00b677a7),
    version(1.0)
]
interface hello
{
    void HelloProc([in, string] unsigned char * pszString);
    void Shutdown(void);
}
```

 

 