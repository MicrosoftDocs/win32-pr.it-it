---
description: I moduli unione (file MSM) possono essere creati per contenere attributi configurabili dall'utente del modulo merge.
ms.assetid: 461436f0-3a91-4a49-934a-f975bf13df40
title: Moduli merge configurabili
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 716688d947ae84279dc3409bf97abe4eb58a69d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319024"
---
# <a name="configurable-merge-modules"></a>Moduli merge configurabili

I moduli unione (file MSM) possono essere creati per contenere attributi configurabili dall'utente del modulo merge. In questo modo è possibile configurare il modulo merge nel momento in cui il pacchetto di installazione e il modulo vengono Uniti e installati dall'utente finale. I moduli merge configurabili richiedono Mergemod.dll versione 2,0, ma possono essere eseguiti in qualsiasi versione del Windows Installer.

L'implementazione dei moduli unione configurabili è costituita da due parti. In primo luogo, quando si crea il modulo merge (file MSM), l'autore del modulo merge aggiunge informazioni al database del modulo che specifica quali elementi possono essere modificati e come tali elementi possono essere configurati dall'utente del modulo. L'autore aggiunge voci alle [tabelle del database del modulo merge](merge-module-database-tables.md) riservate per le informazioni configurabili (tabella[ModuleConfiguration](moduleconfiguration-table.md) e [tabella ModuleSubstitution](modulesubstitution-table.md)), aggiorna la [ \_ tabella di convalida](-validation-table.md)e aggiunge voci per le tabelle del modulo merge configurabili alla [tabella ModuleIgnoreTable](moduleignoretable-table.md). Le aggiunte alla tabella ModuleIgnore sono necessarie per rendere il modulo compatibile con Mergemod.dll versioni precedenti alla 2,0.

In secondo luogo, quando si unisce il modulo in un pacchetto di installazione (file con estensione msi), l'utente finale del modulo usa uno strumento di merge. Lo strumento di merge chiama Mergemod.dll per esporre le informazioni di configurazione nel modulo a uno strumento di configurazione client. Lo strumento di configurazione può interagire con l'utente finale, ma non è necessario esporre tutte le opzioni di configurazione possibili. Se l'utente rifiuta di fornire una selezione per un elemento configurabile, il modulo potrebbe fornire un valore predefinito. Dopo che l'utente ha selezionato lo strumento di configurazione, lo strumento di merge chiama Mergemod.dll per eseguire il merge.

I moduli merge configurabili sono completamente compatibili con gli strumenti precedenti alla versione Mergemod.dll 2,0. In questi casi, lo strumento usa i valori predefiniti nel modulo.

Per ulteriori informazioni, vedere [utilizzo dei moduli unione configurabili](using-configurable-merge-modules.md).

 

 



