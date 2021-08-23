---
title: Salvataggio e ripristino di set di variabili di stato
description: È possibile salvare e ripristinare i valori di una raccolta di variabili di stato in uno stack di attributi con le funzioni glPushAttrib e glPopAttrib.
ms.assetid: 339de633-4158-4907-b985-2d75b465fb2a
keywords:
- Variabili di stato OpenGL
- salvataggio di variabili di stato OpenGL
- ripristino di variabili di stato OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 197a05d80e72479aecdade3323899464bf0b1f4afa2d9f2a8a1a1add6e56db78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119553811"
---
# <a name="saving-and-restoring-sets-of-state-variables"></a>Salvataggio e ripristino di set di variabili di stato

È possibile salvare e ripristinare i valori di una raccolta di variabili di stato in uno stack di attributi con le funzioni [**glPushAttrib**](glpushattrib.md) [**e glPopAttrib.**](glpopattrib.md) Lo stack di attributi ha una profondità di almeno 16. Per ottenere la profondità effettiva, usare GL \_ MAX \_ ATTRIB \_ STACK DEPTH \_ con [**glGetIntegerv**](glgetintegerv.md). Il push di uno stack completo o la rimozione di uno stack vuoto genera un errore.

In genere è più veloce usare **glPushAttrib** e **glPopAttrib** rispetto a ottenere e ripristinare i valori manualmente. È possibile eseguire il push e il recupero di alcuni valori nell'hardware e salvarli e ripristinarli può richiedere un uso intensivo delle risorse. Inoltre, se si opera su un client remoto, tutti i dati degli attributi devono essere trasferiti attraverso la connessione di rete e di nuovo quando vengono salvati e ripristinati. Tuttavia, l'implementazione OpenGL mantiene lo stack di attributi nel server, evitando inutili ritardi di rete.

Il prototipo **di glPushAttrib** è:

**void** **glPushAttrib**(**GLbitfield** *mask* );

[**L'uso di glPushAttrib**](glpushattrib.md) salva tutti gli attributi indicati dai bit in *mask* mediante il push nello stack di attributi. Per un elenco dei possibili bit di maschera che è possibile usare logicamente con OR per salvare qualsiasi combinazione di attributi, vedere [Gruppi di attributi.](attribute-groups.md) Ogni bit corrisponde a una raccolta di singole variabili di stato. Ad esempio, GL LIGHTING BIT si riferisce a tutte le variabili di stato correlate all'illuminazione, che includono il colore del materiale corrente, l'ambiente, la luce \_ diffusa, speculare e emessa, un elenco delle luci abilitate e le direzioni dei \_ riflettori. Quando si chiama [**glPopAttrib,**](glpopattrib.md)tutte queste variabili vengono ripristinate. Per scoprire esattamente quali attributi vengono salvati per determinati valori di maschera, vedere [Variabili di stato OpenGL.](opengl-state-variables.md)

 

 




