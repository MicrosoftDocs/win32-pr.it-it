---
title: Caricamento del carattere predefinito
description: Caricamento del carattere predefinito
ms.assetid: 4e91aef5-8402-401d-b09f-83be25011027
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 387715b5078c4ec875c9abce47039898e4998cf7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298175"
---
# <a name="loading-the-default-character"></a>Caricamento del carattere predefinito

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Anziché caricare direttamente un carattere specifico specificando il relativo nome file, è possibile caricare il *carattere predefinito*. Il carattere predefinito è un servizio destinato a fornire un assistente di Windows centrale condiviso scelto dall'utente. Microsoft Agent include una finestra delle proprietà come parte del servizio character predefinito, noto come carattere Finestra Proprietà, che consente all'utente di modificare la selezione del carattere predefinito.

La selezione del carattere predefinito è limitata a un carattere che supporta il set di animazioni standard, garantendo un livello di coerenza di base tra i caratteri. Questa operazione non esclude un carattere dall'avere animazioni aggiuntive.

Tuttavia, poiché il carattere predefinito è destinato all'uso generico e può essere condiviso da altre applicazioni nello stesso momento, evitare di caricare il carattere predefinito quando si desidera un carattere esclusivo per l'applicazione.

Per caricare il carattere predefinito, chiamare il metodo [**Load**](load-method.md) senza specificare un nome file o un percorso. Microsoft Agent carica automaticamente il set di caratteri corrente come carattere predefinito. Se l'utente non ha ancora selezionato un carattere predefinito, Agent selezionerà il primo carattere che supporta il set di animazioni standard. Se non ne è disponibile alcuno, il metodo avrà esito negativo e segnalerà la cause.

Anche se un'applicazione client può richiedere l'identità del carattere, solo un utente può modificare le impostazioni. È possibile usare [**ShowDefaultCharacterProperties**](showdefaultcharacterproperties-method.md) per visualizzare il carattere finestra Proprietà.

Il server invierà una notifica ai client che hanno caricato il carattere predefinito quando un utente modifica la selezione dei caratteri e passa il GUID del nuovo carattere. Il server Scarica automaticamente il carattere precedente e ricarica il nuovo carattere. Le code di tutti i client che hanno caricato il carattere predefinito vengono interrotte e scaricate. Tuttavia, le code dei client che hanno caricato il carattere in modo esplicito utilizzando il nome file del carattere non sono interessate. Se necessario, il server gestisce anche la reimpostazione automatica del motore di sintesi vocale (TTS) per il nuovo carattere.

 

 




