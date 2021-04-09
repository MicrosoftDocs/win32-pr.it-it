---
title: Funzione midl_user_allocate
description: La \_ funzione di \_ allocazione utente MIDL è una procedura che deve essere fornita dagli sviluppatori di applicazioni RPC.
ms.assetid: 3def405c-da05-4cce-9dc4-499864a0de6e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12b2e3196de79992f5856b7117b25f05ad782d26
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118115"
---
# <a name="the-midl_user_allocate-function"></a><span data-ttu-id="5c194-103">Funzione di \_ \_ allocazione utente MIDL</span><span class="sxs-lookup"><span data-stu-id="5c194-103">The midl\_user\_allocate Function</span></span>

<span data-ttu-id="5c194-104">La funzione di **\_ \_ allocazione utente MIDL** è una procedura che deve essere fornita dagli sviluppatori di applicazioni RPC.</span><span class="sxs-lookup"><span data-stu-id="5c194-104">The **midl\_user\_allocate** function is a procedure that must be supplied by developers of RPC applications.</span></span> <span data-ttu-id="5c194-105">Alloca la memoria per gli stub RPC e le routine della libreria.</span><span class="sxs-lookup"><span data-stu-id="5c194-105">It allocates memory for the RPC stubs and library routines.</span></span> <span data-ttu-id="5c194-106">La funzione di **\_ \_ allocazione utente MIDL** deve corrispondere al prototipo seguente:</span><span class="sxs-lookup"><span data-stu-id="5c194-106">Your **midl\_user\_allocate** function must match the following prototype:</span></span>

``` syntax
void __RPC_FAR * __RPC_USER midl_user_allocate (size_t cBytes);
```

<span data-ttu-id="5c194-107">Il parametro *cBytes* specifica il numero di byte da allocare.</span><span class="sxs-lookup"><span data-stu-id="5c194-107">The *cBytes* parameter specifies the number of bytes to allocate.</span></span> <span data-ttu-id="5c194-108">Sia le applicazioni client che le applicazioni server devono implementare la funzione di **\_ \_ allocazione utente MIDL** a meno che non si stia eseguendo la compilazione in modalità OSF-Compatibility (/OSF).</span><span class="sxs-lookup"><span data-stu-id="5c194-108">Both client applications and server applications must implement the **midl\_user\_allocate** function unless you are compiling in OSF-compatibility (/osf) mode.</span></span> <span data-ttu-id="5c194-109">Le applicazioni e gli stub generati chiamano l' **\_ utente MIDL \_ allocare** direttamente o indirettamente per gestire gli oggetti allocati.</span><span class="sxs-lookup"><span data-stu-id="5c194-109">Applications and generated stubs call **midl\_user\_allocate** directly or indirectly to manage allocated objects.</span></span> <span data-ttu-id="5c194-110">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="5c194-110">For example:</span></span>

-   <span data-ttu-id="5c194-111">Le applicazioni client e server chiamano **MIDL \_ User \_ allocate** per allocare memoria per l'applicazione, ad esempio quando si crea un nuovo nodo in un albero o un elenco collegato.</span><span class="sxs-lookup"><span data-stu-id="5c194-111">The client and server applications call **midl\_user\_allocate** to allocate memory for the application, such as when creating a new node in a tree or linked list.</span></span>
-   <span data-ttu-id="5c194-112">Lo stub del server chiama l' **\_ utente MIDL \_ allocate** quando si esegue l'unmarshalling dei dati nello spazio degli indirizzi del server.</span><span class="sxs-lookup"><span data-stu-id="5c194-112">The server stub calls **midl\_user\_allocate** when unmarshaling data into the server address space.</span></span>
-   <span data-ttu-id="5c194-113">Lo stub client chiama **l' \_ utente MIDL \_ allocate** quando si esegue l'unmarshalling dei dati dal server a cui fa riferimento un \[ \] puntatore out.</span><span class="sxs-lookup"><span data-stu-id="5c194-113">The client stub calls **midl\_user\_allocate** when unmarshaling data from the server that is referenced by an \[out\] pointer.</span></span> <span data-ttu-id="5c194-114">Si noti che per i \[ \] \[ \] \[ puntatori univoci in, out e Unique \] , lo stub client chiama l' **\_ utente MIDL \_ allocare** solo se il \[ valore del \] puntatore univoco è null per l'input e viene modificato in un valore non null durante la chiamata.</span><span class="sxs-lookup"><span data-stu-id="5c194-114">Note that for \[in\], \[out\], and \[unique\] pointers, the client stub calls **midl\_user\_allocate** only if the \[unique\] pointer value was null on input and changes to a non-null value during the call.</span></span> <span data-ttu-id="5c194-115">Se \[ per l' \] input il puntatore univoco è diverso da null, lo stub client scrive i dati associati nella memoria esistente.</span><span class="sxs-lookup"><span data-stu-id="5c194-115">If the \[unique\] pointer was non-null on input, the client stub writes the associated data into existing memory.</span></span>

<span data-ttu-id="5c194-116">Se **\_ \_ allocare l'utente MIDL** non riesce ad allocare memoria, deve restituire un puntatore null.</span><span class="sxs-lookup"><span data-stu-id="5c194-116">If **midl\_user\_allocate** fails to allocate memory, it should return a null pointer.</span></span>

<span data-ttu-id="5c194-117">La funzione di **\_ \_ allocazione utente MIDL** deve restituire un puntatore allineato a 8 byte.</span><span class="sxs-lookup"><span data-stu-id="5c194-117">The **midl\_user\_allocate** function should return an 8-byte aligned pointer.</span></span>

<span data-ttu-id="5c194-118">Ad esempio, i programmi di esempio forniti con Platform Software Development Kit (SDK) implementano l' **\_ utente MIDL \_ allocato** in termini della funzione C [**malloc**](pointers-and-memory-allocation.md):</span><span class="sxs-lookup"><span data-stu-id="5c194-118">For example, the sample programs provided with the Platform Software Development Kit (SDK) implement **midl\_user\_allocate** in terms of the C function [**malloc**](pointers-and-memory-allocation.md):</span></span>


```C++
void __RPC_FAR * __RPC_USER midl_user_allocate(size_t cBytes)
{
    return((void __RPC_FAR *) malloc(cBytes));
}
```



> [!Note]  
> <span data-ttu-id="5c194-119">Se il pacchetto RpcSs è abilitato (ad esempio, come risultato dell'utilizzo dell'attributo \[ [**enable \_ allocate**](/windows/desktop/Midl/enable-allocate) \] ), utilizzare [**RpcSmAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmallocate) per allocare memoria sul lato server.</span><span class="sxs-lookup"><span data-stu-id="5c194-119">If the RpcSs package is enabled (for example, as the result of using the \[ [**enable\_allocate**](/windows/desktop/Midl/enable-allocate)\] attribute), use [**RpcSmAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmallocate) to allocate memory on the server side.</span></span> <span data-ttu-id="5c194-120">Per altre informazioni su \[ **enable \_ allocate** \] , vedere [riferimento a MIDL](/windows/desktop/Midl/midl-language-reference).</span><span class="sxs-lookup"><span data-stu-id="5c194-120">For additional information on \[**enable\_allocate**\], see [MIDL Reference](/windows/desktop/Midl/midl-language-reference).</span></span>

 

 

 