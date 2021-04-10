---
description: Gli handle opachi vengono usati in TSPI per fare riferimento alle strutture di dati che rappresentano linee, telefoni e aspetto delle chiamate.
ms.assetid: aa1742aa-6cd4-461a-ad92-972eefcf637f
title: Handle opachi e strutture di dati private
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2cd8c7b911de5f85f84b56a8e25e28eb805c5bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966855"
---
# <a name="opaque-handles-and-private-data-structures"></a><span data-ttu-id="ac7d1-103">Handle opachi e strutture di dati private</span><span class="sxs-lookup"><span data-stu-id="ac7d1-103">Opaque Handles and Private Data Structures</span></span>

<span data-ttu-id="ac7d1-104">Gli handle opachi vengono usati in TSPI per fare riferimento alle strutture di dati che rappresentano linee, telefoni e aspetto delle chiamate.</span><span class="sxs-lookup"><span data-stu-id="ac7d1-104">Opaque handles are used in TSPI to refer to the data structures representing lines, phones, and call appearances.</span></span> <span data-ttu-id="ac7d1-105">Questi vengono visualizzati come parametri per la maggior parte delle funzioni e dei callback.</span><span class="sxs-lookup"><span data-stu-id="ac7d1-105">These appear as parameters to most of the functions and callbacks.</span></span> <span data-ttu-id="ac7d1-106">Sono disponibili poche funzioni che fanno riferimento al dispositivo usando un identificatore di dispositivo anziché un handle opaco.</span><span class="sxs-lookup"><span data-stu-id="ac7d1-106">There are few functions that refer to the device using a device identifier instead of an opaque handle.</span></span> <span data-ttu-id="ac7d1-107">In tal caso, il riferimento è al dispositivo stesso piuttosto che a una struttura di dati.</span><span class="sxs-lookup"><span data-stu-id="ac7d1-107">In such a case, the reference is to the device itself rather than to a data structure.</span></span> <span data-ttu-id="ac7d1-108">Le funzioni che funzionano in questo modo sono in genere quelle chiamate in fase di inizializzazione anticipata prima della creazione di strutture di dati e lo scambio di handle opachi.</span><span class="sxs-lookup"><span data-stu-id="ac7d1-108">Functions that work in this fashion are typically those called at early initialization times before data structures are created and opaque handles are exchanged.</span></span>

<span data-ttu-id="ac7d1-109">Il provider di servizi deve decidere come interpretare questi handle.</span><span class="sxs-lookup"><span data-stu-id="ac7d1-109">The service provider must decide how to interpret these handles.</span></span> <span data-ttu-id="ac7d1-110">Un provider di servizi utilizza in genere il puntatore alla relativa struttura di dati o all'indice in una matrice di strutture di dati come handle opaco.</span><span class="sxs-lookup"><span data-stu-id="ac7d1-110">A service provider typically uses the pointer to its data structure or to the index into an array of data structures as its opaque handle.</span></span> <span data-ttu-id="ac7d1-111">L'unica restrizione è che il provider di servizi non può usare il valore 0 come [HDRVLINE](hdrvline.md), HDRVCALL o [HDRVPHONE](hdrvphone.md).</span><span class="sxs-lookup"><span data-stu-id="ac7d1-111">The only restriction is that the service provider cannot use the value 0 as an [HDRVLINE](hdrvline.md), HDRVCALL, or [HDRVPHONE](hdrvphone.md).</span></span> <span data-ttu-id="ac7d1-112">Il valore 0 o **null** per un handle ha un significato speciale in alcune operazioni.</span><span class="sxs-lookup"><span data-stu-id="ac7d1-112">The value 0 or **NULL** for a handle has a special meaning in some operations.</span></span>

 

 



