---
title: Commenti e suggerimenti
description: In modalità di feedback, ogni primitiva da rasterizzare genera un blocco di valori copiati nella matrice di commenti.
ms.assetid: 92f14fe2-71f7-4b59-94a5-9669e986fb30
keywords:
- modalità feedback, OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af46ecbef5c371c4c4344cb480ef77f4fcc6a7d3
ms.sourcegitcommit: 628fda3e63fd1d513ce9a5f55be8bbc4af4b2a4b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320837"
---
# <a name="feedback-mode"></a><span data-ttu-id="5429e-104">Modalità feedback</span><span class="sxs-lookup"><span data-stu-id="5429e-104">Feedback mode</span></span>

<span data-ttu-id="5429e-105">In modalità di feedback, ogni primitiva da rasterizzare genera un blocco di valori copiati nella matrice di commenti.</span><span class="sxs-lookup"><span data-stu-id="5429e-105">In feedback mode, each primitive to be rasterized generates a block of values that is copied into the feedback array.</span></span> <span data-ttu-id="5429e-106">Specificare questa matrice con [**glFeedbackBuffer**](glfeedbackbuffer.md), che è necessario chiamare prima di inserire OpenGL in modalità feedback.</span><span class="sxs-lookup"><span data-stu-id="5429e-106">Supply this array with [**glFeedbackBuffer**](glfeedbackbuffer.md), which you must call before putting OpenGL into feedback mode.</span></span> <span data-ttu-id="5429e-107">Ogni blocco di valori inizia con un codice che indica il tipo primitivo, seguito da valori che descrivono i vertici della primitiva e i dati associati.</span><span class="sxs-lookup"><span data-stu-id="5429e-107">Each block of values begins with a code indicating the primitive type, followed by values that describe the primitive's vertices and associated data.</span></span> <span data-ttu-id="5429e-108">Le voci vengono scritte anche per le bitmap e i rettangoli dei pixel.</span><span class="sxs-lookup"><span data-stu-id="5429e-108">Entries are also written for bitmaps and pixel rectangles.</span></span> <span data-ttu-id="5429e-109">Non è garantito che i valori vengano scritti nella matrice di commenti fino a quando non si chiama [**glRenderMode**](glrendermode.md) per portare OpenGL fuori dalla modalità di feedback.</span><span class="sxs-lookup"><span data-stu-id="5429e-109">Values are not guaranteed to be written into the feedback array until you call [**glRenderMode**](glrendermode.md) to take OpenGL out of feedback mode.</span></span> <span data-ttu-id="5429e-110">È possibile utilizzare [**glPassThrough**](glpassthrough.md) per fornire un marcatore restituito in modalità feedback come se fosse una primitiva.</span><span class="sxs-lookup"><span data-stu-id="5429e-110">You can use [**glPassThrough**](glpassthrough.md) to supply a marker that is returned in feedback mode as if it were a primitive.</span></span>

 

 




