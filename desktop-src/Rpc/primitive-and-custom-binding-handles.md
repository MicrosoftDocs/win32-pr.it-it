---
title: Handle di binding primitivi e personalizzati
description: Tutti gli handle dichiarati con i \_ tipi handle t o \_ binding RPC \_ sono handle di associazione primitivi.
ms.assetid: 7a948aad-02fa-421d-b32c-f5dab071bd04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d496a9a54ba0ee7b9552326f7c4dc15792a72bce
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047245"
---
# <a name="primitive-and-custom-binding-handles"></a><span data-ttu-id="21ee2-103">Handle di binding primitivi e personalizzati</span><span class="sxs-lookup"><span data-stu-id="21ee2-103">Primitive and Custom Binding Handles</span></span>

<span data-ttu-id="21ee2-104">Tutti gli handle dichiarati con i tipi handle [ \_ t](/windows/desktop/Midl/handle-t) o [**\_ binding RPC \_**](rpc-binding-handle.md) sono handle di associazione primitivi.</span><span class="sxs-lookup"><span data-stu-id="21ee2-104">All handles declared with the [handle\_t](/windows/desktop/Midl/handle-t) or [**RPC\_BINDING\_HANDLE**](rpc-binding-handle.md) types are primitive binding handles.</span></span> <span data-ttu-id="21ee2-105">È possibile estendere i tipi handle [ \_ t](/windows/desktop/Midl/handle-t) o [**\_ binding \_ RPC**](rpc-binding-handle.md) per includere informazioni più o diverse rispetto a quelle contenute nel tipo di handle primitivo.</span><span class="sxs-lookup"><span data-stu-id="21ee2-105">You can extend the [handle\_t](/windows/desktop/Midl/handle-t) or [**RPC\_BINDING\_HANDLE**](rpc-binding-handle.md) types to include more or different information than the primitive handle type contains.</span></span> <span data-ttu-id="21ee2-106">Quando si esegue questa operazione, viene creato un handle di binding personalizzato.</span><span class="sxs-lookup"><span data-stu-id="21ee2-106">When you do, you create a custom binding handle.</span></span>

<span data-ttu-id="21ee2-107">Per creare un handle di binding personalizzato per l'applicazione distribuita, è necessario creare un tipo di dati personalizzato e specificare l' \[ attributo [handle](/windows/desktop/Midl/handle) in \] una definizione di tipo nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="21ee2-107">To make a custom binding handle for your distributed application, you will need to create your own data type and specify the \[ [handle](/windows/desktop/Midl/handle)\] attribute on a type definition in your IDL file.</span></span> <span data-ttu-id="21ee2-108">Infine, i file stub mappano gli handle di associazione personalizzati agli handle primitivi.</span><span class="sxs-lookup"><span data-stu-id="21ee2-108">Ultimately, the stub files map custom binding handles to primitive handles.</span></span>

<span data-ttu-id="21ee2-109">Se si crea un tipo di handle di binding personalizzato, è necessario fornire anche le routine BIND e UNBIND che lo stub client usa per eseguire il mapping di un handle personalizzato a un handle primitivo.</span><span class="sxs-lookup"><span data-stu-id="21ee2-109">If you do create your own binding handle type, you must also supply bind and unbind routines that the client stub uses to map a custom handle to a primitive handle.</span></span> <span data-ttu-id="21ee2-110">Lo stub chiama le routine BIND e UNBIND all'inizio e alla fine di ogni chiamata di procedura remota.</span><span class="sxs-lookup"><span data-stu-id="21ee2-110">The stub calls your bind and unbind routines at the beginning and end of each remote procedure call.</span></span> <span data-ttu-id="21ee2-111">Le routine BIND e UNBIND devono essere conformi ai prototipi di funzione seguenti.</span><span class="sxs-lookup"><span data-stu-id="21ee2-111">The bind and unbind routines must conform to the following function prototypes.</span></span>



