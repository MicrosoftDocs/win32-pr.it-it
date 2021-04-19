---
description: Fornisce un modello per la creazione di class factory.
ms.assetid: 3dbe6402-15f8-4490-9fe2-bebaa4e79170
title: Classe CFactoryTemplate (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CFactoryTemplate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: be5ca9b8319eeddf777cbf0071c1930f21524369
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329814"
---
# <a name="cfactorytemplate-class"></a><span data-ttu-id="d7c57-103">Classe CFactoryTemplate</span><span class="sxs-lookup"><span data-stu-id="d7c57-103">CFactoryTemplate class</span></span>

<span data-ttu-id="d7c57-104">Fornisce un modello per la creazione di class factory.</span><span class="sxs-lookup"><span data-stu-id="d7c57-104">Provides a template for creating class factories.</span></span>

<span data-ttu-id="d7c57-105">In DirectShow, le class factory sono specializzate mediante la classe **CFactoryTemplate** , denominata anche *modello Factory*.</span><span class="sxs-lookup"><span data-stu-id="d7c57-105">In DirectShow, class factories are specialized using the **CFactoryTemplate** class, also called the *factory template*.</span></span> <span data-ttu-id="d7c57-106">Ogni class factory include un puntatore a un modello Factory.</span><span class="sxs-lookup"><span data-stu-id="d7c57-106">Each class factory holds a pointer to a factory template.</span></span> <span data-ttu-id="d7c57-107">Il modello Factory contiene informazioni su un oggetto COM, incluso l'identificatore di classe (CLSID) dell'oggetto e un puntatore a una funzione che crea l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d7c57-107">The factory template contains information about a COM object, including the object's class identifier (CLSID) and a pointer to a function that creates the object.</span></span>

<span data-ttu-id="d7c57-108">Nella DLL dichiarare una matrice globale di modelli Factory denominati *g \_ templates*.</span><span class="sxs-lookup"><span data-stu-id="d7c57-108">In your DLL, declare a global array of factory templates named *g\_Templates*.</span></span> <span data-ttu-id="d7c57-109">Includere un modello di Factory per ogni oggetto della DLL.</span><span class="sxs-lookup"><span data-stu-id="d7c57-109">Include one factory template for each object in the DLL.</span></span> <span data-ttu-id="d7c57-110">Quando la funzione [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) crea un nuovo class factory, Cerca nella matrice un modello con un CLSID corrispondente.</span><span class="sxs-lookup"><span data-stu-id="d7c57-110">When the [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) function makes a new class factory, it searches the array for a template with a matching CLSID.</span></span> <span data-ttu-id="d7c57-111">Presumendo che ne trovi uno, viene creato un class factory che include un puntatore al modello corrispondente.</span><span class="sxs-lookup"><span data-stu-id="d7c57-111">Assuming it finds one, it creates a class factory that holds a pointer to the matching template.</span></span> <span data-ttu-id="d7c57-112">Quando il client chiama **IClassFactory:: CreateInstance**, il class factory chiama la funzione di creazione di istanze definita nel modello.</span><span class="sxs-lookup"><span data-stu-id="d7c57-112">When the client calls **IClassFactory::CreateInstance**, the class factory calls the instantiation function defined in the template.</span></span>

<span data-ttu-id="d7c57-113">Per ulteriori informazioni, vedere [How to create an DirectShow Filter DLL](how-to-create-a-dll.md).</span><span class="sxs-lookup"><span data-stu-id="d7c57-113">For more information, see [How to Create a DirectShow Filter DLL](how-to-create-a-dll.md).</span></span>



| <span data-ttu-id="d7c57-114">Variabili membro pubblico</span><span class="sxs-lookup"><span data-stu-id="d7c57-114">Public Member Variables</span></span>                                                   | <span data-ttu-id="d7c57-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d7c57-115">Description</span></span>                                                                |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="d7c57-116">**\_nome m**</span><span class="sxs-lookup"><span data-stu-id="d7c57-116">**m\_Name**</span></span>](cfactorytemplate-m-name.md)                                | <span data-ttu-id="d7c57-117">Nome del filtro.</span><span class="sxs-lookup"><span data-stu-id="d7c57-117">Name of the filter.</span></span>                                                        |
| [<span data-ttu-id="d7c57-118">**\_CLSID m**</span><span class="sxs-lookup"><span data-stu-id="d7c57-118">**m\_ClsID**</span></span>](cfactorytemplate-m-clsid.md)                              | <span data-ttu-id="d7c57-119">Puntatore al CLSID dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d7c57-119">Pointer to the CLSID of the object.</span></span>                                        |
| [<span data-ttu-id="d7c57-120">**\_lpfnNew m**</span><span class="sxs-lookup"><span data-stu-id="d7c57-120">**m\_lpfnNew**</span></span>](cfactorytemplate-m-lpfnnew.md)                          | <span data-ttu-id="d7c57-121">Puntatore a una funzione che crea un'istanza dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d7c57-121">Pointer to a function that creates an instance of the object.</span></span>              |
| [<span data-ttu-id="d7c57-122">**\_lpfnInit m**</span><span class="sxs-lookup"><span data-stu-id="d7c57-122">**m\_lpfnInit**</span></span>](cfactorytemplate-m-lpfninit.md)                        | <span data-ttu-id="d7c57-123">Puntatore a una funzione che viene chiamata dal punto di ingresso della DLL.</span><span class="sxs-lookup"><span data-stu-id="d7c57-123">Pointer to a function that gets called from the DLL entry point.</span></span>           |
| [<span data-ttu-id="d7c57-124">**\_filtro pAMovieSetup \_ m**</span><span class="sxs-lookup"><span data-stu-id="d7c57-124">**m\_pAMovieSetup\_Filter**</span></span>](cfactorytemplate-m-pamoviesetup-filter.md) | <span data-ttu-id="d7c57-125">Puntatore a una struttura di [**\_ filtro AMOVIESETUP**](amoviesetup-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="d7c57-125">Pointer to an [**AMOVIESETUP\_FILTER**](amoviesetup-filter.md) structure.</span></span> |
| <span data-ttu-id="d7c57-126">Metodi pubblici</span><span class="sxs-lookup"><span data-stu-id="d7c57-126">Public Methods</span></span>                                                            | <span data-ttu-id="d7c57-127">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d7c57-127">Description</span></span>                                                                |
| [<span data-ttu-id="d7c57-128">**IsClassID**</span><span class="sxs-lookup"><span data-stu-id="d7c57-128">**IsClassID**</span></span>](cfactorytemplate-isclassid.md)                           | <span data-ttu-id="d7c57-129">Determina se un CLSID corrisponde a questo modello di classe.</span><span class="sxs-lookup"><span data-stu-id="d7c57-129">Determines whether a CLSID matches this class template.</span></span>                    |
| [<span data-ttu-id="d7c57-130">**CreateInstance**</span><span class="sxs-lookup"><span data-stu-id="d7c57-130">**CreateInstance**</span></span>](cfactorytemplate-createinstance.md)                 | <span data-ttu-id="d7c57-131">Chiama la funzione di creazione di oggetti per la classe.</span><span class="sxs-lookup"><span data-stu-id="d7c57-131">Calls the object-creation function for the class.</span></span>                          |



 

## <a name="requirements"></a><span data-ttu-id="d7c57-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d7c57-132">Requirements</span></span>



| <span data-ttu-id="d7c57-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7c57-133">Requirement</span></span> | <span data-ttu-id="d7c57-134">Valore</span><span class="sxs-lookup"><span data-stu-id="d7c57-134">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7c57-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d7c57-135">Header</span></span><br/>  | <dl> <span data-ttu-id="d7c57-136"><dt>ComBase. h (Includi Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d7c57-136"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="d7c57-137">Libreria</span><span class="sxs-lookup"><span data-stu-id="d7c57-137">Library</span></span><br/> | <dl> <span data-ttu-id="d7c57-138"><dt>Strmbase. lib; </dt> <dt>Strmbasd. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d7c57-138"><dt>Strmbase.lib; </dt> <dt>Strmbasd.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7c57-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d7c57-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7c57-140">Riferimento alla classe di base</span><span class="sxs-lookup"><span data-stu-id="d7c57-140">Base Class Reference</span></span>](base-class-reference.md)
</dt> </dl>

 

