---
description: Gli sviluppatori di Windows installer possono scegliere di usare un'azione personalizzata di tipo 1 quando le azioni standard non sono sufficienti per eseguire l'installazione.
ms.assetid: 277b875f-37f1-4f4d-98ae-7a18131de4f0
title: Tipo di azione personalizzata 1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3437fcd8a9a0da84ecb03f2527d30b6644210b2feb2ccc6c5f6558c3667a0d9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044901"
---
# <a name="custom-action-type-1"></a>Tipo di azione personalizzata 1

Questa azione personalizzata chiama una libreria a collegamento dinamico (DLL) scritta in C o C++.

## <a name="source"></a>Source (Sorgente)

La DLL viene generata da un flusso binario temporaneo. Il campo Source della [tabella CustomAction](customaction-table.md) contiene una chiave per la [tabella Binary](binary-table.md).

La colonna Data nella tabella Binary contiene i dati del flusso. Per ogni riga viene allocato un flusso separato. È possibile inserire nuovi dati binari da un file usando [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) seguito da [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) per inserire il record nella tabella. Quando viene richiamata l'azione personalizzata, i dati del flusso vengono copiati in un file temporaneo, che viene quindi elaborato a seconda del tipo di azione personalizzata.

## <a name="type-value"></a>Valore del tipo

Includere i bit di flag seguenti nella colonna Tipo della [tabella CustomAction per](customaction-table.md) specificare il tipo numerico di base.



| Costanti                                                          | Valore esadecimale | Decimal |
|--------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeDll**  +  **msidbCustomActionTypeBinaryData** | 0x001       | 1       |



 

## <a name="target"></a>Destinazione

La DLL viene chiamata tramite il punto di ingresso denominato nel campo Target della [tabella CustomAction](customaction-table.md), passando un singolo argomento che rappresenta l'handle alla sessione di installazione corrente. Il nome del punto di ingresso specificato nella tabella deve corrispondere a quello esportato dalla DLL. Si noti che se la funzione entry non è specificata da un oggetto . File DEF o tramite una specifica del linker /EXPORT: il nome può avere un carattere di sottolineatura iniziale e un suffisso " @4 ". La funzione chiamata deve specificare la \_ \_ convenzione di chiamata stdcall.

## <a name="return-processing-options"></a>Opzioni di elaborazione restituite

Includere i bit di flag facoltativi nella colonna Tipo della [tabella CustomAction per](customaction-table.md) specificare le opzioni di elaborazione restituite. Per una descrizione delle opzioni e dei valori, vedere [Custom Action Return Processing Options](custom-action-return-processing-options.md).

## <a name="execution-scheduling-options"></a>Opzioni di pianificazione dell'esecuzione

Includere bit di flag facoltativi nella colonna Tipo della [tabella CustomAction per](customaction-table.md) specificare le opzioni di pianificazione dell'esecuzione. Queste opzioni controllano l'esecuzione multipla di azioni personalizzate. Per una descrizione delle opzioni, vedere [Opzioni di pianificazione dell'esecuzione di azioni personalizzate](custom-action-execution-scheduling-options.md).

## <a name="in-script-execution-options"></a>In-Script opzioni di esecuzione

Includere bit di flag facoltativi nella colonna Tipo della [tabella CustomAction per](customaction-table.md) specificare un'opzione di esecuzione nello script. Queste opzioni copiano il codice azione nello script di esecuzione, rollback o commit. Per una descrizione delle opzioni, vedere [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).

## <a name="return-values"></a>Valori restituiti

Vedere [Valori restituiti dell'azione personalizzata](custom-action-return-values.md).

## <a name="remarks"></a>Commenti

Un'azione personalizzata che chiama una libreria a collegamento dinamico (DLL) richiede un handle per la sessione di installazione. Se si tratta anche di un'azione personalizzata di esecuzione posticipata, la sessione potrebbe non esistere più durante l'esecuzione dello script di installazione. Per informazioni sul modo in cui un'azione personalizzata di questo tipo può ottenere informazioni sul contesto, vedere Recupero di informazioni sul contesto per le azioni personalizzate [di esecuzione posticipata.](obtaining-context-information-for-deferred-execution-custom-actions.md)

Quando viene esportata una tabella di database, ogni flusso viene scritto come file separato nella sottocartella denominata dopo la tabella, usando la chiave primaria come nome file (colonna Nome per la tabella binaria), con estensione predefinita ".ibd". Il nome deve usare il formato 8.3 se il file system o il sistema di controllo della versione non supporta nomi di file lunghi. Il file di archivio permanente sostituisce i dati del flusso con il nome file usato, in modo che i dati possano essere individuati quando la tabella viene importata.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Azioni \_ personalizzate](custom-actions.md)
</dt> <dt>

[Librerie a collegamento dinamico](dynamic-link-libraries.md)
</dt> <dt>

[Recupero di informazioni di contesto per azioni personalizzate di esecuzione posticipata](obtaining-context-information-for-deferred-execution-custom-actions.md)
</dt> </dl>

 

 



