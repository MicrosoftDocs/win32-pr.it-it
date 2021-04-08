---
title: Corpo dell'interfaccia IDL
description: Il corpo dell'interfaccia IDL contiene i tipi di dati utilizzati nelle chiamate a procedure remote e i prototipi di funzione per le procedure remote.
ms.assetid: b07524a7-b27e-4ea2-ae34-068c07d9a444
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 565cbe6493bd865030b77b5e9ef6275b444ca451
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728671"
---
# <a name="the-idl-interface-body"></a><span data-ttu-id="f47bb-103">Corpo dell'interfaccia IDL</span><span class="sxs-lookup"><span data-stu-id="f47bb-103">The IDL Interface Body</span></span>

<span data-ttu-id="f47bb-104">Il corpo dell'interfaccia IDL contiene i tipi di dati utilizzati nelle chiamate a procedure remote e i prototipi di funzione per le procedure remote.</span><span class="sxs-lookup"><span data-stu-id="f47bb-104">The IDL interface body contains data types used in remote procedure calls and the function prototypes for the remote procedures.</span></span> <span data-ttu-id="f47bb-105">Il corpo dell'interfaccia può contenere anche importazioni, pragma, dichiarazioni di costanti e dichiarazioni di tipo.</span><span class="sxs-lookup"><span data-stu-id="f47bb-105">The interface body can also contain imports, pragmas, constant declarations, and type declarations.</span></span> <span data-ttu-id="f47bb-106">In modalità estensioni Microsoft, il compilatore MIDL consente anche dichiarazioni implicite sotto forma di definizioni di variabili.</span><span class="sxs-lookup"><span data-stu-id="f47bb-106">In Microsoft-extensions mode, the MIDL compiler also allows implicit declarations in the form of variable definitions.</span></span>

<span data-ttu-id="f47bb-107">Nell'esempio seguente viene illustrato un file IDL contenente la definizione di un'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="f47bb-107">The following example shows an IDL file containing the definition of an interface.</span></span> <span data-ttu-id="f47bb-108">Il corpo della definizione dell'interfaccia, che si verifica tra parentesi graffe, contiene la definizione di una costante (**bufsize**), un tipo (**tipo di \_ handle \_ pContext**) e alcune procedure remote (**RemoteOpen**, **RemoteRead**, **RemoteClose** e **Shutdown**).</span><span class="sxs-lookup"><span data-stu-id="f47bb-108">The body of the interface definition, which occurs between the curly brackets, contains the definition of a constant (**BUFSIZE**), a type (**PCONTEXT\_HANDLE\_TYPE**), and some remote procedures (**RemoteOpen**, **RemoteRead**, **RemoteClose**, and **Shutdown**).</span></span>

``` syntax
[ 
  uuid (ba209999-0c6c-11d2-97cf-00c04f8eea45), 
  version(1.0), 
  pointer_default(unique) 
] 
interface cxhndl 
{ 
 
  const short BUFSIZE = 1024;  
 
  typedef [context_handle] void *PCONTEXT_HANDLE_TYPE; 
 
  short RemoteOpen( 
      [out] PCONTEXT_HANDLE_TYPE *pphContext, 
      [in, string] unsigned char *pszFile 
  ); 
 
   short RemoteRead( 
      [in]  PCONTEXT_HANDLE_TYPE phContext, 
      [out] unsigned char achBuf[BUFSIZE], 
      [out] short *pcbBuf 
  ); 
 
  short RemoteClose( [in, out] PCONTEXT_HANDLE_TYPE *pphContext ); 
 
  void Shutdown(void); 
 
}
```

<span data-ttu-id="f47bb-109">Per ulteriori informazioni, vedere la Guida di [riferimento al linguaggio MIDL](/windows/desktop/Midl/midl-language-reference).</span><span class="sxs-lookup"><span data-stu-id="f47bb-109">For more information see the [MIDL Language Reference](/windows/desktop/Midl/midl-language-reference).</span></span>

 

 