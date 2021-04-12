---
title: Funzioni di callback dello stato
description: Funzioni di callback dello stato
ms.assetid: fe89fb97-0b56-4956-a1a6-f4ad2d06befa
keywords:
- Funzioni di callback AVICap, stato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40b4b4bf4cad5f689f1e146986f9d1b55b00f1aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395983"
---
# <a name="status-callback-functions"></a>Funzioni di callback dello stato

Una finestra di acquisizione può inviare messaggi alla funzione di callback dello stato durante l'acquisizione del video su disco o durante altre operazioni lunghe per notificare all'applicazione lo stato di avanzamento di un'operazione. Le informazioni sullo stato includono un identificatore del messaggio e una stringa di testo formattata pronta per la visualizzazione. L'applicazione può utilizzare l'identificatore del messaggio per filtrare le notifiche e limitare i messaggi da presentare all'utente. Durante le operazioni di acquisizione, il primo messaggio inviato alla funzione di callback è sempre \_ il limite di ID \_ iniziale e l'ultimo è sempre l'estremità del limite degli ID \_ \_ . Un identificatore di messaggio zero indica che è in corso l'avvio di una nuova operazione e che la funzione di callback deve cancellare lo stato corrente.

 

 




