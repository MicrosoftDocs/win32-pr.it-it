---
title: Salvataggio e ripristino di set di variabili di stato
description: È possibile salvare e ripristinare i valori di una raccolta di variabili di stato in uno stack di attributi con le funzioni glPushAttrib e glPopAttrib.
ms.assetid: 339de633-4158-4907-b985-2d75b465fb2a
keywords:
- Variabili di stato OpenGL
- salvataggio delle variabili di stato OpenGL
- ripristino delle variabili di stato OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b3192c228ea35005c5755802d3cd1b873f7b7fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298523"
---
# <a name="saving-and-restoring-sets-of-state-variables"></a>Salvataggio e ripristino di set di variabili di stato

È possibile salvare e ripristinare i valori di una raccolta di variabili di stato in uno stack di attributi con le funzioni [**glPushAttrib**](glpushattrib.md) e [**glPopAttrib**](glpopattrib.md) . Lo stack degli attributi ha una profondità di almeno 16. Per ottenere la profondità effettiva, usare la \_ \_ \_ profondità dello stack GL max attrib \_ con [**glGetIntegerv**](glgetintegerv.md). Il push di uno stack completo o la visualizzazione di un oggetto vuoto genera un errore.

È in genere più veloce usare **glPushAttrib** e **glPopAttrib** anziché ottenere e ripristinare i valori manualmente. Alcuni valori potrebbero essere inseriti e estratti nell'hardware e il salvataggio e il ripristino possono richiedere un utilizzo intensivo delle risorse. Inoltre, se si opera su un client remoto, tutti i dati degli attributi devono essere trasferiti attraverso la connessione di rete e viceversa mentre vengono salvati e ripristinati. Tuttavia, l'implementazione di OpenGL mantiene lo stack degli attributi sul server, evitando ritardi di rete non necessari.

Il prototipo di **glPushAttrib** è:

**void** **glPushAttrib**(**GLbitfield** *mask* );

L'uso di [**glPushAttrib**](glpushattrib.md) Salva tutti gli attributi indicati dai bit nella *maschera* inserendoli nello stack degli attributi. Per un elenco dei bit di maschera possibili che è possibile combinare logicamente o insieme per salvare qualsiasi combinazione di attributi, vedere [gruppi](attribute-groups.md)di attributi. Ogni bit corrisponde a una raccolta di singole variabili di stato. Ad esempio, il \_ bit di illuminazione GL \_ si riferisce a tutte le variabili di stato correlate all'illuminazione, che includono il colore del materiale corrente, l'ambiente, la diffusione, il speculare e la luce emessa, un elenco delle luci abilitate e le direzioni dei faretti. Quando si chiama [**glPopAttrib**](glpopattrib.md), vengono ripristinate tutte le variabili. Per conoscere esattamente quali attributi vengono salvati per determinati valori di maschera, vedere [variabili di stato OpenGL](opengl-state-variables.md).

 

 




