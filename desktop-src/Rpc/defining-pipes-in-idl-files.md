---
title: Definizione di pipe nei file IDL
description: Quando si definisce una pipe in un file IDL, il compilatore MIDL genera una struttura di controllo pipe i cui membri sono puntatori alle procedure push, pull e Alloc, oltre a una variabile di stato che coordina queste procedure.
ms.assetid: f6c282e4-3056-48c4-bd12-dfcae6d238d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 115be7fc5d00458d13df102afebe9ba5b55de070
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399394"
---
# <a name="defining-pipes-in-idl-files"></a><span data-ttu-id="a686e-103">Definizione di pipe nei file IDL</span><span class="sxs-lookup"><span data-stu-id="a686e-103">Defining Pipes in IDL Files</span></span>

<span data-ttu-id="a686e-104">Quando si definisce una pipe in un file IDL, il compilatore MIDL genera una struttura di controllo pipe i cui membri sono puntatori alle procedure push, pull e Alloc, oltre a una variabile di stato che coordina queste procedure.</span><span class="sxs-lookup"><span data-stu-id="a686e-104">When a pipe is defined in an IDL file, the MIDL compiler generates a pipe control structure whose members are pointers to push, pull, and alloc procedures as well as a state variable that coordinates these procedures.</span></span> <span data-ttu-id="a686e-105">L'applicazione client Inizializza i campi nella struttura del controllo pipe, gestisce la variabile di stato e gestisce il trasferimento dei dati con le proprie funzioni push, pull e allocazione.</span><span class="sxs-lookup"><span data-stu-id="a686e-105">The client application initializes the fields in the pipe control structure, maintains its state variable, and manages the data transfer with its own push, pull, and alloc functions.</span></span> <span data-ttu-id="a686e-106">Il codice stub client chiama queste funzioni dell'applicazione nei cicli durante il trasferimento dei dati.</span><span class="sxs-lookup"><span data-stu-id="a686e-106">The client stub code calls these application functions in loops during data transfer.</span></span> <span data-ttu-id="a686e-107">Per una pipe di input, lo stub client esegue il marshalling dei dati di trasferimento e li trasmette allo stub del server.</span><span class="sxs-lookup"><span data-stu-id="a686e-107">For an input pipe, the client stub marshals the transfer data and transmits it to the server stub.</span></span> <span data-ttu-id="a686e-108">Per una pipe di output, lo stub client esegue l'unmarshalling dei dati in un buffer e passa un puntatore a tale buffer all'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="a686e-108">For an output pipe, the client stub unmarshals the data into a buffer and passes a pointer to that buffer back to the client application.</span></span>

<span data-ttu-id="a686e-109">Il codice stub del server Inizializza i campi della struttura del controllo pipe su una variabile di stato, nonché i puntatori alle routine push e pull.</span><span class="sxs-lookup"><span data-stu-id="a686e-109">The server stub code initializes the fields of the pipe control structure to a state variable, as well as pointers to push and pull routines.</span></span> <span data-ttu-id="a686e-110">Lo stub del server gestisce lo stato e gestisce la propria archiviazione privata per i dati di trasferimento.</span><span class="sxs-lookup"><span data-stu-id="a686e-110">The server stub maintains the state and manages its private storage for the transfer data.</span></span> <span data-ttu-id="a686e-111">L'applicazione server chiama le routine pull e push nei cicli durante la chiamata di procedura remota mentre riceve ed esegue l'unmarshalling dei dati dallo stub client oppure effettua il marshalling e trasmette i dati allo stub client.</span><span class="sxs-lookup"><span data-stu-id="a686e-111">The server application calls the pull and push routines in loops during the remote procedure call as it receives and unmarshals data from the client stub, or marshals and transmits data to the client stub.</span></span>

<span data-ttu-id="a686e-112">Il file IDL di esempio seguente definisce una pipe di tipo LONG \_ pipe, le cui dimensioni degli elementi sono definite come **Long**.</span><span class="sxs-lookup"><span data-stu-id="a686e-112">The following example IDL file defines a pipe type LONG\_PIPE, whose element size is defined as **long**.</span></span> <span data-ttu-id="a686e-113">Dichiara inoltre i prototipi di funzione per le chiamate di procedura remota inpipe e outpipe, per inviare e ricevere dati, rispettivamente.</span><span class="sxs-lookup"><span data-stu-id="a686e-113">It also declares function prototypes for the remote procedure calls InPipe and OutPipe, to send and receive data, respectively.</span></span> <span data-ttu-id="a686e-114">Quando il compilatore MIDL elabora il file IDL, genera il file di intestazione illustrato nell'esempio.</span><span class="sxs-lookup"><span data-stu-id="a686e-114">When the MIDL compiler processes the IDL file, it generates the header file shown in the example.</span></span>

## <a name="example"></a><span data-ttu-id="a686e-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="a686e-115">Example</span></span>

``` syntax
// File: pipedemo.idl
typedef pipe long LONG_PIPE;
void InPipe( [in] LONG_PIPE pipe_data );
void OutPipe( [out] LONG_PIPE *pipe_data ); 
//end pipedemo.idl
 
// File: pipedemo.h (fragment)
// Generated by the MIDL compiler from pipedemo.idl
typedef struct pipe_LONG_PIPE
{
    void (__RPC_FAR * pull) (
        char __RPC_FAR * state,
        long __RPC_FAR * buf,
        unsigned long esize,
        unsigned long __RPC_FAR * ecount );
    void (__RPC_FAR * push) (
        char __RPC_FAR * state,
        long __RPC_FAR * buf,
        unsigned long ecount );
    void (__RPC_FAR * alloc) (
        char __RPC_FAR * state,
        unsigned long bsize,
        long __RPC_FAR * __RPC_FAR * buf,
        unsigned long __RPC_FAR * bcount );
    char __RPC_FAR * state;
} LONG_PIPE;
 
void InPipe( 
    /* [in] */ LONG_PIPE pipe_data);
void OutPipe( 
    /* [out] */ LONG_PIPE __RPC_FAR *pipe_data);
//end pipedemo.h
```

## <a name="related-topics"></a><span data-ttu-id="a686e-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a686e-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a686e-117">inviare tramite pipe</span><span class="sxs-lookup"><span data-stu-id="a686e-117">pipe</span></span>](/windows/desktop/Midl/pipe)
</dt> <dt>

[<span data-ttu-id="a686e-118">**/OI**</span><span class="sxs-lookup"><span data-stu-id="a686e-118">**/Oi**</span></span>](/windows/desktop/Midl/-oi)
</dt> </dl>

 

 