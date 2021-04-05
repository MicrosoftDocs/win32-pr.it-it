---
description: È possibile definire gli ambiti di input personalizzati usando modelli di linguaggio composte da espressioni regolari per la grafia e assegnando loro i campi. Se, ad esempio, si crea un'applicazione di database per le parti del magazzino e si desidera che gli utenti siano in grado di immettere numeri di parte utilizzando il riquadro di scrittura del pannello di input di Tablet PC. Se la sintassi del numero di parte è costituita da tre lettere seguite da quattro numeri seguiti da un'altra lettera (ad esempio, ABC1234D), il riconoscimento della grafia potrebbe avere un tempo difficile per riconoscere tale input perché non è definito nel modello di linguaggio. Non esiste alcun controllo del controllo predefinito corrispondente a tale sintassi, né Microsoft può includere la sintassi per ogni possibile campo che potrebbe essere necessario per un'applicazione. Le espressioni regolari di grafia consentono alle applicazioni di definire in modo semplice un modello di linguaggio specifico per un particolare campo di utilizzo speciale. Nota Quando si lavora in un'applicazione abilitata per l'input penna che usa la proprietà del controllo dell'oggetto RecognizerContext, non è possibile usare la versione 1 factoids in un'espressione regolare.
ms.assetid: 71f80196-0a36-4a14-a115-712bc909f6d7
title: Ambiti di input personalizzati con espressioni regolari
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bdd7807221aca7b05ed4dc1facf7ddb01470c8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049294"
---
# <a name="custom-input-scopes-with-regular-expressions"></a>Ambiti di input personalizzati con espressioni regolari

È possibile definire gli ambiti di input personalizzati usando modelli di linguaggio composte da espressioni regolari per la grafia e assegnando loro i campi.

Se, ad esempio, si crea un'applicazione di database per le parti del magazzino e si desidera che gli utenti siano in grado di immettere numeri di parte utilizzando il riquadro di scrittura del pannello di input di Tablet PC. Se la sintassi del numero di parte è costituita da tre lettere seguite da quattro numeri seguiti da un'altra lettera (ad esempio, ABC1234D), il riconoscimento della grafia potrebbe avere un tempo difficile per riconoscere tale input perché non è definito nel modello di linguaggio. Non esiste alcun controllo del controllo predefinito corrispondente a tale sintassi, né Microsoft può includere la sintassi per ogni possibile campo che potrebbe essere necessario per un'applicazione. Le espressioni regolari di grafia consentono alle applicazioni di definire in modo semplice un modello di linguaggio specifico per un particolare campo di utilizzo speciale.

> [!Note]  
> Quando si lavora in un'applicazione abilitata per l'input penna che [**Usa la proprietà del controllo**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) dell'oggetto [**RecognizerContext**](inkrecognizercontext-class.md) , non è possibile usare la versione 1 factoids in un'espressione regolare.

 

 

 



