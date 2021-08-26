---
description: Gli sviluppatori di Windows pacchetti del programma di installazione possono scegliere di usare un'azione personalizzata di tipo 2 quando le azioni standard non sono sufficienti per eseguire l'installazione.
ms.assetid: 79ae0582-c991-4c0a-860b-0f5197ad0c7c
title: Tipo di azione personalizzata 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba648578ecdd9d300a5cf15793e3abd9407f78853830f49c16a26db184ff3683
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996851"
---
# <a name="custom-action-type-2"></a>Tipo di azione personalizzata 2

Questa azione personalizzata chiama un eseguibile avviato con una riga di comando.

## <a name="source"></a>Source (Sorgente)

L'eseguibile viene generato da un flusso binario temporaneo. Il campo Source della [tabella CustomAction](customaction-table.md) contiene una chiave per la [tabella Binary](binary-table.md). La colonna Data nella tabella Binary contiene i dati del flusso. Per ogni riga viene allocato un flusso separato.

È possibile inserire nuovi dati binari da un file usando [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) seguito da [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) per inserire il record nella tabella. Quando viene richiamata l'azione personalizzata, i dati del flusso vengono copiati in un file temporaneo, che viene quindi elaborato a seconda del tipo di azione personalizzata.

## <a name="type-value"></a>Valore del tipo

Includere il valore seguente nella colonna Tipo della tabella [CustomAction per](customaction-table.md) specificare il tipo numerico di base.



| Costanti                                                          | Valore esadecimale | Decimal |
|--------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeExe**  +  **msidbCustomActionTypeBinaryData** | 0x002       | 2       |



 

## <a name="target"></a>Destinazione

La colonna Target della [tabella CustomAction contiene](customaction-table.md) la stringa della riga di comando per il file eseguibile denominato nella colonna Source.

## <a name="return-processing-options"></a>Opzioni di elaborazione restituite

Includere i bit di flag facoltativi nella colonna Tipo della tabella CustomAction per specificare le opzioni di elaborazione restituite. Per una descrizione delle opzioni e dei valori, vedere [Custom Action Return Processing Options](custom-action-return-processing-options.md).

## <a name="execution-scheduling-options"></a>Opzioni di pianificazione dell'esecuzione

Includere i bit di flag facoltativi nella colonna Tipo della tabella CustomAction per specificare le opzioni di pianificazione dell'esecuzione. Queste opzioni controllano l'esecuzione multipla di azioni personalizzate. Per una descrizione delle opzioni, vedere [Opzioni di pianificazione dell'esecuzione di azioni personalizzate](custom-action-execution-scheduling-options.md).

## <a name="in-script-execution-options"></a>In-Script opzioni di esecuzione

Includere bit di flag facoltativi nella colonna Tipo della tabella CustomAction per specificare un'opzione di esecuzione nello script. Queste opzioni copiano il codice azione nello script di esecuzione, rollback o commit. Per una descrizione delle opzioni, vedere [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).

## <a name="return-values"></a>Valori restituiti

Le azioni personalizzate che sono [file eseguibili](executable-files.md) devono restituire il valore 0 per l'esito positivo. Il programma di installazione interpreta qualsiasi altro valore restituito come errore. Per ignorare i valori restituiti, impostare il flag di bit **msidbCustomActionTypeContinue** nel campo Tipo della tabella CustomAction.

## <a name="remarks"></a>Commenti

Un'azione personalizzata che avvia un eseguibile accetta una riga di comando, che in genere contiene proprietà designate dinamicamente. Se si tratta [](deferred-execution-custom-actions.md)anche di un'azione personalizzata di esecuzione posticipata, il programma di installazione usa [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) o [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) per creare il processo quando l'azione personalizzata viene richiamata dallo script di installazione.

Quando viene esportata una tabella di database, ogni flusso viene scritto come file separato nella sottocartella denominata dopo la tabella, usando la chiave primaria come nome file (colonna Nome per la tabella binaria), con estensione predefinita ".ibd". Il nome deve usare il formato 8.3 se il file system o il sistema di controllo della versione non supporta nomi di file lunghi. Il file di archivio permanente sostituisce i dati del flusso con il nome file usato, in modo che i dati possano essere individuati quando la tabella viene importata.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Azioni \_ personalizzate](custom-actions.md)
</dt> <dt>

[File eseguibili](executable-files.md)
</dt> </dl>

 

 
