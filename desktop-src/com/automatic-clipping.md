---
title: Ritaglio automatico
description: Ritaglio automatico
ms.assetid: 9107ee47-52aa-48c8-b141-c821f93fda45
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71fb39f3a9f15ed6e1e96493ed2cbdd62db40403
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331271"
---
# <a name="automatic-clipping"></a><span data-ttu-id="61ee5-103">Ritaglio automatico</span><span class="sxs-lookup"><span data-stu-id="61ee5-103">Automatic Clipping</span></span>

<span data-ttu-id="61ee5-104">Si consiglia vivamente che un contenitore di controlli ActiveX supporti il ritaglio automatico dei controlli.</span><span class="sxs-lookup"><span data-stu-id="61ee5-104">It is strongly recommended that an ActiveX control container supports automatic clipping of its controls.</span></span> <span data-ttu-id="61ee5-105">Questa operazione comporterà una maggiore efficienza per la maggior parte dei controlli.</span><span class="sxs-lookup"><span data-stu-id="61ee5-105">This will result in more efficient operation for most controls.</span></span> <span data-ttu-id="61ee5-106">Se il ritaglio automatico è supportato, la proprietà di ambiente AutoClip deve essere supportata e avere un valore **true**.</span><span class="sxs-lookup"><span data-stu-id="61ee5-106">If automatic clipping is supported, the AutoClip ambient property must be supported and have a value of **TRUE**.</span></span>

<span data-ttu-id="61ee5-107">Il ritaglio automatico è la capacità di un contenitore di garantire che l'output disegnato di un controllo venga inserito solo nell'area di visualizzazione corrente del contenitore.</span><span class="sxs-lookup"><span data-stu-id="61ee5-107">Automatic clipping is the ability of a container to ensure that a control's drawn output goes only to the container's current clipping region.</span></span> <span data-ttu-id="61ee5-108">In un contenitore che supporta il ritaglio automatico, un controllo può disegnare senza considerare l'area di ritaglio, perché il contenitore ridurrà automaticamente qualsiasi disegno che si verifica all'esterno dell'area del controllo.</span><span class="sxs-lookup"><span data-stu-id="61ee5-108">In a container that supports automatic clipping, a control can paint without regard to its clipping region, because the container will automatically clip any painting that occurs outside the control's area.</span></span> <span data-ttu-id="61ee5-109">Se un contenitore non supporta il ritaglio automatico, i controlli generati da CDK creerà una finestra padre aggiuntiva se viene passata un'area di ridimensionamento non null.</span><span class="sxs-lookup"><span data-stu-id="61ee5-109">If a container does not support automatic clipping, then CDK-generated controls will create an extra parent window if a non-null clipping region is passed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="61ee5-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="61ee5-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61ee5-111">Contenitori</span><span class="sxs-lookup"><span data-stu-id="61ee5-111">Containers</span></span>](containers.md)
</dt> </dl>

 

 




