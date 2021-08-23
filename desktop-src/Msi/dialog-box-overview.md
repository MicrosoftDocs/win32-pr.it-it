---
description: Il processo di creazione di una finestra di dialogo nel programma di installazione Windows è simile al processo di creazione di una finestra di dialogo a livello di codice usando un modello di finestra di dialogo dell'API Windows Microsoft.
ms.assetid: c46f6b7b-e78c-4dd8-a4ff-7da5465391f9
title: Panoramica della finestra di dialogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a17963148100d8f0d99a6fdb9e043654e089880b81ade0a943b92b4bfcd35f7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764171"
---
# <a name="dialog-box-overview"></a>Panoramica della finestra di dialogo

Il processo di creazione di una finestra di dialogo nel programma di installazione Windows è simile al processo di creazione di una finestra di dialogo a livello di codice usando un modello di finestra di dialogo dell'API Windows Microsoft. Mentre un Windows di finestra di dialogo viene archiviato in una stringa di caratteri con terminazione Null, Windows Installer archivia i parametri della finestra di dialogo nella tabella Dialog. La tabella Dialog contiene una colonna attributes analoga agli stili window nell'API dell'interfaccia Windows Microsoft. Tuttavia, il numero di bit di stile del dialogo in Windows Installer è un set ridotto e specializzato.

Per creare fisicamente la finestra di dialogo usando Windows'API dell'interfaccia utente, Viene chiamato [**DialogBox**](/windows/win32/api/winuser/nf-winuser-dialogboxa) e viene passato un puntatore al modello. In Windows installer, la finestra di dialogo viene creata durante l'esecuzione di una delle tre tabelle della sequenza dell'interfaccia utente.

Windows Il programma di installazione non contiene un'interfaccia utente predefinita che gli autori di pacchetti possono usare per i pacchetti. Contiene un set limitato di finestre di dialogo predefinite che visualizzano messaggi di errore e informazioni, ma vengono visualizzate solo se il programma di installazione di Windows esegue una query sulle tabelle Dialog e Sequenza dell'interfaccia utente e rileva che non sono disponibili finestre di dialogo personalizzate.

L'SDK del programma di installazione include un database minimo denominato Uisample.msi che contiene tabelle popolate dell'interfaccia utente e della sequenza di esecuzione e un'interfaccia utente completa. Questo database è facilmente personalizzabile e unito a qualsiasi pacchetto.

Alcune azioni standard e condizioni di errore Windows installer restituiscono un set specifico di dati dell'interfaccia utente e pertanto richiedono una finestra di dialogo con un set specifico di controlli per contenere i dati. Windows Il programma di installazione controlla due posizioni separate per gli identificatori per queste finestre di dialogo.

-   Windows Il programma di installazione contiene un set di nomi di finestre di dialogo incorporate. L'azione personalizzata esegue una query nella tabella Dialog per questi nomi riservati.
-   In ognuna delle tre tabelle di sequenza dell'interfaccia utente, i nomi dei dialogati con un numero di sequenza -1,-2 o -3 vengono visualizzati in risposta all'uscita, all'uscita richiesta dall'utente e ai messaggi di errore irreversibili da Windows Installer.

Nelle finestre di dialogo è disponibile un elenco completo dei nomi delle finestre di dialogo [della chiave primaria riservata.](dialog-boxes.md) Si noti che il nome della finestra di dialogo chiave primaria è riservato solo dal programma di installazione e non esiste alcuna implementazione specifica della finestra di dialogo all'interno Windows Installer. Gli autori di pacchetti devono comunque popolare tutti i campi del database che specificano gli attributi e i controlli di queste finestre di dialogo riservate.

 

 
