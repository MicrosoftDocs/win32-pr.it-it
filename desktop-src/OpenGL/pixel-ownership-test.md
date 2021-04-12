---
title: Test di proprietà pixel
description: Il test di proprietà del pixel determina se il contesto OpenGL corrente è proprietario del pixel nel framebuffer corrispondente a un frammento specifico.
ms.assetid: aa9428a6-cc05-4df4-ba31-444f999006a8
keywords:
- Pipeline di elaborazione OpenGL, test di proprietà pixel
- test di proprietà pixel OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85ad5ae57dbbff9f3551ecc222cd0a628193c97f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330591"
---
# <a name="pixel-ownership-test"></a><span data-ttu-id="d1768-105">Test di proprietà pixel</span><span class="sxs-lookup"><span data-stu-id="d1768-105">Pixel Ownership Test</span></span>

<span data-ttu-id="d1768-106">Il test di proprietà del pixel determina se il contesto OpenGL corrente è proprietario del pixel nel framebuffer corrispondente a un frammento specifico.</span><span class="sxs-lookup"><span data-stu-id="d1768-106">The pixel ownership test determines whether the current OpenGL context owns the pixel in the framebuffer corresponding to a particular fragment.</span></span> <span data-ttu-id="d1768-107">In tal caso, il frammento procede al test successivo.</span><span class="sxs-lookup"><span data-stu-id="d1768-107">If so, the fragment proceeds to the next test.</span></span> <span data-ttu-id="d1768-108">In caso contrario, il sistema di Windows determina se il frammento viene eliminato o se verranno eseguite altre operazioni di frammento con tale frammento.</span><span class="sxs-lookup"><span data-stu-id="d1768-108">If not, the window system determines whether the fragment is discarded or whether any further fragment operations will be performed with that fragment.</span></span> <span data-ttu-id="d1768-109">Con questo test, il sistema finestra Controlla il comportamento quando, ad esempio, una finestra OpenGL viene nascosta.</span><span class="sxs-lookup"><span data-stu-id="d1768-109">With this test, the window system controls behavior when, for example, an OpenGL window is obscured.</span></span>

 

 




