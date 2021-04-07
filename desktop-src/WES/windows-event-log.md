---
title: Registro eventi di Windows
description: L'API registro eventi di Windows definisce lo schema usato per scrivere un manifesto di strumentazione.
ms.assetid: 738c8afa-4714-4d4f-9231-b8fbdb5159c5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b9df51efc878af2770ad056e6e1f84b8f4f2566
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872934"
---
# <a name="windows-event-log"></a>Registro eventi di Windows

## <a name="purpose"></a>Scopo

L'API registro eventi di Windows definisce lo schema usato per scrivere un manifesto di strumentazione. Un manifesto di strumentazione identifica il provider di eventi e gli eventi registrati. L'API include anche le funzioni utilizzate da un consumer di eventi, ad esempio il [Visualizzatore eventi](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc766042(v=ws.11)), per leggere ed eseguire il rendering degli eventi. Per scrivere gli eventi definiti nel manifesto, usare le funzioni incluse nell'API [traccia eventi](/windows/desktop/ETW/event-tracing-portal) (ETW).

Il registro eventi di Windows sostituisce l'API di [registrazione eventi](/windows/desktop/EventLog/event-logging) a partire dal sistema operativo Windows Vista.

## <a name="developer-audience"></a>Sviluppatori

Il registro eventi di Windows è progettato per i programmatori C/C++.

## <a name="run-time-requirements"></a>Requisiti di runtime

Il registro eventi di Windows è incluso nel sistema operativo a partire da Windows Vista e Windows Server 2008.

Per informazioni sui requisiti della fase di esecuzione per un particolare elemento di programmazione, vedere la sezione requisiti della pagina di riferimento per tale elemento.

Per la cronologia delle versioni completa [, vedere Novità](what-s-new.md).

## <a name="in-this-section"></a>Contenuto della sezione


| Argomento                                                        | Descrizione                                                                                       |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [Utilizzo del registro eventi di Windows](using-windows-event-log.md)        | Guida procedurale che illustra come usare l'API registro eventi di Windows.                                 |
| [Riferimento al registro eventi di Windows](windows-event-log-reference.md)| Tipi di dati, funzioni, enumerazioni, strutture, costanti e schemi inclusi nell'API.|