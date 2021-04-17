---
title: Configurazione ripristino configurazione di sistema
description: Ripristino configurazione di sistema utilizza Strumentazione gestione Windows (WMI) per fornire uno script per la configurazione e l'utilizzo delle relative funzionalità. Espone due classi, SystemRestore e SystemRestoreConfig, nello \\ spazio dei nomi predefinito radice.
ms.assetid: b510c5b7-71ec-47f9-b567-45fde8c79f57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 323f75cd80f7838e643922d8b9ffa7bf2b121945
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399264"
---
# <a name="configuring-system-restore"></a>Configurazione ripristino configurazione di sistema

Ripristino configurazione di sistema utilizza [Strumentazione gestione Windows](/windows/desktop/WmiSdk/wmi-start-page) (WMI) per fornire uno script per la configurazione e l'utilizzo delle relative funzionalità. Espone due classi, [**SystemRestore**](systemrestore.md) e [**SystemRestoreConfig**](systemrestoreconfig.md), nello \\ spazio dei nomi predefinito radice.

La classe [**SystemRestore**](systemrestore.md) fornisce i metodi per le attività seguenti:

-   Disabilitazione e abilitazione del monitoraggio
-   Elenco di punti di ripristino disponibili
-   Avvio di un ripristino nel sistema locale
-   Recupero dello stato dell'ultimo ripristino di sistema

La classe [**SystemRestoreConfig**](systemrestoreconfig.md) fornisce le proprietà per controllare la frequenza di creazione di punti di ripristino pianificati e la quantità di spazio su disco utilizzata da ripristino configurazione di sistema in ogni unità.

È possibile accedere a entrambe le classi in modalità remota utilizzando tecniche WMI standard. Per una descrizione completa di WMI, vedere [Strumentazione gestione Windows](/windows/desktop/WmiSdk/wmi-start-page).

 

 