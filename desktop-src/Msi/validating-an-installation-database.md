---
description: Gli autori dei pacchetti di installazione devono sempre eseguire la convalida nei pacchetti prima di provare a installare il pacchetto per la prima volta ed eseguire di nuovo la convalida ogni volta che si apportano modifiche al pacchetto.
ms.assetid: 1f16a349-4919-46d2-9b78-2533b8679a73
title: Convalida di un database di installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d28d4d1937b5946d6c1df85a4c6c21ec8113ef6463b5aaad0e181f4bdc711e70
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995821"
---
# <a name="validating-an-installation-database"></a>Convalida di un database di installazione

Gli autori dei pacchetti di installazione devono sempre eseguire la convalida nei pacchetti prima di provare a installare il pacchetto per la prima volta ed eseguire di nuovo la convalida ogni volta che si apportano modifiche al pacchetto. La convalida analizza il database alla ricerca di errori che possono apparire validi singolarmente, ma che causano un comportamento non corretto nel contesto dell'intero database. Il tentativo di installare un pacchetto che non supera la convalida può danneggiare il sistema dell'utente. Vedere le sezioni [Convalida dei pacchetti](package-validation.md) e Analizzatori di [coerenza interna - ICE.](internal-consistency-evaluators-ices.md)

È possibile convalidare il pacchetto di esempio [ usandoOrca.exe](orca-exe.md) [ oMsival2.exe](msival2-exe.md). Per visualizzare la Guida per Msival2.exe directory delle modifiche e immettere nella riga di comando.

Msival2 -?

Il file con estensione cub darice.cub contiene le azioni personalizzate ICE necessarie Msival2.exe eseguire la convalida. Per convalidare il MNP2000.msi immettere

msival2 MNP2000.msi Darice.cub

Per una descrizione dei messaggi di errore e di avviso restituiti dalla convalida, vedere [le informazioni di riferimento ice](ice-reference.md). Correggere tutti gli errori nel pacchetto ed eseguire di nuovo la convalida in base alle esigenze finché il pacchetto non supera la convalida senza errori.

Dopo che il pacchetto ha superato la convalida, è possibile installare il pacchetto di esempio facendo clic sull'icona MNP2000.msi o dalla riga di comando usando le opzioni della riga [di comando](command-line-options.md).

Questa operazione completa l'installazione di esempio.

## <a name="next-example"></a>Esempio successivo

[Esempio di aggiornamento](an-upgrade-example.md)

 

 



