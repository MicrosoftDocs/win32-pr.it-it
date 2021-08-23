---
description: Gli sviluppatori di Windows pacchetti del programma di installazione possono scegliere di usare un'azione personalizzata di tipo 35 quando le azioni standard non sono sufficienti per eseguire l'installazione.
ms.assetid: b88b5f48-5353-4876-9dda-2eeda288fa4b
title: Tipo di azione personalizzata 35
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a724fa5a7fc469ea688c64e5935242f088c010da02d963f2f1dc4b05f5eb5e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947969"
---
# <a name="custom-action-type-35"></a>Tipo di azione personalizzata 35

Questa azione personalizzata imposta la directory di installazione da una stringa di testo formattata. Per altre informazioni, vedere [Modifica del percorso di destinazione per una directory](changing-the-target-location-for-a-directory.md)

## <a name="source"></a>Source (Sorgente)

Il campo Source della [tabella CustomAction](customaction-table.md) contiene una chiave per la [tabella Directory](directory-table.md). La directory designata viene impostata dalla stringa formattata nel campo Target usando [**MsiSetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha). In questo modo il percorso di destinazione e la proprietà associata vengono impostate sul valore espanso della stringa di testo formattata nel campo Destinazione. Non tentare di modificare il percorso di una directory di destinazione durante [un'installazione di manutenzione.](maintenance-installation.md) Non tentare di modificare il percorso della directory di destinazione se alcuni componenti che usano tale percorso sono già installati per qualsiasi utente.

## <a name="type-value"></a>Valore del tipo

Includere il valore seguente nella colonna Tipo della tabella [CustomAction per](customaction-table.md) specificare il tipo numerico di base.



| Costanti                                                              | Valore esadecimale | Decimal |
|------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeTextData**  +  **msidbCustomActionTypeDirectory** | 0x023       | 35      |



 

## <a name="target"></a>Destinazione

La colonna Target della [tabella CustomAction](customaction-table.md) contiene una stringa di testo formattata usando la funzionalità specificata in [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) (senza gli identificatori di campo numerici). I parametri da sostituire sono racchiusi tra parentesi quadre ... e possono essere proprietà, variabili di ambiente (% prefisso), percorsi di file (prefisso) o percorsi di directory dei componenti \[ \] \# (prefisso $). Si noti che i percorsi di directory terminano sempre con un separatore di directory.

## <a name="return-processing-options"></a>Opzioni di elaborazione restituite

L'azione personalizzata non usa queste opzioni.

## <a name="execution-scheduling-options"></a>Opzioni di pianificazione dell'esecuzione

Includere bit di flag facoltativi nella colonna Tipo della [tabella CustomAction per](customaction-table.md) specificare le opzioni di pianificazione dell'esecuzione. Queste opzioni controllano l'esecuzione multipla di azioni personalizzate. Per una descrizione delle opzioni, vedere [Opzioni di pianificazione dell'esecuzione di azioni personalizzate](custom-action-execution-scheduling-options.md).

## <a name="in-script-execution-options"></a>In-Script opzioni di esecuzione

L'azione personalizzata non usa queste opzioni.

## <a name="return-values"></a>Valori restituiti

Vedere [Valori restituiti dell'azione personalizzata](custom-action-return-values.md).

## <a name="remarks"></a>Commenti

Se si imposta una [proprietà privata](private-properties.md) nella sequenza dell'interfaccia utente mediante la creazione di un'azione personalizzata in una delle tabelle della sequenza dell'interfaccia utente, tale proprietà non viene impostata nella sequenza di esecuzione. Per impostare la proprietà nella sequenza di esecuzione, è necessario inserire anche un'azione personalizzata in una tabella della sequenza di esecuzione. In alternativa, è possibile impostare la proprietà come [proprietà pubblica](public-properties.md) e includerla nella [**proprietà SecureCustomProperties**](securecustomproperties.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Azioni \_ personalizzate](custom-actions.md)
</dt> <dt>

[Azioni personalizzate del testo formattato](formatted-text-custom-actions.md)
</dt> </dl>

 

 



