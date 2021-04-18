---
description: I tipi di formato testo dei dati configurabili possono essere stringhe di testo di qualsiasi lunghezza. I valori null incorporati non sono consentiti.
ms.assetid: 71b89f87-43ba-41cd-a969-765d45da4ba4
title: Tipi di formato testo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4a8f05a0804569667a74c52392d322f3fed2818
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319426"
---
# <a name="text-format-types"></a>Tipi di formato testo

I tipi di formato testo dei dati configurabili possono essere stringhe di testo di qualsiasi lunghezza. I valori null incorporati non sono consentiti.

Sono disponibili i seguenti tipi di formato testo:

[Testo arbitrario](arbitrary-text-type.md)

[RTF](rtf-type.md)

[Formattato](formatted-type.md)

[Enumerazione](enum-type.md)

[Tipo di identificatore](identifier-type.md)

Gli elementi configurabili del tipo di formato testo vengono utilizzati in campi di database non binari e in generale potrebbero essere sostituiti da qualsiasi stringa di qualsiasi lunghezza. Tuttavia, particolari elementi configurabili presentano anche restrizioni semantiche. Ad esempio, un elemento configurabile che è necessario per essere una chiave esterna in una tabella specifica presenta restrizioni semantiche aggiuntive. Tali restrizioni semantiche non vengono applicate da Mergemod.dll e pertanto gli autori dei moduli devono essere preparati a gestire qualsiasi stringa che soddisfi il tipo di formato di testo specificato.

 

 



