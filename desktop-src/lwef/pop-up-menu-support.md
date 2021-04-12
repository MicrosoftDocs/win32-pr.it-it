---
title: Supporto menu popup
description: Supporto menu popup
ms.assetid: a8a1cf91-c18a-497f-89a7-b47536eaca0a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 890d7eab6595200cb00e8422644b10f39807bab2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337343"
---
# <a name="pop-up-menu-support"></a>Supporto menu popup

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Microsoft Agent include un menu a comparsa (noto anche come menu contestuale) per ogni carattere. Il server Visualizza questo menu popup automaticamente quando un utente fa clic con il pulsante destro del mouse sul carattere. È possibile aggiungere comandi per l'applicazione client al menu definendo una raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) . Per ogni comando della raccolta definita, è possibile specificare la [**didascalia**](caption-property.md) e le proprietà [**visibili**](visible-property.md) . La **didascalia** è il testo visualizzato nel menu quando la proprietà **Visible** è impostata su **true**. È anche possibile usare la proprietà [**Enabled**](enabled-property.md) per visualizzare il comando nel menu come disabilitato e [**HelpContextID**](helpcontextid-property.md) per supportare la guida per la proprietà. Definire la chiave di accesso per il testo del menu includendo una e commerciale (&) prima del carattere di testo dell'impostazione del testo della **didascalia** .

Il server aggiunge automaticamente ai comandi di menu per aprire la finestra dei comandi vocali e nascondere il carattere, nonché le didascalie dei [**comandi**](/windows/desktop/lwef/the-commands-collection-object) di altri client del carattere per consentire agli utenti di passare da un client all'altro. Il server aggiunge automaticamente un separatore al menu tra le voci di menu e quelle definite dal client. I separatori vengono visualizzati solo se nel menu sono presenti elementi da separare.

Per rimuovere i comandi da un menu, usare il metodo [**Remove**](remove-method.md) . Si noti che le voci di menu non cambiano mentre viene visualizzato il menu. Se si aggiungono o rimuovono comandi o se ne modificano le proprietà, il menu Visualizza le modifiche quando l'utente visualizza nuovamente il menu.

Se si preferisce specificare i propri servizi per i menu popup per un carattere, è possibile usare la proprietà [**AutoPopupMenu**](autopopupmenu-property.md) per disattivare la gestione del server dell'azione di clic con il pulsante destro del mouse. È quindi possibile usare la notifica degli eventi [**Click**](click-event.md) per creare un comportamento di gestione del menu personalizzato.

Quando l'utente seleziona un comando dal menu di scelta rapida di un carattere o dalla finestra comandi vocali, il server attiva l'evento di [**comando**](command-event.md) del client associato e passa di nuovo i parametri dell'input utilizzando l'oggetto [**userinput**](/windows/desktop/lwef/iagentuserinput) .

Il server fornisce anche un menu a comparsa per l'icona della barra delle applicazioni del carattere. Quando il carattere è visibile, fare clic con il pulsante destro del mouse su questo menu per visualizzare gli stessi comandi visualizzati facendo clic con il pulsante destro del mouse sul carattere. Tuttavia, quando il carattere è nascosto, vengono inclusi solo i comandi forniti dal server.

 

 