---
title: Selezione del motore vocale
description: Selezione del motore vocale
ms.assetid: f5afedc6-093f-4247-a5c8-277d6b2d646c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a548f0201ba37c8acb867091cc690a913277ff06
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855978"
---
# <a name="speech-engine-selection"></a>Selezione del motore vocale

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

L'impostazione dell'ID lingua di un carattere determina la lingua di input vocale predefinita; Microsoft Agent richiede SAPI per un motore installato che corrisponda a tale lingua. Se un'applicazione client non specifica una preferenza per la lingua, Microsoft Agent tenterà di trovare un motore di riconoscimento vocale corrispondente all'ID lingua predefinito dell'utente (usando l'ID lingua principale, quindi l'ID della lingua secondaria). Se non è disponibile alcun motore corrispondente a questa lingua, il riconoscimento vocale viene disabilitato per tale carattere.

È anche possibile richiedere un motore di riconoscimento vocale specifico specificando l'ID modalità (usando la proprietà Character [**SRModeID**](srmodeid-property.md) ). Tuttavia, se l'ID lingua per l'ID modalità non corrisponde all'impostazione della lingua del client, la chiamata avrà esito negativo (genera un errore nel controllo). Il motore di riconoscimento vocale rimarrà quindi l'ultimo motore impostato correttamente dal client o, se non lo è, il motore che corrisponde all'ID lingua del sistema corrente. Se non è ancora presente alcuna corrispondenza, l'input vocale non è disponibile per quel client.

Microsoft Agent carica automaticamente un motore di riconoscimento vocale quando l'input vocale viene avviato da un utente che preme la scelta rapida in ascolto o il client di input-attivo chiama il metodo [**Listen**](listen-method.md) . Tuttavia, è possibile caricare un motore anche quando si imposta o si esegue una query sull'ID modalità, si imposta o si esegue una query sulle proprietà della finestra dei comandi vocali, si esegue una query su [**SRStatus**](srstatus-property.md)o quando la voce vocale è abilitata e l'utente Visualizza la pagina di input vocale delle opzioni per caratteri avanzati. Tuttavia, Microsoft Agent mantiene solo i motori di riconoscimento vocale utilizzati dai client.

 

 




