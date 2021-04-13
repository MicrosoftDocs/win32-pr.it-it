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
# <a name="multiple-functionality-with-one-pen"></a>Funzionalità multiple con una penna

Una penna di Tablet PC può avere più di un'estremità che può interagire con il digitalizzatore. Se entrambe le estremità della penna possono generare eventi, è possibile usare un'estremità per impostare l'input penna, Select e Point e l'altra estremità per altre funzioni, ad esempio la cancellazione.

Per implementare tale funzionalità, l'applicazione deve essere in grado di determinare quale estremità della penna viene utilizzata e quindi quando modificare l'aspetto del cursore. Questa operazione può essere eseguita cercando lo stato della proprietà [**invertita**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_inverted) sull'oggetto [**cursore**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) .

Per informazioni dettagliate sull'uso del retro della penna per la cancellazione, vedere [cancellazione dell'input penna con la penna](erasing-ink-with-the-pen.md). Inoltre, nell' [esempio di cancellazione dell'input](ink-erasing-sample.md) penna viene illustrato come utilizzare il retro della penna per cancellare l'input penna.

 

 