| <span data-ttu-id="21ee2-112">Prototipo di funzione</span><span class="sxs-lookup"><span data-stu-id="21ee2-112">Function prototype</span></span>                     | <span data-ttu-id="21ee2-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="21ee2-113">Description</span></span>       |
|----------------------------------------|-------------------|
| <span data-ttu-id="21ee2-114">\_binding di tipo handle t \_ (*tipo*)</span><span class="sxs-lookup"><span data-stu-id="21ee2-114">handle\_t type\_bind(*type*)</span></span>           | <span data-ttu-id="21ee2-115">Routine di associazione</span><span class="sxs-lookup"><span data-stu-id="21ee2-115">Binding routine</span></span>   |
| <span data-ttu-id="21ee2-116">void Type \_ UNBIND (*Type*, *handle \_ t*)</span><span class="sxs-lookup"><span data-stu-id="21ee2-116">void type\_unbind(*type*, *handle\_t*)</span></span> | <span data-ttu-id="21ee2-117">Annullamento dell'associazione della routine</span><span class="sxs-lookup"><span data-stu-id="21ee2-117">Unbinding routine</span></span> |



 

<span data-ttu-id="21ee2-118">Nell'esempio seguente viene illustrato come è possibile definire un handle di binding personalizzato nel file IDL:</span><span class="sxs-lookup"><span data-stu-id="21ee2-118">The following example shows how a custom binding handle can be defined in the IDL file:</span></span>

``` syntax
/* usrdef.idl */
[
  uuid(20B309B1-015C-101A-B308-02608C4C9B53),
  version(1.0),
  pointer_default(unique)
]
interface usrdef
{
  typedef struct _DATA_TYPE 
  {
      unsigned char * pszUuid;
      unsigned char * pszProtocolSequence;
      unsigned char * pszNetworkAddress;
      unsigned char * pszEndpoint;
      unsigned char * pszOptions;
  } DATA_TYPE;
 
  typedef [handle] DATA_TYPE * DATA_HANDLE_TYPE;
  void UsrdefProc([in] DATA_HANDLE_TYPE  hBinding,
                  [in, string] unsigned char *   pszString);
 
  void Shutdown([in] DATA_HANDLE_TYPE hBinding);
}
```

<span data-ttu-id="21ee2-119">Se la routine di binding rileva un errore, deve generare un'eccezione usando la funzione [**RpcRaiseException**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcraiseexception) .</span><span class="sxs-lookup"><span data-stu-id="21ee2-119">If the bind routine encounters an error, it should raise an exception using the [**RpcRaiseException**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcraiseexception) function.</span></span> <span data-ttu-id="21ee2-120">Lo stub client eseguirà quindi la pulizia e configurerà il filtro eccezioni per il blocco di eccezioni che circonda la chiamata RPC sul lato client.</span><span class="sxs-lookup"><span data-stu-id="21ee2-120">The client stub will then clean up, and let the exception filter through to the exception block surrounding the remote procedure call on the client side.</span></span> <span data-ttu-id="21ee2-121">Se la routine BIND restituisce semplicemente **null**, il codice client ottiene l'errore di \_ binding RPC S \_ non valido \_ .</span><span class="sxs-lookup"><span data-stu-id="21ee2-121">If the bind routine simply returns **NULL**, the client code gets error RPC\_S\_INVALID\_BINDING.</span></span> <span data-ttu-id="21ee2-122">Sebbene questo potrebbe essere accettabile in determinate situazioni, altre situazioni, ad esempio memoria insufficiente, non rispondono correttamente.</span><span class="sxs-lookup"><span data-stu-id="21ee2-122">While this might be acceptable in certain situations, other situations (such as being out of memory) do not respond well.</span></span> <span data-ttu-id="21ee2-123">La routine UNBIND deve essere progettata in modo da non avere esito negativo.</span><span class="sxs-lookup"><span data-stu-id="21ee2-123">The unbind routine should be designed so that it does not fail.</span></span> <span data-ttu-id="21ee2-124">La routine UNBIND non deve generare eccezioni.</span><span class="sxs-lookup"><span data-stu-id="21ee2-124">The unbind routine should not raise exceptions.</span></span>

