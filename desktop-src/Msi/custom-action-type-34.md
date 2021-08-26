---
description: Gli sviluppatori di Windows installer possono scegliere di usare un'azione personalizzata di tipo 34 quando le azioni standard non sono sufficienti per eseguire l'installazione.
ms.assetid: 4d0e4f01-0530-4202-bc78-b6e52670b8e5
title: Tipo di azione personalizzata 34
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4173633e7912897a3327d6d4c9c556d33f38bbd7f45cca6d4a1d96ef916b08ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077941"
---
# <a name="custom-action-type-34"></a>Tipo di azione personalizzata 34

Questa azione personalizzata chiama un eseguibile avviato con una riga di comando. Per altre informazioni, vedere [File eseguibili.](executable-files.md)

## <a name="source"></a>Source (Sorgente)

L'eseguibile viene generato da un file. Il campo Source della [tabella CustomAction](customaction-table.md) contiene una chiave nella [tabella Directory.](directory-table.md) La voce della tabella Directory a cui si fa riferimento viene usata per risolvere il percorso completo di una directory di lavoro. Non è necessario che sia il percorso della directory contenente il file eseguibile.

## <a name="type-value"></a>Valore tipo

Includere il valore seguente nella colonna Type della tabella [CustomAction](customaction-table.md) per specificare il tipo numerico di base.



| Costanti                                                         | Valore esadecimale | Decimal |
|-------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeExe**  +  **msidbCustomActionTypeDirectory** | 0x022       | 34      |



 

## <a name="target"></a>Destinazione

La colonna Target della tabella [CustomAction](customaction-table.md) contiene il percorso completo e il nome del file eseguibile seguito da argomenti facoltativi per l'eseguibile. Il percorso completo e il nome del file eseguibile sono obbligatori. È necessario utilizzare le virgolette per i percorsi o i nomi di file lunghi. Il valore viene considerato come [testo formattato](formatted.md) e può contenere riferimenti a proprietà, file, directory o altri attributi di testo formattato.

## <a name="return-processing-options"></a>Opzioni di elaborazione dei valori restituiti

Includere bit di flag facoltativi nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare le opzioni di elaborazione restituite. Per una descrizione delle opzioni e dei valori, vedere [Custom Action Return Processing Options](custom-action-return-processing-options.md).

## <a name="execution-scheduling-options"></a>Opzioni di pianificazione dell'esecuzione

Includere bit di flag facoltativi nella colonna Tipo della [tabella CustomAction](customaction-table.md) per specificare le opzioni di pianificazione dell'esecuzione. Queste opzioni controllano l'esecuzione multipla di azioni personalizzate. Per una descrizione delle opzioni, vedere [Opzioni di pianificazione dell'esecuzione di azioni personalizzate.](custom-action-execution-scheduling-options.md)

## <a name="in-script-execution-options"></a>In-Script opzioni di esecuzione

Includere bit di flag facoltativi nella colonna Type della [tabella CustomAction](customaction-table.md) per specificare un'opzione di esecuzione nello script. Queste opzioni copiano il codice dell'azione nello script di esecuzione, rollback o commit. Per una descrizione delle opzioni, vedere [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).

## <a name="return-values"></a>Valori restituiti

Le azioni personalizzate che sono [file eseguibili](executable-files.md) devono restituire il valore 0 per l'esito positivo. Il programma di installazione interpreta qualsiasi altro valore restituito come errore. Per ignorare i valori restituiti, impostare il flag di bit **msidbCustomActionTypeContinue** nel campo Tipo della [tabella CustomAction.](customaction-table.md)

## <a name="remarks"></a>Commenti

Un'azione personalizzata che avvia un eseguibile accetta una riga di comando, che in genere contiene proprietà designate in modo dinamico. Se si tratta anche di un'azione personalizzata di esecuzione [posticipata,](deferred-execution-custom-actions.md)il programma di installazione usa [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) o [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) per creare il processo quando l'azione personalizzata viene richiamata dallo script di installazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Azioni \_ personalizzate](custom-actions.md)
</dt> </dl>

 

 
