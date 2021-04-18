---
description: Gli oggetti flusso sono un'astrazione del flusso multimediale o dei flussi associati a una sessione di chiamata.
ms.assetid: 4bd7a305-69ff-4892-bf03-df9c6479adab
title: Oggetti Stream
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eeb89dbacf73baaffbca9aa3791aa73937a69e80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314128"
---
# <a name="stream-objects"></a>Oggetti Stream

Gli oggetti flusso sono un'astrazione del flusso multimediale o dei flussi associati a una sessione di chiamata. Le interfacce e i metodi esposti negli oggetti flusso e sottoflusso consentono a un'applicazione di eseguire controlli molto dettagliati, ad esempio la sospensione di un flusso, l'aggiunta di nuovi tipi di supporti a una sessione di comunicazione o la modifica del volume audio di un particolare partecipante della conferenza.

I due tipi principali di flusso sono il flusso e il sottoflusso. Le interfacce e i metodi di un'implementazione standard sono simili per entrambi, ma il sottoflusso consente un livello di controllo più basso. Tutti i provider di servizi multimediali (MSPs) devono implementare le interfacce di controllo del flusso di base, ma il supporto per i flussi sottoflussi è facoltativo.

Alcuni provider di servizi implementano inoltre [interfacce specifiche del provider](provider-specific-interfaces.md) per i flussi. Ad esempio, l'MSP IPConf fornisce controlli a livello di partecipante. Per un riepilogo, vedere [IPConf msp Interfaces](ipconf-msp-interfaces.md) . Per altre interfacce che potrebbero essere implementate, vedere la documentazione del provider di servizi.

MSP e TAPI creano oggetti flusso per una chiamata durante la configurazione iniziale di una sessione in uscita o in ingresso. L'applicazione è responsabile dell'identificazione dei terminali appropriati per questi flussi e della selezione dei terminali sui flussi.

Si noti che in alcuni casi un MSP potrebbe richiedere che l'applicazione arresti o sospenda i flussi prima di determinate operazioni della sessione di chiamata.

Le interfacce di flusso sono documentate nel [riferimento MSPI (Media Service Provider Interface)](media-service-provider-interface-mspi-reference.md).

L'esempio [Select a Terminal](select-a-terminal.md) Code Mostra un esempio di enumerazione dei flussi e selezione di terminali su di essi.

 

 



