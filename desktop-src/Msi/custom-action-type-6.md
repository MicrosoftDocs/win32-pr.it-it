---
description: Gli sviluppatori di Windows Installer pacchetti possono scegliere di utilizzare un'azione personalizzata di tipo 6 quando le azioni standard non sono sufficienti per eseguire l'installazione.
ms.assetid: d63449e1-231a-4601-b39e-1b69857ccb86
title: Tipo di azione personalizzata 6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 007cd224caff801592bdde7389cfe3e77820f650
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314299"
---
# <a name="custom-action-type-6"></a>Tipo di azione personalizzata 6

Questa azione personalizzata è scritta in VBScript. Per ulteriori informazioni, vedere [script](scripts.md).

## <a name="source"></a>Source (Sorgente)

Lo script viene generato da un flusso binario temporaneo. Il campo di origine della [tabella CustomAction](customaction-table.md) contiene una chiave per la [tabella binaria](binary-table.md). La colonna di dati nella tabella binaria contiene i dati del flusso. Per ogni riga viene allocato un flusso separato.

I nuovi dati binari possono essere inseriti da un file usando [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) seguito da [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) per inserire il record nella tabella. Quando viene richiamata l'azione personalizzata, i dati del flusso vengono copiati in un file temporaneo, che viene quindi elaborato a seconda del tipo di azione personalizzata.

## <a name="type-value"></a>Valore tipo

Includere il valore seguente nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare il tipo numerico di base di un'azione personalizzata a 32 bit.



| Costanti                                                               | Valore esadecimale | Decimal |
|-------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeVBScript**  +  **msidbCustomActionTypeBinaryData** | 0x006       | 6       |



 

Windows Installer possibile utilizzare azioni personalizzate a 64 bit sui sistemi operativi a 64 bit. Un'azione personalizzata a 64 bit basata sugli script deve includere il bit **msidbCustomActionType64BitScript** nel tipo numerico. Per informazioni, vedere [azioni personalizzate a 64 bit](64-bit-custom-actions.md). Includere il valore seguente nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare il tipo numerico di base di un'azione personalizzata a 64 bit.



| Costanti                                                                                                      | Valore esadecimale | Decimal |
|----------------------------------------------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeVBScript**  +  **msidbCustomActionTypeBinaryData**  +  **msidbCustomActionType64BitScript** | 0x0001006   | 4102    |



 

## <a name="target"></a>Destinazione

Il campo di destinazione della [tabella CustomAction](customaction-table.md) contiene una funzione script facoltativa. L'elaborazione invia innanzitutto lo script per l'analisi e quindi chiama la funzione script facoltativa.

## <a name="return-processing-options"></a>Opzioni di elaborazione restituite

Includere i bit di flag facoltativi nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare le opzioni di elaborazione della restituzione. Per una descrizione delle opzioni e dei valori, vedere [Opzioni di elaborazione della restituzione di un'azione personalizzata](custom-action-return-processing-options.md).

## <a name="execution-scheduling-options"></a>Opzioni di pianificazione dell'esecuzione

Includere i bit di flag facoltativi nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare le opzioni di pianificazione dell'esecuzione. Queste opzioni controllano la multipla esecuzione di azioni personalizzate. Per una descrizione delle opzioni, vedere [Opzioni di pianificazione dell'esecuzione dell'azione personalizzata](custom-action-execution-scheduling-options.md).

## <a name="in-script-execution-options"></a>Opzioni di esecuzione In-Script

Includere i bit di flag facoltativi nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare un'opzione di esecuzione in-script. Queste opzioni copiano il codice dell'azione nello script di esecuzione, rollback o commit. Per una descrizione delle opzioni, vedere [azione personalizzata In-Script opzioni di esecuzione](custom-action-in-script-execution-options.md).

## <a name="return-values"></a>Valori restituiti

Le funzioni facoltative scritte nello script devono restituire uno dei valori descritti in [valori restituiti di azioni personalizzate JScript e VBScript](return-values-of-jscript-and-vbscript-custom-actions.md).

## <a name="remarks"></a>Commenti

Un'azione personalizzata scritta in JScript o VBScript richiede l'installazione dell' [**oggetto Session**](session-object.md). Il programma di installazione associa l'oggetto **sessione** allo script con la *sessione* del nome. Poiché l'oggetto **Session** potrebbe non esistere durante il rollback dell'installazione, un'azione personalizzata posticipata scritta nello script deve usare uno dei metodi o delle proprietà dell'oggetto **Session** descritto nella sezione recupero delle [informazioni di contesto per le azioni personalizzate di esecuzione posticipata](obtaining-context-information-for-deferred-execution-custom-actions.md) per recuperare il contesto.

Quando viene esportata una tabella di database, ogni flusso viene scritto come file separato nella sottocartella denominata dopo la tabella, utilizzando la chiave primaria come nome file (colonna nome per la tabella binaria), con un'estensione predefinita ". IBD". Il nome deve usare il formato del nome file 8,3 Se il file system o il sistema di controllo della versione non supporta nomi di file lunghi. Il file di archivio permanente sostituisce i dati del flusso con il nome file utilizzato, in modo che i dati possano essere individuati quando la tabella viene importata.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[\_Azioni personalizzate](custom-actions.md)
</dt> </dl>

 

 



