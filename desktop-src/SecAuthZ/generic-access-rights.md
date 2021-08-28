---
description: Gli oggetti a protezione diretta usano un formato maschera di accesso in cui i quattro bit di ordine elevato specificano diritti di accesso generici.
ms.assetid: e18cede9-9bf7-4866-850b-5d7fa43a5b0f
title: Diritti di accesso generici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee90a6866afc294cfef1c8fdad96e239f76ce8f9c251aeabc2d2a907e3e0bbe5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119672091"
---
# <a name="generic-access-rights"></a>Diritti di accesso generici

Gli oggetti a protezione diretta usano un [formato maschera di](access-mask-format.md) accesso in cui i quattro bit di ordine elevato specificano diritti di accesso generici. Ogni tipo di oggetto a protezione diretta esegue il mapping di questi bit a un set di diritti di accesso standard e specifici dell'oggetto. Ad esempio, un oggetto file Windows esegue il mapping del bit READ GENERICO ai diritti di accesso standard READ CONTROL e SYNCHRONIZE e ai diritti di accesso specifici dell'oggetto \_ \_ FILE READ \_ \_ DATA, FILE READ EA e FILE READ \_ \_ \_ \_ ATTRIBUTES. Altri tipi di oggetti eseggono il bit GENERIC READ a qualsiasi set di diritti di \_ accesso appropriato per tale tipo di oggetto.

È possibile usare diritti di accesso generici per specificare il tipo di accesso necessario quando si apre un handle a un oggetto. Questa operazione è in genere più semplice rispetto alla specifica di tutti i diritti standard e specifici corrispondenti.

Nella tabella seguente vengono illustrate le costanti definite per i diritti di accesso generici.



| Costante         | Significato generico            |
|------------------|----------------------------|
| GENERIC \_ ALL     | Tutti i diritti di accesso possibili |
| ESECUZIONE \_ GENERICA | Eseguire l'accesso             |
| LETTURA \_ GENERICA    | accesso in lettura                |
| SCRITTURA \_ GENERICA   | Accesso in scrittura               |



 

Anche le applicazioni che definiscono oggetti a protezione diretta privati possono usare i diritti di accesso generici.

 

 



