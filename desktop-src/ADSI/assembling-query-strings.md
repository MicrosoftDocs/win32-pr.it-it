---
title: Assemblaggio di stringhe di query
description: In Active Directory l'uso di criteri di filtro specifici può migliorare le prestazioni di ricerca. Ciò è dovuto al fatto che Active Directory valuta tutti i predicati, identifica gli indici e quindi seleziona un indice che probabilmente restituirà il set più piccolo di valori restituiti.
ms.assetid: 4139eedb-1383-4654-9b40-5e294a71be24
ms.tgt_platform: multiple
keywords:
- Assemblaggio di stringhe di query ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 610ba78d6536d9cfe12f296fcbfa46d04cd572ae05cdb7d3bb8b0e1e7b5d32a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962200"
---
# <a name="assembling-query-strings"></a>Assemblaggio di stringhe di query

In Active Directory l'uso di criteri di filtro specifici può migliorare le prestazioni di ricerca. Ciò è dovuto al fatto che Active Directory valuta tutti i predicati, identifica gli indici e quindi seleziona un indice che probabilmente restituirà il set più piccolo di valori restituiti.

Evitare la ricerca di testo al centro o alla fine di una stringa, ad esempio "cn= \* \* hille" o "cn= \* larouse".

Quando possibile, cercare gli attributi indicizzati. Gli attributi indicizzati vengono archiviati in tutti i controller di dominio, quindi molto probabilmente la query sarà più veloce rispetto alla ricerca di un attributo non indicizzato.

 

 




