---
description: Il metodo Render Inizializza il grafico del filtro DVD.
ms.assetid: 910f1e3f-b3bb-498b-93da-3a974a3117e8
title: Metodo Render
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 677abab1c669642c1e51e0041c98949d923147c7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303898"
---
# <a name="render-method"></a><span data-ttu-id="89cd9-103">Metodo Render</span><span class="sxs-lookup"><span data-stu-id="89cd9-103">Render Method</span></span>

> [!Note]  
> <span data-ttu-id="89cd9-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="89cd9-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="89cd9-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="89cd9-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="89cd9-106">Il `Render` metodo inizializza il grafico del filtro DVD.</span><span class="sxs-lookup"><span data-stu-id="89cd9-106">The `Render` method initializes the DVD filter graph.</span></span>

``` syntax
MSWebDVD.Render(iRender = 0)
```

## <a name="parameters"></a><span data-ttu-id="89cd9-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="89cd9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89cd9-108"><span id="iRender"></span><span id="irender"></span><span id="IRENDER"></span>*iRender*</span><span class="sxs-lookup"><span data-stu-id="89cd9-108"><span id="iRender"></span><span id="irender"></span><span id="IRENDER"></span>*iRender*</span></span>
</dt> <dd>

<span data-ttu-id="89cd9-109">Specifica un valore intero che indica se il grafico del filtro verrà eliminato e ricompilato.</span><span class="sxs-lookup"><span data-stu-id="89cd9-109">Specifies an integer value indicating whether the filter graph will be destroyed and rebuilt.</span></span>



| <span data-ttu-id="89cd9-110">Valore</span><span class="sxs-lookup"><span data-stu-id="89cd9-110">Value</span></span> | <span data-ttu-id="89cd9-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="89cd9-111">Description</span></span>                                                                                         |
|-------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89cd9-112">0</span><span class="sxs-lookup"><span data-stu-id="89cd9-112">0</span></span>     | <span data-ttu-id="89cd9-113">Il grafico del filtro non verrà eliminato e ricompilato se esiste già.</span><span class="sxs-lookup"><span data-stu-id="89cd9-113">The filter graph will not be destroyed and rebuilt if it already exists.</span></span> <span data-ttu-id="89cd9-114">Rappresenta il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="89cd9-114">This is the default value.</span></span> |
| <span data-ttu-id="89cd9-115">1</span><span class="sxs-lookup"><span data-stu-id="89cd9-115">1</span></span>     | <span data-ttu-id="89cd9-116">Il grafico del filtro verrà eliminato e ricompilato se esiste già.</span><span class="sxs-lookup"><span data-stu-id="89cd9-116">The filter graph will be destroyed and rebuilt if it already exists.</span></span>                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89cd9-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="89cd9-117">Return Value</span></span>

<span data-ttu-id="89cd9-118">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="89cd9-118">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="89cd9-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="89cd9-119">Remarks</span></span>

<span data-ttu-id="89cd9-120">Il `Render` metodo consente all'oggetto **mswebdvd** di inizializzare completamente il grafo del filtro DirectShow sottostante all'avvio.</span><span class="sxs-lookup"><span data-stu-id="89cd9-120">The `Render` method enables the **MSWebDVD** object to fully initialize the underlying DirectShow filter graph on startup.</span></span> <span data-ttu-id="89cd9-121">In questo modo si elimina il lieve ritardo che altrimenti si verifica quando l'utente rilascia il primo comando per riprodurre un disco o visualizzare un menu.</span><span class="sxs-lookup"><span data-stu-id="89cd9-121">This eliminates the slight delay that otherwise occurs when the user issues the first command to play a disc or show a menu.</span></span> <span data-ttu-id="89cd9-122">Non esistono casi in cui `Render` deve essere chiamato prima di chiamare qualsiasi altro metodo.</span><span class="sxs-lookup"><span data-stu-id="89cd9-122">There is no case in which `Render` needs to be called before calling any other method.</span></span> <span data-ttu-id="89cd9-123">Se, ad esempio, l'applicazione chiama [**PlayTitle**](playtitle-method.md) prima che il grafico di filtro sia stato inizializzato, l'oggetto **mswebdvd** chiama `Render` automaticamente prima di provare a riprodurre il disco.</span><span class="sxs-lookup"><span data-stu-id="89cd9-123">For example, if the application calls [**PlayTitle**](playtitle-method.md) before the filter graph has been initialized, the **MSWebDVD** object calls `Render` automatically before attempting to play the disc.</span></span>

 

 



