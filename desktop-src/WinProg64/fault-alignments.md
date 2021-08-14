---
title: Errori di allineamento
description: Errori di allineamento
ms.assetid: 16e69aec-3aec-4684-bf37-b3e5db6e4f87
keywords:
- errori di allineamento a 64 bit Windows programmazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d813a47cb3428c57ee6235442491f26f8d126a997dd7fcfa6844d551e7958b92
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119412911"
---
# <a name="alignment-faults"></a>Errori di allineamento

Il gestore degli errori di allineamento del sistema è disattivato per impostazione predefinita nei sistemi basati su Itanium. Pertanto, qualsiasi accesso ai dati non allineato genera un'eccezione che non verrà corretta automaticamente dal sistema a meno che l'applicazione non rileva l'eccezione in un gestore di eccezioni basato [su frame.](/windows/desktop/Debug/frame-based-exception-handling) Per abilitare la gestione degli errori di allineamento del sistema, chiamare la [**funzione SetErrorMode**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-seterrormode) **con SEM \_ NOALIGNMENTFAULTEXCEPT.** Si noti tuttavia che i processi possono avere una riduzione significativa delle prestazioni se il gestore degli errori di allineamento del sistema è abilitato e il processo genera errori di allineamento.

Se il debugger WinDbg è stato installato come debugger di sistema, WinDbg verrà avviato automaticamente se un processo nel sistema genera un'eccezione non gestita. Se non è installato un debugger come debugger di sistema, il sistema visualizza una finestra di dialogo che indica che l'applicazione ha rilevato un errore e offre la possibilità di segnalare il problema a Microsoft.

Nei sistemi x64 e ARM64 gli eventuali errori di allineamento vengono gestiti da una combinazione di hardware e software. Per ottenere prestazioni ottimali, tutti gli accessi alla memoria devono essere allineati correttamente. Inoltre, è consigliabile evitare l'accesso non allineato alle variabili [interlocked](/windows/desktop/Sync/interlocked-variable-access) in ARM64, perché queste operazioni non sono atomico-safe.

 

 