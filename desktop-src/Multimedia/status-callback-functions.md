---
title: Funzioni di callback di stato
description: Funzioni di callback di stato
ms.assetid: fe89fb97-0b56-4956-a1a6-f4ad2d06befa
keywords:
- Funzioni di callback AVICap, stato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f07539b016ea344f2a38d54a7274d01006532ed040ea3fa96990bff09e22d470
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037161"
---
# <a name="status-callback-functions"></a>Funzioni di callback di stato

Una finestra di acquisizione può inviare messaggi alla funzione di callback di stato durante l'acquisizione di video su disco o durante altre operazioni di lunga durata per notificare all'applicazione lo stato di un'operazione. Le informazioni sullo stato includono un identificatore di messaggio e una stringa di testo formattata pronta per la visualizzazione. L'applicazione può usare l'identificatore del messaggio per filtrare le notifiche e limitare i messaggi da presentare all'utente. Durante le operazioni di acquisizione, il primo messaggio inviato alla funzione di callback è sempre IDS CAP BEGIN e l'ultimo è \_ \_ sempre IDS CAP \_ \_ END. Un identificatore di messaggio pari a zero indica che è in corso una nuova operazione e che la funzione di callback deve cancellare lo stato corrente.

 

 




