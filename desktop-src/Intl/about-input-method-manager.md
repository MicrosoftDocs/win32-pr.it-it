---
description: L'uso della funzionalità IMM nell'applicazione in grado di riconoscere gli IME consente agli utenti di ricordare tutti i possibili valori di caratteri.
ms.assetid: 43b3e561-b844-4688-ab3d-d99f92ed140e
title: Informazioni su Gestione metodi di input
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af7b96c64eba5ddfb6966c96d88792fd657f94aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314311"
---
# <a name="about-input-method-manager"></a>Informazioni su Gestione metodi di input

L'uso della funzionalità IMM nell'applicazione in grado di riconoscere gli IME consente agli utenti di ricordare tutti i possibili valori di caratteri. Consente invece di monitorare le sequenze di tasti di un utente, prevedere i caratteri desiderati dall'utente e presentare un elenco di caratteri candidati da cui scegliere.

> [!Note]  
> IMM esegue operazioni simili a quelle del Framework dei [servizi di testo](../tsf/text-services-framework.md), utilizzate da applicazioni che comunicano con i servizi di testo.

 

Per impostazione predefinita, IMM fornisce una finestra IME tramite cui l'utente immette le sequenze di tasti e le visualizzazioni e seleziona i candidati. Le applicazioni possono utilizzare le funzioni e i messaggi di IMM per creare e gestire le proprie finestre IME, offrendo un'interfaccia personalizzata utilizzando le funzionalità di conversione dell'IME.

IMM è abilitato solo nei sistemi operativi Windows localizzati nell'Asia orientale (cinese, giapponese, coreano). In questi sistemi, l'applicazione chiama [GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) con SM \_ DBCSENABLED per determinare se IMM è abilitato.

**Windows 2000:** Il supporto di IMM completo è disponibile in tutte le versioni in lingua localizzata. Tuttavia, l'IMM è abilitato solo quando viene installato un Language Pack asiatico. Un'applicazione che supporta IME può chiamare [GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) con SM \_ IMMENABLED per determinare se IMM è abilitato.

In questo argomento sono contenute le sezioni seguenti.

-   [Elenchi candidati](candidate-lists.md)
-   [Stringa di composizione](composition-string.md)
-   [IME HexToUnicode](hextounicode-ime.md)
-   [Hot Keys](hot-keys.md)
-   [Messaggi IME](ime-messages.md)
-   [Classe della finestra IME](ime-window-class.md)
-   [Contesto di input](input-context.md)
-   [Finestre stato, composizione e candidati](status--composition--and-candidates-windows.md)

 

 
