---
description: Gli sviluppatori di Windows Installer pacchetti possono scegliere di utilizzare un tipo di azione personalizzato 35 quando le azioni standard non sono sufficienti per eseguire l'installazione.
ms.assetid: b88b5f48-5353-4876-9dda-2eeda288fa4b
title: Tipo di azione personalizzata 35
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8401f26f40ccc7de811ea0d290d556789284680f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318287"
---
# <a name="custom-action-type-35"></a>Tipo di azione personalizzata 35

Questa azione personalizzata imposta la directory di installazione da una stringa di testo formattata. Per ulteriori informazioni, vedere [modifica del percorso di destinazione per una directory](changing-the-target-location-for-a-directory.md)

## <a name="source"></a>Source (Sorgente)

Il campo di origine della [tabella CustomAction](customaction-table.md) contiene una chiave per la [tabella di directory](directory-table.md). La directory designata viene impostata dalla stringa formattata nel campo di destinazione usando [**MsiSetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha). In questo modo, il percorso di destinazione e la proprietà associata vengono impostati sul valore espanso della stringa di testo formattata nel campo di destinazione. Non tentare di modificare il percorso di una directory di destinazione durante un' [installazione di manutenzione](maintenance-installation.md). Non tentare di modificare il percorso della directory di destinazione se alcuni componenti che usano tale percorso sono già installati per qualsiasi utente.

## <a name="type-value"></a>Valore tipo

Includere il valore seguente nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare il tipo numerico di base.



| Costanti                                                              | Valore esadecimale | Decimal |
|------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeTextData**  +  **msidbCustomActionTypeDirectory** | 0x023       | 35      |



 

## <a name="target"></a>Destinazione

La colonna di destinazione della [tabella CustomAction](customaction-table.md) contiene una stringa di testo formattata utilizzando la funzionalità specificata in [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) (senza gli identificatori dei campi numerici). I parametri da sostituire sono racchiusi tra parentesi quadre \[ ... \] e possono essere proprietà, variabili di ambiente (% prefix), percorsi di file ( \# prefisso) o percorsi di directory dei componenti ($ prefix). Si noti che i percorsi di directory terminano sempre con un separatore di directory.

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

 

 



