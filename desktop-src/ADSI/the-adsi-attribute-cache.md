---
title: Cache degli attributi ADSI
description: Il modello a oggetti ADSI fornisce una cache degli attributi sul lato client per ogni oggetto ADSI.
ms.assetid: 0d2b4117-11f2-4b39-8fe5-3b176e4256f4
ms.tgt_platform: multiple
keywords:
- ADSI cache degli attributi ADSI
- ADSI ADSI, uso, accesso e manipolazione di dati con ADSI, cache degli attributi
- attributi ADSI, caching degli attributi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df3062ed5862f11e9db5dadd83b80ac624218c81
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707375"
---
# <a name="the-adsi-attribute-cache"></a><span data-ttu-id="cdd1f-106">Cache degli attributi ADSI</span><span class="sxs-lookup"><span data-stu-id="cdd1f-106">The ADSI Attribute Cache</span></span>

<span data-ttu-id="cdd1f-107">Il modello a oggetti ADSI fornisce una cache degli attributi sul lato client per ogni oggetto ADSI.</span><span class="sxs-lookup"><span data-stu-id="cdd1f-107">The ADSI object model provides a client-side attribute cache for each ADSI object.</span></span> <span data-ttu-id="cdd1f-108">La cache degli attributi è paragonabile a una tabella in memoria che contiene i nomi e i valori della maggior parte degli attributi degli oggetti che sono stati scaricati.</span><span class="sxs-lookup"><span data-stu-id="cdd1f-108">The attribute cache is comparable to a table in memory that contains the names and values of most object attributes that have been downloaded.</span></span> <span data-ttu-id="cdd1f-109">Alcuni attributi, ad esempio gli attributi operativi, non vengono memorizzati nella cache.</span><span class="sxs-lookup"><span data-stu-id="cdd1f-109">Some attributes, such as operational attributes, are not cached.</span></span> <span data-ttu-id="cdd1f-110">ADSI utilizza la memorizzazione nella cache delle proprietà per migliorare le prestazioni della manipolazione degli attributi e aggiungere la funzionalità di transazione per le operazioni di lettura e scrittura degli attributi.</span><span class="sxs-lookup"><span data-stu-id="cdd1f-110">ADSI uses property caching to enhance the performance of attribute manipulation and add transactioning capability for attribute read and write operations.</span></span> <span data-ttu-id="cdd1f-111">Questa funzionalità è essenziale per i client scritti in linguaggi che non dispongono di un meccanismo di invio in batch nativo per l'impostazione di attributi, ad esempio Microsoft Visual Basic Development System.</span><span class="sxs-lookup"><span data-stu-id="cdd1f-111">This capability is critical for clients written in languages that have no native batching mechanism for setting attributes, such as Microsoft Visual Basic development system.</span></span> <span data-ttu-id="cdd1f-112">Senza la cache delle proprietà ADSI, tali client dovranno accedere al server ogni volta che un attributo viene letto o scritto.</span><span class="sxs-lookup"><span data-stu-id="cdd1f-112">Without the ADSI property cache, such clients would have to access the server every time an attribute is read or written.</span></span>

<span data-ttu-id="cdd1f-113">Quando un oggetto viene creato o associato per la prima volta a, la cache delle proprietà per l'oggetto è vuota.</span><span class="sxs-lookup"><span data-stu-id="cdd1f-113">When an object is created or first bound to, the property cache for the object is empty.</span></span> <span data-ttu-id="cdd1f-114">Quando viene chiamato il metodo [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) , ADSI carica gli attributi richiesti per l'oggetto dal servizio directory sottostante nella cache locale.</span><span class="sxs-lookup"><span data-stu-id="cdd1f-114">When the [**IADs::GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) method is called, ADSI loads the requested attributes for the object from the underlying directory service into the local cache.</span></span> <span data-ttu-id="cdd1f-115">Quando viene letto un valore di attributo specifico e la cache è vuota, ADSI esegue una chiamata implicita al metodo **IADs:: GetInfo** .</span><span class="sxs-lookup"><span data-stu-id="cdd1f-115">When a specific attribute value is read and the cache is empty, ADSI makes an implicit call to the **IADs::GetInfo** method.</span></span> <span data-ttu-id="cdd1f-116">Quando la cache viene riempita, tutte le operazioni di lettura degli attributi funzionano solo sul contenuto della cache.</span><span class="sxs-lookup"><span data-stu-id="cdd1f-116">When the cache is filled, all attribute read operations work on the contents of the cache only.</span></span>

<span data-ttu-id="cdd1f-117">Quando viene scritto un valore di attributo, il nuovo valore viene archiviato nella cache locale fino a quando non viene chiamato il metodo [**IADs:: SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) .</span><span class="sxs-lookup"><span data-stu-id="cdd1f-117">When an attribute value is written, the new value is stored in the local cache until the [**IADs::SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) method is called.</span></span> <span data-ttu-id="cdd1f-118">Quando viene chiamato il metodo **IADs:: SetInfo** , viene eseguito il commit degli attributi nella cache nel servizio directory sottostante.</span><span class="sxs-lookup"><span data-stu-id="cdd1f-118">When the **IADs::SetInfo** method is called, the attributes in the cache are committed to the underlying directory service.</span></span> <span data-ttu-id="cdd1f-119">Dopo la chiamata al metodo **IADs:: SetInfo** , i valori rimangono nella cache fino a quando non vengono aggiornati in modo esplicito con un'altra chiamata al metodo [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) .</span><span class="sxs-lookup"><span data-stu-id="cdd1f-119">After the **IADs::SetInfo** method is called, the values remain in the cache until explicitly refreshed with another call to the [**IADs::GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) method.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cdd1f-120">È necessario usare attentamente il metodo [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) perché questo metodo sovrascriverà sempre i valori dell'attributo nella cache dal servizio directory sottostante, anche se il valore memorizzato nella cache è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="cdd1f-120">The [**IADs::GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) method must be used carefully because this method will always overwrite the attribute values in the cache from the underlying directory service, even if the cached value has been changed.</span></span> <span data-ttu-id="cdd1f-121">Ovvero, sovrascriverà i valori di attributo che sono stati modificati nella cache, ma non ne è stato eseguito il commit nel servizio directory sottostante con una chiamata al metodo [**IADs:: SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) .</span><span class="sxs-lookup"><span data-stu-id="cdd1f-121">That is, it will overwrite attribute values that have been changed in the cache, but not committed to the underlying directory service with a call to the [**IADs::SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) method.</span></span>

 

<span data-ttu-id="cdd1f-122">Nella figura seguente vengono illustrati i diversi metodi utilizzati per operare sulla cache.</span><span class="sxs-lookup"><span data-stu-id="cdd1f-122">The following figure shows the different methods used to operate on the cache.</span></span>

![cache degli attributi ADSI](images/ds2propc.png)

 

 




