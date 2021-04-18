---
description: Anche se non è possibile accedere a un&\# 160; contesto di riconoscimento&\# 160; su due thread contemporaneamente dalla piattaforma Tablet PC, la funzione AdviseInkChange può essere chiamata in qualsiasi momento in qualsiasi thread.
ms.assetid: 2cd19819-08d0-418d-830b-2288a66ca0d0
title: Considerazioni sul threading del riconoscimento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4297cc28e084bbb7c1c09593deb5babc2319ab43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315555"
---
# <a name="recognizer-threading-considerations"></a>Considerazioni sul threading del riconoscimento

Sebbene non sia possibile accedere a un [contesto di riconoscimento](hrecocontext-handle.md) su due thread contemporaneamente dalla piattaforma Tablet PC, la funzione [**AdviseInkChange**](/windows/desktop/api/recapis/nf-recapis-adviseinkchange) può essere chiamata in qualsiasi momento in qualsiasi thread. Poiché la piattaforma Tablet PC non garantisce la presenza di un solo contesto di riconoscimento alla volta, due contesti di riconoscimento distinti in thread distinti possono tentare contemporaneamente di accedere al [riconoscimento](hrecognizer-handle.md). Pertanto, le variabili globali nel motore di riconoscimento devono essere thread-safe.

Gli elenchi di parole sono un'implementazione facoltativa usata per aumentare la precisione. Se il riconoscimento implementa elenchi di parole, deve essere thread-safe. Per ulteriori informazioni sull'utilizzo degli elenchi di parole, vedere [utilizzo dei dizionari delle applicazioni](using-application-dictionaries.md).

Per informazioni dettagliate sulle altre considerazioni relative al threading, vedere [considerazioni sul threading di Tablet PC](tablet-pc-threading-considerations.md).

 

 



