---
title: Finestra Opzioni carattere avanzate (finestra Comandi vocali)
description: Informazioni sulla finestra Opzioni carattere avanzate, che offre agli utenti le opzioni per modificare l'interazione con tutti i caratteri.
ms.assetid: c2f784e9-d1c5-4fa3-b3f7-5061c9b7e6d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd49ff2f3c948594756f8d02bd4417e4f4f684fc
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404360"
---
# <a name="advanced-character-options-window-voice-commands-window"></a>Finestra Opzioni carattere avanzate (finestra Comandi vocali)

\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Nella finestra Opzioni carattere avanzate sono disponibili opzioni che consentono agli utenti di modificare l'interazione con tutti i caratteri. Ad esempio, gli utenti possono disabilitare l'input vocale o modificare i parametri di input. Gli utenti possono anche modificare le impostazioni di output per il fumetto. Queste impostazioni eseguono l'override di qualsiasi set impostato da un'applicazione client o impostato come parte della definizione del carattere. L'applicazione non può modificare o disabilitare queste opzioni, perché si applicano alle preferenze utente generali per il funzionamento di tutti i caratteri. Tuttavia, il server invierà una notifica all'applicazione ([**DefaultCharacterChange**](defaultcharacterchange-event.md)) quando l'utente cambia e applica un'opzione. È anche possibile visualizzare o chiudere la finestra usando la proprietà [**Visible**](visible-property.md) della finestra e accedervi tramite le [**proprietà Top**](top-property.md) [**e Left.**](left-property.md)

Oltre a supportare l'animazione di un carattere, Microsoft Agent supporta l'output audio per il carattere. Sono inclusi l'output parlato e gli effetti sonori. Per l'output parlato, il server sincronizza automaticamente le immagini della bocca definite del carattere nell'output. È possibile scegliere la sintesi vocale (TTS), l'audio registrato o solo l'output di testo del fumetto.

 

 




