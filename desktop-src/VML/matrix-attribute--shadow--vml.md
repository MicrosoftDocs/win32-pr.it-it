---
title: Attributo Matrix (Shadow) (la)
description: Attributo Matrix (Shadow) (la)
ms.assetid: 29bebd2f-7f66-4883-8c12-57fef4a0ac9e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d599aa817e87481aefdec43dbe345b7235fc54bd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399631"
---
# <a name="matrix-attribute-shadowvml"></a><span data-ttu-id="ea84b-103">Attributo Matrix (Shadow) (la)</span><span class="sxs-lookup"><span data-stu-id="ea84b-103">Matrix Attribute (Shadow)(VML)</span></span>

<span data-ttu-id="ea84b-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="ea84b-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="ea84b-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="ea84b-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="ea84b-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="ea84b-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="ea84b-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="ea84b-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="ea84b-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="ea84b-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="ea84b-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="ea84b-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="ea84b-110">Definisce una trasformazione della prospettiva per un'ombreggiatura.</span><span class="sxs-lookup"><span data-stu-id="ea84b-110">Defines a perspective transform for a shadow.</span></span> <span data-ttu-id="ea84b-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="ea84b-111">Read/write.</span></span> <span data-ttu-id="ea84b-112">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="ea84b-112">**String**.</span></span>

<span data-ttu-id="ea84b-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="ea84b-113">**Applies To**</span></span>

[<span data-ttu-id="ea84b-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="ea84b-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="ea84b-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="ea84b-115">**Tag Syntax**</span></span>

<span data-ttu-id="ea84b-116"><v: *element* Matrix = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="ea84b-116"><v: *element* matrix=" *expression* "></span></span>

<span data-ttu-id="ea84b-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="ea84b-117">**Script Syntax**</span></span>

<span data-ttu-id="ea84b-118">*element* . Matrix = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="ea84b-118">*element* .matrix="*expression*"</span></span>

<span data-ttu-id="ea84b-119">*espressione* = *element*. Matrix</span><span class="sxs-lookup"><span data-stu-id="ea84b-119">*expression*=*element*.matrix</span></span>

<span data-ttu-id="ea84b-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="ea84b-120">**Remarks**</span></span>

<span data-ttu-id="ea84b-121">Una matrice di trasformazione prospettica nel formato "SXX, SXY, SYX, SYY, px, py" WHERE s = scale e p = Perspective.</span><span class="sxs-lookup"><span data-stu-id="ea84b-121">A perspective transform matrix in the form "sxx,sxy,syx,syy,px,py" where s= scale and p = perspective.</span></span> <span data-ttu-id="ea84b-122">Se l'offset è in unità assolute, il px, py si trova in unità di 1/Emu; in caso contrario, si tratta di una frazione inversa della dimensione della forma.</span><span class="sxs-lookup"><span data-stu-id="ea84b-122">If offset is in absolute units then px, py are in 1/emu units; otherwise they are an inverse fraction of the shape size.</span></span>

<span data-ttu-id="ea84b-123">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="ea84b-123">*VML Standard Attribute*</span></span>

 

 