---
title: Informazioni sui file di risorse
description: Viene descritto come includere risorse nell'applicazione Windows basata su criteri con RC.
ms.assetid: af7c7aed-5d28-40ac-ad00-da0986fd89c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24f351592c57cb628204ad6528a48bfa1a10507f5e7aad90a524ea2f6034f304
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034469"
---
# <a name="about-resource-files"></a>Informazioni sui file di risorse

Per includere risorse nell'applicazione Windows con RC, eseguire le operazioni seguenti:

1.  Creare singoli file per cursori, icone, bitmap, finestre di dialogo e tipi di carattere.
2.  Creare uno script di definizione delle risorse (file RC) che descrive le risorse usate dall'applicazione.
3.  Compilare lo script con RC. Per altre informazioni, vedere [Uso di RC (riga di comando RC).](using-rc-the-rc-command-line-.md)
4.  Collegare il file di risorse compilato (con estensione res) al file eseguibile dell'applicazione con il linker.

Un file di risorse è un file di testo con estensione rc. Il file può usare caratteri a byte singolo, a byte doppio o Unicode. La sintassi e la semantica per il preprocessore RC sono simili a quelle del compilatore Microsoft C/C++. Tuttavia, RC supporta un subset delle direttive, delle definizioni e dei pragma del preprocessore in uno script.

Il file script definisce le risorse. Per una risorsa presente in un file separato, ad esempio un'icona o un cursore, lo script specifica la risorsa e il file che la contiene. Per alcune risorse, ad esempio un menu, l'intera definizione della risorsa esiste all'interno dello script.

Negli argomenti seguenti vengono descritte le informazioni che un file script può contenere:

-   [Commenti ,](comments.md)che sono note che devono essere ignorate da RC.
-   [Macro predefinite , che](predefined-macros.md)non accettano argomenti e non possono essere ridefiniti.
-   [Direttive del preprocessore](preprocessor-directives.md), che indica a RC di eseguire azioni sullo script prima di compilarlo.
-   [Operatori del preprocessore](preprocessor-operators.md), usati con la **\# direttiva define.**
-   [Direttive pragma](pragma-directives.md)
-   [Istruzioni di definizione delle risorse](resource-definition-statements.md), che denotono e descrivono le risorse.

 

 




