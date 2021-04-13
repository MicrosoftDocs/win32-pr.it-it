---
description: Una penna di Tablet PC può avere più di un'estremità che può interagire con il digitalizzatore.
ms.assetid: c1aa0d65-cfea-4720-ad09-7add724e03c7
title: Funzionalità multiple con una penna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8313e6a13cb48900e0c0d31c2e1e590e07df6c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349881"
---
# <a name="multiple-functionality-with-one-pen"></a><span data-ttu-id="ef13a-103">Funzionalità multiple con una penna</span><span class="sxs-lookup"><span data-stu-id="ef13a-103">Multiple Functionality with One Pen</span></span>

<span data-ttu-id="ef13a-104">Una penna di Tablet PC può avere più di un'estremità che può interagire con il digitalizzatore.</span><span class="sxs-lookup"><span data-stu-id="ef13a-104">A Tablet PC pen may have more than one end that can interact with the digitizer.</span></span> <span data-ttu-id="ef13a-105">Se entrambe le estremità della penna possono generare eventi, è possibile usare un'estremità per impostare l'input penna, Select e Point e l'altra estremità per altre funzioni, ad esempio la cancellazione.</span><span class="sxs-lookup"><span data-stu-id="ef13a-105">If both ends of the pen can generate events, one end may be used to lay down ink, select, and point, and the other end may be used for other functions such as erasing.</span></span>

<span data-ttu-id="ef13a-106">Per implementare tale funzionalità, l'applicazione deve essere in grado di determinare quale estremità della penna viene utilizzata e quindi quando modificare l'aspetto del cursore.</span><span class="sxs-lookup"><span data-stu-id="ef13a-106">To implement such functionality, your application must be able to determine which end of the pen is being used and hence when to change the appearance of the cursor.</span></span> <span data-ttu-id="ef13a-107">Questa operazione può essere eseguita cercando lo stato della proprietà [**invertita**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_inverted) sull'oggetto [**cursore**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) .</span><span class="sxs-lookup"><span data-stu-id="ef13a-107">It can do this by looking for the state of the [**Inverted**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_inverted) property on the [**Cursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object.</span></span>

<span data-ttu-id="ef13a-108">Per informazioni dettagliate sull'uso del retro della penna per la cancellazione, vedere [cancellazione dell'input penna con la penna](erasing-ink-with-the-pen.md).</span><span class="sxs-lookup"><span data-stu-id="ef13a-108">For specific details about using the back of the pen for erasing, see [Erasing Ink with the Pen](erasing-ink-with-the-pen.md).</span></span> <span data-ttu-id="ef13a-109">Inoltre, nell' [esempio di cancellazione dell'input](ink-erasing-sample.md) penna viene illustrato come utilizzare il retro della penna per cancellare l'input penna.</span><span class="sxs-lookup"><span data-stu-id="ef13a-109">In addition, the [Ink Erasing Sample](ink-erasing-sample.md) demonstrates how to use the back of the pen to erase ink.</span></span>

 

 



