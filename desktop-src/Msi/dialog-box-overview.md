---
description: Il processo di creazione di una finestra di dialogo in Windows Installer è simile al processo di creazione di una finestra di dialogo a livello di codice tramite un modello di finestra di dialogo dell'API Microsoft Windows.
ms.assetid: c46f6b7b-e78c-4dd8-a4ff-7da5465391f9
title: Cenni preliminari sulla finestra di dialogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 884c85f06bc06588084311aee370700d5b2a5290
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346336"
---
# <a name="dialog-box-overview"></a>Cenni preliminari sulla finestra di dialogo

Il processo di creazione di una finestra di dialogo in Windows Installer è simile al processo di creazione di una finestra di dialogo a livello di codice tramite un modello di finestra di dialogo dell'API Microsoft Windows. Mentre un modello di finestra di dialogo di Windows viene archiviato in una stringa di caratteri con terminazione null, Windows Installer archivia i parametri della finestra di dialogo nella tabella della finestra di dialogo. La tabella della finestra di dialogo contiene una colonna Attributes che è analoga agli stili della finestra nell'API dell'interfaccia utente di Microsoft Windows. Tuttavia, il numero di bit di stile della finestra di dialogo in Windows Installer è un set ridotto e specializzato.

Per creare fisicamente la finestra di dialogo utilizzando l'API dell'interfaccia utente di Windows, viene chiamato [**DialogBox**](/windows/win32/api/winuser/nf-winuser-dialogboxa) e viene passato un puntatore al modello. In Windows Installer la finestra di dialogo viene creata durante l'esecuzione di una delle tre tabelle di sequenza dell'interfaccia utente.

Windows Installer non contiene un'interfaccia utente predefinita che gli autori di pacchetti possono utilizzare per i pacchetti. Contiene un set limitato di finestre di dialogo predefinite che visualizzano messaggi di errore e informativi, ma vengono visualizzati solo se Windows Installer esegue una query nelle tabelle della finestra di dialogo e della sequenza dell'interfaccia utente e rileva che non sono disponibili finestre di dialogo personalizzate.

L'SDK del programma di installazione include un database minimo denominato Uisample.msi che contiene le tabelle dell'interfaccia utente e delle sequenze di esecuzione popolate e un'interfaccia utente completa. Questo database è facilmente personalizzabile e Unito a tutti i pacchetti.

Alcune azioni standard e le condizioni di errore interne Windows Installer restituiscono un set specifico di dati dell'interfaccia utente e pertanto richiedono una finestra di dialogo con un set specifico di controlli che contengano tali dati. Windows Installer verifica due posizioni separate per gli identificatori di queste finestre di dialogo.

-   Windows Installer contiene un set di nomi di finestra di dialogo incorporati. L'azione personalizzata esegue una query nella tabella della finestra di dialogo per questi nomi riservati.
-   In ognuna delle tre tabelle di sequenza dell'interfaccia utente, i nomi delle finestre di dialogo con un numero di sequenza pari a-1,-2 o-3 vengono visualizzati in risposta a uscita, uscita richiesta dall'utente e messaggi di errore irreversibili da Windows Installer.

Un elenco completo dei nomi delle finestre di dialogo delle chiavi primarie riservate è disponibile nelle [finestre di dialogo](dialog-boxes.md). Si noti che il nome della finestra di dialogo chiave primaria è riservato solo dal programma di installazione e non è presente alcuna implementazione specifica della finestra di dialogo in Windows Installer. Gli autori di pacchetti devono comunque compilare tutti i campi del database che specificano gli attributi e i controlli di queste finestre di dialogo riservate.

 

 
