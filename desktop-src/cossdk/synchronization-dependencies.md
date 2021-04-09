---
description: I valori di sincronizzazione possono essere determinati o vincolati automaticamente dalla configurazione di altre proprietà, ad esempio i requisiti transazionali e l'attivazione JIT (just-in-Time).
ms.assetid: 16771121-cb10-42b4-babc-59270188495a
title: Dipendenze di sincronizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c139d0d6e78288b25e42bd0a84b29432cebb44ca
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877613"
---
# <a name="synchronization-dependencies"></a>Dipendenze di sincronizzazione

I valori di sincronizzazione possono essere determinati o vincolati automaticamente dalla configurazione di altre proprietà, ad esempio i requisiti transazionali e l'attivazione JIT (just-in-Time). COM+, ad esempio, impone la sincronizzazione sia per i componenti transazionali che per quelli attivati da JIT.

Queste dipendenze sono dovute al fatto che i componenti che sono attivati tramite JIT o che partecipano alle transazioni devono avere un comportamento di isolamento e concorrenza appropriato. Per questo motivo, COM+ richiede che l'accesso a questi componenti venga serializzato tramite l'applicazione della sincronizzazione. Per informazioni dettagliate su queste dipendenze, vedere [attivazione JIT (just-in-Time](com--just-in-time-activation.md)) di com+.

Nelle tabelle seguenti sono illustrate le caratteristiche dei valori degli attributi di sincronizzazione COM+.

### <a name="transactional-requirement"></a>Requisito transazionale



| Quando le transazioni sono impostate su | La sincronizzazione può essere impostata su                    |
|------------------------------|--------------------------------------------------|
| Disabled<br/>          | Qualsiasi elemento, a seconda dell'attivazione JIT<br/> |
| Non supportato<br/>     | Qualsiasi elemento, a seconda dell'attivazione JIT<br/> |
| Supportato<br/>         | Obbligatoria<br/>                              |
| Obbligatoria<br/>          | Obbligatoria<br/>                              |
| RequiresNew<br/>      | Obbligatorio o richiede nuovo<br/>              |



 

### <a name="jit-activation"></a>Attivazione JIT



| Quando l'attivazione JIT è impostata su | La sincronizzazione può essere impostata su       |
|-------------------------------|-------------------------------------|
| Abilitato<br/>            | Obbligatorio o richiede nuovo<br/> |
| Disabled<br/>           | Nulla<br/>                 |



 

Per informazioni più dettagliate sul comportamento delle transazioni, dell'attivazione JIT e degli attributi di sincronizzazione, vedere [Configuring Transactions](configuring-transactions.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Impostazione dell'attributo di sincronizzazione](setting-the-synchronization-attribute.md)
</dt> <dt>

[Valori degli attributi di sincronizzazione](synchronization-attribute-values.md)
</dt> </dl>

 

 




