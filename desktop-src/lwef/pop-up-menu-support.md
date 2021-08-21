---
title: Supporto del menu a comparsa
description: Supporto del menu a comparsa
ms.assetid: a8a1cf91-c18a-497f-89a7-b47536eaca0a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7dc8ab6984b06f4ea4f2ead4878ab0b9e2807327da9ce974c17d36e821c69ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117882914"
---
# <a name="pop-up-menu-support"></a>Supporto del menu a comparsa

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Microsoft Agent include un menu a comparsa (noto anche come menu contestuale) per ogni carattere. Il server visualizza automaticamente questo menu a comparsa quando un utente fa clic con il pulsante destro del mouse sul carattere. È possibile aggiungere comandi per l'applicazione client al menu definendo una [**raccolta Commands.**](/windows/desktop/lwef/the-commands-collection-object) Per ogni comando nella raccolta definita, è possibile specificare le [**proprietà Caption**](caption-property.md) [**e Visible.**](visible-property.md) Caption **è** il testo visualizzato nel menu quando la **proprietà Visible** è impostata su **True.** È anche possibile usare la [**proprietà Enabled**](enabled-property.md) per visualizzare il comando nel menu come disabilitato e [**HelpContextID**](helpcontextid-property.md) per supportare il supporto della Guida per la proprietà . Definire il tasto di scelta per il testo del menu includendo una e commerciale (&) prima del carattere di testo dell'impostazione **Testo** didascalia.

Il server aggiunge automaticamente ai comandi di menu per aprire la [](/windows/desktop/lwef/the-commands-collection-object) finestra Comandi vocali e nascondere il carattere e le didascalie Comandi di altri client del carattere per consentire agli utenti di passare da un client all'altro. Il server aggiunge automaticamente un separatore al menu tra le voci di menu e quelle definite dal client. I separatori vengono visualizzati solo quando sono presenti voci nel menu da separare.

Per rimuovere i comandi da un menu, usare il [**metodo Remove.**](remove-method.md) Si noti che le voci di menu non cambiano mentre viene visualizzato il menu. Se si aggiungono o rimuovono comandi o si modificano le relative proprietà, il menu visualizza le modifiche quando l'utente visualizza nuovamente il menu.

Se si preferisce fornire servizi di menu popup personalizzati per un carattere, è possibile usare la proprietà [**AutoPopupMenu**](autopopupmenu-property.md) per disattivare la gestione del server dell'azione di clic con il pulsante destro del mouse. È quindi possibile usare la [**notifica dell'evento Click**](click-event.md) per creare un comportamento di gestione dei menu personalizzato.

Quando l'utente seleziona un comando dal menu a comparsa di un carattere o dalla finestra Comandi vocali, il server attiva l'evento [**Command**](command-event.md) del client associato e passa nuovamente i parametri dell'input usando l'oggetto [**UserInput.**](/windows/desktop/lwef/iagentuserinput)

Il server fornisce anche un menu a comparsa per l'icona della barra delle applicazioni del carattere. Quando il carattere è visibile, facendo clic con il pulsante destro del mouse su questo menu vengono visualizzati gli stessi comandi visualizzati facendo clic con il pulsante destro del mouse sul carattere. Tuttavia, quando il carattere è nascosto, vengono inclusi solo i comandi forniti dal server.

 

 