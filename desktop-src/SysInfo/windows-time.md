---
description: Windows tempo è il numero di millisecondi trascorsi dall'ultimo avvio del sistema.
ms.assetid: 95c00204-bfdf-4376-9aae-8d8139ba6750
title: Ora di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 363f455842a144decc9db7f4d15fa3353b16e74290252b911a814eb62832a790
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118884047"
---
# <a name="windows-time"></a>Ora di Windows

*Windows tempo è* il numero di millisecondi trascorsi dall'ultimo avvio del sistema. Questo formato esiste principalmente per la compatibilità con le versioni precedenti con le versioni a 16 bit Windows. Per garantire che le applicazioni progettate per l'esecuzione Windows a 16 bit continuino a essere eseguite correttamente, la funzione [**GetTickCount**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) restituisce l'ora Windows corrente.

In genere si usa la [**funzione GetTickCount**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) o [**GetTickCount64**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount64) per confrontare l'ora Windows corrente con l'ora restituita dalla [**funzione GetMessageTime.**](/windows/win32/api/winuser/nf-winuser-getmessagetime) **GetMessageTime** restituisce il Windows momento in cui è stato creato il messaggio specificato. **GetTickCount** e **GetTickCount64** sono limitati alla risoluzione del timer di sistema, che è di circa 10 millisecondi a 16 millisecondi. Il tempo trascorso recuperato da GetTickCount o **GetTickCount64** include il tempo trascorso dal sistema in sospensione o ibernazione. 

Se è necessario un timer con risoluzione più elevata, usare la [**funzione QueryUnbiasedInterruptTime,**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) un [timer](/windows/desktop/Multimedia/multimedia-timers)multimediale o un timer ad [alta risoluzione.](../winmsg/about-timers.md) Il tempo trascorso recuperato dalla funzione **QueryUnbiasedInterruptTime** include solo il tempo trascorso dal sistema nello stato di lavoro.

**Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP/2000:** La [**funzione QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) è disponibile a partire da Windows 7 e Windows Server 2008 R2.

È possibile usare il contatore delle prestazioni Tempo di attività del sistema per ottenere il numero di secondi trascorsi dall'avvio del computer. Questo contatore delle prestazioni può essere recuperato dai dati sulle prestazioni nella chiave del Registro di sistema **HKEY \_ PERFORMANCE \_ DATA**. Il valore restituito è un valore a 8 byte. Per altre informazioni, vedere [i contatori delle prestazioni](/windows/desktop/PerfCtrs/performance-counters-portal).

 

 
