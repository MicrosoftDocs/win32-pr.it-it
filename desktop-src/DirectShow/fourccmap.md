---
description: La classe FOURCCMap fornisce la conversione tra sottotipi di supporti GUID e tag multimediali FOURCC a 32 bit di vecchio stile.
ms.assetid: f77f1da9-34f6-44a0-9f1a-7db2e5a26268
title: Classe FOURCCMap
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FOURCCMap
api_type:
- COM
api_location: ''
ms.openlocfilehash: b9254986bebadeffafaa832817f59194bfc58e12
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908859"
---
# <a name="fourccmap-class"></a><span data-ttu-id="878e7-103">Classe FOURCCMap</span><span class="sxs-lookup"><span data-stu-id="878e7-103">FOURCCMap class</span></span>

![Gerarchia di classi fourccmap](images/fourcc01.png)

<span data-ttu-id="878e7-105">La **classe FOURCCMap** fornisce la conversione tra **sottotipi di** supporti GUID e tag multimediali **FOURCC** a 32 bit di vecchio stile.</span><span class="sxs-lookup"><span data-stu-id="878e7-105">The **FOURCCMap** class provides conversion between **GUID** media subtypes and old-style **FOURCC** 32-bit media tags.</span></span> <span data-ttu-id="878e7-106">Nelle API multimediali windows originali, i tipi di supporti sono stati contrassegnati con valori a 32 bit creati da quattro caratteri a 8 bit ed erano noti come **FOURCC.**</span><span class="sxs-lookup"><span data-stu-id="878e7-106">In the original Windows multimedia APIs, media types were tagged with 32-bit values created from four 8-bit characters and were known as **FOURCC** s.</span></span> <span data-ttu-id="878e7-107">I tipi di supporti DirectShow hanno **GUID** per il sottotipo, in parte perché sono più semplici da creare (la creazione di un nuovo **FOURCC** richiede la registrazione con Microsoft).</span><span class="sxs-lookup"><span data-stu-id="878e7-107">DirectShow media types have **GUID** s for the subtype, partly because these are simpler to create (creation of a new **FOURCC** requires its registration with Microsoft).</span></span> <span data-ttu-id="878e7-108">Poiché **fourcc** s sono univoci, è stato reso possibile un mapping uno-a-uno allocando un intervallo di 4.000 milioni di **GUID** che rappresentano **FOURCC** s.</span><span class="sxs-lookup"><span data-stu-id="878e7-108">Because **FOURCC** s are unique, a one-to-one mapping has been made possible by allocating a range of 4,000 million **GUID** s representing **FOURCC** s.</span></span> <span data-ttu-id="878e7-109">Questo intervallo è tutto **GUID** nel formato:</span><span class="sxs-lookup"><span data-stu-id="878e7-109">This range is all **GUID** s of the form:</span></span>

`XXXXXXXX-0000-0010-8000-00AA00389B71`

<span data-ttu-id="878e7-110">Questa classe semplifica la conversione **tra GUID** e **FOURCC** s.</span><span class="sxs-lookup"><span data-stu-id="878e7-110">This class simplifies conversion between **GUID** s and **FOURCC** s.</span></span> <span data-ttu-id="878e7-111">Questo è solo per la compatibilità.</span><span class="sxs-lookup"><span data-stu-id="878e7-111">This is for compatibility only.</span></span> <span data-ttu-id="878e7-112">È consigliabile che tutti i nuovi sottotipi multimediali siano rappresentati da **GUID** creati da Guidgen.exe o da uno strumento simile e non tramite il mapping **di FOURCC** s.</span><span class="sxs-lookup"><span data-stu-id="878e7-112">It is recommended that all new media subtypes be represented by **GUID** s created by Guidgen.exe or a similar tool, and not by mapping **FOURCC** s.</span></span>

<span data-ttu-id="878e7-113">L'oggetto è derivato da **un GUID**, senza membri dati aggiuntivi e può essere eseguito il cast a un **GUID**.</span><span class="sxs-lookup"><span data-stu-id="878e7-113">The object is derived from a **GUID**, with no extra data members, and can be cast to a **GUID**.</span></span> <span data-ttu-id="878e7-114">L'oggetto può essere passato a **FOURCC** in fase di costruzione.</span><span class="sxs-lookup"><span data-stu-id="878e7-114">The object can be passed a **FOURCC** at construction time.</span></span> <span data-ttu-id="878e7-115">Il costruttore predefinito inizializzerà **FOURCC** su zero.</span><span class="sxs-lookup"><span data-stu-id="878e7-115">The default constructor will initialize the **FOURCC** to zero.</span></span>

<span data-ttu-id="878e7-116">I [**metodi GetFOURCC**](fourccmap-getfourcc.md) e [**SetFOURCC**](fourccmap-setfourcc.md) non verificano che le parti fisse del **GUID** corrispondano all'intervallo **FOURCC.**</span><span class="sxs-lookup"><span data-stu-id="878e7-116">The [**GetFOURCC**](fourccmap-getfourcc.md) and [**SetFOURCC**](fourccmap-setfourcc.md) methods do not check that the fixed portions of the **GUID** correspond to the **FOURCC** range.</span></span> <span data-ttu-id="878e7-117">Pertanto, se si esegue il cast di un puntatore a un **GUID** in un puntatore a **fourcc** e quindi si imposta o si ottiene il campo **FOURCC,** è necessario verificare separatamente che il **GUID** sia compreso nell'intervallo **FOURCC.**</span><span class="sxs-lookup"><span data-stu-id="878e7-117">Thus, if you cast a pointer to a **GUID** into a pointer to a **FOURCC** and then set or get the **FOURCC** field, you also need to check separately that the **GUID** is within the **FOURCC** range.</span></span>

## <a name="member-functions"></a><span data-ttu-id="878e7-118">Funzioni di membro</span><span class="sxs-lookup"><span data-stu-id="878e7-118">Member Functions</span></span>



| <span data-ttu-id="878e7-119">Label</span><span class="sxs-lookup"><span data-stu-id="878e7-119">Label</span></span> | <span data-ttu-id="878e7-120">Valore</span><span class="sxs-lookup"><span data-stu-id="878e7-120">Value</span></span> |
|------------------------------------------|----------------------------------------------------------|
| [<span data-ttu-id="878e7-121">**FOURCCMap**</span><span class="sxs-lookup"><span data-stu-id="878e7-121">**FOURCCMap**</span></span>](fourccmap-fourccmap.md) | <span data-ttu-id="878e7-122">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="878e7-122">Constructor method.</span></span>                                      |
| [<span data-ttu-id="878e7-123">**GetFOURCC**</span><span class="sxs-lookup"><span data-stu-id="878e7-123">**GetFOURCC**</span></span>](fourccmap-getfourcc.md) | <span data-ttu-id="878e7-124">Recupera **l'oggetto FOURCC** da un **oggetto FOURCCMap.**</span><span class="sxs-lookup"><span data-stu-id="878e7-124">Retrieves the **FOURCC** from a **FOURCCMap** object.</span></span>    |
| [<span data-ttu-id="878e7-125">**SetFOURCC**</span><span class="sxs-lookup"><span data-stu-id="878e7-125">**SetFOURCC**</span></span>](fourccmap-setfourcc.md) | <span data-ttu-id="878e7-126">Imposta la **parte FOURCC** dell'oggetto **FOURCCMap.**</span><span class="sxs-lookup"><span data-stu-id="878e7-126">Sets the **FOURCC** portion of the **FOURCCMap** object.</span></span> |



 

 

 



