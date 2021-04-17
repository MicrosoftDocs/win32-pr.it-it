---
title: Errori di allineamento
description: Errori di allineamento
ms.assetid: 16e69aec-3aec-4684-bf37-b3e5db6e4f87
keywords:
- 'errori di allineamento: programmazione Windows a 64 bit'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 318a7a55010ac148354d000ece32c91a8652f821
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300290"
---
# <a name="alignment-faults"></a>Errori di allineamento

Il gestore degli errori di allineamento del sistema è disattivato per impostazione predefinita nei sistemi basati su Itanium. Pertanto, qualsiasi accesso ai dati non allineato genera un'eccezione che non verrà corretta automaticamente dal sistema, a meno che l'applicazione non riprenda l'eccezione in un [gestore di eccezioni basato su frame](/windows/desktop/Debug/frame-based-exception-handling). Per abilitare il gestore degli errori di allineamento del sistema, chiamare la funzione [**SetErrorMode**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-seterrormode) con **sem \_ NOALIGNMENTFAULTEXCEPT**. Si noti tuttavia che i processi possono comportare un peggioramento delle prestazioni se il gestore degli errori di allineamento del sistema è abilitato e il processo genera errori di allineamento.

Se il debugger WinDbg è stato installato come debugger di sistema, WinDbg verrà avviato automaticamente se un processo del sistema genera un'eccezione non gestita. Se non si dispone di un debugger installato come debugger del sistema, viene visualizzata una finestra di dialogo che informa che l'applicazione ha rilevato un errore e che è stata rilevata la possibilità di segnalare il problema a Microsoft.

Nei sistemi x64 e ARM64 tutti gli errori di allineamento vengono gestiti da una combinazione di hardware e software. Per ottenere prestazioni ottimali, tutti gli accessi alla memoria devono essere allineati correttamente. Inoltre, [l'accesso a variabili Interlocked](/windows/desktop/Sync/interlocked-variable-access) non allineate deve essere evitato su ARM64, poiché queste operazioni non sono atomiche.

 

 