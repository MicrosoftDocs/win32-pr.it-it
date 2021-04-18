---
title: Handle di binding espliciti
description: Per il massimo controllo sul processo di associazione, le applicazioni client/server possono utilizzare handle di binding espliciti.
ms.assetid: e711ce37-92f0-4e60-a126-148c27662c26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b391c339ac3747928e3394152e9c0de7c1c7aa0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298343"
---
# <a name="explicit-binding-handles"></a><span data-ttu-id="846a2-103">Handle di binding espliciti</span><span class="sxs-lookup"><span data-stu-id="846a2-103">Explicit Binding Handles</span></span>

<span data-ttu-id="846a2-104">Per il massimo controllo sul processo di associazione, le applicazioni client/server possono utilizzare handle di binding espliciti.</span><span class="sxs-lookup"><span data-stu-id="846a2-104">For maximum control over the binding process, client/server applications may use explicit binding handles.</span></span> <span data-ttu-id="846a2-105">Analogamente agli handle impliciti, gli handle di binding espliciti consentono all'applicazione client di selezionare un server per l'esecuzione delle chiamate.</span><span class="sxs-lookup"><span data-stu-id="846a2-105">Like implicit handles, explicit binding handles enable your client application to select a server to execute its calls.</span></span> <span data-ttu-id="846a2-106">Inoltre, gli handle di binding espliciti consentono all'applicazione client/server di creare una sessione di comunicazione RPC autenticata.</span><span class="sxs-lookup"><span data-stu-id="846a2-106">In addition, explicit binding handles enable your client/server application to create an authenticated RPC communication session.</span></span> <span data-ttu-id="846a2-107">Con gli handle espliciti, il client può connettersi a più di un server ed eseguire procedure remote su più server.</span><span class="sxs-lookup"><span data-stu-id="846a2-107">With explicit handles, your client can connect to more than one server and execute remote procedures on multiple servers.</span></span> <span data-ttu-id="846a2-108">Le applicazioni client multithreading e asincrone possono anche connettersi a più server ed eseguire contemporaneamente più procedure remote.</span><span class="sxs-lookup"><span data-stu-id="846a2-108">Multithreaded and asynchronous client applications can even connect to multiple servers and execute multiple remote procedures at the same time.</span></span>

<span data-ttu-id="846a2-109">L'applicazione client deve passare l'handle esplicito come parametro a ogni chiamata di procedura remota.</span><span class="sxs-lookup"><span data-stu-id="846a2-109">Your client application must pass the explicit handle as a parameter to each remote procedure call.</span></span> <span data-ttu-id="846a2-110">Per essere conforme allo standard OSF, l'handle deve essere specificato come primo parametro in ogni procedura remota.</span><span class="sxs-lookup"><span data-stu-id="846a2-110">To conform to the OSF standard, the handle should be specified as the first parameter on each remote procedure.</span></span> <span data-ttu-id="846a2-111">Tuttavia, le estensioni Microsoft per RPC consentono di specificare il gestore di associazione in altre posizioni.</span><span class="sxs-lookup"><span data-stu-id="846a2-111">However, the Microsoft extensions to RPC enable you to specify the binding handle in other positions.</span></span> <span data-ttu-id="846a2-112">Per ulteriori informazioni, vedere [Microsoft RPC Binding-Handle Extensions](microsoft-rpc-binding-handle-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="846a2-112">For more information, see [Microsoft RPC Binding-Handle Extensions](microsoft-rpc-binding-handle-extensions.md).</span></span>

<span data-ttu-id="846a2-113">Per creare un handle esplicito, dichiarare l'handle come parametro per le operazioni remote nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="846a2-113">To create an explicit handle, declare the handle as a parameter to the remote operations in the IDL file.</span></span> <span data-ttu-id="846a2-114">È possibile ridefinire l' [esempio Hello World](tutorial.md) per usare un handle esplicito, come illustrato di seguito:</span><span class="sxs-lookup"><span data-stu-id="846a2-114">The [Hello, World example](tutorial.md) can be redefined to use an explicit handle as shown:</span></span>

``` syntax
/* IDL file for explicit handles */
 
[ 
  uuid(20B309B1-015C-101A-B308-02608C4C9B53),
  version(1.0) 
]
interface hello
{
  void HelloProc([in] handle_t h1,
                 [in, string] char *  pszString); 
}
```

<span data-ttu-id="846a2-115">È possibile combinare handle espliciti e impliciti in una singola interfaccia.</span><span class="sxs-lookup"><span data-stu-id="846a2-115">You can combine explicit and implicit handles in a single interface.</span></span> <span data-ttu-id="846a2-116">Se una funzione dispone di un handle esplicito nell'elenco di parametri, verrà usato tale handle.</span><span class="sxs-lookup"><span data-stu-id="846a2-116">If a function has an explicit handle in its parameter list, that handle will be used.</span></span> <span data-ttu-id="846a2-117">Se una funzione in un'interfaccia che usa handle impliciti non specifica un handle esplicito, verrà utilizzato l'handle implicito predefinito.</span><span class="sxs-lookup"><span data-stu-id="846a2-117">If a function in an interface using implicit handles does not specify an explicit handle, then the default implicit handle will be used.</span></span>

 

 




