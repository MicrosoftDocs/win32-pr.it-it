---
title: Elementi semplici
description: Un elemento semplice è un elemento dell'interfaccia utente che condivide un oggetto IAccessible con altri elementi e si basa su tale oggetto IAccessible, in genere il padre, per esporre le relative proprietà.
ms.assetid: 3f6bd992-4e0a-4dba-b6e9-e70dca77c880
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8f8cb00b19719a4a8779a61f37b079633ada40c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298863"
---
# <a name="simple-elements"></a>Elementi semplici

Un *elemento semplice* è un elemento dell'interfaccia utente che condivide un oggetto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) con altri elementi e si basa su tale oggetto **IAccessible** , in genere il padre, per esporre le relative proprietà. Per distinguere tra gli elementi che condividono un oggetto **IAccessible** , il server assegna un identificatore figlio univoco positivo a ogni elemento semplice. Questa assegnazione viene eseguita per ogni singola istanza, quindi gli ID devono essere univoci all'interno di tale contesto. Molte implementazioni assegnano questi ID in sequenza, a partire da 1. Questo schema non consente agli elementi semplici di avere elementi figlio. Gli elementi semplici sono noti anche come *figli*.

Per essere identificato ed esposto in modo univoco, un elemento semplice richiede un oggetto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) e un ID figlio. Pertanto, quando si comunica con un oggetto **IAccessible** , i client devono fornire l'ID figlio appropriato. Un identificatore speciale, **CHILDID \_ self**, può essere usato per fare riferimento all'oggetto accessibile, anziché a uno dei relativi elementi figlio.

L'oggetto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) condiviso tra gli elementi semplici corrisponde spesso a un oggetto padre comune nell'interfaccia utente. Ad esempio, le caselle di riepilogo sistema espongono un oggetto accessibile per la casella di riepilogo complessiva e gli elementi semplici per ogni elemento casella di riepilogo. In questo caso, l'oggetto **IAccessible** per la casella di riepilogo è anche il padre o il contenitore degli elementi dell'elenco.

Per ulteriori informazioni sugli oggetti accessibili, vedere [oggetti accessibili](accessible-objects.md).

 

 




