---
description: Un'applicazione riempie l'area interna di un'area chiamando la funzione FillRgn e fornendo un handle che identifica un pennello specifico.
ms.assetid: 6174b2ea-836a-4538-a0ad-e123c88fc6f6
title: Aree di riempimento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62709869f5f25a6cde11812844efdab6162b1e9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049724"
---
# <a name="filling-regions"></a><span data-ttu-id="827b1-103">Aree di riempimento</span><span class="sxs-lookup"><span data-stu-id="827b1-103">Filling Regions</span></span>

<span data-ttu-id="827b1-104">Un'applicazione riempie l'area interna di un'area chiamando la funzione [**FillRgn**](/windows/desktop/api/Wingdi/nf-wingdi-fillrgn) e fornendo un handle che identifica un pennello specifico.</span><span class="sxs-lookup"><span data-stu-id="827b1-104">An application fills the interior of a region by calling the [**FillRgn**](/windows/desktop/api/Wingdi/nf-wingdi-fillrgn) function and supplying a handle that identifies a specific brush.</span></span> <span data-ttu-id="827b1-105">Quando un'applicazione chiama FillRgn, il sistema riempie l'area con il pennello usando la modalità di riempimento corrente per il contesto di dispositivo specificato.</span><span class="sxs-lookup"><span data-stu-id="827b1-105">When an application calls FillRgn , the system fills the region with the brush by using the current fill mode for the specified device context.</span></span> <span data-ttu-id="827b1-106">Sono disponibili due modalità di riempimento: alternativa e avvolgimento.</span><span class="sxs-lookup"><span data-stu-id="827b1-106">There are two fill modes: alternate and winding.</span></span> <span data-ttu-id="827b1-107">L'applicazione può impostare la modalità di riempimento per un contesto di dispositivo chiamando la funzione [**SetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode) .</span><span class="sxs-lookup"><span data-stu-id="827b1-107">The application can set the fill mode for a device context by calling the [**SetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode) function.</span></span> <span data-ttu-id="827b1-108">L'applicazione può recuperare la modalità di riempimento corrente per un contesto di dispositivo chiamando la funzione [**GetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-getpolyfillmode) .</span><span class="sxs-lookup"><span data-stu-id="827b1-108">The application can retrieve the current fill mode for a device context by calling the [**GetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-getpolyfillmode) function.</span></span>

<span data-ttu-id="827b1-109">Nella figura seguente sono illustrate due aree identiche: una riempita usando la modalità alternativa e l'altra riempita usando la modalità di avvolgimento.</span><span class="sxs-lookup"><span data-stu-id="827b1-109">The following illustration shows two identical regions: one filled using alternate mode and the other filled using winding mode.</span></span>

![illustrazione che mostra le stelle a 2 5 punte: una riempita solo nei punti, l'altra riempita completamente](images/csrgn-03.png)

## <a name="alternate-mode"></a><span data-ttu-id="827b1-111">Modalità alternativa</span><span class="sxs-lookup"><span data-stu-id="827b1-111">Alternate Mode</span></span>

<span data-ttu-id="827b1-112">Per determinare i pixel evidenziati dal sistema quando si specifica la modalità alternativa, eseguire il test seguente:</span><span class="sxs-lookup"><span data-stu-id="827b1-112">To determine which pixels the system highlights when alternate mode is specified, perform the following test:</span></span>

1.  <span data-ttu-id="827b1-113">Selezionare un pixel all'interno dell'area interna.</span><span class="sxs-lookup"><span data-stu-id="827b1-113">Select a pixel within the region's interior.</span></span>
2.  <span data-ttu-id="827b1-114">Creare un raggio immaginario, nella direzione x positiva, dal pixel verso l'infinito.</span><span class="sxs-lookup"><span data-stu-id="827b1-114">Draw an imaginary ray, in the positive x-direction, from that pixel toward infinity.</span></span>
3.  <span data-ttu-id="827b1-115">Ogni volta che il raggio interseca una linea di limite, incrementare un valore di conteggio.</span><span class="sxs-lookup"><span data-stu-id="827b1-115">Each time the ray intersects a boundary line, increment a count value.</span></span>

<span data-ttu-id="827b1-116">Il sistema evidenzia il pixel se il valore del conteggio è un numero dispari.</span><span class="sxs-lookup"><span data-stu-id="827b1-116">The system highlights the pixel if the count value is an odd number.</span></span>

## <a name="winding-mode"></a><span data-ttu-id="827b1-117">Modalità di avvolgimento</span><span class="sxs-lookup"><span data-stu-id="827b1-117">Winding Mode</span></span>

<span data-ttu-id="827b1-118">Per determinare i pixel evidenziati dal sistema quando si specifica la modalità di rimozione, eseguire il test seguente:</span><span class="sxs-lookup"><span data-stu-id="827b1-118">To determine which pixels the system highlights when winding mode is specified, perform the following test:</span></span>

1.  <span data-ttu-id="827b1-119">Determinare la direzione in cui ogni linea di limite viene disegnata.</span><span class="sxs-lookup"><span data-stu-id="827b1-119">Determine the direction in which each boundary line is drawn.</span></span>
2.  <span data-ttu-id="827b1-120">Selezionare un pixel all'interno dell'area interna.</span><span class="sxs-lookup"><span data-stu-id="827b1-120">Select a pixel within the region's interior.</span></span>
3.  <span data-ttu-id="827b1-121">Creare un raggio immaginario, nella direzione x positiva, dal pixel verso l'infinito.</span><span class="sxs-lookup"><span data-stu-id="827b1-121">Draw an imaginary ray, in the positive x-direction, from the pixel toward infinity.</span></span>
4.  <span data-ttu-id="827b1-122">Ogni volta che il raggio interseca una linea di limite con un componente y positivo, incrementa un valore di conteggio.</span><span class="sxs-lookup"><span data-stu-id="827b1-122">Each time the ray intersects a boundary line with a positive y-component, increment a count value.</span></span> <span data-ttu-id="827b1-123">Ogni volta che il raggio interseca una linea di limite con un componente y negativo, decrementa il valore del conteggio.</span><span class="sxs-lookup"><span data-stu-id="827b1-123">Each time the ray intersects a boundary line with a negative y-component, decrement the count value.</span></span>

<span data-ttu-id="827b1-124">Il sistema evidenzia il pixel se il valore del conteggio è diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="827b1-124">The system highlights the pixel if the count value is nonzero.</span></span>

 

 



