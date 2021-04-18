---
description: Questo evento di controllo esegue un file specificato. Se il file non esiste o se l'evento ha esito negativo, Windows Installer registra l'errore nel log dettagliato senza visualizzare una finestra di dialogo contenente un messaggio di errore.
ms.assetid: a185c5a1-6584-4916-967a-313e6b7cf97c
title: ControlEvent MsiLaunchApp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 298867868a80eb2cb831a2304325d14355adc669
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309470"
---
# <a name="msilaunchapp-controlevent"></a>ControlEvent MsiLaunchApp

Questo evento di controllo esegue un file specificato. Se il file non esiste o se l'evento ha esito negativo, Windows Installer registra l'errore nel log dettagliato senza visualizzare una finestra di dialogo contenente un messaggio di errore.

**[Windows Installer 4,5 o versioni precedenti](not-supported-in-windows-installer-4-5.md):** Non supportato. Questo ControlEvent è disponibile a partire da Windows Installer 5,0.

## <a name="published-by"></a>Pubblicato da

Questo ControlEvent viene pubblicato dal programma di installazione.

## <a name="argument"></a>Argomento

I campi del valore dell'argomento sono delimitati da spazi. Il primo campo contiene un valore stringa che specifica il file da eseguire. Usare un valore stringa di \[ \# *FileKey* \] per identificare il file e sostituire *FileKey* con l'identificatore del file visualizzato nella colonna file della tabella [file](file-table.md) . Tutti i campi rimanenti dell'argomento possono contenere parametri usati dal file in esecuzione.

## <a name="action-on-subscribers"></a>Azione sui sottoscrittori

Questo ControlEvent non esegue alcuna azione nei Sottoscrittori.

## <a name="typical-use"></a>Utilizzo tipico

Per consentire a un utente di scegliere di eseguire un file al termine di un'installazione. Questo evento può essere condizionato da una proprietà impostata da un controllo [CheckBox](checkbox-control.md) visualizzato nella finestra di dialogo finale dell'installazione. Il controllo CheckBox non deve essere visualizzato durante la rimozione del pacchetto.

 

 



