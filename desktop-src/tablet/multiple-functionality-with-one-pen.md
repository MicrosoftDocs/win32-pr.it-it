---
description: Una penna tablet PC può avere più estremità che possono interagire con il digitalizzatore.
ms.assetid: c1aa0d65-cfea-4720-ad09-7add724e03c7
title: Funzionalità multiple con una sola penna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22cbba4c95ef215b8ae1e0c94cbe1d43eaceb966fd775284c57a365bbba2f7fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449672"
---
# <a name="multiple-functionality-with-one-pen"></a>Funzionalità multiple con una sola penna

Una penna tablet PC può avere più estremità che possono interagire con il digitalizzatore. Se entrambe le estremità della penna possono generare eventi, è possibile usare un'estremità per posizionare l'input penna, selezionare e puntare e l'altra estremità può essere usata per altre funzioni, ad esempio la cancellazione.

Per implementare questa funzionalità, l'applicazione deve essere in grado di determinare quale estremità della penna viene usata e quindi quando modificare l'aspetto del cursore. A tale scopo, cercare lo stato della proprietà [**Inverted**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_inverted) [**nell'oggetto Cursor.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)

Per informazioni dettagliate specifiche sull'uso della parte posteriore della penna per la cancellazione, vedere [Cancellazione dell'input penna con la penna](erasing-ink-with-the-pen.md). Inoltre, [l'esempio di cancellazione dell'input penna](ink-erasing-sample.md) illustra come usare la parte posteriore della penna per cancellare l'input penna.

 

 



