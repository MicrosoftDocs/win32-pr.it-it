---
description: Gli sviluppatori di Windows Installer pacchetti possono scegliere di utilizzare un tipo di azione personalizzato 34 quando le azioni standard non sono sufficienti per eseguire l'installazione.
ms.assetid: 4d0e4f01-0530-4202-bc78-b6e52670b8e5
title: Tipo di azione personalizzata 34
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76ba17c9a4dc5b35d8d03e9cca2707079cb15bf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315475"
---
# <a name="custom-action-type-34"></a>Tipo di azione personalizzata 34

Questa azione personalizzata chiama un eseguibile avviato con una riga di comando. Per ulteriori informazioni, vedere [file eseguibili](executable-files.md).

## <a name="source"></a>Source (Sorgente)

Il file eseguibile viene generato da un file. Il campo di origine della tabella [CustomAction](customaction-table.md) contiene una chiave nella tabella [directory](directory-table.md) . La voce della tabella di directory a cui viene fatto riferimento viene usata per risolvere il percorso completo di una directory di lavoro. Non è necessario che sia il percorso della directory che contiene il file eseguibile.

## <a name="type-value"></a>Valore tipo

Includere il valore seguente nella colonna Type della tabella [CustomAction](customaction-table.md) per specificare il tipo numerico di base.



| Costanti                                                         | Valore esadecimale | Decimal |
|-------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeExe**  +  **msidbCustomActionTypeDirectory** | 0x022       | 34      |



 

## <a name="target"></a>Destinazione

La colonna di destinazione della tabella [CustomAction](customaction-table.md) contiene il percorso completo e il nome del file eseguibile seguito da argomenti facoltativi per l'eseguibile. Il percorso completo e il nome del file eseguibile sono obbligatori. Le virgolette devono essere utilizzate per i nomi di file o i percorsi lunghi. Il valore viene trattato come testo [formattato](formatted.md) e può contenere riferimenti a proprietà, file, directory o altri attributi di testo formattato.

## <a name="return-processing-options"></a>Opzioni di elaborazione restituite

Includere i bit di flag facoltativi nella colonna Type della tabella [CustomAction](customaction-table.md) per specificare le opzioni di elaborazione della restituzione. Per una descrizione delle opzioni e dei valori, vedere [Opzioni di elaborazione della restituzione di un'azione personalizzata](custom-action-return-processing-options.md).

## <a name="execution-scheduling-options"></a>Opzioni di pianificazione dell'esecuzione

Includere i bit di flag facoltativi nella colonna Type della tabella [CustomAction](customaction-table.md) per specificare le opzioni di pianificazione dell'esecuzione. Queste opzioni controllano la multipla esecuzione di azioni personalizzate. Per una descrizione delle opzioni, vedere [Opzioni di pianificazione dell'esecuzione dell'azione personalizzata](custom-action-execution-scheduling-options.md).

## <a name="in-script-execution-options"></a>Opzioni di esecuzione In-Script

Includere i bit di flag facoltativi nella colonna Type della tabella [CustomAction](customaction-table.md) per specificare un'opzione di esecuzione in-script. Queste opzioni copiano il codice dell'azione nello script di esecuzione, rollback o commit. Per una descrizione delle opzioni, vedere [azione personalizzata In-Script opzioni di esecuzione](custom-action-in-script-execution-options.md).

## <a name="return-values"></a>Valori restituiti

Per l'esito positivo, le azioni personalizzate che sono [file eseguibili](executable-files.md) devono restituire un valore pari a 0. Il programma di installazione interpreta qualsiasi altro valore restituito come errore. Per ignorare i valori restituiti, impostare il flag di bit **msidbCustomActionTypeContinue** nel campo Type della tabella [CustomAction](customaction-table.md) .

## <a name="remarks"></a>Commenti

Un'azione personalizzata che avvia un file eseguibile accetta una riga di comando, che in genere contiene proprietà designate dinamicamente. Se si tratta anche di un' [azione personalizzata di esecuzione posticipata](deferred-execution-custom-actions.md), il programma di installazione utilizza [**CreateProcessAsUser ha**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) o [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) per creare il processo quando viene richiamata l'azione personalizzata dallo script di installazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[\_Azioni personalizzate](custom-actions.md)
</dt> </dl>

 

 
