---
description: I valori di sincronizzazione possono essere determinati o vincolati automaticamente dalla configurazione di altre proprietà, ad esempio requisiti transazionali e attivazione JIT.
ms.assetid: 16771121-cb10-42b4-babc-59270188495a
title: Dipendenze di sincronizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed2976426d652ca50c4e7399f39e98ba13ef337d15ef8c15a2271d4a562d1790
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119499731"
---
# <a name="synchronization-dependencies"></a>Dipendenze di sincronizzazione

I valori di sincronizzazione possono essere determinati o vincolati automaticamente dalla configurazione di altre proprietà, ad esempio requisiti transazionali e attivazione JIT. Ad esempio, COM+ applica la sincronizzazione sia per i componenti transazionali che per i componenti attivati tramite JIT.

Queste dipendenze esistono perché i componenti attivati tramite JIT o che partecipano alle transazioni devono avere un comportamento di isolamento e concorrenza appropriato. Com+ richiede quindi che l'accesso a questi componenti sia serializzato tramite l'applicazione della sincronizzazione. Per informazioni dettagliate su queste dipendenze, vedere [Attivazione just-in-time COM+.](com--just-in-time-activation.md)

Le tabelle seguenti illustrano le caratteristiche dei valori degli attributi di sincronizzazione COM+.

### <a name="transactional-requirement"></a>Requisito transazionale



| Quando le transazioni sono impostate su | La sincronizzazione può essere impostata su                    |
|------------------------------|--------------------------------------------------|
| Disabled<br/>          | Qualsiasi elemento, a seconda dell'attivazione JIT<br/> |
| Non supportato<br/>     | Qualsiasi elemento, a seconda dell'attivazione JIT<br/> |
| Supportato<br/>         | Obbligatoria<br/>                              |
| Obbligatoria<br/>          | Obbligatoria<br/>                              |
| RequiresNew<br/>      | Obbligatorio o nuovo<br/>              |



 

### <a name="jit-activation"></a>Attivazione JIT



| Quando l'attivazione JIT è impostata su | La sincronizzazione può essere impostata su       |
|-------------------------------|-------------------------------------|
| Attivato<br/>            | Obbligatorio o nuovo<br/> |
| Disabled<br/>           | Nulla<br/>                 |



 

Per altre informazioni sul comportamento degli attributi di transazione, attivazione JIT e sincronizzazione, vedere [Configurazione delle transazioni](configuring-transactions.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Impostazione dell'attributo di sincronizzazione](setting-the-synchronization-attribute.md)
</dt> <dt>

[Valori degli attributi di sincronizzazione](synchronization-attribute-values.md)
</dt> </dl>

 

 




