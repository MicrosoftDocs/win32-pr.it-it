---
description: Le app possono attendere un evento quando il rendering sullo schermo non è necessario, ovvero quando sono bloccati.
ms.assetid: B9EC23C9-A311-4BD9-BBE8-908A1334A541
title: In attesa di un evento quando il rendering non è necessario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b553ef52e812c5117e5d9669ba13b47b9f4280c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303670"
---
# <a name="waiting-on-an-event-when-rendering-is-unnecessary"></a>In attesa di un evento quando il rendering non è necessario

Le app possono attendere un evento quando il rendering sullo schermo non è necessario, ovvero quando sono bloccati. Quando il Gestione finestre desktop (DWM) o un'app è bloccato, non è necessario eseguire il rendering e il sistema operativo può rimanere in uno stato di alimentazione inferiore per periodi di tempo più lunghi. Questo consente di risparmiare energia ed estendere la durata della batteria.

Un'app può attendere un evento nei casi seguenti:

-   Tutti i monitoraggi sono disattivati.
-   La sessione in cui viene eseguita l'app è disconnessa.
-   L'app viene eseguita a schermo intero esclusivamente in una singola configurazione di monitoraggio.
-   L'app viene eseguita su un desktop diverso rispetto al desktop attivo e non dispone dell'autorizzazione per eseguire il rendering sul desktop attivo.

Il sistema operativo attiva l'evento quando l'app è in grado di eseguire nuovamente il rendering. L'evento non viene cancellato durante un aggiornamento del driver o la processi di rilevamento e ripristino del timeout (TDR), ma viene cancellato quando il nuovo adapter e i monitoraggi diventano attivi.

Se si vuole che l'app riceva una notifica sulle modifiche dello stato di occlusione, l'app deve registrarsi per tali modifiche. Un'app può registrarsi per ricevere notifiche sulle modifiche dello stato di occlusione tramite un messaggio a una finestra o tramite la segnalazione degli eventi. Per eseguire la registrazione per ricevere messaggi di notifica a una finestra in merito alle modifiche dello stato di occlusione, un'app chiama il metodo [**IDXGIFactory2:: RegisterOcclusionStatusWindow**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatuswindow) . Per eseguire la registrazione per ricevere la notifica delle modifiche dello stato di occlusione tramite segnalazione eventi, un'app chiama il metodo [**IDXGIFactory2:: RegisterOcclusionStatusEvent**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatusevent) . Entrambi i metodi restituiscono un puntatore a un valore di chiave che l'app può usare per annullare la registrazione della notifica. Per annullare la registrazione della notifica, l'app passa il valore della chiave al metodo [**IDXGIFactory2:: UnregisterOcclusionStatus**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-unregisterocclusionstatus) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Miglioramenti di DXGI 1,2](dxgi-1-2-improvements.md)
</dt> </dl>

 

 



