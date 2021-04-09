---
description: Gli sviluppatori di Windows Installer pacchetti possono scegliere di utilizzare un tipo di azione personalizzato 51 quando le azioni standard non sono sufficienti per eseguire l'installazione.
ms.assetid: cdad16ad-426c-4e04-8003-b32c67be7329
title: Tipo di azione personalizzata 51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef3224add3a425131ee3308bc4f610b086cd99a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968103"
---
# <a name="custom-action-type-51"></a>Tipo di azione personalizzata 51

Questa azione personalizzata imposta una proprietà da una stringa di testo formattata.

Per influenzare una proprietà utilizzata in una condizione su un componente o una funzionalità, l'azione personalizzata deve precedere l' [azione CostFinalize secondo](costfinalize-action.md) nella sequenza di azione.

## <a name="source"></a>Source (Sorgente)

Il campo di origine della [tabella CustomAction](customaction-table.md) può contenere il nome di una proprietà o una chiave per la [tabella delle proprietà](property-table.md). Questa proprietà viene impostata dalla stringa formattata nel campo di destinazione usando [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya).

## <a name="type-value"></a>Valore tipo

Includere il valore seguente nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare il tipo numerico di base.



| Costanti                                                             | Valore esadecimale | Decimal |
|-----------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeTextData**  +  **msidbCustomActionTypeProperty** | 0x033       | 51      |



 

## <a name="target"></a>Destinazione

La colonna di destinazione della [tabella CustomAction](customaction-table.md) contiene una stringa di testo formattata utilizzando la funzionalità specificata in [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) (senza gli identificatori dei campi numerici). I parametri da sostituire sono racchiusi tra parentesi quadre, \[ ... \] e possono essere proprietà, variabili di ambiente (% prefix), percorsi di file ( \# prefisso) o percorsi di directory dei componenti ($ prefix).

## <a name="return-processing-options"></a>Opzioni di elaborazione restituite

L'azione personalizzata non usa queste opzioni.

## <a name="execution-scheduling-options"></a>Opzioni di pianificazione dell'esecuzione

Includere i bit di flag facoltativi nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare le opzioni di pianificazione dell'esecuzione. Queste opzioni controllano la multipla esecuzione di azioni personalizzate. Per una descrizione delle opzioni, vedere [Opzioni di pianificazione dell'esecuzione dell'azione personalizzata](custom-action-execution-scheduling-options.md).

## <a name="in-script-execution-options"></a>Opzioni di esecuzione In-Script

L'azione personalizzata non usa queste opzioni.

## <a name="return-values"></a>Valori restituiti

Vedere [valori restituiti dell'azione personalizzata](custom-action-return-values.md).

## <a name="remarks"></a>Commenti

Se si imposta una [proprietà privata](private-properties.md) nella sequenza dell'interfaccia utente creando un'azione personalizzata in una delle tabelle di sequenza dell'interfaccia utente, tale proprietà non viene impostata nella sequenza di esecuzione. Per impostare la proprietà nella sequenza di esecuzione, è inoltre necessario inserire un'azione personalizzata in una tabella della sequenza di esecuzione. In alternativa, è possibile rendere la proprietà una [proprietà pubblica](public-properties.md) e includerla nella [**proprietà SecureCustomProperties**](securecustomproperties.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[\_Azioni personalizzate](custom-actions.md)
</dt> <dt>

[Azioni personalizzate del testo formattato](formatted-text-custom-actions.md)
</dt> </dl>

 

 