<span data-ttu-id="21ee2-125">Nell'applicazione client vengono visualizzate le routine BIND e UNBIND definite dal programmatore.</span><span class="sxs-lookup"><span data-stu-id="21ee2-125">The programmer-defined bind and unbind routines appear in the client application.</span></span> <span data-ttu-id="21ee2-126">Nell'esempio seguente, la routine BIND chiama [**errore in RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) per convertire le informazioni di associazione di stringa in un handle di associazione.</span><span class="sxs-lookup"><span data-stu-id="21ee2-126">In the following example, the bind routine calls [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) to convert the string-binding information to a binding handle.</span></span> <span data-ttu-id="21ee2-127">La routine UNBIND chiama [**RpcBindingFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) per liberare l'handle di associazione.</span><span class="sxs-lookup"><span data-stu-id="21ee2-127">The unbind routine calls [**RpcBindingFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) to free the binding handle.</span></span>

<span data-ttu-id="21ee2-128">Il nome dell'handle di binding definito dal programmatore, il \_ tipo di handle di dati \_ , viene visualizzato come parte del nome delle funzioni.</span><span class="sxs-lookup"><span data-stu-id="21ee2-128">The name of the programmer-defined binding handle, DATA\_HANDLE\_TYPE, appears as part of the name of the functions.</span></span> <span data-ttu-id="21ee2-129">Viene anche usato come tipo di parametro nei parametri della funzione.</span><span class="sxs-lookup"><span data-stu-id="21ee2-129">It is also used as the parameter type in the function parameters.</span></span>

``` syntax
/* The client stub calls this _bind routine at the */
/* beginning of each remote procedure call                */
 
RPC_BINDING_HANDLE __RPC_USER DATA_HANDLE_TYPE_bind(
    DATA_HANDLE_TYPE dh1)
{
    RPC_BINDING_HANDLE hBinding;
    RPC_STATUS status;
 
    unsigned char *pszStringBinding;
 
    status = RpcStringBindingCompose(
          dh1.pszUuid,
          dh1.pszProtocolSequence,
          dh1.pszNetworkAddress,
          dh1.pszEndpoint,
          dh1.pszOptions,
          &pszStringBinding);
          ...
 
    status = RpcBindingFromStringBinding(
          pszStringBinding,
          &hBinding);
          ...
 
    status = RpcStringFree(&pszStringBinding); 
    ...
 
    return(hBinding);
}
 
/* The client stub calls this _unbind routine */
/* after each remote procedure call.                            */
void __RPC_USER DATA_HANDLE_TYPE_unbind(
    DATA_HANDLE_TYPE dh1, 
    RPC_BINDING_HANDLE h1)
{
    RPC_STATUS status;
    status = RpcBindingFree(&h1); 
    ...
}
```

<span data-ttu-id="21ee2-130">Gli handle di associazione impliciti ed espliciti possono essere di tipo primitivo o personalizzato.</span><span class="sxs-lookup"><span data-stu-id="21ee2-130">Both implicit and explicit binding handles can either be primitive or custom handles.</span></span> <span data-ttu-id="21ee2-131">Ovvero, un handle può essere:</span><span class="sxs-lookup"><span data-stu-id="21ee2-131">That is, a handle may be:</span></span>

-   <span data-ttu-id="21ee2-132">Primitive e implicite</span><span class="sxs-lookup"><span data-stu-id="21ee2-132">Primitive and implicit</span></span>
-   <span data-ttu-id="21ee2-133">Personalizzata e implicita</span><span class="sxs-lookup"><span data-stu-id="21ee2-133">Custom and implicit</span></span>
-   <span data-ttu-id="21ee2-134">Primitive ed esplicite</span><span class="sxs-lookup"><span data-stu-id="21ee2-134">Primitive and explicit</span></span>
-   <span data-ttu-id="21ee2-135">Personalizzata ed esplicita</span><span class="sxs-lookup"><span data-stu-id="21ee2-135">Custom and explicit</span></span>

 

 