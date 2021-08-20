---
description: La composizione predittiva è un'applicazione che in genere viene eseguita in un server di telefonia del call center.
ms.assetid: c8d0b2b5-61eb-4ab0-b09d-c54c282b730e
title: Composizione predittiva
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d930a0a49751c7f1851600e277d2cf201f0acbe1a9da3f7be5aa9f2e4b38439c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060599"
---
# <a name="predictive-dialing"></a>Composizione predittiva

La composizione predittiva è un'applicazione che in genere viene eseguita in un server di telefonia del call center. Usa un elenco di numeri di telefono, spesso ottenuti da un database, per tentare le chiamate in uscita. Quando una chiamata viene *completata,* la chiamata viene assegnata automaticamente a un agente per la gestione. L'applicazione può usare  una porta di composizione predittiva su un commutatore, ovvero un dispositivo in grado di effettuare chiamate in uscita e con capacità speciali (tramite DSP e così via) di rilevare i toni di avanzamento delle chiamate e altre indicazioni udibili dello stato della chiamata. Quando una chiamata viene effettuata su una porta di composizione predittiva, in genere viene trasferita automaticamente a un altro dispositivo sul commutatore quando la chiamata raggiunge uno stato specifico o al rilevamento di un particolare tipo di supporto; questo dispositivo di destinazione può essere una coda per gli agenti che gestisce le chiamate in uscita.

Le applicazioni identificano un dispositivo come con funzionalità di composizione predittiva dal bit LINEADDRCAPFLAGS PREDICTIVEDIALER nel membro \_ **dwAddrCapFlags** in [**LINEADDRESSCAPS.**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) Il **membro dwPredictiveAutoTransferStates** in **LINEADDRESSCAPS** indica gli stati su cui è possibile eseguire il comando della porta di composizione predittiva per trasferire automaticamente una chiamata. Se questo membro è zero, indica che il trasferimento automatico non è disponibile e che è responsabilità dell'applicazione trasferire le chiamate in modo esplicito al rilevamento dello stato di chiamata appropriato (o del tipo di supporto o di altri criteri). Preferibilmente, i produttori di commutatore renderanno disponibile il trasferimento automatico e manuale e consentiranno alle applicazioni di selezionare il meccanismo preferito, ma i provider di servizi devono modellare il comportamento delle apparecchiature legacy. Una singola porta di composizione predittiva (dispositivo/indirizzo di linea) può supportare l'esecuzione simultanea di più chiamate in uscita, come indicato dal membro **dwMaxNumActiveCalls** in **LINEADDRESSCAPS.** La funzionalità di composizione predittiva può essere resa disponibile anche in qualsiasi dispositivo, usando un pool condiviso di processori di segnali di composizione predittiva, che vengono con bridge sulla linea da comporre su richiesta.

Quando la funzione [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) viene usata su una linea in grado di effettuare una composizione predittiva (una porta con l'opzione LINEADDRCAPFLAGS PREDICTIVEDIALER impostata) e la composizione predittiva viene richiesta usando \_ LINECALLPARAMFLAGS PREDICTIVEDIAL, la chiamata viene effettuata in modo predittivo con rilevamento dello stato di avanzamento delle chiamate acustico \_ avanzato. I campi e le costanti aggiuntivi sono definiti nella struttura [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) passata a **lineMakeCall** per controllare il comportamento della porta di composizione predittiva. Il membro **dwPredictiveAutoTransferStates** indica gli stati di chiamata di riga che, all'ingresso della chiamata in uno di essi, la porta di composizione predittiva deve trasferire automaticamente la chiamata alla destinazione designata (i bit devono essere un subset corretto degli stati di trasferimento automatico supportati indicati in [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)); L'applicazione può lasciare il campo impostato su 0 se vuole monitorare gli stati di chiamata e usare [**lineBlindTransfer**](/windows/desktop/api/Tapi/nf-tapi-lineblindtransfer) per trasferire la chiamata quando raggiunge la condizione desiderata. L'applicazione deve specificare l'indirizzo desiderato a cui deve essere trasferita automaticamente la chiamata nel campo della variabile definito dai membri **dwTargetAddressSize** e **dwTargetAddressOffset** in **LINECALLPARAMS.**

Le applicazioni possono anche impostare un timeout per le chiamate in uscita in modo che il provider di servizi le esezioni automaticamente a uno stato disconnesso in caso di risposta non disponibile. Questa operazione viene controllata tramite **il membro dwNoAnswerTimeout** in [**LINECALLPARAMS.**](/windows/desktop/api/Tapi/ns-tapi-linecallparams)

 

 



