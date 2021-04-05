---
title: Informazioni sui file di risorse
description: Viene descritto come includere le risorse nell'applicazione basata su Windows con RC.
ms.assetid: af7c7aed-5d28-40ac-ad00-da0986fd89c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c43e9df59cf0b6507b6c6a53c42299b8792634f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044719"
---
# <a name="about-resource-files"></a>Informazioni sui file di risorse

Per includere le risorse nell'applicazione basata su Windows con RC, seguire questa procedura:

1.  Creare singoli file per i cursori, le icone, le bitmap, le finestre di dialogo e i tipi di carattere.
2.  Creare uno script di definizione di risorsa (file RC) che descriva le risorse usate dall'applicazione.
3.  Compilare lo script con RC. Per altre informazioni, vedere [uso di RC (riga di comando RC)](using-rc-the-rc-command-line-.md).
4.  Collegare il file di risorse compilato (res) al file eseguibile dell'applicazione con il linker.

Un file di risorse è un file di testo con estensione RC. Il file può utilizzare caratteri a byte singolo, a doppio byte o Unicode. La sintassi e la semantica per il preprocessore RC sono simili a quelle del compilatore Microsoft C/C++. Tuttavia, RC supporta un subset delle direttive per il preprocessore, definisce e pragma in uno script.

Il file di script definisce le risorse. Per una risorsa esistente in un file separato, ad esempio un'icona o un cursore, lo script specifica la risorsa e il file che lo contiene. Per alcune risorse, ad esempio un menu, l'intera definizione della risorsa è presente nello script.

Negli argomenti seguenti vengono descritte le informazioni che possono essere contenute in un file script:

-   [Commenti](comments.md), che sono note che devono essere ignorate da RC.
-   Le [macro predefinite](predefined-macros.md), che non accettano argomenti e non possono essere ridefinite.
-   [Direttive per il preprocessore](preprocessor-directives.md), che indicano a RC di eseguire azioni sullo script prima di compilarlo.
-   [Operatori del preprocessore](preprocessor-operators.md), utilizzati con la direttiva **\# define** .
-   [Direttive pragma](pragma-directives.md)
-   [Istruzioni per la definizione delle](resource-definition-statements.md)risorse, che denominano e descrivono le risorse.

 

 




