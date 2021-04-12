---
title: Serializzazione del buffer fissa
description: Serializzazione del buffer fissa.
ms.assetid: 3432f468-89f2-48e2-8d86-15ba549f0fc7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c87e3cad0a272ccd493cf9088fedeb272f1206b8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396139"
---
# <a name="fixed-buffer-serialization"></a><span data-ttu-id="baefe-103">Serializzazione del buffer fissa</span><span class="sxs-lookup"><span data-stu-id="baefe-103">Fixed Buffer Serialization</span></span>

<span data-ttu-id="baefe-104">Quando si utilizza lo stile di buffer fisso, specificare un buffer sufficientemente grande per supportare le operazioni di codifica (marshalling) eseguite con l'handle.</span><span class="sxs-lookup"><span data-stu-id="baefe-104">When using the fixed buffer style, specify a buffer that is large enough to accommodate the encoding (marshalling) operations performed with the handle.</span></span> <span data-ttu-id="baefe-105">Quando si esegue l'unmarshalling, si fornisce il buffer che contiene tutti i dati da decodificare.</span><span class="sxs-lookup"><span data-stu-id="baefe-105">When unmarshaling, you provide the buffer that contains all of the data to decode.</span></span>

<span data-ttu-id="baefe-106">Lo stile di buffer fisso della serializzazione usa le routine seguenti:</span><span class="sxs-lookup"><span data-stu-id="baefe-106">The fixed buffer style of serialization uses the following routines:</span></span>

-   [<span data-ttu-id="baefe-107">**MesEncodeFixedBufferHandleCreate**</span><span class="sxs-lookup"><span data-stu-id="baefe-107">**MesEncodeFixedBufferHandleCreate**</span></span>](/windows/desktop/api/Midles/nf-midles-mesencodefixedbufferhandlecreate)
-   [<span data-ttu-id="baefe-108">**MesDecodeBufferHandleCreate**</span><span class="sxs-lookup"><span data-stu-id="baefe-108">**MesDecodeBufferHandleCreate**</span></span>](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate)
-   [<span data-ttu-id="baefe-109">**MesBufferHandleReset**</span><span class="sxs-lookup"><span data-stu-id="baefe-109">**MesBufferHandleReset**</span></span>](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset)
-   [<span data-ttu-id="baefe-110">**MesHandleFree**</span><span class="sxs-lookup"><span data-stu-id="baefe-110">**MesHandleFree**</span></span>](/windows/desktop/api/Midles/nf-midles-meshandlefree)

<span data-ttu-id="baefe-111">La funzione **MesEncodeFixedBufferHandleCreate** alloca la memoria necessaria per l'handle di codifica, quindi la Inizializza.</span><span class="sxs-lookup"><span data-stu-id="baefe-111">The **MesEncodeFixedBufferHandleCreate** function allocates the memory needed for the encoding handle, and then initializes it.</span></span> <span data-ttu-id="baefe-112">L'applicazione può chiamare [**MesBufferHandleReset**](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset) per reinizializzare l'handle oppure può chiamare [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree) per liberare la memoria dell'handle.</span><span class="sxs-lookup"><span data-stu-id="baefe-112">The application can call [**MesBufferHandleReset**](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset) to reinitialize the handle, or it can call [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree) to free the handle's memory.</span></span> <span data-ttu-id="baefe-113">Per creare un handle di decodifica corrispondente all'handle di codifica a stile fisso, è necessario usare [**MesDecodeBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate).</span><span class="sxs-lookup"><span data-stu-id="baefe-113">To create a decoding handle corresponding to the fixed style–encoding handle, you must use [**MesDecodeBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate).</span></span>

<span data-ttu-id="baefe-114">L'applicazione chiama [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree) per liberare la codifica o la decodifica dell'handle del buffer.</span><span class="sxs-lookup"><span data-stu-id="baefe-114">The application calls [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree) to free the encoding or decoding buffer handle.</span></span>

## <a name="examples-of-fixed-buffer-encoding"></a><span data-ttu-id="baefe-115">Esempi di codifica del buffer fisso</span><span class="sxs-lookup"><span data-stu-id="baefe-115">Examples of Fixed Buffer Encoding</span></span>

<span data-ttu-id="baefe-116">Nella sezione seguente viene fornito un esempio di utilizzo di uno stile di buffer fisso, ovvero la serializzazione dell'handle per la codifica delle procedure.</span><span class="sxs-lookup"><span data-stu-id="baefe-116">The following section provides an example of how to use a fixed buffer style–serializing handle for procedure encoding.</span></span>

``` syntax
/*This is a fragment of the IDL file defining MooProc */

...
void __RPC_USER
MyProc( [in] handle_t Handle, [in,out] MyType * pMyObject,
        [in, out] ThisType * pThisObject);
...

/*This is an ACF file. MyProc is defined in the IDL file */

[
    explicit_handle
]
interface regress
{
    [ encode,decode ] MyProc();
}
```

<span data-ttu-id="baefe-117">Nell'estratto seguente viene rappresentata una parte di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="baefe-117">The following excerpt represents a part of an application.</span></span>

``` syntax
if (MesEncodeFixedBufferHandleCreate (
        Buffer, BufferSize, 
        pEncodedSize, &Handle) == RPC_S_OK)
{
    ...
    /* Manufacture a MyObject and a ThisObject */
    ...
    /* The serialization works from the beginning of the buffer because 
   the handle is in the initial state. The function MyProc does the    
   following when called with an encoding handle:
     - sizes all the parameters for marshalling,
     - marshalls into the buffer (and sets the internal state 
    appropriately) 
    */

    MyProc ( Handle, pMyObject, pThisObject );
    ...
    MesHandleFree ();
}
if (MesDecodeBufferHandleCreate (Buffer, BufferSize, &Handle) ==
    RPC_S_OK)
{

    /* The MooProc does the following for you when called with a decoding 
    handle:
     - unmarshalls the objects from the buffer into *pMooObject and 
       *pBarObject
*/

MyProc ( Handle, pMyObject, pThisObject);
...
MesHandleFree ( Handle );
}
```

<span data-ttu-id="baefe-118">Nella sezione seguente viene fornito un esempio di utilizzo di uno stile di buffer fisso, ovvero un handle di serializzazione per la codifica dei tipi.</span><span class="sxs-lookup"><span data-stu-id="baefe-118">The following section provides an example of how to use a fixed buffer style–serializing handle for type encoding.</span></span>

``` syntax
/* This is an ACF file. MyType is defined in the IDL file */

[    
    explicit_handle
]
interface regress
{
    typedef [ encode,decode ] MyType;
}
```

<span data-ttu-id="baefe-119">L'estratto seguente rappresenta i frammenti dell'applicazione pertinenti.</span><span class="sxs-lookup"><span data-stu-id="baefe-119">The following excerpt represents the relevant application fragments.</span></span>


```C++
if (MesEncodeFixedBufferHandleCreate (Buffer, BufferSize, 
    pEncodedSize, &Handle) == RPC_S_OK)
{
    //...
    /* Manufacture a MyObject and a pMyObject */
    //...
    MyType_Encode ( Handle, pMyObject );
    //...
    MesHandleFree ();
}
if (MesDecodeBufferHandleCreate (Buffer, BufferSize, &Handle) ==
    RPC_S_OK )
{
    MooType_Decode (Handle, pMooObject);
    //...
    MesHandleFree ( Handle );
}
```



 

 




