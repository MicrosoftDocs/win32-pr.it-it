---
title: Pianificazione comandi
description: A ogni comando è associata una priorità.
ms.assetid: 63f6ba9d-0b87-403b-916b-aa8550f98a11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06512f0748aa88f6b32de3291e2ed1c262212ba2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298397"
---
# <a name="command-scheduling"></a>Pianificazione comandi

## <a name="command-scheduling"></a>Pianificazione comandi

I comandi possono essere inviati a TBS da più contesti in qualsiasi momento. Tuttavia, un TPM fisico può elaborare un solo comando alla volta e alcuni comandi possono essere eseguiti per un periodo di tempo significativo. Quando più comandi sono in sospeso, TBS decide quale comando inviare al TPM. Quando viene inviato un comando, a ogni comando è associata una priorità. TBS usa queste priorità per determinare quale comando in sospeso inviare ogni volta che il TPM è libero. I quattro livelli di priorità sono low, Normal, High e System. Le applicazioni devono utilizzare la priorità bassa, normale o alta. Anche se i comandi ad alta priorità vengono in genere eseguiti prima di quelli con priorità bassa, l'utilità di pianificazione dei comandi di TBS dispone di un criterio di invecchiamento che fornisce una priorità molto elevata ai comandi che sono stati bloccati per periodi di tempo significativi.

## <a name="context-management"></a>Gestione del contesto

Quando un \_ comando TPM SaveContext o TPM2 ContextSave viene inviato con un handle virtuale a una risorsa gestita da TBS, TBS esegue il comando appropriato sulla risorsa fisica e restituisce il risultato al chiamante se la risorsa è fisicamente presente nel TPM. Se la risorsa non è fisicamente presente nel TPM, la pre-elaborazione del \_ comando TPM SaveContext o TPM2 \_ ContextSave causa il ricaricamento della risorsa, a quel punto il contesto verrà salvato e restituito al chiamante. Se la risorsa salvata è di un tipo che in genere viene scaricata automaticamente dal TPM dopo il salvataggio, il comando TBS invalida la risorsa virtuale al completamento di questo comando. Quando un \_ comando TPM LoadContext o TPM2 \_ ContextLoad viene inviato a TBS, il comando viene eseguito immediatamente da TBS. Se il comando viene completato correttamente, TBS virtualizza l'handle di risorsa e passa il flusso di byte TPM risultante al chiamante. Quando un \_ comando TPM FlushSpecific o TPM2 \_ FlushContext viene inviato con un handle virtuale a una risorsa gestita da TBS, TBS esegue un \_ comando TPM FlushSpecific o TPM2 \_ FlushContext per rimuovere la risorsa dal TPM se è fisicamente presente. In questo caso, TBS invalida la risorsa virtuale e restituisce il risultato del comando flush al chiamante. Se la risorsa non è fisicamente presente nel TPM, la pre-elaborazione del \_ comando TPM FlushSpecific o TPM2 \_ FlushContext caricherà la risorsa corrispondente all'handle virtuale, che verrà quindi scaricata quando il comando verrà effettivamente elaborato. TBS non supporta il \_ bit KEYCONTROLOWNER TPM o la funzionalità keepHandle dell' \_ operazione LoadContext TPM, quindi non fornirà a una risorsa lo stesso handle prima del salvataggio del contesto.

## <a name="other-commands"></a>Altri comandi

I comandi che non vengono citati in questa documentazione vengono elaborati sostituendo gli handle di chiave virtuale con handle di chiave fisici (se necessario) e inviando questi ultimi al TPM. Questa operazione viene eseguita dopo l'esecuzione delle operazioni appropriate per garantire che le risorse utilizzate siano fisicamente presenti sul TPM. Non viene eseguita alcuna elaborazione speciale aggiuntiva. TBS non tenta di migliorare la fedeltà della virtualizzazione modificando i dati passati dal TPM come parte di una \_ query GetCapabilities o TPM2 \_ GetCapability del TPM. TBS supporta anche i comandi di presenza fisica TCG. TBS funge da pass-through per i comandi di presenza fisica. non viene eseguita alcuna elaborazione speciale da TBS.

## <a name="cleanup"></a>Pulizia

Quando si esce da un contesto, viene eseguita la pulizia di tutte le risorse fisiche e virtuali associate, in modo che non utilizzino più risorse di sistema.

 

 




