---
description: Il modello CMSPArray implementa una Smart Array che aumenterà su richiesta.
ms.assetid: 9b30885c-01a4-4aea-a1c3-5d7966e4697f
title: CMSPArray
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a6c14d4bdc0b57a295efa5bcc2adfd79d23d31d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967601"
---
# <a name="cmsparray"></a>CMSPArray

Il modello CMSPArray implementa una Smart Array che aumenterà su richiesta. È progettato per mantenere piccole matrici con tipi di dati semplici. Non ha una sezione critica. Le uniche dipendenze sono **realloc** e **memmove**. Viene usato internamente per contenere elenchi di puntatori a oggetti. È simile all'implementazione **CSimpleArray** di ATL, ma è più efficiente per le allocazioni iniziali.

Questo modello è definito in MSPutils. h.

 

 



