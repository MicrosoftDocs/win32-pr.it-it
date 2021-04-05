---
title: Caricamento di un carattere
description: Caricamento di un carattere
ms.assetid: 973de75b-b530-40c6-896d-e2ab0755ae2c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3590698040f40f8fbf0964177e12ba6ed253c37d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710378"
---
# <a name="loading-a-character"></a>Caricamento di un carattere

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Per animare un carattere, è necessario innanzitutto caricare il carattere. Utilizzare il metodo [**Load**](load-method.md) per caricare i dati del carattere. Microsoft Agent supporta due formati per i dati di tipo carattere e animazione: un singolo file strutturato e file separati. In genere, si usa il formato di file singolo (. ACS) quando i dati vengono archiviati localmente. Il formato del file multiplo (. ACF,. ACA) funziona meglio quando si desidera scaricare animazioni singolarmente, ad esempio quando si accede alle animazioni da un server HTTP.

Un'applicazione client può caricare una sola istanza dello stesso carattere. Qualsiasi tentativo di caricare lo stesso carattere più di una volta avrà esito negativo. Tuttavia, un'applicazione può disporre di più istanze dello stesso carattere caricate fornendo connessioni separate a Microsoft Agent. Ad esempio, un'applicazione potrebbe caricare lo stesso carattere da due copie del controllo Microsoft Agent.

È anche possibile definire i propri caratteri da usare con Microsoft Agent. È possibile utilizzare qualsiasi strumento di rendering che si preferisce creare le immagini, purché si disponga di file in formato bitmap di Windows. Per assemblare e compilare immagini di un carattere in animazioni da usare con Microsoft Agent, usare l'editor dei caratteri di Microsoft Agent. Questo strumento consente di definire le proprietà predefinite di un carattere, nonché di definire animazioni per il carattere. L'editor dei caratteri di Microsoft Agent consente inoltre di selezionare il formato di file appropriato quando si crea un carattere.

 

 




