---
description: Per applicare un aggiornamento principale tramite il programma di installazione di Windows, il pacchetto di installazione del prodotto originale deve specificare una proprietà UpgradeCode, descritta in Preparazione di un'applicazione per gli aggiornamenti principali futuri, e il pacchetto di aggiornamento deve avere una tabella di aggiornamento.
ms.assetid: 041f5bab-cb13-4e17-8465-484bcd3c6957
title: Aggiornamento della tabella di aggiornamento per un aggiornamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba65db43019c09e27824c54265244c65b900e4f3c94dacd24405e7fac2e0272a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809751"
---
# <a name="updating-upgrade-table-for-an-upgrade"></a>Aggiornamento della tabella di aggiornamento per un aggiornamento

Per applicare un aggiornamento principale tramite il programma di installazione di Windows, il pacchetto di installazione del prodotto originale deve specificare una proprietà [**UpgradeCode,**](upgradecode.md) descritta [in](preparing-an-application-for-future-major-upgrades.md)Preparazione di un'applicazione per gli aggiornamenti principali futuri, e il pacchetto di aggiornamento deve avere una tabella [di](upgrade-table.md)aggiornamento .

Per altre informazioni sugli aggiornamenti principali, vedere [Aggiornamenti principali](major-upgrades.md) in Applicazione di patch [e aggiornamenti.](patching-and-upgrades.md)

Al pacchetto di installazione MNP2000.msi è stata assegnata [**una proprietà UpgradeCode,**](upgradecode.md) come descritto nella sezione [Specifica delle proprietà](specifying-properties.md).

Windows Il programma di installazione applica l'aggiornamento se l'utente ha già installato le versioni da 1.0 a 1.4 (incluse) dell'MNP2000 in lingua inglese. Windows Il programma di installazione esegue la migrazione di tutte le impostazioni delle funzionalità del prodotto originale al prodotto aggiornato. Il programma di installazione rimuove i file appartenenti ai prodotti originali non usati dall'aggiornamento del prodotto.

Se la copia di MNP2001.msi non include una tabella [di](upgrade-table.md)aggiornamento, usare Orca o un altro editor di tabelle per importare una tabella di aggiornamento vuota nel database da Schema.msi. L'SDK fornisce una copia dei Schema.msi. Usare l'editor di database per MNP2001.msi e immettere i dati seguenti nella tabella Upgrade vuota.



| Codice di aggiornamento                            | VersionMin | VersionMax | Linguaggio | Attributi | Rimuovi | ActionProperty |
|----------------------------------------|------------|------------|----------|------------|--------|----------------|
| {908E378A-9551-4772-BF1D-5CFAF6FD9CB4} | 01.00.0000 | 01.40.0000 | 1033     | 769        |        | OLDAPPFOUND    |



 

[Continua](updating-properties-for-an-upgrade.md)

 

 



