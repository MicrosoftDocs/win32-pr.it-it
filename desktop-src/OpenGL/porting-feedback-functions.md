---
title: Porting di funzioni di feedback
description: Con IRIS GL, il modo in cui viene gestito il feedback varia a seconda del computer che esegue IRIS GL.
ms.assetid: 170a3eae-5e0e-47f5-80dc-f8db5af98f76
keywords:
- Porting di IRIS GL, commenti e suggerimenti
- porting da IRIS GL, commenti e suggerimenti
- porting in OpenGL da IRIS GL, commenti e suggerimenti
- Porting OpenGL da IRIS GL, commenti e suggerimenti
- feedback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a04bcfe2c1d914a178ad7ad0dca95fb85d86bbc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221823"
---
# <a name="porting-feedback-functions"></a><span data-ttu-id="a073b-108">Porting di funzioni di feedback</span><span class="sxs-lookup"><span data-stu-id="a073b-108">Porting Feedback Functions</span></span>

<span data-ttu-id="a073b-109">Con IRIS GL, il modo in cui viene gestito il feedback varia a seconda del computer che esegue IRIS GL.</span><span class="sxs-lookup"><span data-stu-id="a073b-109">With IRIS GL, the way that feedback is handled differs depending on the computer running IRIS GL.</span></span> <span data-ttu-id="a073b-110">OpenGL standardizza le funzioni di feedback per poter contare su feedback coerenti tra varie piattaforme hardware.</span><span class="sxs-lookup"><span data-stu-id="a073b-110">OpenGL standardizes feedback functions so you can rely on consistent feedback among various hardware platforms.</span></span> <span data-ttu-id="a073b-111">La tabella seguente elenca le funzioni di feedback di IRIS GL e le relative funzioni OpenGL equivalenti.</span><span class="sxs-lookup"><span data-stu-id="a073b-111">The following table lists the IRIS GL feedback functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="a073b-112">Funzione IRIS GL</span><span class="sxs-lookup"><span data-stu-id="a073b-112">IRIS GL function</span></span> | <span data-ttu-id="a073b-113">OpenGL (funzione)</span><span class="sxs-lookup"><span data-stu-id="a073b-113">OpenGL function</span></span>                                                                                            | <span data-ttu-id="a073b-114">Significato</span><span class="sxs-lookup"><span data-stu-id="a073b-114">Meaning</span></span>                                       |
|------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span data-ttu-id="a073b-115">**feedback**</span><span class="sxs-lookup"><span data-stu-id="a073b-115">**feedback**</span></span>     | <span data-ttu-id="a073b-116">[**glRenderMode**](glrendermode.md) ( \_ feedback GL)</span><span class="sxs-lookup"><span data-stu-id="a073b-116">[**glRenderMode**](glrendermode.md) ( GL\_FEEDBACK )</span></span>                                                      | <span data-ttu-id="a073b-117">Passa alla modalità di feedback.</span><span class="sxs-lookup"><span data-stu-id="a073b-117">Switches to feedback mode.</span></span>                    |
| <span data-ttu-id="a073b-118">**endfeedback**</span><span class="sxs-lookup"><span data-stu-id="a073b-118">**endfeedback**</span></span>  | <span data-ttu-id="a073b-119">[**glRenderMode**](glrendermode.md) ( \_ rendering GL)[**glFeedbackBuffer**](glfeedbackbuffer.md)</span><span class="sxs-lookup"><span data-stu-id="a073b-119">[**glRenderMode**](glrendermode.md) ( GL\_RENDER )[**glFeedbackBuffer**](glfeedbackbuffer.md)</span></span><br/> | <span data-ttu-id="a073b-120">Passa alla modalità di rendering.</span><span class="sxs-lookup"><span data-stu-id="a073b-120">Switches to rendering mode.</span></span>                   |
| <span data-ttu-id="a073b-121">**pass-through**</span><span class="sxs-lookup"><span data-stu-id="a073b-121">**passthrough**</span></span>  | [<span data-ttu-id="a073b-122">**glPassThrough**</span><span class="sxs-lookup"><span data-stu-id="a073b-122">**glPassThrough**</span></span>](glpassthrough.md)                                                                     | <span data-ttu-id="a073b-123">Inserisce un marcatore del token nel buffer di feedback.</span><span class="sxs-lookup"><span data-stu-id="a073b-123">Places a token marker in the feedback buffer.</span></span> |



 

 

 





