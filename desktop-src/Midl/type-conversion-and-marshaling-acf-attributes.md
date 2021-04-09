---
title: Type-Conversion e marshalling degli attributi ACF
description: Usare questi attributi per controllare la modalità di trasmissione dei dati in rete.
ms.assetid: 6af635f6-eeee-4fa6-85db-5d60434a1235
keywords:
- MIDL, attributi, conversione di tipi e marshalling di ACF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14367be3df97cc1185fca64e46aafe1d342f3526
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955717"
---
# <a name="type-conversion-and-marshaling-acf-attributes"></a><span data-ttu-id="b38db-104">Type-Conversion e marshalling degli attributi ACF</span><span class="sxs-lookup"><span data-stu-id="b38db-104">Type-Conversion and Marshaling ACF Attributes</span></span>

<span data-ttu-id="b38db-105">Usare questi attributi per controllare la modalità di trasmissione dei dati in rete.</span><span class="sxs-lookup"><span data-stu-id="b38db-105">Use these attributes to control how your data is transmitted over the network.</span></span>



| <span data-ttu-id="b38db-106">Attributo</span><span class="sxs-lookup"><span data-stu-id="b38db-106">Attribute</span></span>                                        | <span data-ttu-id="b38db-107">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="b38db-107">Usage</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b38db-108">[**codifica**](encode.md)[ decodifica](decode.md)</span><span class="sxs-lookup"><span data-stu-id="b38db-108">[**encode**](encode.md)[**decode**](decode.md)</span></span> | <span data-ttu-id="b38db-109">Indica a MIDL di esporre le routine di serializzazione di tipo o routine (selezione) generate per gli stub.</span><span class="sxs-lookup"><span data-stu-id="b38db-109">Instructs MIDL to expose the type or procedure serialization (pickling) routines it generates for the stubs.</span></span> <span data-ttu-id="b38db-110">L'applicazione client può chiamare le routine per effettuare il marshalling dei dati in base al valore.</span><span class="sxs-lookup"><span data-stu-id="b38db-110">Your client application can call those routines to marshal data by value.</span></span>                                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="b38db-111">**rappresenta \_ come**</span><span class="sxs-lookup"><span data-stu-id="b38db-111">**represent\_as**</span></span>](represent-as.md)            | <span data-ttu-id="b38db-112">Specifica la modalità di rappresentazione di un tipo di dati in transito, quando la natura esatta del tipo di dati di un client non è importante per il server, perché richiede solo i dati stessi e non la struttura effettiva, oppure il tipo di client effettivo è sconosciuto a MIDL in fase di compilazione.</span><span class="sxs-lookup"><span data-stu-id="b38db-112">Specifies how a data type will be represented on the wire, when the exact nature of a client's data type is unimportant to the server (because it only needs the data itself and not the actual structure), or the actual client type is unknown to MIDL at compile time.</span></span> <span data-ttu-id="b38db-113">Se, ad esempio, l'applicazione client usa un elenco collegato di numeri a virgola mobile, è possibile specificare che la rappresentazione Wire di tale elenco sia una matrice di tipo [**float**](float.md).</span><span class="sxs-lookup"><span data-stu-id="b38db-113">For example, if your client application uses a linked list of floating-point numbers, you could specify that the wire-representation of that list be an array of type [**float**](float.md).</span></span> |
| [<span data-ttu-id="b38db-114">**\_marshalling utente**</span><span class="sxs-lookup"><span data-stu-id="b38db-114">**user\_marshal**</span></span>](user-marshal.md)            | <span data-ttu-id="b38db-115">Controlla il modo in cui i dati vengono trasmessi in rete implementando routine di marshalling personalizzate.</span><span class="sxs-lookup"><span data-stu-id="b38db-115">Controls how data is transmitted over the wire by implementing your own marshaling routines.</span></span> <span data-ttu-id="b38db-116">Questo attributo è utile se si dispone di un tipo di dati sconosciuto a MIDL o se si passano informazioni tra le piattaforme big-endian e Little-endian.</span><span class="sxs-lookup"><span data-stu-id="b38db-116">This attribute is useful if you have a data type that is unknown to MIDL or if you are passing information between big-endian and little-endian platforms.</span></span>                                                                                                                                                                                                                 |



 

<span data-ttu-id="b38db-117">Gli attributi di marshalling DCE [**in \_ linea**](in-line.md) e non in [**\_ \_ linea**](out-of-line.md) non sono implementati in Microsoft RPC.</span><span class="sxs-lookup"><span data-stu-id="b38db-117">The DCE marshaling attributes [**in\_line**](in-line.md) and [**out\_of\_line**](out-of-line.md) are not implemented in Microsoft RPC.</span></span> <span data-ttu-id="b38db-118">Il compilatore MIDL esegue automaticamente il marshalling dei tipi di dati complessi out-of-line.</span><span class="sxs-lookup"><span data-stu-id="b38db-118">The MIDL compiler automatically marshals complex data types out-of-line.</span></span>

 

 




