---
title: Uso dei servizi di serializzazione
description: MIDL genera uno stub di serializzazione per la procedura con gli attributi \ Encode \ e \ Decode \.
ms.assetid: b1fce133-32e3-4b5e-9f9d-ffbe60e9d9cd
keywords:
- RPC (Remote Procedure Call), attività, uso dei servizi di serializzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 317156a2da954e001b687cca12eb0c6df23ef4ee
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047316"
---
# <a name="using-serialization-services"></a><span data-ttu-id="6af47-104">Uso dei servizi di serializzazione</span><span class="sxs-lookup"><span data-stu-id="6af47-104">Using Serialization Services</span></span>

<span data-ttu-id="6af47-105">MIDL genera uno stub di serializzazione per la procedura con gli attributi \[ [**Encode**](/windows/desktop/Midl/encode) \] e \[ [**Decode**](/windows/desktop/Midl/decode) \] .</span><span class="sxs-lookup"><span data-stu-id="6af47-105">MIDL generates a serialization stub for the procedure with the attributes \[[**encode**](/windows/desktop/Midl/encode)\] and \[[**decode**](/windows/desktop/Midl/decode)\].</span></span> <span data-ttu-id="6af47-106">Quando si chiama questa routine, si esegue una chiamata di serializzazione anziché una chiamata remota.</span><span class="sxs-lookup"><span data-stu-id="6af47-106">When you call this routine, you execute a serialization call instead of a remote call.</span></span> <span data-ttu-id="6af47-107">Viene eseguito il marshalling o l'unmarshalling degli argomenti della routine da un buffer nel modo consueto.</span><span class="sxs-lookup"><span data-stu-id="6af47-107">The procedure arguments are marshaled to or unmarshaled from a buffer in the usual way.</span></span> <span data-ttu-id="6af47-108">Si avrà quindi il controllo completo dei buffer.</span><span class="sxs-lookup"><span data-stu-id="6af47-108">You then have complete control of the buffers.</span></span>

<span data-ttu-id="6af47-109">Al contrario, quando il programma esegue la serializzazione del tipo (un tipo è contrassegnato con attributi di serializzazione), MIDL genera routine per ridimensionare, codificare e decodificare oggetti di quel tipo.</span><span class="sxs-lookup"><span data-stu-id="6af47-109">In contrast, when your program performs type serialization (a type is labeled with serialization attributes), MIDL generates routines to size, encode, and decode objects of that type.</span></span> <span data-ttu-id="6af47-110">Per serializzare i dati, è necessario chiamare queste routine nel modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="6af47-110">To serialize data, you must call these routines in the appropriate way.</span></span> <span data-ttu-id="6af47-111">La serializzazione del tipo è un'estensione Microsoft e, di conseguenza, non è disponibile quando si esegue la compilazione in modalità di compatibilità DCE ([**/OSF**](/windows/desktop/Midl/-osf)).</span><span class="sxs-lookup"><span data-stu-id="6af47-111">Type serialization is a Microsoft extension and, as such, is not available when you compile in DCE-compatibility ([**/osf**](/windows/desktop/Midl/-osf)) mode.</span></span> <span data-ttu-id="6af47-112">Utilizzando gli attributi \[ [**Encode**](/windows/desktop/Midl/encode) \] e \[ [**Decode**](/windows/desktop/Midl/decode) \] come attributi di interfaccia, RPC applica la codifica a tutti i tipi e routine definiti nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="6af47-112">By using the \[[**encode**](/windows/desktop/Midl/encode)\] and \[[**decode**](/windows/desktop/Midl/decode)\] attributes as interface attributes, RPC applies encoding to all the types and routines defined in the IDL file.</span></span>

<span data-ttu-id="6af47-113">È necessario fornire buffer allineati in modo adeguato quando si utilizzano i servizi di serializzazione.</span><span class="sxs-lookup"><span data-stu-id="6af47-113">You must supply adequately aligned buffers when using serialization services.</span></span> <span data-ttu-id="6af47-114">L'inizio del buffer deve essere allineato a un indirizzo che è un multiplo di 8 o a 8 byte allineato.</span><span class="sxs-lookup"><span data-stu-id="6af47-114">The beginning of the buffer must be aligned at an address that is a multiple of 8, or 8-byte aligned.</span></span> <span data-ttu-id="6af47-115">Per la serializzazione delle procedure, ogni chiamata di routine deve effettuare il marshalling o l'unmarshalling da una posizione del buffer a 8 byte allineata.</span><span class="sxs-lookup"><span data-stu-id="6af47-115">For procedure serialization, each procedure call must marshal into or unmarshal from a buffer position that is 8-byte aligned.</span></span> <span data-ttu-id="6af47-116">Per la serializzazione dei tipi, il ridimensionamento, la codifica e la decodifica devono iniziare a una posizione allineata a 8 byte.</span><span class="sxs-lookup"><span data-stu-id="6af47-116">For type serialization, sizing, encoding, and decoding must start at a position that is 8-byte aligned.</span></span>

<span data-ttu-id="6af47-117">Un modo per garantire che i buffer siano allineati per l'applicazione consiste nel scrivere la funzione di [**\_ \_ allocazione utente MIDL**](/windows/desktop/Midl/midl-user-allocate-1) in modo da creare buffer allineati.</span><span class="sxs-lookup"><span data-stu-id="6af47-117">One way for your application to ensure that its buffers are aligned is to write the [**midl\_user\_allocate**](/windows/desktop/Midl/midl-user-allocate-1) function such that it creates aligned buffers.</span></span> <span data-ttu-id="6af47-118">Nell'esempio di codice riportato di seguito viene illustrato come eseguire questa operazione.</span><span class="sxs-lookup"><span data-stu-id="6af47-118">The following code sample demonstrates how this can be done.</span></span>


```C++
#include <windows.h>

#define ALIGN_TO8(p)   (char *)((unsigned long)((char *)p + 7) & ~7)

void __RPC_FAR *__RPC_USER  MIDL_user_allocate(size_t sizeInBytes)
{
    unsigned char *pcAllocated;
    unsigned char *pcUserPtr;

    pcAllocated = (unsigned char *) malloc( sizeInBytes + 15 );
    pcUserPtr =  ALIGN_TO8( pcAllocated );
    if ( pcUserPtr == pcAllocated )
        pcUserPtr = pcAllocated + 8;

    *(pcUserPtr - 1) = pcUserPtr - pcAllocated;

    return( pcUserPtr );
}
```



<span data-ttu-id="6af47-119">Nell'esempio seguente viene illustrata la funzione di [**MIDL \_ User \_ Free**](/windows/desktop/Midl/midl-user-free-1) corrispondente.</span><span class="sxs-lookup"><span data-stu-id="6af47-119">The following example shows the corresponding [**midl\_user\_free**](/windows/desktop/Midl/midl-user-free-1) function.</span></span>


```C++
void __RPC_USER  MIDL_user_free(void __RPC_FAR *f)
{
    unsigned char * pcAllocated;
    unsigned char * pcUserPtr;

    pcUserPtr = (unsigned char *) f;
    pcAllocated = pcUserPtr - *(pcUserPtr - 1);

    free( pcAllocated );
}
```



 

 