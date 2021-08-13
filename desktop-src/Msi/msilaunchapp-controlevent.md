---
description: Questo evento di controllo esegue un file specificato. Se il file non esiste o se l'evento ha esito negativo, Windows Installer registra l'errore nel log dettagliato senza visualizzare una finestra di dialogo contenente un messaggio di errore.
ms.assetid: a185c5a1-6584-4916-967a-313e6b7cf97c
title: MsiLaunchApp ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 982152d58748ba8b1b8f9d302766e1e9c55eb2ee3c9fa0ce7582507c017dc9b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118627789"
---
# <a name="msilaunchapp-controlevent"></a>MsiLaunchApp ControlEvent

Questo evento di controllo esegue un file specificato. Se il file non esiste o se l'evento ha esito negativo, Windows Installer registra l'errore nel log dettagliato senza visualizzare una finestra di dialogo contenente un messaggio di errore.

**[Windows Installer 4.5 o versioni precedenti:](not-supported-in-windows-installer-4-5.md)** Non supportato. Questo ControlEvent è disponibile a partire da Windows Installer 5.0.

## <a name="published-by"></a>Pubblicato da

Questo ControlEvent viene pubblicato dal programma di installazione.

## <a name="argument"></a>Argomento

I campi del valore dell'argomento sono delimitati da spazi. Il primo campo contiene un valore stringa che specifica il file da eseguire. Usare un valore stringa filekey per identificare il file e sostituire filekey con \[ \#  \] l'identificatore  del file visualizzato nella colonna File della [tabella File.](file-table.md) Tutti i campi rimanenti dell'argomento possono contenere parametri usati dal file in esecuzione.

## <a name="action-on-subscribers"></a>Azione nei Sottoscrittori

Questo ControlEvent non esegue alcuna azione sui sottoscrittori.

## <a name="typical-use"></a>Utilizzo tipico

Per consentire a un utente di scegliere di eseguire un file al termine di un'installazione. Questo evento può essere condizionato su una proprietà impostata da un [controllo CheckBox](checkbox-control.md) visualizzato nella finestra di dialogo finale dell'installazione. Il controllo CheckBox non deve essere visualizzato durante la rimozione del pacchetto.

 

 



