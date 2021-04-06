---
title: Errore
description: Errore
ms.assetid: d3a087e4-7b57-4070-aa82-3673bc18a54f
keywords:
- Funzioni di callback AVICap, messaggi di notifica degli errori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f418f16ae2af15902e96927990d79a4ecac08b1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045133"
---
# <a name="error"></a>Errore

Una finestra di acquisizione usa i messaggi di notifica degli errori per notificare l'applicazione degli errori AVICap, ad esempio l'esaurimento dello spazio su disco, il tentativo di scrittura in un file di sola lettura, l'errore di accesso all'hardware o l'eliminazione di un numero eccessivo di frame. Il contenuto di una notifica di errore include un identificatore di messaggio e una stringa di testo formattata pronta per la visualizzazione. L'applicazione può utilizzare l'identificatore del messaggio per filtrare le notifiche e limitare i messaggi da presentare all'utente. Un identificatore di messaggio zero indica che è in corso l'avvio di una nuova operazione e che la funzione di callback deve cancellare qualsiasi messaggio di errore visualizzato.

 

 




