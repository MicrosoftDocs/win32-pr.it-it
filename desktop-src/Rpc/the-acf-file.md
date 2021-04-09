---
title: Il file ACF
description: Il file ACF consente di personalizzare l'interfaccia RPC del client e/o delle applicazioni server senza influire sulle caratteristiche di rete dell'interfaccia.
ms.assetid: 7d3fef5c-b645-4e10-b08d-b339025718b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9e803201004cd73a4be507aaba2affd20f1ea3d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963412"
---
# <a name="the-acf-file"></a><span data-ttu-id="459b3-103">Il file ACF</span><span class="sxs-lookup"><span data-stu-id="459b3-103">The ACF File</span></span>

<span data-ttu-id="459b3-104">Il file ACF consente di personalizzare l'interfaccia RPC del client e/o delle applicazioni server senza influire sulle caratteristiche di rete dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="459b3-104">The ACF file enables you to customize your client and/or server applications' RPC interface without affecting the network characteristics of the interface.</span></span> <span data-ttu-id="459b3-105">Se, ad esempio, l'applicazione client contiene una struttura di dati complessa che ha un significato solo nel computer locale, è possibile specificare nel file ACF il modo in cui i dati della struttura possono essere rappresentati in un form indipendente dal computer per le chiamate di procedure remote.</span><span class="sxs-lookup"><span data-stu-id="459b3-105">For example, if your client application contains a complex data structure that only has meaning on the local machine, you can specify in the ACF file how the data in that structure can be represented in a machine-independent form for remote procedure calls.</span></span>

<span data-ttu-id="459b3-106">In questa esercitazione viene illustrato un altro utilizzo del file ACF, che specifica il tipo di handle di associazione che rappresenta la connessione tra client e server.</span><span class="sxs-lookup"><span data-stu-id="459b3-106">This tutorial demonstrates another use of the ACF file—specifying the type of binding handle that represents the connection between client and server.</span></span> <span data-ttu-id="459b3-107">L' **\[** [**attributo \_ handle implicito**](/windows/desktop/Midl/implicit-handle) **\]** nell'intestazione ACF consente all'applicazione client di selezionare un server per la chiamata di procedura remota.</span><span class="sxs-lookup"><span data-stu-id="459b3-107">The **\[**[**implicit\_handle**](/windows/desktop/Midl/implicit-handle)**\]** attribute in the ACF header allows the client application to select a server for its remote procedure call.</span></span> <span data-ttu-id="459b3-108">L'oggetto ACF definisce l'handle che deve essere del tipo [**handle \_ t**](/windows/desktop/Midl/handle-t) (un tipo di dati primitivo MIDL).</span><span class="sxs-lookup"><span data-stu-id="459b3-108">The ACF defines the handle to be of the type [**handle\_t**](/windows/desktop/Midl/handle-t) (a MIDL primitive data type).</span></span> <span data-ttu-id="459b3-109">Il compilatore MIDL inserisce il nome dell'handle di associazione specificato da ACF, Hello \_ IfHandle nel file di intestazione generato.</span><span class="sxs-lookup"><span data-stu-id="459b3-109">The MIDL compiler will put the binding handle name that the ACF specified, hello\_IfHandle into the header file it generates.</span></span> <span data-ttu-id="459b3-110">Si noti che questo particolare file ACF ha un corpo vuoto.</span><span class="sxs-lookup"><span data-stu-id="459b3-110">Notice that this particular ACF file has an empty body.</span></span>

``` syntax
//file: hello.acf
[
    implicit_handle (handle_t hello_IfHandle)
] 
interface hello
{
}
```

<span data-ttu-id="459b3-111">Il compilatore MIDL dispone di un'opzione, [**/app \_ config**](/windows/desktop/Midl/-app-config), che consente di includere determinati attributi ACF, ad **esempio \_ handle implicito**, nel file IDL, anziché creare un file ACF separato.</span><span class="sxs-lookup"><span data-stu-id="459b3-111">The MIDL compiler has an option, [**/app\_config**](/windows/desktop/Midl/-app-config), that lets you include certain ACF attributes, such as **implicit\_handle**, in the IDL file, rather than creating a separate ACF file.</span></span> <span data-ttu-id="459b3-112">Provare a usare questa opzione se l'applicazione non richiede una grande configurazione speciale e se la compatibilità OSF rigida non costituisce un problema.</span><span class="sxs-lookup"><span data-stu-id="459b3-112">Consider using this option if your application doesn't require a lot of special configuration and if strict OSF compatibility is not an issue.</span></span>

 

 