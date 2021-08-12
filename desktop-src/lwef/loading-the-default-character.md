---
title: Caricamento del carattere predefinito
description: Caricamento del carattere predefinito
ms.assetid: 4e91aef5-8402-401d-b09f-83be25011027
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f99d194843c6196f69e287857ce08097e849f328738c5f5d1a6e7feba0c53d18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118247608"
---
# <a name="loading-the-default-character"></a>Caricamento del carattere predefinito

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Anziché caricare direttamente solo un carattere specifico specificandone il nome file, è possibile caricare il *carattere predefinito*. Il carattere predefinito è un servizio destinato a fornire un assistente Windows centrale condiviso scelto dall'utente. Microsoft Agent include una finestra delle proprietà come parte del servizio di caratteri predefinito, noto come character Finestra Proprietà, che consente all'utente di modificare la selezione del carattere predefinito.

La selezione del carattere predefinito è limitata a un carattere che supporta il set di animazioni standard, garantendo un livello di coerenza di base tra i caratteri. Ciò non esclude che un carattere abbia animazioni aggiuntive.

Tuttavia, poiché il carattere predefinito è destinato all'uso generico e può essere condiviso contemporaneamente da altre applicazioni, evitare di caricare il carattere predefinito quando si vuole un carattere esclusivamente per l'applicazione.

Per caricare il carattere predefinito, chiamare il [**metodo Load**](load-method.md) senza specificare un nome file o un percorso. Microsoft Agent carica automaticamente il set di caratteri corrente come carattere predefinito. Se l'utente non ha ancora selezionato un carattere predefinito, Agent selezionerà il primo carattere che supporta il set di animazioni standard. Se non è disponibile, il metodo avrà esito negativo e restituisce la causa.

Anche se un'applicazione client può chiedere informazioni sull'identità del carattere, solo un utente può modificarne le impostazioni. È possibile usare [**ShowDefaultCharacterProperties per**](showdefaultcharacterproperties-method.md) visualizzare l'oggetto Character Finestra Proprietà.

Il server invierà una notifica ai client che hanno caricato il carattere predefinito quando un utente modifica una selezione di caratteri e passerà il GUID del nuovo carattere. Il server scarica automaticamente il carattere precedente e ricarica il nuovo carattere. Le code di tutti i client che hanno caricato il carattere predefinito vengono arrestate e scaricate. Tuttavia, le code dei client che hanno caricato il carattere in modo esplicito usando il nome del file del carattere non sono interessate. Se necessario, il server gestisce anche la reimpostazione automatica del motore di sintesi vocale (TTS) per il nuovo carattere.

 

 




