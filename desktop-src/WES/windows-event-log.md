---
title: Registro eventi di Windows
description: L Windows API registro eventi definisce lo schema utilizzato per scrivere un manifesto di strumentazione.
ms.assetid: 738c8afa-4714-4d4f-9231-b8fbdb5159c5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c4306ce9722aba5b06109265c71cf387af2b35f63aef1cec070936400fff61f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118587196"
---
# <a name="windows-event-log"></a>Registro eventi di Windows

## <a name="purpose"></a>Scopo

L Windows API registro eventi definisce lo schema utilizzato per scrivere un manifesto di strumentazione. Un manifesto di strumentazione identifica il provider di eventi e gli eventi registrati. L'API include anche le funzioni che un consumer di eventi, ad esempio il Visualizzatore eventi [,](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc766042(v=ws.11))userà per leggere ed eseguire il rendering degli eventi. Per scrivere gli eventi definiti nel manifesto, usare le funzioni incluse nell'API [Event Tracing](/windows/desktop/ETW/event-tracing-portal) (ETW).

Windows Il registro eventi sostituisce l'API [di registrazione eventi](/windows/desktop/EventLog/event-logging) a partire dal Windows sistema operativo Vista.

## <a name="developer-audience"></a>Sviluppatori

Windows Il registro eventi è progettato per i programmatori C/C++.

## <a name="run-time-requirements"></a>Requisiti di runtime

Windows Il registro eventi è incluso nel sistema operativo a partire da Windows Vista e Windows Server 2008.

Per informazioni sui requisiti di run-time per un particolare elemento di programmazione, vedere la sezione Requisiti della pagina di riferimento per tale elemento.

Per la cronologia delle versioni completa, [vedere Novità.](what-s-new.md)

## <a name="in-this-section"></a>Contenuto della sezione


| Argomento                                                        | Descrizione                                                                                       |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [Uso Windows registro eventi](using-windows-event-log.md)        | Guida procedurale che illustra come usare l'API Windows registro eventi.                                 |
| [Windows Informazioni di riferimento sul registro eventi](windows-event-log-reference.md)| Tipi di dati, funzioni, enumerazioni, strutture, costanti e schemi inclusi nell'API.|