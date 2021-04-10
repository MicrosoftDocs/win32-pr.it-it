---
description: La classe FOURCCMap fornisce la conversione tra sottotipi di supporto GUID e tag per supporti FOURCC a 32 bit obsoleti.
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
ms.openlocfilehash: fd30a0f04d98b4c6ba4b7716a1a72d527873dbff
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124551"
---
# <a name="fourccmap-class"></a><span data-ttu-id="21efa-103">Classe FOURCCMap</span><span class="sxs-lookup"><span data-stu-id="21efa-103">FOURCCMap class</span></span>

![gerarchia di classi fourccmap](images/fourcc01.png)

<span data-ttu-id="21efa-105">La classe **FOURCCMap** fornisce la conversione tra sottotipi di supporto **GUID** e tag per supporti **fourcc** a 32 bit obsoleti.</span><span class="sxs-lookup"><span data-stu-id="21efa-105">The **FOURCCMap** class provides conversion between **GUID** media subtypes and old-style **FOURCC** 32-bit media tags.</span></span> <span data-ttu-id="21efa-106">Nelle API multimediali di Windows originali, i tipi di supporto sono stati contrassegnati con i valori a 32 bit creati da caratteri a 4 8 bit ed erano noti come **fourcc** s.</span><span class="sxs-lookup"><span data-stu-id="21efa-106">In the original Windows multimedia APIs, media types were tagged with 32-bit values created from four 8-bit characters and were known as **FOURCC** s.</span></span> <span data-ttu-id="21efa-107">I tipi di supporto DirectShow hanno **GUID** per il sottotipo, in parte perché sono più semplici da creare (la creazione di un nuovo **fourcc** richiede la registrazione con Microsoft).</span><span class="sxs-lookup"><span data-stu-id="21efa-107">DirectShow media types have **GUID** s for the subtype, partly because these are simpler to create (creation of a new **FOURCC** requires its registration with Microsoft).</span></span> <span data-ttu-id="21efa-108">Poiché i **fourcc** sono univoci, è possibile eseguire un mapping uno-a-uno allocando un intervallo di 4 miliardi **GUID** che rappresenta **fourcc** s.</span><span class="sxs-lookup"><span data-stu-id="21efa-108">Because **FOURCC** s are unique, a one-to-one mapping has been made possible by allocating a range of 4,000 million **GUID** s representing **FOURCC** s.</span></span> <span data-ttu-id="21efa-109">Questo intervallo è costituito da tutti i **GUID** nel formato:</span><span class="sxs-lookup"><span data-stu-id="21efa-109">This range is all **GUID** s of the form:</span></span>

`XXXXXXXX-0000-0010-8000-00AA00389B71`

<span data-ttu-id="21efa-110">Questa classe semplifica la conversione tra **GUID** s e **fourcc** s.</span><span class="sxs-lookup"><span data-stu-id="21efa-110">This class simplifies conversion between **GUID** s and **FOURCC** s.</span></span> <span data-ttu-id="21efa-111">Questa operazione è solo per compatibilità.</span><span class="sxs-lookup"><span data-stu-id="21efa-111">This is for compatibility only.</span></span> <span data-ttu-id="21efa-112">È consigliabile che tutti i nuovi sottotipi di supporti siano rappresentati da **GUID** s creati da Guidgen.exe o da uno strumento simile e non dal mapping di **fourcc** s.</span><span class="sxs-lookup"><span data-stu-id="21efa-112">It is recommended that all new media subtypes be represented by **GUID** s created by Guidgen.exe or a similar tool, and not by mapping **FOURCC** s.</span></span>

<span data-ttu-id="21efa-113">L'oggetto è derivato da un **GUID**, senza membri dati aggiuntivi, ed è possibile eseguirne il cast in un **GUID**.</span><span class="sxs-lookup"><span data-stu-id="21efa-113">The object is derived from a **GUID**, with no extra data members, and can be cast to a **GUID**.</span></span> <span data-ttu-id="21efa-114">È possibile passare un **fourcc** all'oggetto in fase di costruzione.</span><span class="sxs-lookup"><span data-stu-id="21efa-114">The object can be passed a **FOURCC** at construction time.</span></span> <span data-ttu-id="21efa-115">Il costruttore predefinito inizializza **fourcc** su zero.</span><span class="sxs-lookup"><span data-stu-id="21efa-115">The default constructor will initialize the **FOURCC** to zero.</span></span>

<span data-ttu-id="21efa-116">I metodi [**GetFOURCC**](fourccmap-getfourcc.md) e [**SetFOURCC**](fourccmap-setfourcc.md) non verificano che le parti fisse del **GUID** corrispondano all'intervallo di **fourcc** .</span><span class="sxs-lookup"><span data-stu-id="21efa-116">The [**GetFOURCC**](fourccmap-getfourcc.md) and [**SetFOURCC**](fourccmap-setfourcc.md) methods do not check that the fixed portions of the **GUID** correspond to the **FOURCC** range.</span></span> <span data-ttu-id="21efa-117">Pertanto, se si esegue il cast di un puntatore a un **GUID** in un puntatore a un **fourcc** e quindi si imposta o si ottiene il campo **fourcc** , è necessario controllare separatamente che il **GUID** sia compreso nell'intervallo di **fourcc** .</span><span class="sxs-lookup"><span data-stu-id="21efa-117">Thus, if you cast a pointer to a **GUID** into a pointer to a **FOURCC** and then set or get the **FOURCC** field, you also need to check separately that the **GUID** is within the **FOURCC** range.</span></span>

## <a name="member-functions"></a><span data-ttu-id="21efa-118">Funzioni di membro</span><span class="sxs-lookup"><span data-stu-id="21efa-118">Member Functions</span></span>



|                                          |                                                          |
|------------------------------------------|----------------------------------------------------------|
| [<span data-ttu-id="21efa-119">**FOURCCMap**</span><span class="sxs-lookup"><span data-stu-id="21efa-119">**FOURCCMap**</span></span>](fourccmap-fourccmap.md) | <span data-ttu-id="21efa-120">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="21efa-120">Constructor method.</span></span>                                      |
| [<span data-ttu-id="21efa-121">**GetFOURCC**</span><span class="sxs-lookup"><span data-stu-id="21efa-121">**GetFOURCC**</span></span>](fourccmap-getfourcc.md) | <span data-ttu-id="21efa-122">Recupera **fourcc** da un oggetto **FOURCCMap** .</span><span class="sxs-lookup"><span data-stu-id="21efa-122">Retrieves the **FOURCC** from a **FOURCCMap** object.</span></span>    |
| [<span data-ttu-id="21efa-123">**SetFOURCC**</span><span class="sxs-lookup"><span data-stu-id="21efa-123">**SetFOURCC**</span></span>](fourccmap-setfourcc.md) | <span data-ttu-id="21efa-124">Imposta la parte **fourcc** dell'oggetto **FOURCCMap** .</span><span class="sxs-lookup"><span data-stu-id="21efa-124">Sets the **FOURCC** portion of the **FOURCCMap** object.</span></span> |



 

 

 



