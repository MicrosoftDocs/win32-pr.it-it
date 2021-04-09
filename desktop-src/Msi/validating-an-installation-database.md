---
description: Gli autori dei pacchetti di installazione devono sempre eseguire la convalida sui pacchetti prima di tentare di installare il pacchetto per la prima volta ed eseguire di nuovo la convalida ogni volta che vengono apportate modifiche al pacchetto.
ms.assetid: 1f16a349-4919-46d2-9b78-2533b8679a73
title: Convalida di un database di installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6db262a280afa1d9222696d40a6f5949d69ece0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878537"
---
# <a name="validating-an-installation-database"></a>Convalida di un database di installazione

Gli autori dei pacchetti di installazione devono sempre eseguire la convalida sui pacchetti prima di tentare di installare il pacchetto per la prima volta ed eseguire di nuovo la convalida ogni volta che vengono apportate modifiche al pacchetto. La convalida esegue l'analisi del database per individuare eventuali errori che possono apparire validi singolarmente, ma che provocano un comportamento non corretto nel contesto dell'intero database. Il tentativo di installare un pacchetto che non riesce a eseguire la convalida può danneggiare il sistema dell'utente. Vedere le sezioni [convalida dei pacchetti](package-validation.md) e [analizzatori di coerenza interni-CIEM](internal-consistency-evaluators-ices.md).

È possibile convalidare il pacchetto di esempio utilizzando [Orca.exe](orca-exe.md) o [Msival2.exe](msival2-exe.md). Per visualizzare la guida per Msival2.exe modificare le directory e immettere nella riga di comando.

Msival2 -?

Il file con estensione cub Darice. cub contiene le azioni personalizzate ICE richieste da Msival2.exe per eseguire la convalida. Per convalidare il MNP2000.msi immettere

MSIVal2 MNP2000.msi Darice. cub

Per una descrizione dei messaggi di errore e di avviso restituiti dalla convalida, vedere la Guida di [riferimento a Ice](ice-reference.md). Correggere tutti gli errori nel pacchetto ed eseguire di nuovo la convalida se necessario finché il pacchetto non supera la convalida senza errori.

Una volta che il pacchetto ha superato la convalida, è possibile installare il pacchetto di esempio facendo clic sull'icona MNP2000.msi o dalla riga di comando usando le [Opzioni della riga di comando](command-line-options.md).

Questa operazione completa l'installazione di esempio.

## <a name="next-example"></a>Esempio successivo

[Esempio di aggiornamento](an-upgrade-example.md)

 

 



