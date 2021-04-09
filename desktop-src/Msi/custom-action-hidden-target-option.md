---
description: Usare i flag di opzione seguenti per specificare che il programma di installazione non scrive il valore immesso nel campo di destinazione della tabella CustomAction nel log. Per impostare l'opzione, aggiungere il valore di questa tabella al valore nel campo Type della tabella CustomAction.
ms.assetid: b0f99851-a774-4804-8c85-f94943c2d2b0
title: Opzione di destinazione nascosta azione personalizzata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acca69e4c3efc2b43302bf926a56bc53b2bf5e7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050155"
---
# <a name="custom-action-hidden-target-option"></a>Opzione di destinazione nascosta azione personalizzata

Usare i flag di opzione seguenti per specificare che il programma di installazione non scrive il valore immesso nel campo di destinazione della [tabella CustomAction](customaction-table.md) nel log. Per impostare l'opzione, aggiungere il valore di questa tabella al valore nel campo Type della tabella CustomAction.



| Costante                            | Valore esadecimale | Decimal | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------|-------------|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| (nessuna)                              | 0x0000      | 0       | Il programma di installazione può scrivere il valore nella colonna di destinazione della tabella CustomAction nel file di log.                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| **msidbCustomActionTypeHideTarget** | 0x2000      | 8192    | Al programma di installazione non è consentito scrivere il valore nella colonna di destinazione della [tabella CustomAction](customaction-table.md) nel file di log. Inoltre, la proprietà CustomActionData non viene registrata quando il programma di installazione esegue l'azione personalizzata.<br/> Poiché il programma di installazione imposta il valore di CustomActionData da una proprietà con lo stesso nome dell'azione personalizzata, tale proprietà deve essere elencata nella proprietà [**MsiHiddenProperties**](msihiddenproperties.md) per impedire che il relativo valore venga visualizzato nel log.<br/> |



 

Per ulteriori informazioni, vedere la pagina relativa alla [prevenzione della scrittura di informazioni riservate nel file di log](preventing-confidential-information-from-being-written-into-the-log-file.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento all'azione personalizzata](custom-action-reference.md)
</dt> <dt>

[Informazioni sulle azioni personalizzate](about-custom-actions.md)
</dt> <dt>

[Uso di azioni personalizzate](using-custom-actions.md)
</dt> </dl>

 

 




