---
description: Gli sviluppatori di Windows Installer pacchetti possono scegliere di utilizzare un tipo di azione personalizzata 2 quando le azioni standard non sono sufficienti per eseguire l'installazione.
ms.assetid: 79ae0582-c991-4c0a-860b-0f5197ad0c7c
title: Tipo di azione personalizzata 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0497b2a76dc2fac7f5e56f7347b50deac867757f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315476"
---
# <a name="custom-action-type-2"></a>Tipo di azione personalizzata 2

Questa azione personalizzata chiama un eseguibile avviato con una riga di comando.

## <a name="source"></a>Source (Sorgente)

Il file eseguibile viene generato da un flusso binario temporaneo. Il campo di origine della [tabella CustomAction](customaction-table.md) contiene una chiave per la [tabella binaria](binary-table.md). La colonna di dati nella tabella binaria contiene i dati del flusso. Per ogni riga viene allocato un flusso separato.

I nuovi dati binari possono essere inseriti da un file usando [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) seguito da [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) per inserire il record nella tabella. Quando viene richiamata l'azione personalizzata, i dati del flusso vengono copiati in un file temporaneo, che viene quindi elaborato a seconda del tipo di azione personalizzata.

## <a name="type-value"></a>Valore tipo

Includere il valore seguente nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare il tipo numerico di base.



| Costanti                                                          | Valore esadecimale | Decimal |
|--------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeExe**  +  **msidbCustomActionTypeBinaryData** | 0x002       | 2       |



 

## <a name="target"></a>Destinazione

La colonna di destinazione della [tabella CustomAction](customaction-table.md) contiene la stringa della riga di comando per il file eseguibile denominato nella colonna di origine.

## <a name="return-processing-options"></a>Opzioni di elaborazione restituite

Includere i bit di flag facoltativi nella colonna Type della tabella CustomAction per specificare le opzioni di elaborazione della restituzione. Per una descrizione delle opzioni e dei valori, vedere [Opzioni di elaborazione della restituzione di un'azione personalizzata](custom-action-return-processing-options.md).

## <a name="execution-scheduling-options"></a>Opzioni di pianificazione dell'esecuzione

Includere i bit di flag facoltativi nella colonna Type della tabella CustomAction per specificare le opzioni di pianificazione dell'esecuzione. Queste opzioni controllano la multipla esecuzione di azioni personalizzate. Per una descrizione delle opzioni, vedere [Opzioni di pianificazione dell'esecuzione dell'azione personalizzata](custom-action-execution-scheduling-options.md).

## <a name="in-script-execution-options"></a>Opzioni di esecuzione In-Script

Includere i bit di flag facoltativi nella colonna Type della tabella CustomAction per specificare un'opzione di esecuzione in-script. Queste opzioni copiano il codice dell'azione nello script di esecuzione, rollback o commit. Per una descrizione delle opzioni, vedere [azione personalizzata In-Script opzioni di esecuzione](custom-action-in-script-execution-options.md).

## <a name="return-values"></a>Valori restituiti

Per l'esito positivo, le azioni personalizzate che sono [file eseguibili](executable-files.md) devono restituire un valore pari a 0. Il programma di installazione interpreta qualsiasi altro valore restituito come errore. Per ignorare i valori restituiti, impostare il flag di bit **msidbCustomActionTypeContinue** nel campo Type della tabella CustomAction.

## <a name="remarks"></a>Commenti

Un'azione personalizzata che avvia un file eseguibile accetta una riga di comando, che in genere contiene proprietà designate dinamicamente. Se si tratta anche di un' [azione personalizzata di esecuzione posticipata](deferred-execution-custom-actions.md), il programma di installazione utilizza [**CreateProcessAsUser ha**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) o [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) per creare il processo quando viene richiamata l'azione personalizzata dallo script di installazione.

Quando viene esportata una tabella di database, ogni flusso viene scritto come file separato nella sottocartella denominata dopo la tabella, utilizzando la chiave primaria come nome file (colonna nome per la tabella binaria), con un'estensione predefinita ". IBD". Il nome deve usare il formato 8,3 Se il sistema di controllo della versione o file system non supporta nomi di file lunghi. Il file di archivio permanente sostituisce i dati del flusso con il nome file utilizzato, in modo che i dati possano essere individuati quando la tabella viene importata.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[\_Azioni personalizzate](custom-actions.md)
</dt> <dt>

[File eseguibili](executable-files.md)
</dt> </dl>

 

 
