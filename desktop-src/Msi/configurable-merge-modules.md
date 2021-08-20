---
description: I moduli unione (file con estensione msm) possono essere creati per contenere attributi configurabili dal consumer del modulo unione.
ms.assetid: 461436f0-3a91-4a49-934a-f975bf13df40
title: Moduli unione configurabili
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0ca110b45e1ec9bd28662c24440124bb75d0dde73d6e425146e8be640ae2de5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118144270"
---
# <a name="configurable-merge-modules"></a>Moduli unione configurabili

I moduli unione (file con estensione msm) possono essere creati per contenere attributi configurabili dal consumer del modulo unione. In questo modo il modulo unione può essere configurato nel momento in cui il pacchetto di installazione e il modulo vengono uniti e installati dall'utente finale. I moduli unione configurabili Mergemod.dll versione 2.0, ma possono essere eseguiti in qualsiasi versione Windows Installer.

L'implementazione di moduli unione configurabili è costituita da due parti. In primo luogo, quando si crea il modulo unione (file con estensione msm), l'autore del modulo unione aggiunge al database del modulo informazioni che specificano quali elementi possono essere modificati e come questi elementi possono essere configurati dall'utente del modulo. L'autore aggiunge le voci alle tabelle di [database](merge-module-database-tables.md) del modulo unione riservate alle informazioni configurabili ([tabella ModuleConfiguration](moduleconfiguration-table.md) e [tabella ModuleSubstitution](modulesubstitution-table.md)), aggiorna la tabella [ \_ Validation](-validation-table.md)e aggiunge voci per le tabelle del modulo unione configurabili alla tabella [ModuleIgnoreTable](moduleignoretable-table.md). Le aggiunte alla tabella ModuleIgnore sono necessarie per rendere il modulo compatibile con Mergemod.dll precedenti alla 2.0.

In secondo piano, quando si unisce il modulo in un pacchetto di installazione (file .msi), l'utente finale del modulo usa uno strumento di unione. Lo strumento di unione chiama Mergemod.dll per esporre le informazioni di configurazione nel modulo a uno strumento di configurazione client. Lo strumento di configurazione può interagire con l'utente finale, ma non è necessario per esporre tutte le possibili opzioni di configurazione. Se l'utente rifiuta di fornire una selezione per un elemento configurabile, il modulo può fornire un valore predefinito. Dopo che l'utente ha selezionato lo strumento di configurazione, lo strumento di merge chiama Mergemod.dll per eseguire l'unione.

I moduli unione configurabili sono completamente compatibili con gli strumenti precedenti Mergemod.dll versione 2.0. In questi casi, lo strumento usa i valori predefiniti nel modulo.

Per altre informazioni, vedere [Uso di moduli unione configurabili.](using-configurable-merge-modules.md)

 

 



