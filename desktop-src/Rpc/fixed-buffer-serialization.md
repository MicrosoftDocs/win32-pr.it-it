---
title: Serializzazione del buffer fisso
description: Correzione della serializzazione del buffer.
ms.assetid: 3432f468-89f2-48e2-8d86-15ba549f0fc7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ce58d3bdf92673c97ae8dc9fbbf8f366cb4a59a9e3ce114431de1581af30ec2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021211"
---
# <a name="fixed-buffer-serialization"></a>Serializzazione del buffer fisso

Quando si usa lo stile di buffer fisso, specificare un buffer sufficientemente grande da contenere le operazioni di codifica (marshalling) eseguite con l'handle. Quando si esegue l'unmarshaling, si fornisce il buffer che contiene tutti i dati da decodificare.

Lo stile di buffer fisso della serializzazione usa le routine seguenti:

-   [**MesEncodeFixedBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodefixedbufferhandlecreate)
-   [**MesDecodeBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate)
-   [**MesBufferHandleReset**](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset)
-   [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree)

La **funzione MesEncodeFixedBufferHandleCreate** alloca la memoria necessaria per l'handle di codifica e quindi lo inizializza. L'applicazione può chiamare [**MesBufferHandleReset**](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset) per reinizializzare l'handle oppure può chiamare [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree) per liberare la memoria dell'handle. Per creare un handle di decodifica corrispondente all'handle di codifica dello stile fisso, è necessario usare [**MesDecodeBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate).

L'applicazione chiama [**MesHandleFree per**](/windows/desktop/api/Midles/nf-midles-meshandlefree) liberare l'handle del buffer di codifica o decodifica.

## <a name="examples-of-fixed-buffer-encoding"></a>Esempi di codifica del buffer fisso

Nella sezione seguente viene fornito un esempio di come usare un handle di serializzazione dello stile del buffer fisso per la codifica della procedura.

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

L'estratto seguente rappresenta una parte di un'applicazione.

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

Nella sezione seguente viene fornito un esempio di come usare un handle di serializzazione dello stile del buffer fisso per la codifica dei tipi.

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

L'estratto seguente rappresenta i frammenti dell'applicazione pertinenti.


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



 

 




