---
title: Reflection del messaggio
description: Reflection del messaggio
ms.assetid: 26a124d7-6499-4e8f-9001-d2782c1cc290
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96cb563597e5aa92440e1b1434420e983268d9b3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044035"
---
# <a name="message-reflection"></a><span data-ttu-id="60ba2-103">Reflection del messaggio</span><span class="sxs-lookup"><span data-stu-id="60ba2-103">Message Reflection</span></span>

<span data-ttu-id="60ba2-104">Si consiglia vivamente che un contenitore di controlli ActiveX supporti la reflection del messaggio.</span><span class="sxs-lookup"><span data-stu-id="60ba2-104">It is strongly recommended that an ActiveX control container supports message reflection.</span></span> <span data-ttu-id="60ba2-105">Questo comporterà un'operazione più efficiente per i controlli sottoclassati.</span><span class="sxs-lookup"><span data-stu-id="60ba2-105">This will result in more efficient operation for subclassed controls.</span></span> <span data-ttu-id="60ba2-106">Se è supportata la reflection del messaggio, la proprietà di ambiente MessageReflect deve essere supportata e avere un valore **true**.</span><span class="sxs-lookup"><span data-stu-id="60ba2-106">If message reflection is supported, the MessageReflect ambient property must be supported and have a value of **TRUE**.</span></span> <span data-ttu-id="60ba2-107">Se un contenitore non implementa la reflection del messaggio, il CDK OLE crea due finestre per ogni controllo sottoclassato, per fornire la reflection del messaggio per conto del contenitore di controlli.</span><span class="sxs-lookup"><span data-stu-id="60ba2-107">If a container does not implement message reflection, then the OLE CDK creates two windows for every subclassed control, to provide message reflection on behalf on the control container.</span></span>

## <a name="related-topics"></a><span data-ttu-id="60ba2-108">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="60ba2-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60ba2-109">Contenitori</span><span class="sxs-lookup"><span data-stu-id="60ba2-109">Containers</span></span>](containers.md)
</dt> </dl>

 

 




