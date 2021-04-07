---
description: L'ora di sistema è la data e l'ora correnti del giorno.
ms.assetid: 1a1e251e-2375-4134-bbd8-1e4670b9f9d2
title: Ora di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0c727e8898fc2bc973d963c3a3c90524ca50958
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885830"
---
# <a name="system-time"></a>Ora di sistema

L' *ora di sistema* è la data e l'ora correnti del giorno. Il sistema mantiene il tempo in modo che le applicazioni siano in grado di accedere all'ora esatta. Il sistema basa l'ora di sistema sull'ora UTC ( *Coordinated Universal Time* ). L'ora basata su UTC è definita in modo generico come data e ora correnti del giorno di Greenwich, Inghilterra.

Quando il sistema viene avviato per la prima volta, imposta l'ora di sistema su un valore basato sull'orologio in tempo reale del computer e quindi aggiorna regolarmente l'ora. Per recuperare l'ora di sistema, utilizzare la funzione [**GetSystemTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtime) . **GetSystemTime** copia il tempo in una struttura [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) che contiene singoli membri per mese, giorno, anno, giorno della settimana, ora, minuti, secondi e millisecondi. È facile visualizzare questo formato a un utente.

È anche possibile ottenere l'ora di sistema nel formato di ora file usando la funzione [**GetSystemTimeAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimeasfiletime) . **GetSystemTimeAsFileTime** copia l'ora in una struttura [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) .

Per impostare l'ora di sistema, utilizzare la funzione [**SetSystemTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setsystemtime) . **SetSystemTime** presuppone che sia stata specificata un'ora basata su UTC.

Le funzioni [**GetSystemTimeAdjustment**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimeadjustment) e [**SetSystemTimeAdjustment**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setsystemtimeadjustment) sincronizzano il clock dell'ora del giorno con un'altra origine ora usando una regolazione periodica dell'ora applicata a ogni interrupt del clock.

Si noti che il sistema può aggiornare periodicamente l'ora sincronizzando con un'origine dell'ora. Poiché l'ora di sistema può essere regolata in avanti o indietro, non confrontare le letture dell'ora di sistema per determinare il tempo trascorso. Usare invece uno dei metodi descritti in ora di [Windows](windows-time.md).

 

 
