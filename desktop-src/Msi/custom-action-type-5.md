---
description: Gli sviluppatori di Windows Installer possono scegliere di usare un'azione personalizzata di tipo 5 quando le azioni standard non sono sufficienti per eseguire l'installazione.
ms.assetid: 32b10271-44b1-4c5d-9c8b-eed1b4cd31e2
title: Tipo di azione personalizzata 5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7e5d6ea37d8efcc5a5d9517b36fb3ae5620830ae1a84173cb9a5488c57cc24e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086221"
---
# <a name="custom-action-type-5"></a>Tipo di azione personalizzata 5

Questa azione personalizzata è scritta in JScript, ad esempio ECMA 262. Windows Il programma di installazione non supporta JScript 1.0. Per altre informazioni, vedere [Script.](scripts.md)

## <a name="source"></a>Source (Sorgente)

Lo script viene generato da un flusso binario temporaneo. Il campo Source della [tabella CustomAction contiene](customaction-table.md) una chiave per la [tabella Binary](binary-table.md). La colonna Data della tabella Binary contiene i dati del flusso. Per ogni riga viene allocato un flusso separato.

È possibile inserire nuovi dati binari da un file usando [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) seguito da [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) per inserire il record nella tabella. Quando viene richiamata l'azione personalizzata, i dati del flusso vengono copiati in un file temporaneo, che viene quindi elaborato in base al tipo di azione personalizzata.

## <a name="type-value"></a>Valore tipo

Includere il valore seguente nella colonna Type della tabella [CustomAction](customaction-table.md) per specificare il tipo numerico di base dell'azione personalizzata a 32 bit.



| Costanti                                                              | Valore esadecimale | Decimal |
|------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeJScript**  +  **msidbCustomActionTypeBinaryData** | 0x05        | 5       |



 

Windows Il programma di installazione può usare azioni personalizzate a 64 bit nei sistemi operativi a 64 bit. Un'azione personalizzata a 64 bit basata su script deve includere il bit **msidbCustomActionType64BitScript** nel tipo numerico. Per informazioni, vedere [Azioni personalizzate a 64 bit.](64-bit-custom-actions.md) Includere il valore seguente nella colonna Type della tabella [CustomAction](customaction-table.md) per specificare il tipo numerico di base di un'azione personalizzata a 64 bit.



| Costanti                                                                                                     | Valore esadecimale | Decimal |
|---------------------------------------------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeJScript**  +  **msidbCustomActionTypeBinaryData**  +  **msidbCustomActionType64BitScript** | 0x0001005   | 4101    |



 

## <a name="target"></a>Destinazione

Il campo Target della [tabella CustomAction contiene](customaction-table.md) una funzione script facoltativa. L'elaborazione invia prima di tutto lo script per l'analisi e quindi chiama la funzione script facoltativa.

## <a name="return-processing-options"></a>Opzioni di elaborazione dei valori restituiti

Includere bit di flag facoltativi nella colonna Type della [tabella CustomAction per](customaction-table.md) specificare le opzioni di elaborazione restituite. Per una descrizione delle opzioni e dei valori, vedere [Custom Action Return Processing Options](custom-action-return-processing-options.md).

## <a name="execution-scheduling-options"></a>Opzioni di pianificazione dell'esecuzione

Includere bit di flag facoltativi nella colonna Tipo della [tabella CustomAction per](customaction-table.md) specificare le opzioni di pianificazione dell'esecuzione. Queste opzioni controllano l'esecuzione multipla di azioni personalizzate. Per una descrizione delle opzioni, vedere [Opzioni di pianificazione dell'esecuzione di azioni personalizzate.](custom-action-execution-scheduling-options.md)

## <a name="in-script-execution-options"></a>In-Script opzioni di esecuzione

Includere bit di flag facoltativi nella colonna Type della [tabella CustomAction per](customaction-table.md) specificare un'opzione di esecuzione nello script. Queste opzioni copiano il codice dell'azione nello script di esecuzione, rollback o commit. Per una descrizione delle opzioni, vedere [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).

## <a name="return-values"></a>Valori restituiti

Le funzioni facoltative scritte nello script devono restituire uno dei valori descritti in Valori restituiti di [JScript e azioni personalizzate VBScript.](return-values-of-jscript-and-vbscript-custom-actions.md)

## <a name="remarks"></a>Commenti

Un'azione personalizzata scritta in JScript o VBScript richiede l'installazione [**dell'oggetto sessione**](session-object.md). Il programma di installazione collega **l'oggetto Session** allo script con il nome *Session*. [Poiché](obtaining-context-information-for-deferred-execution-custom-actions.md) l'oggetto **Session** potrebbe non esistere durante un rollback dell'installazione, un'azione personalizzata posticipata scritta nello script deve usare uno dei metodi o delle proprietà dell'oggetto **Session** descritto nella sezione Recupero di informazioni di contesto per le azioni personalizzate di esecuzione posticipata per recuperarne il contesto.

Quando viene esportata una tabella di database, ogni flusso viene scritto come file separato nella sottocartella denominata in base alla tabella, usando la chiave primaria come nome file (colonna Nome per la tabella binaria), con estensione predefinita ".ibd". Il nome deve usare il formato 8.3 se il file system o il sistema di controllo della versione non supporta nomi di file lunghi. Il file di archivio permanente sostituisce i dati del flusso con il nome file usato, in modo che i dati possano essere individuati quando viene importata la tabella.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Azioni \_ personalizzate](custom-actions.md)
</dt> </dl>

 

 



