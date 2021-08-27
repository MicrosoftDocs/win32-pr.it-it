---
description: Windows Il programma di installazione offre agli sviluppatori di pacchetti la possibilità di creare un'interfaccia utente interna con più livelli di funzionalità.
ms.assetid: 9f5796a7-e244-4fc8-af85-52a147bb2c0b
title: Interfaccia utente livelli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bbe932ea10b62d20ca06a027b935ff04289cdef
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478067"
---
# <a name="user-interface-levels"></a>Interfaccia utente livelli

Windows Il programma di installazione offre agli sviluppatori di pacchetti la possibilità di creare un'interfaccia utente interna con più livelli di funzionalità. Poiché l'interfaccia utente interna deve essere creata dall'autore del pacchetto, il comportamento dell'interfaccia utente completa, dell'interfaccia utente ridotta, dell'interfaccia utente di base e dei livelli Nessuno dipende dal pacchetto di installazione. La tabella seguente descrive le funzionalità comunemente attribuite ai livelli dell'interfaccia utente.




| Livello interfaccia utente | Descrizione | 
|----------|-------------|
| Interfaccia utente completa | Visualizza le finestre di dialogo modali e non modali che sono state scritte nell'interfaccia utente interna. Visualizza le finestre <a href="error-dialog.md">di dialogo di errore</a> personalizzate.<blockquote>[!Note]<br />Le finestre di dialogo modali richiedono l'input dell'utente prima che l'installazione possa continuare e vengono specificate impostando <a href="modal-dialog-style-bit.md">il bit di</a> stile della finestra di dialogo modale nella colonna Attributi della tabella <a href="dialog-table.md">Dialog.</a> Una finestra di dialogo non modabile non richiede l'input dell'utente per continuare l'installazione.</blockquote><br /> Un'interfaccia utente completa in genere <a href="user-interface-wizard-behavior.md">Interfaccia utente procedura guidata.</a><br /> | 
| Interfaccia utente ridotta | Visualizza tutte le finestre di dialogo non modali che sono state scritte nell'interfaccia utente. Non vengono visualizzate finestre di dialogo modali personalizzate. Visualizza le finestre <a href="error-dialog.md">di dialogo di errore</a> personalizzate. Visualizza <a href="authoring-disk-prompt-messages.md">i messaggi di richiesta del</a> disco. Visualizza <a href="filesinuse-dialog.md">le finestre di dialogo FileInUsa.</a> | 
| Interfaccia utente di base | Visualizza le finestre di dialogo non modali incorporate che visualizzano i messaggi di stato. Visualizza le finestre di dialogo di errore incorporate. Non vengono visualizzate finestre di dialogo personalizzate. Richiede agli utenti di inserire un disco visualizzando una finestra di dialogo contenente il <a href="diskprompt.md"><strong>valore della proprietà DiskPrompt.</strong></a> | 
| Nessuno | Nessuno indica un'installazione invisibile all'utente che non visualizza alcuna interfaccia utente. | 




 

Il livello dell'interfaccia utente interna può essere impostato [**usando MsiSetInternalUI.**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) Il programma di installazione imposta [**la proprietà UILevel**](uilevel.md) sul livello corrente dell'interfaccia utente.

Se la [**proprietà LIMITUI**](limitui.md) è impostata, il livello dell'interfaccia utente usato durante l'installazione del pacchetto è limitato a Basic.

Per un esempio di creazione dell'interfaccia utente, vedere [An Installation Example](an-installation-example.md).

 

 




