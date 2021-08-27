---
description: Gli sviluppatori di Windows Installer possono scegliere di usare un tipo di azione personalizzata 51 quando le azioni standard non sono sufficienti per eseguire l'installazione.
ms.assetid: cdad16ad-426c-4e04-8003-b32c67be7329
title: Tipo di azione personalizzata 51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e780c1a38b60c855f4bfe665f5f68a3f6a037a078f4a2875d1a2ea57c5e7e8dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075051"
---
# <a name="custom-action-type-51"></a>Tipo di azione personalizzata 51

Questa azione personalizzata imposta una proprietà da una stringa di testo formattata.

Per influire su una proprietà usata in una condizione di un componente o di una funzionalità, l'azione personalizzata deve essere eseguita prima dell'azione [CostFinalize](costfinalize-action.md) nella sequenza di azione.

## <a name="source"></a>Source (Sorgente)

Il campo Source della [tabella CustomAction](customaction-table.md) può contenere il nome di una proprietà o una chiave per la [tabella Property](property-table.md). Questa proprietà viene impostata dalla stringa formattata nel campo Target usando [**MsiSetProperty.**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya)

## <a name="type-value"></a>Valore tipo

Includere il valore seguente nella colonna Type della tabella [CustomAction per](customaction-table.md) specificare il tipo numerico di base.



| Costanti                                                             | Valore esadecimale | Decimal |
|-----------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeTextData**  +  **msidbCustomActionTypeProperty** | 0x033       | 51      |



 

## <a name="target"></a>Destinazione

La colonna Target della [tabella CustomAction](customaction-table.md) contiene una stringa di testo formattata usando la funzionalità specificata in [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) (senza gli identificatori di campo numerico). I parametri da sostituire sono racchiusi tra parentesi quadre, ... e possono essere proprietà, variabili di ambiente (prefisso %), percorsi di file (prefisso) o percorsi di \[ \] directory dei componenti \# (prefisso $).

## <a name="return-processing-options"></a>Opzioni di elaborazione dei valori restituiti

L'azione personalizzata non usa queste opzioni.

## <a name="execution-scheduling-options"></a>Opzioni di pianificazione dell'esecuzione

Includere bit di flag facoltativi nella colonna Tipo della [tabella CustomAction per](customaction-table.md) specificare le opzioni di pianificazione dell'esecuzione. Queste opzioni controllano l'esecuzione multipla di azioni personalizzate. Per una descrizione delle opzioni, vedere [Opzioni di pianificazione dell'esecuzione di azioni personalizzate.](custom-action-execution-scheduling-options.md)

## <a name="in-script-execution-options"></a>In-Script opzioni di esecuzione

L'azione personalizzata non usa queste opzioni.

## <a name="return-values"></a>Valori restituiti

Vedere [Valori restituiti dell'azione personalizzata.](custom-action-return-values.md)

## <a name="remarks"></a>Commenti

Se si imposta una [proprietà](private-properties.md) privata nella sequenza dell'interfaccia utente mediante la creazione di un'azione personalizzata in una delle tabelle di sequenza dell'interfaccia utente, tale proprietà non viene impostata nella sequenza di esecuzione. Per impostare la proprietà nella sequenza di esecuzione, è necessario inserire anche un'azione personalizzata in una tabella della sequenza di esecuzione. In alternativa, è possibile impostare la proprietà come [proprietà pubblica](public-properties.md) e includerla nella [**proprietà SecureCustomProperties**](securecustomproperties.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Azioni \_ personalizzate](custom-actions.md)
</dt> <dt>

[Azioni personalizzate di testo formattato](formatted-text-custom-actions.md)
</dt> </dl>

 

 



