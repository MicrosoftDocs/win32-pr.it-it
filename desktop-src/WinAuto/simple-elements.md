---
title: Elementi semplici
description: Un elemento semplice è un elemento dell'interfaccia utente che condivide un oggetto IAccessible con altri elementi e si basa su tale oggetto IAccessible (in genere l'elemento padre) per esporre le relative proprietà.
ms.assetid: 3f6bd992-4e0a-4dba-b6e9-e70dca77c880
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9676b8bf4198f8be753b3788fcc6defdec2d6a1d8ad3ff3fed2f41da4f256554
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133644"
---
# <a name="simple-elements"></a>Elementi semplici

Un *elemento semplice è* un elemento dell'interfaccia utente che condivide un oggetto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) con altri elementi e si basa su tale **oggetto IAccessible** (in genere l'elemento padre) per esporre le relative proprietà. Per distinguere tra gli elementi che condividono **un oggetto IAccessible,** il server assegna un identificatore figlio positivo univoco a ogni elemento semplice. Questa assegnazione viene eseguita in base all'istanza dell'interfaccia, quindi gli ID devono essere univoci all'interno di tale contesto. Molte implementazioni assegnano questi ID in sequenza, a partire da 1. Questo schema non consente agli elementi semplici di avere elementi figlio propri. Gli elementi semplici sono noti anche come *elementi figlio.*

Per essere identificato ed esposto in modo univoco, un elemento semplice richiede un [**oggetto IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) e un ID figlio. Pertanto, quando comunicano con un **oggetto IAccessible,** i client devono fornire l'ID figlio appropriato. Un identificatore speciale, **CHILDID \_ SELF,** può essere usato per fare riferimento all'oggetto accessibile stesso, anziché a uno dei relativi elementi figlio.

[**L'oggetto IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) condiviso tra elementi semplici spesso corrisponde a un oggetto padre comune nell'interfaccia utente. Ad esempio, le caselle di riepilogo di sistema espongono un oggetto accessibile per la casella di riepilogo complessiva e gli elementi semplici per ogni elemento della casella di riepilogo. In questo caso, **l'oggetto IAccessible** per la casella di riepilogo è anche l'elemento padre o il contenitore degli elementi dell'elenco.

Per altre informazioni sugli oggetti accessibili, vedere [Oggetti accessibili.](accessible-objects.md)

 

 




