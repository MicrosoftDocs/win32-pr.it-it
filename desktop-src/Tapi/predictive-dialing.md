---
description: La composizione predittiva è un'applicazione che in genere viene eseguita in un server di telefonia del Call Center.
ms.assetid: c8d0b2b5-61eb-4ab0-b09d-c54c282b730e
title: Composizione predittiva
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 576ebffff5d4b9925fd50ecce082e4f515065c5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316041"
---
# <a name="predictive-dialing"></a>Composizione predittiva

La composizione predittiva è un'applicazione che in genere viene eseguita in un server di telefonia del Call Center. Usa un elenco di numeri di telefono, spesso ottenuti da un database, per tentare le chiamate in uscita; Quando una chiamata viene *completata*, la chiamata viene assegnata automaticamente a un agente per la gestione. L'applicazione può usare una porta di *Composizione predittiva* in un compartitore, ovvero un dispositivo che può effettuare chiamate in uscita e avere capacità speciali (tramite DSP e così via) per rilevare i toni di avanzamento delle chiamate e altre indicazioni acustiche dello stato della chiamata. Quando viene effettuata una chiamata su una porta di composizione predittiva, viene in genere trasferita automaticamente a un altro dispositivo nel compartimento quando la chiamata raggiunge un determinato stato o al rilevamento di un particolare tipo di supporto. Questo dispositivo di destinazione può essere una coda per gli agenti che gestiscono le chiamate in uscita.

Le applicazioni identificano un dispositivo come avente la funzionalità di composizione predittiva del \_ bit LINEADDRCAPFLAGS PREDICTIVEDIALER nel membro **DwAddrCapFlags** in [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps). Il membro **dwPredictiveAutoTransferStates** in **LINEADDRESSCAPS** indica gli Stati su cui è possibile eseguire il comando della porta di composizione predittiva per trasferire automaticamente una chiamata; Se questo membro è zero, indica che il trasferimento automatico non è disponibile e che è responsabilità dell'applicazione trasferire le chiamate in modo esplicito durante il rilevamento dello stato di chiamata appropriato (o il tipo di supporto o altri criteri). Preferibilmente, i costruttori comportano la disponibilità di trasferimenti automatici e manuali e consentono alle applicazioni di selezionare il meccanismo preferito, ma i provider di servizi dovrebbero modellare il comportamento delle apparecchiature legacy. Una singola porta di composizione predittiva (dispositivo/Indirizzo linea) può supportare l'esecuzione simultanea di più chiamate in uscita, come indicato dal membro **dwMaxNumActiveCalls** in **LINEADDRESSCAPS**. La funzionalità di composizione predittiva può anche essere resa disponibile su qualsiasi dispositivo, usando un pool condiviso di processori di segnali di composizione predittiva, che vengono ponticellati sulla riga in fase di richiesta.

Quando la funzione [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) viene utilizzata su una riga in grado di comporre Predictive (una porta con il \_ set di PREDICTIVEDIALER LINEADDRCAPFLAGS) e la composizione predittiva viene richiesta utilizzando LINECALLPARAMFLAGS \_ PREDICTIVEDIAL, la chiamata viene eseguita in modo predittivo con il rilevamento dello stato di avanzamento delle chiamate acustico migliorato. Campi e costanti aggiuntivi vengono definiti nella struttura [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) passata a **lineMakeCall** per controllare il comportamento della porta di composizione predittiva. Il membro **dwPredictiveAutoTransferStates** indica che la chiamata di riga dichiara che, al momento dell'immissione della chiamata in uno di essi, la porta di composizione predittiva deve trasferire automaticamente la chiamata alla destinazione designata. i bit devono essere un subset appropriato degli Stati di trasferimento automatico supportati indicati in [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps). l'applicazione può lasciare il campo impostato su 0 se desidera monitorare gli Stati di chiamata e usare [**lineBlindTransfer**](/windows/desktop/api/Tapi/nf-tapi-lineblindtransfer) per trasferire la chiamata quando raggiunge la condizione desiderata. L'applicazione deve specificare l'indirizzo desiderato a cui la chiamata deve essere trasferita automaticamente nel campo variabile definito dai membri **dwTargetAddressSize** e **dwTargetAddressOffset** in **LINECALLPARAMS**.

Le applicazioni possono inoltre impostare un timeout per le chiamate in uscita, in modo che il provider di servizi ne esegua automaticamente la transizione a uno stato disconnesso se non viene risposto. Questa operazione viene controllata usando il membro **dwNoAnswerTimeout** in [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams).

 

 



