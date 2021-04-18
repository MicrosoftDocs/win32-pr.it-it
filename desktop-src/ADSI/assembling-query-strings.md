---
title: Assemblaggio di stringhe di query
description: In Active Directory, l'uso di criteri di filtro specifici può migliorare le prestazioni di ricerca. Ciò è dovuto al fatto che Active Directory valuta tutti i predicati, identifica gli indici e quindi seleziona un indice con la probabilità di ottenere il set più piccolo di valori restituiti.
ms.assetid: 4139eedb-1383-4654-9b40-5e294a71be24
ms.tgt_platform: multiple
keywords:
- Assemblaggio di stringhe di query ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e56dec34f63a4a3e12385a36ad5fe5339a0f3d9c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297697"
---
# <a name="assembling-query-strings"></a>Assemblaggio di stringhe di query

In Active Directory, l'uso di criteri di filtro specifici può migliorare le prestazioni di ricerca. Ciò è dovuto al fatto che Active Directory valuta tutti i predicati, identifica gli indici e quindi seleziona un indice con la probabilità di ottenere il set più piccolo di valori restituiti.

Evitare la ricerca di testo al centro o alla fine di una stringa, ad esempio "CN = \* Hille \* " o "CN = \* Larouse".

Quando possibile, cercare gli attributi indicizzati. Gli attributi indicizzati vengono archiviati in tutti i controller di dominio, pertanto la query sarà probabilmente più veloce rispetto alla ricerca di un attributo non indicizzato.

 

 




