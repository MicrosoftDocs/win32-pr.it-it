---
description: Per applicare un aggiornamento principale mediante Windows Installer, il pacchetto di installazione del prodotto originale deve specificare una proprietà UpgradeCode, descritta in preparazione di un'applicazione per aggiornamenti principali futuri, e il pacchetto di aggiornamento deve disporre di una tabella di aggiornamento.
ms.assetid: 041f5bab-cb13-4e17-8465-484bcd3c6957
title: Aggiornamento della tabella di aggiornamento per un aggiornamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc1b4c2cc2b650d49fb4ba40f97d69ed84911273
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131195"
---
# <a name="updating-upgrade-table-for-an-upgrade"></a>Aggiornamento della tabella di aggiornamento per un aggiornamento

Per applicare un aggiornamento principale mediante Windows Installer, il pacchetto di installazione del prodotto originale deve specificare una proprietà [**UpgradeCode**](upgradecode.md) , descritta in [preparazione di un'applicazione per aggiornamenti principali futuri](preparing-an-application-for-future-major-upgrades.md), e il pacchetto di aggiornamento deve disporre di una [tabella di aggiornamento](upgrade-table.md).

Per ulteriori informazioni sugli aggiornamenti principali, vedere [aggiornamenti principali](major-upgrades.md) per l'applicazione di [patch e aggiornamenti](patching-and-upgrades.md).

Al pacchetto di installazione di MNP2000.msi è stata assegnata una proprietà [**UpgradeCode**](upgradecode.md) , come descritto nella sezione [specifica delle proprietà](specifying-properties.md).

Windows Installer applica l'aggiornamento se l'utente ha già installato le versioni da 1,0 a 1,4 (incluse) della lingua inglese MNP2000. Windows Installer esegue la migrazione di tutte le impostazioni della funzionalità del prodotto originale al prodotto aggiornato. Il programma di installazione rimuove i file appartenenti ai prodotti originali non usati dall'aggiornamento del prodotto.

Se la copia di MNP2001.msi non include una [tabella di aggiornamento](upgrade-table.md), utilizzare Orca o un altro editor di tabella per importare una tabella di aggiornamento vuota nel database da Schema.msi. L'SDK fornisce una copia di Schema.msi. Utilizzare l'editor di database per aprire MNP2001.msi e immettere i dati seguenti nella tabella di aggiornamento vuota.



| UpgradeCode                            | VersionMin | VersionMax | Linguaggio | Attributi | Rimuovi | ActionProperty |
|----------------------------------------|------------|------------|----------|------------|--------|----------------|
| {908E378A-9551-4772-BF1D-5CFAF6FD9CB4} | 01.00.0000 | 01.40.0000 | 1033     | 769        |        | OLDAPPFOUND    |



 

[Continua](updating-properties-for-an-upgrade.md)

 

 



