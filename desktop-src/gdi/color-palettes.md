---
description: Una tavolozza di colori è una matrice che contiene i valori dei colori che identificano i colori che possono essere visualizzati o disegnati sul dispositivo di output.
ms.assetid: 260c5924-d082-4ed2-a8ed-b8a3ad1ca1a9
title: Tavolozze dei colori (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db6da2aab08d2b482eb678e8541ec166156b78f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130811"
---
# <a name="color-palettes-windows-gdi"></a><span data-ttu-id="53713-103">Tavolozze dei colori (Windows GDI)</span><span class="sxs-lookup"><span data-stu-id="53713-103">Color Palettes (Windows GDI)</span></span>

<span data-ttu-id="53713-104">Una tavolozza di colori è una matrice che contiene i valori dei colori che identificano i colori che possono essere visualizzati o disegnati sul dispositivo di output.</span><span class="sxs-lookup"><span data-stu-id="53713-104">A color palette is an array that contains color values identifying the colors that can currently be displayed or drawn on the output device.</span></span> <span data-ttu-id="53713-105">Le tavolozze dei colori vengono usate dai dispositivi in grado di generare molti colori ma che possono solo visualizzare o creare un subset di questi in un determinato momento.</span><span class="sxs-lookup"><span data-stu-id="53713-105">Color palettes are used by devices that are capable of generating many colors but that can only display or draw a subset of these at any given time.</span></span> <span data-ttu-id="53713-106">Per tali dispositivi, il sistema gestisce una *tavolozza di sistema* per tenere traccia e gestire i colori correnti del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="53713-106">For such devices, the system maintains a *system palette* to track and manage the current colors of the device.</span></span> <span data-ttu-id="53713-107">Le applicazioni non hanno accesso diretto alla tavolozza di sistema.</span><span class="sxs-lookup"><span data-stu-id="53713-107">Applications do not have direct access to the system palette.</span></span> <span data-ttu-id="53713-108">Al contrario, il sistema associa una tavolozza predefinita a ogni contesto di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="53713-108">Instead, the system associates a default palette with each device context.</span></span> <span data-ttu-id="53713-109">Le applicazioni possono utilizzare i colori della tavolozza predefinita o definire i propri colori creando *tavolozze logiche* e associando loro i singoli contesti di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="53713-109">Applications can use the colors in the default palette or define their own colors by creating *logical palettes* and associating them with individual device contexts.</span></span>

<span data-ttu-id="53713-110">Un'applicazione può determinare se un dispositivo supporta le tavolozze dei colori controllando il \_ bit della tavolozza RC nel valore RasterCaps restituito dalla funzione [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) .</span><span class="sxs-lookup"><span data-stu-id="53713-110">An application can determine whether a device supports color palettes by checking for the RC\_PALETTE bit in the RASTERCAPS value returned by the [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) function.</span></span>

 

 



