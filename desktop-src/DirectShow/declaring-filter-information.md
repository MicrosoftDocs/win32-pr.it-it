---
description: Dichiarazione delle informazioni sul filtro
ms.assetid: ed3c1d44-ccef-4dde-819b-f5d4d3be6d1e
title: Dichiarazione delle informazioni sul filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8975217f1b7746b26dc5dd16ce9f4e7f694f44bc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747410"
---
# <a name="declaring-filter-information"></a><span data-ttu-id="e63f3-103">Dichiarazione delle informazioni sul filtro</span><span class="sxs-lookup"><span data-stu-id="e63f3-103">Declaring Filter Information</span></span>

<span data-ttu-id="e63f3-104">Il primo passaggio consiste nel dichiarare le informazioni del filtro, se necessario.</span><span class="sxs-lookup"><span data-stu-id="e63f3-104">The first step is to declare the filter information, if needed.</span></span> <span data-ttu-id="e63f3-105">DirectShow definisce le strutture seguenti per la descrizione di filtri, pin e tipi di supporto:</span><span class="sxs-lookup"><span data-stu-id="e63f3-105">DirectShow defines the following structures for describing filters, pins, and media types:</span></span>



| <span data-ttu-id="e63f3-106">Struttura</span><span class="sxs-lookup"><span data-stu-id="e63f3-106">Structure</span></span>                                               | <span data-ttu-id="e63f3-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e63f3-107">Description</span></span>             |
|---------------------------------------------------------|-------------------------|
| [<span data-ttu-id="e63f3-108">**\_filtro AMOVIESETUP**</span><span class="sxs-lookup"><span data-stu-id="e63f3-108">**AMOVIESETUP\_FILTER**</span></span>](amoviesetup-filter.md)       | <span data-ttu-id="e63f3-109">Descrive un filtro.</span><span class="sxs-lookup"><span data-stu-id="e63f3-109">Describes a filter.</span></span>     |
| [<span data-ttu-id="e63f3-110">**\_pin AMOVIESETUP**</span><span class="sxs-lookup"><span data-stu-id="e63f3-110">**AMOVIESETUP\_PIN**</span></span>](amoviesetup-pin.md)             | <span data-ttu-id="e63f3-111">Descrive un PIN.</span><span class="sxs-lookup"><span data-stu-id="e63f3-111">Describes a pin.</span></span>        |
| [<span data-ttu-id="e63f3-112">**\_MEDIATYPE AMOVIESETUP**</span><span class="sxs-lookup"><span data-stu-id="e63f3-112">**AMOVIESETUP\_MEDIATYPE**</span></span>](amoviesetup-mediatype.md) | <span data-ttu-id="e63f3-113">Descrive un tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="e63f3-113">Describes a media type.</span></span> |



 

<span data-ttu-id="e63f3-114">Queste strutture sono annidate.</span><span class="sxs-lookup"><span data-stu-id="e63f3-114">These structures are nested.</span></span> <span data-ttu-id="e63f3-115">La struttura del **\_ filtro AMOVEIESETUP** include un puntatore a una matrice di strutture **AMOVIESETUP \_ pin** e ognuna di esse dispone di un puntatore a una matrice di strutture **AMOVEIESETUP \_ MEDIATYPE** .</span><span class="sxs-lookup"><span data-stu-id="e63f3-115">The **AMOVEIESETUP\_FILTER** structure has a pointer to an array of **AMOVIESETUP\_PIN** structures, and each of these has a pointer to an array of **AMOVEIESETUP\_MEDIATYPE** structures.</span></span> <span data-ttu-id="e63f3-116">Insieme, queste strutture forniscono informazioni sufficienti per l'interfaccia [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) per individuare un filtro.</span><span class="sxs-lookup"><span data-stu-id="e63f3-116">Taken together, these structures provide enough information for the [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) interface to locate a filter.</span></span> <span data-ttu-id="e63f3-117">Non sono una descrizione completa di un filtro.</span><span class="sxs-lookup"><span data-stu-id="e63f3-117">They are not a complete description of a filter.</span></span> <span data-ttu-id="e63f3-118">Se, ad esempio, il filtro crea più istanze dello stesso pin, è necessario dichiarare solo una struttura di [**\_ pin AMOVIESETUP**](amoviesetup-pin.md) per tale pin.</span><span class="sxs-lookup"><span data-stu-id="e63f3-118">For example, if the filter creates multiple instances of the same pin, you should declare only one [**AMOVIESETUP\_PIN**](amoviesetup-pin.md) structure for that pin.</span></span> <span data-ttu-id="e63f3-119">Inoltre, non è necessario un filtro per supportare ogni combinazione di tipi di supporto registrato; non è necessario per registrare tutti i tipi di supporto supportati.</span><span class="sxs-lookup"><span data-stu-id="e63f3-119">Also, a filter is not required to support every combination of media types that it registers; nor is required to register every media type that it supports.</span></span>

<span data-ttu-id="e63f3-120">Dichiarare le strutture di configurazione come variabili globali all'interno della DLL.</span><span class="sxs-lookup"><span data-stu-id="e63f3-120">Declare the set-up structures as global variables within your DLL.</span></span> <span data-ttu-id="e63f3-121">L'esempio seguente mostra un filtro con un pin di output:</span><span class="sxs-lookup"><span data-stu-id="e63f3-121">The following example shows a filter with one output pin:</span></span>


```C++
static const WCHAR g_wszName[] = L"Some Filter";

AMOVIESETUP_MEDIATYPE sudMediaTypes[] = {
    { &MEDIATYPE_Video, &MEDIASUBTYPE_RGB24 },
    { &MEDIATYPE_Video, &MEDIASUBTYPE_RGB32 },
};

AMOVIESETUP_PIN sudOutputPin = {
    L"",            // Obsolete, not used.
    FALSE,          // Is this pin rendered?
    TRUE,           // Is it an output pin?
    FALSE,          // Can the filter create zero instances?
    FALSE,          // Does the filter create multiple instances?
    &GUID_NULL,     // Obsolete.
    NULL,           // Obsolete.
    2,              // Number of media types.
    sudMediaTypes   // Pointer to media types.
};

AMOVIESETUP_FILTER sudFilterReg = {
    &CLSID_SomeFilter,      // Filter CLSID.
    g_wszName,              // Filter name.
    MERIT_NORMAL,           // Merit.
    1,                      // Number of pin types.
    &sudOutputPin           // Pointer to pin information.
};
```



<span data-ttu-id="e63f3-122">Il nome del filtro viene dichiarato come variabile globale statica, perché verrà usato di nuovo altrove.</span><span class="sxs-lookup"><span data-stu-id="e63f3-122">The filter name is declared as a static global variable, because it will be used again elsewhere.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e63f3-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e63f3-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e63f3-124">Come registrare i filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="e63f3-124">How to Register DirectShow Filters</span></span>](how-to-register-directshow-filters.md)
</dt> </dl>

 

 



