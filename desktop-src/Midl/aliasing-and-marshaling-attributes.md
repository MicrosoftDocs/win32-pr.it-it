---
title: Attributi di aliasing e marshalling
description: Le applicazioni distribuite passano quasi sempre i dati tra i programmi client e server quando chiamano procedure di interfaccia.
ms.assetid: 64895c64-f16b-47c4-928d-5149808b0476
keywords:
- IDL MIDL, attributi MIDL, aliasing e marshalling
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ac66aa04210a878c67ee6bcf1a50ff21fa1d1d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045295"
---
# <a name="aliasing-and-marshaling-attributes"></a><span data-ttu-id="054d9-104">Attributi di aliasing e marshalling</span><span class="sxs-lookup"><span data-stu-id="054d9-104">Aliasing and Marshaling Attributes</span></span>

<span data-ttu-id="054d9-105">Le applicazioni distribuite passano quasi sempre i dati tra i programmi client e server quando chiamano procedure di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="054d9-105">Distributed applications almost always pass data between client and server programs when they call interface procedures.</span></span> <span data-ttu-id="054d9-106">Gli sviluppatori utilizzano MIDL per descrivere i dati che i programmi client e server passano in modo standard.</span><span class="sxs-lookup"><span data-stu-id="054d9-106">Developers use MIDL to describe the data that client and server programs pass in a standard way.</span></span> <span data-ttu-id="054d9-107">Il compilatore MIDL crea Stub applicazione, o proxy, programmi per il client e il server che convertono i dati in un formato standardizzato che può essere inviato in rete.</span><span class="sxs-lookup"><span data-stu-id="054d9-107">The MIDL compiler creates application stub, or proxy, programs for the client and the server that convert the data into a standardized form that can be sent over a network.</span></span> <span data-ttu-id="054d9-108">Questo formato, il formato di rappresentazione dei dati di rete (NDR), viene spesso definito formato wire dei dati.</span><span class="sxs-lookup"><span data-stu-id="054d9-108">This format, the Network Data Representation (NDR) format, is often called the wire format of the data.</span></span> <span data-ttu-id="054d9-109">Gli stub devono convertire i dati dal formato nativo nello spazio di memoria del programma in un rapporto di mancato recapito.</span><span class="sxs-lookup"><span data-stu-id="054d9-109">The stubs must convert data from its native format in the program's memory space to NDR.</span></span> <span data-ttu-id="054d9-110">Questa conversione viene definita marshalling dei dati.</span><span class="sxs-lookup"><span data-stu-id="054d9-110">This conversion is termed marshaling the data.</span></span> <span data-ttu-id="054d9-111">Quando un client o un programma server riceve dati, deve convertire i dati da NDR al formato nativo per il programma.</span><span class="sxs-lookup"><span data-stu-id="054d9-111">When a client or server program receives data, it must convert the data from NDR to the native format for that program.</span></span> <span data-ttu-id="054d9-112">Questa operazione è denominata unmarshaling the data.</span><span class="sxs-lookup"><span data-stu-id="054d9-112">This is called unmarshaling the data.</span></span>

<span data-ttu-id="054d9-113">Usare gli attributi di aliasing e di marshalling per controllare come i dati vengono inseriti in un pacchetto in formato NDR e trasmessi in rete.</span><span class="sxs-lookup"><span data-stu-id="054d9-113">Use aliasing and marshaling attributes to control how your data is packaged into NDR format and transmitted over the network.</span></span>



| <span data-ttu-id="054d9-114">Attributo</span><span class="sxs-lookup"><span data-stu-id="054d9-114">Attribute</span></span>                             | <span data-ttu-id="054d9-115">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="054d9-115">Usage</span></span>                                                                                                                         |
|---------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="054d9-116">**chiama \_ come**</span><span class="sxs-lookup"><span data-stu-id="054d9-116">**call\_as**</span></span>](call-as.md)           | <span data-ttu-id="054d9-117">Esegue il mapping di una funzione non a una chiamata di procedura remota.</span><span class="sxs-lookup"><span data-stu-id="054d9-117">Maps a nonremotable function to a remote procedure call.</span></span>                                                                      |
| [<span data-ttu-id="054d9-118">**IID \_ è**</span><span class="sxs-lookup"><span data-stu-id="054d9-118">**iid\_is**</span></span>](iid-is.md)             | <span data-ttu-id="054d9-119">Fornisce l'identificatore di interfaccia dell'interfaccia COM che rappresenta l'oggetto dell'indicatore di misura.</span><span class="sxs-lookup"><span data-stu-id="054d9-119">Provides the interface identifier of the COM interface that is the object of the pointer.</span></span>                                     |
| [<span data-ttu-id="054d9-120">**Trasmetti \_ come**</span><span class="sxs-lookup"><span data-stu-id="054d9-120">**transmit\_as**</span></span>](transmit-as.md)   | <span data-ttu-id="054d9-121">Converte un tipo di dati in un tipo più semplice per la trasmissione in rete.</span><span class="sxs-lookup"><span data-stu-id="054d9-121">Converts a data type to a simpler type for transmission over a network.</span></span>                                                       |
| [<span data-ttu-id="054d9-122">**\_marshalling di rete**</span><span class="sxs-lookup"><span data-stu-id="054d9-122">**wire\_marshal**</span></span>](wire-marshal.md) | <span data-ttu-id="054d9-123">Simile a [**trasmettere \_ come**](transmit-as.md) , ma si implementano le routine per ridimensionare, effettuare il marshalling, annullare il marshalling e liberare i dati.</span><span class="sxs-lookup"><span data-stu-id="054d9-123">Similar to [**transmit\_as**](transmit-as.md) but you implement the routines to size, marshal, unmarshal, and free the data.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="054d9-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="054d9-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="054d9-125">Conversione di tipi e attributi ACF di marshalling</span><span class="sxs-lookup"><span data-stu-id="054d9-125">Type Conversion and Marshaling ACF Attributes</span></span>](type-conversion-and-marshaling-acf-attributes.md)
</dt> </dl>

 

 




