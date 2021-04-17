---
title: Funzione midl_user_free
description: La \_ funzione User \_ Free MIDL deve essere fornita dagli sviluppatori RPC.
ms.assetid: 5e940e93-bdd4-48cc-b84e-654637699719
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4713ed05173b709780b6496f233051fa3adddff8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399635"
---
# <a name="the-midl_user_free-function"></a><span data-ttu-id="0f842-103">\_Funzione gratuita dell'utente MIDL \_</span><span class="sxs-lookup"><span data-stu-id="0f842-103">The midl\_user\_free Function</span></span>

<span data-ttu-id="0f842-104">La **funzione \_ User \_ Free MIDL** deve essere fornita dagli sviluppatori RPC.</span><span class="sxs-lookup"><span data-stu-id="0f842-104">The **midl\_user\_free** function must be supplied by RPC developers.</span></span> <span data-ttu-id="0f842-105">Alloca la memoria per gli stub RPC e le routine della libreria.</span><span class="sxs-lookup"><span data-stu-id="0f842-105">It allocates memory for the RPC stubs and library routines.</span></span> <span data-ttu-id="0f842-106">La funzione della versione **\_ \_ gratuita dell'utente MIDL** deve corrispondere al prototipo seguente:</span><span class="sxs-lookup"><span data-stu-id="0f842-106">Your **midl\_user\_free** function must match the following prototype:</span></span>

``` syntax
void __RPC_USER midl_user_free(void * pBuffer);
```

<span data-ttu-id="0f842-107">Il parametro *pbuffer* specifica un puntatore alla memoria che deve essere liberata.</span><span class="sxs-lookup"><span data-stu-id="0f842-107">The *pBuffer* parameter specifies a pointer to the memory that is to be freed.</span></span> <span data-ttu-id="0f842-108">Sia l'applicazione client che l'applicazione server devono implementare la funzione di utilizzo **\_ \_ gratuito di MIDL** , a meno che non si stia eseguendo la compilazione in modalità OSF-Compatibility ([**/OSF**](/windows/desktop/Midl/-osf)).</span><span class="sxs-lookup"><span data-stu-id="0f842-108">Both client application and server application must implement the **midl\_user\_free** function unless you are compiling in OSF-compatibility ([**/osf**](/windows/desktop/Midl/-osf)) mode.</span></span> <span data-ttu-id="0f842-109">La **funzione \_ User \_ Free MIDL** deve essere in grado di liberare tutte le archiviazioni allocate dall' [**\_ utente MIDL \_ allocate**](the-midl-user-allocate-function.md).</span><span class="sxs-lookup"><span data-stu-id="0f842-109">The **midl\_user\_free** function must be able to free all storage allocated by [**midl\_user\_allocate**](the-midl-user-allocate-function.md).</span></span>

<span data-ttu-id="0f842-110">Le applicazioni e gli stub chiamano l' **\_ utente MIDL \_ gratis** quando si gestiscono gli oggetti allocati:</span><span class="sxs-lookup"><span data-stu-id="0f842-110">Applications and stubs call **midl\_user\_free** when dealing with allocated objects:</span></span>

-   <span data-ttu-id="0f842-111">L'applicazione server deve chiamare **l' \_ utente \_ MIDL** per liberare la memoria allocata dall'applicazione, ad esempio quando si elimina un nodo di dati allocato in modo dinamico.</span><span class="sxs-lookup"><span data-stu-id="0f842-111">The server application should call **midl\_user\_free** to free memory allocated by the application, such as when deleting a dynamically allocated node of data.</span></span>
-   <span data-ttu-id="0f842-112">Lo stub del server chiama l' **\_ utente MIDL \_ gratuitamente** a rilasciare la memoria nel server dopo aver eseguito il marshalling di tutti gli \[ \] argomenti out, \[ in \] , \[ out \] arguments e il valore restituito della funzione.</span><span class="sxs-lookup"><span data-stu-id="0f842-112">The server stub calls **midl\_user\_free** to release memory on the server after marshaling all \[out\] arguments, \[in\],\[out\] arguments, and the function return value.</span></span>

<span data-ttu-id="0f842-113">Ad esempio, il programma RPC Windows Sample che Visualizza "Hello, World" implementa l' **\_ utente MIDL \_ gratuitamente** in termini di funzione C gratuita:</span><span class="sxs-lookup"><span data-stu-id="0f842-113">For example, the RPC Windows sample program that displays "Hello, world" implements **midl\_user\_free** in terms of the C function free:</span></span>


```C++
void __RPC_USER midl_user_free(void __RPC_FAR * p)
{
    free(p);
}
```



> [!Note]  
> <span data-ttu-id="0f842-114">Se il pacchetto RpcSs è abilitato, ad esempio in seguito all'utilizzo dell' \[ attributo [**enable \_ allocate**](/windows/desktop/Midl/enable-allocate) \] , il programma server deve utilizzare [**RpcSmFree**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmfree) per liberare memoria.</span><span class="sxs-lookup"><span data-stu-id="0f842-114">If the RpcSs package is enabled (for example, as the result of using the \[ [**enable\_allocate**](/windows/desktop/Midl/enable-allocate)\] attribute), your server program should use [**RpcSmFree**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmfree) to free memory.</span></span> <span data-ttu-id="0f842-115">Per ulteriori informazioni, vedere il [pacchetto di gestione della memoria RPCSS](rpcss-memory-management-package.md).</span><span class="sxs-lookup"><span data-stu-id="0f842-115">For more information, see [RpcSs Memory Management Package](rpcss-memory-management-package.md).</span></span>

 

 

 