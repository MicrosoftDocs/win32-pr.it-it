---
description: Ora di Windows indica il numero di millisecondi trascorsi dall'ultimo avvio del sistema.
ms.assetid: 95c00204-bfdf-4376-9aae-8d8139ba6750
title: Ora di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33af776e2cc5a36993f6be0e0776d5b73fab6622
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131283"
---
# <a name="windows-time"></a>Ora di Windows

*Ora di Windows* indica il numero di millisecondi trascorsi dall'ultimo avvio del sistema. Questo formato esiste principalmente per la compatibilità con le versioni precedenti di Windows a 16 bit. Per garantire che le applicazioni progettate per Windows a 16 bit continuino a funzionare correttamente, la funzione [**GetTickCount**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) restituisce l'ora di Windows corrente.

In genere si usa la funzione [**GetTickCount**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) o [**GetTickCount64**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount64) per confrontare l'ora di Windows corrente con l'ora restituita dalla funzione [**GetMessageTime**](/windows/win32/api/winuser/nf-winuser-getmessagetime) . **GetMessageTime** restituisce l'ora di Windows in cui è stato creato il messaggio specificato. **GetTickCount** e **GetTickCount64** sono limitati alla risoluzione del timer di sistema, che è di circa 10 millisecondi per 16 millisecondi. Il tempo trascorso recuperato da **GetTickCount** o **GetTickCount64** include il tempo impiegato dal sistema per la sospensione o l'ibernazione.

Se è necessario un timer di risoluzione superiore, usare la funzione [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) , un [timer multimediale](/windows/desktop/Multimedia/multimedia-timers)o un [timer ad alta risoluzione](../winmsg/about-timers.md). Il tempo trascorso recuperato dalla funzione **QueryUnbiasedInterruptTime** include solo il tempo impiegato dal sistema nello stato di lavoro.

**Windows server 2008, Windows Vista, Windows server 2003 e Windows XP/2000:** La funzione [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) è disponibile a partire da Windows 7 e windows Server 2008 R2.

È possibile utilizzare il contatore delle prestazioni del tempo di sistema per ottenere il numero di secondi trascorsi dall'avvio del computer. Questo contatore delle prestazioni può essere recuperato dai dati sulle prestazioni nella chiave del registro di sistema **HKEY \_ \_ dati sulle prestazioni**. Il valore restituito è un valore a 8 byte. Per altre informazioni, vedere [i contatori delle prestazioni](/windows/desktop/PerfCtrs/performance-counters-portal).

 

 
