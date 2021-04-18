---
title: Cosa si può sapere e quando è possibile conoscerlo
description: Le applicazioni che sono sensibili agli stati indotti dalla latenza devono riconoscere gli Stati del problema ed eseguire l'azione appropriata.
ms.assetid: d1d0135e-2d67-47dd-82ac-4869203ce85e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e9a8a6c6def8475946ad5faa63615d17742fbcb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297715"
---
# <a name="what-can-you-know-and-when-can-you-know-it"></a>Cosa si può sapere e quando è possibile conoscerlo?

Le applicazioni che sono sensibili agli stati indotti dalla latenza devono riconoscere gli Stati del problema ed eseguire l'azione appropriata. Ci sono due stati di problema: sfasamento della versione e aggiornamento parziale. La distorsione della versione non è rilevabile esaminando il servizio directory (ricordare l'assioma del calcolo distribuito indicato nel [perché Active Directory Domain Services usare questo modello di replica](why-active-directory-domain-services-uses-this-replication-model.md)). L'aggiornamento parziale può essere rilevato aggiungendo metadati agli oggetti che compongono il set correlato. I suggerimenti per tali metadati vengono visualizzati nelle sezioni successive di questo documento. È possibile adottare strategie di prevenzione per ridurre la possibilità di sfasamento della versione e di aggiornamento parziale. Queste strategie vengono inoltre illustrate nelle sezioni successive di questo documento.

 

 




