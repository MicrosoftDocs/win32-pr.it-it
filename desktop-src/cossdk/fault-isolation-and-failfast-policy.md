---
description: Criteri di isolamento degli errori e FailFast
ms.assetid: 219c417c-a8a1-49eb-bc5a-702a16994d66
title: Criteri di isolamento degli errori e FailFast
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc097a6d45f10d4ef8a8d059b1376862edd785ed
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523433"
---
# <a name="fault-isolation-and-failfast-policy"></a>Criteri di isolamento degli errori e FailFast

COM+ esegue verifiche di coerenza e integrità interne estese. Se COM+ rileva una condizione di errore interno imprevista, termina immediatamente il processo. Questi criteri, denominati *FailFast*, facilitano il contenimento degli errori e i risultati in sistemi più affidabili e affidabili.

Si consideri un caso in cui COM+ rileva che una delle relative strutture di dati è in uno stato danneggiato. A questo punto, sia la provocazione che la grandezza del danneggiamento sono sconosciute e, sfortunatamente, COM+ non è in grado di indicare la distanza del danno. Tuttavia, anche se COM+ è in uno stato indeterminato, non viene eseguito in isolamento. Analogamente ad altre dll, è ospitato in un ambiente di processo e condivide un singolo spazio di indirizzi con l'eseguibile del programma principale e molte altre dll. Pertanto, COM+ presuppone che l'intero processo sia stato danneggiato e che il processo venga terminato immediatamente per impedire che la distribuzione di informazioni potenzialmente danneggiate ad altri processi o, peggio ancora, non consenta il commit e la durevolezza dei dati danneggiati.

COM+ non consente la propagazione delle eccezioni all'esterno di un contesto. Se si verifica un'eccezione durante l'esecuzione all'interno di un contesto COM+ e l'applicazione non rileva l'eccezione prima di restituire il contesto, COM+ intercetta l'eccezione e termina il processo. L'uso del criterio FailFast in questo caso si basa sul presupposto che l'eccezione abbia indeterminato lo stato del processo. non è sicuro continuare l'elaborazione.

Per gli sviluppatori o gli amministratori, è necessario esaminare il registro applicazioni Visualizzatore eventi per informazioni dettagliate su qualsiasi azione FailFast o errori gravi dell'applicazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Individuazione dell'origine di un errore](finding-the-source-of-an-error.md)
</dt> <dt>

[Modalità di modifica dei valori restituiti da COM+](how-com--modifies-return-values.md)
</dt> <dt>

[Interpretazione dei codici di errore](interpreting-error-codes.md)
</dt> <dt>

[Strategie per la gestione degli errori in COM+](strategies-for-handling-errors-in-com-.md)
</dt> <dt>

[Risoluzione dei problemi](troubleshooting-the-com--crm.md)
</dt> </dl>

 

 



