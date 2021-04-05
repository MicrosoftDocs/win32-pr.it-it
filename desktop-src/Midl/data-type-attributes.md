---
title: Attributi del tipo di dati
description: È possibile applicare questi attributi ai tipi di dati in un'istruzione typedef per definire ulteriormente l'utilizzo o l'effetto del tipo di dati.
ms.assetid: 9a2e7c3d-f18f-4162-877c-5fc48a36b05d
keywords:
- MIDL di IDL, attributi, tipo di dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57fb2a97639fc17454bfd1cad60466ad277e18ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714368"
---
# <a name="data-type-attributes"></a><span data-ttu-id="4e066-104">Attributi del tipo di dati</span><span class="sxs-lookup"><span data-stu-id="4e066-104">Data Type Attributes</span></span>

<span data-ttu-id="4e066-105">È possibile applicare questi attributi ai tipi di dati in un'istruzione [**typedef**](typedef.md) per definire ulteriormente l'utilizzo o l'effetto del tipo di dati.</span><span class="sxs-lookup"><span data-stu-id="4e066-105">You can apply these attributes to data types in a [**typedef**](typedef.md) statement to further define the usage or effect of the data type.</span></span>



| <span data-ttu-id="4e066-106">Attributo</span><span class="sxs-lookup"><span data-stu-id="4e066-106">Attribute</span></span>                                 | <span data-ttu-id="4e066-107">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="4e066-107">Usage</span></span>                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4e066-108">**handle di contesto \_**</span><span class="sxs-lookup"><span data-stu-id="4e066-108">**context\_handle**</span></span>](context-handle.md) | <span data-ttu-id="4e066-109">Identifica un handle di associazione che mantiene le informazioni sullo stato (contesto) su un particolare server tra le chiamate di procedure remote da un particolare client.</span><span class="sxs-lookup"><span data-stu-id="4e066-109">Identifies a binding handle that maintains state (context) information on a particular server between remote procedure calls from a particular client.</span></span> <span data-ttu-id="4e066-110">Non valido per le funzioni dell'interfaccia dell' [**oggetto**](object.md) .</span><span class="sxs-lookup"><span data-stu-id="4e066-110">Not valid for [**object**](object.md) interface functions.</span></span>                                                                                                         |
| [<span data-ttu-id="4e066-111">**gestire**</span><span class="sxs-lookup"><span data-stu-id="4e066-111">**handle**</span></span>](handle.md)                  | <span data-ttu-id="4e066-112">Specifica un tipo di handle personalizzato specifico per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4e066-112">Specifies a custom handle type specific to the application.</span></span>                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="4e066-113">**MS \_ Union**</span><span class="sxs-lookup"><span data-stu-id="4e066-113">**ms\_union**</span></span>](-ms-union.md)            | <span data-ttu-id="4e066-114">Controlla l'allineamento del rapporto di recapito delle unioni non incapsulate.</span><span class="sxs-lookup"><span data-stu-id="4e066-114">Controls the NDR alignment of nonencapsulated unions.</span></span> <span data-ttu-id="4e066-115">Usare su [**typedef**](typedef.md)per la compatibilità con le interfacce compilate con MIDL 1,0 o 2,0.</span><span class="sxs-lookup"><span data-stu-id="4e066-115">Use on [**typedef**](typedef.md)s for backward compatibility with interfaces built with MIDL 1.0 or 2.0.</span></span>                                                                                                                                                            |
| [<span data-ttu-id="4e066-116">**inviare tramite pipe**</span><span class="sxs-lookup"><span data-stu-id="4e066-116">**pipe**</span></span>](pipe.md)                      | <span data-ttu-id="4e066-117">Consente la trasmissione di un flusso aperto di dati tipizzati in una chiamata di procedura remota.</span><span class="sxs-lookup"><span data-stu-id="4e066-117">Allows transmission of an open-ended stream of typed data across a remote procedure call.</span></span> <span data-ttu-id="4e066-118">Un parametro [**in**](in.md) pipe consente al server di eseguire il pull del flusso di dati dal client durante una chiamata di procedura remota.</span><span class="sxs-lookup"><span data-stu-id="4e066-118">An [**in**](in.md) pipe parameter allows the server to pull the data stream from the client during a remote procedure call.</span></span> <span data-ttu-id="4e066-119">Un parametro [**out**](-out.md) pipe consente al server di eseguire il push del flusso di dati al client.</span><span class="sxs-lookup"><span data-stu-id="4e066-119">An [**out**](-out.md) pipe parameter allows the server to push the data stream back to the client.</span></span> |
| [<span data-ttu-id="4e066-120">**Trasmetti \_ come**</span><span class="sxs-lookup"><span data-stu-id="4e066-120">**transmit\_as**</span></span>](transmit-as.md)       | <span data-ttu-id="4e066-121">Specifica il modo in cui un tipo di dati verrà trasmesso in una rete, usato per il marshalling personalizzato.</span><span class="sxs-lookup"><span data-stu-id="4e066-121">Specifies how a data type will be transmitted over a network, used for custom marshaling.</span></span>                                                                                                                                                                                                                                  |
| [<span data-ttu-id="4e066-122">**\_enum V1**</span><span class="sxs-lookup"><span data-stu-id="4e066-122">**v1\_enum**</span></span>](v1-enum.md)               | <span data-ttu-id="4e066-123">Indica che il tipo enumerato specificato deve essere trasmesso come entità a 32 bit, anziché come valore predefinito a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="4e066-123">Directs that the specified enumerated type be transmitted as a 32-bit entity, rather than the 16-bit default.</span></span>                                                                                                                                                                                                              |
| [<span data-ttu-id="4e066-124">**\_marshalling di rete**</span><span class="sxs-lookup"><span data-stu-id="4e066-124">**wire\_marshal**</span></span>](wire-marshal.md)     | <span data-ttu-id="4e066-125">Simile a [**trasmettere \_ come**](transmit-as.md) , ma si implementano le routine per ridimensionare, effettuare il marshalling, annullare il marshalling e liberare i dati.</span><span class="sxs-lookup"><span data-stu-id="4e066-125">Similar to [**transmit\_as**](transmit-as.md) but you implement the routines to size, marshal, unmarshal, and free the data.</span></span>                                                                                                                                                                                              |



 

 

 




