---
title: Controllo grafico OpenGL
description: Controllo grafico OpenGL
ms.assetid: 327f2920-1bc9-4de7-aa12-3e9f74a94759
keywords:
- OpenGL, controllo grafico
- controllo grafico OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6bb138a2d8c597fae2d92a1d1394c8ff05b03cf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710600"
---
# <a name="opengl-graphic-control"></a><span data-ttu-id="ec307-105">Controllo grafico OpenGL</span><span class="sxs-lookup"><span data-stu-id="ec307-105">OpenGL Graphic Control</span></span>

<span data-ttu-id="ec307-106">OpenGL offre un controllo piuttosto diretto sulle operazioni fondamentali di grafica bidimensionale e tridimensionale.</span><span class="sxs-lookup"><span data-stu-id="ec307-106">OpenGL provides you with fairly direct control over the fundamental operations of two- and three-dimensional graphics.</span></span> <span data-ttu-id="ec307-107">Ciò include la specifica di tali parametri come matrici di trasformazione, coefficienti di equazione di illuminazione, metodi di anti-aliasing e operatori di aggiornamento dei pixel.</span><span class="sxs-lookup"><span data-stu-id="ec307-107">This includes specification of such parameters as transformation matrices, lighting equation coefficients, antialiasing methods, and pixel-update operators.</span></span> <span data-ttu-id="ec307-108">Tuttavia, non fornisce un mezzo per descrivere o modellare oggetti geometrici complessi.</span><span class="sxs-lookup"><span data-stu-id="ec307-108">However, it doesn't provide you with a means for describing or modeling complex geometric objects.</span></span> <span data-ttu-id="ec307-109">Di conseguenza, i comandi OpenGL da emettere specificano il modo in cui deve essere generato un determinato risultato (quale procedura deve essere seguita), anziché esattamente il risultato.</span><span class="sxs-lookup"><span data-stu-id="ec307-109">Thus, the OpenGL commands you issue specify how a certain result should be produced (what procedure should be followed) rather than what exactly that result should look like.</span></span> <span data-ttu-id="ec307-110">Ovvero OpenGL è fondamentalmente procedurale anziché descrittivo.</span><span class="sxs-lookup"><span data-stu-id="ec307-110">That is, OpenGL is fundamentally procedural rather than descriptive.</span></span> <span data-ttu-id="ec307-111">Per comprendere completamente come usare OpenGL, è utile conoscere l'ordine in cui vengono eseguite le operazioni.</span><span class="sxs-lookup"><span data-stu-id="ec307-111">To fully understand how to use OpenGL, it helps to know the order in which it carries out its operations.</span></span>

 

 




