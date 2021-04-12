---
title: Finestra Opzioni carattere avanzato (finestra comandi vocali)
description: Finestra Opzioni carattere avanzato
ms.assetid: c2f784e9-d1c5-4fa3-b3f7-5061c9b7e6d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f481871d3861da99b54829e5c6e1b34c9137060a
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104339972"
---
# <a name="advanced-character-options-window-voice-commands-window"></a>Finestra Opzioni carattere avanzato (finestra comandi vocali)

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Nella finestra Opzioni carattere avanzate sono disponibili opzioni che consentono agli utenti di modificare l'interazione con tutti i caratteri. Ad esempio, gli utenti possono disabilitare l'input vocale o modificare i parametri di input. Gli utenti possono anche modificare le impostazioni di output per la parola fumetto. Queste impostazioni eseguono l'override di tutti i set da un'applicazione client o impostati come parte della definizione del carattere. L'applicazione non può modificare o disabilitare queste opzioni perché si applicano alle preferenze utente generali per il funzionamento di tutti i caratteri. Tuttavia, il server invierà una notifica all'applicazione ([**DefaultCharacterChange**](defaultcharacterchange-event.md)) quando l'utente cambia e applica un'opzione. È anche possibile visualizzare o chiudere la finestra usando la proprietà [**Visible**](visible-property.md) della finestra e accedere alla relativa posizione tramite le proprietà [**Top**](top-property.md) e [**Left**](left-property.md) .

Oltre a supportare l'animazione di un carattere, Microsoft Agent supporta l'output audio per il carattere. Sono inclusi l'output parlato e gli effetti audio. Per l'output parlato, il server sincronizza automaticamente le immagini mouth definite del carattere nell'output. È possibile scegliere Sintesi vocale (TTS), audio registrato o solo output di testo a fumetti.

 

 




