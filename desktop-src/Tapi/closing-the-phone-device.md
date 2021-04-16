---
description: La funzione phoneClose chiude il dispositivo telefonico specificato.
ms.assetid: 7607d779-0715-48a3-a4f2-bcf07026d7c5
title: Chiusura del dispositivo telefonico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f137004e63b4b377e9ee88266d11f9c2b21d0af7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527234"
---
# <a name="closing-the-phone-device"></a>Chiusura del dispositivo telefonico

La funzione [**phoneClose**](/windows/desktop/api/Tapi/nf-tapi-phoneclose) chiude il dispositivo telefonico specificato. Il dispositivo telefonico può anche essere chiuso forzatamente dopo che l'utente ha modificato la configurazione del telefono o del driver. Se l'utente desidera che le modifiche di configurazione vengano applicate immediatamente (a differenza di dopo il successivo riavvio del sistema) e influiscono sulla visualizzazione corrente dell'applicazione del dispositivo (ad esempio una modifica delle funzionalità del dispositivo), un provider di servizi può chiudere forzatamente il dispositivo telefonico.

Questi messaggi possono anche essere inviati non richiesti a causa del mancato rimborso del dispositivo telefonico in un altro modo. Un'applicazione deve pertanto essere preparata a gestire messaggi di [**\_ chiusura telefono**](phone-close.md) non richiesti. Al momento della chiusura del dispositivo telefonico, tutte le risposte asincrone in sospeso relative a tale dispositivo vengono cancellate.

 

 



