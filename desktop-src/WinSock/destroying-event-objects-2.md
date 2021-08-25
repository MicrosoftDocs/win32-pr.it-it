---
description: Uso di WPUCloseEvent per eliminare un oggetto evento (applicazione o provider di servizi) quando l'oggetto evento non è più necessario.
ms.assetid: ad6f7018-3647-4ab8-9a77-d833d18cd4b6
title: Eliminazione di oggetti evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 255413de4b058e01f82db654efd8b27f35bf249f553e26095800ad3938b1ac0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858511"
---
# <a name="destroying-event-objects"></a>Eliminazione di oggetti evento

L'entità che crea un oggetto evento (applicazione o provider di servizi) è responsabile dell'eliminazione dell'oggetto quando non è più necessario. I provider di servizi eseere questa **operazione tramite WPUCloseEvent**.

 

 



