---
description: Usare i flag di opzione seguenti per specificare che il programma di installazione non scrive il valore immesso nel campo Target della tabella CustomAction nel log. Per impostare l'opzione, aggiungere il valore in questa tabella al valore nel campo Tipo della tabella CustomAction.
ms.assetid: b0f99851-a774-4804-8c85-f94943c2d2b0
title: Opzione di destinazione nascosta dell'azione personalizzata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1adc0df477510ac7d5d6bec65025b6fed1bfd7971e6ddf35da3a7e4cbc714690
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118638164"
---
# <a name="custom-action-hidden-target-option"></a>Opzione di destinazione nascosta dell'azione personalizzata

Usare i flag di opzione seguenti per specificare che il programma di installazione non scrive il valore immesso nel campo Target della tabella [CustomAction](customaction-table.md) nel log. Per impostare l'opzione, aggiungere il valore in questa tabella al valore nel campo Tipo della tabella CustomAction.



| Costante                            | Valore esadecimale | Decimal | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------|-------------|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| (nessuna)                              | 0x0000      | 0       | Il programma di installazione può scrivere il valore nella colonna Target della tabella CustomAction nel file di log.                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| **msidbCustomActionTypeHideTarget** | 0x2000      | 8192    | Al programma di installazione non è consentito scrivere il valore nella colonna Target della [tabella CustomAction](customaction-table.md) nel file di log. Anche la proprietà CustomActionData non viene registrata quando il programma di installazione esegue l'azione personalizzata.<br/> Poiché il programma di installazione imposta il valore di CustomActionData da una proprietà con lo stesso nome dell'azione personalizzata, tale proprietà deve essere elencata nella proprietà [**MsiHiddenProperties**](msihiddenproperties.md) per impedirne la visualizzazione nel log.<br/> |



 

Per altre informazioni, vedere [Impedire la scrittura di informazioni](preventing-confidential-information-from-being-written-into-the-log-file.md) riservate nel file di log

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su azioni personalizzate](custom-action-reference.md)
</dt> <dt>

[Informazioni sulle azioni personalizzate](about-custom-actions.md)
</dt> <dt>

[Uso di azioni personalizzate](using-custom-actions.md)
</dt> </dl>

 

 




