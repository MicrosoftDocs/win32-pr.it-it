---
description: Le app possono attendere un evento quando il rendering sullo schermo non è necessario( ovvero, mentre sono occluded).
ms.assetid: B9EC23C9-A311-4BD9-BBE8-908A1334A541
title: Attesa di un evento quando il rendering non è necessario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0db1aa4805aa1dde25947ed25c90d14c9f3c2f4c8693d3599f1382937ee0dbc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118517874"
---
# <a name="waiting-on-an-event-when-rendering-is-unnecessary"></a>Attesa di un evento quando il rendering non è necessario

Le app possono attendere un evento quando il rendering sullo schermo non è necessario( ovvero, mentre sono occluded). Quando il Gestione finestre desktop (DWM) o un'app è occluso, non è necessario alcun rendering e il sistema operativo può rimanere in stati di risparmio energia inferiori per periodi di tempo più lunghi. In questo modo è possibile risparmiare energia ed estendere la durata della batteria.

Un'app può attendere un evento quando:

-   Tutti i monitoraggi sono disattivati.
-   La sessione in cui viene eseguita l'app è disconnessa.
-   L'app viene eseguita a schermo intero esclusivamente in una configurazione a monitoraggio singolo.
-   L'app viene eseguita su un desktop diverso da quello attivo e non dispone dell'autorizzazione per il rendering sul desktop attivo.

Il sistema operativo attiva l'evento quando l'app è in grado di eseguire di nuovo il rendering. L'evento non viene cancellato durante l'aggiornamento di un driver o il rilevamento e il recupero del timeout (TDR), ma viene cancellato quando la nuova scheda e i nuovi monitoraggi diventano attivi.

Se si vuole che l'app invii una notifica sulle modifiche dello stato di occlusione, l'app deve registrarsi per queste modifiche. Un'app può registrarsi per ricevere una notifica sulle modifiche dello stato di occlusione tramite un messaggio in una finestra o tramite la segnalazione di eventi. Per registrarsi per ricevere messaggi di notifica in una finestra sulle modifiche dello stato di occlusione, un'app chiama il [**metodo IDXGIFactory2::RegisterOcclusionStatusWindow.**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatuswindow) Per registrarsi per ricevere la notifica delle modifiche dello stato di occlusione tramite la segnalazione degli eventi, un'app chiama il [**metodo IDXGIFactory2::RegisterOcclusionStatusEvent.**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatusevent) Entrambi i metodi restituiscono un puntatore a un valore di chiave che l'app può usare per annullare la registrazione della notifica. Per annullare la registrazione della notifica, l'app passa questo valore di chiave [**al metodo IDXGIFactory2::UnregisterOcclusionStatus.**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-unregisterocclusionstatus)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Miglioramenti di DXGI 1.2](dxgi-1-2-improvements.md)
</dt> </dl>

 

 



