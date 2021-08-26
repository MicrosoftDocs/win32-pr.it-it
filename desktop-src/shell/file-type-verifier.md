---
description: File Type Verifier è uno strumento che consente ai fornitori di software indipendenti (ISV) di verificare che i relativi tipi di file univoci siano implementati correttamente.
ms.assetid: 1BD7452B-2DF5-44e9-9B09-C29ABFFA5F93
title: Verifica del tipo di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ad3d3e66d85413a209c6899ce16061fa1fd46468fa32462026485d49b7326dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009511"
---
# <a name="file-type-verifier"></a>Verifica del tipo di file

File Type Verifier è uno strumento che consente ai fornitori di software indipendenti (ISV) di verificare che i relativi tipi di file univoci siano implementati correttamente. Le implementazioni di alta qualità dei gestori dei tipi di file sono fondamentali per una buona esperienza utente perché gli utenti interagiscono con il formato di file in molti modi in Windows Explorer. Gli utenti possono eseguire ricerche full-text, ordinare in base ai metadati personalizzati o visualizzare anteprime e anteprime avanzate del formato di file.

Per istruzioni sull'uso di File Type Verifier, vedere [How To Use the File Type Verifier](how-to-use-the-file-type-verifier.md).

## <a name="about-the-file-type-verifier-tool"></a>Informazioni sullo strumento di verifica del tipo di file

File Type Verifier è un programma disponibile come parte di [Windows 7 SDK.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) È progettato per aiutare gli sviluppatori che creano tipi Windows [file](fa-file-types.md) personalizzati per rilevare potenziali problemi con i tipi di file. Anche se File Type Verifier viene eseguito solo in Windows 7 e versioni successive, le regole applicate da File Type Verifier si applicano a tutte le versioni di Windows in cui sono disponibili le funzionalità che controlla.

File Type Verifier esegue diversi test sul tipo di file per verificare che sia registrato correttamente e che fornisce i gestori dei tipi di [file](fa-file-extensions.md) appropriati per visualizzare correttamente il tipo di file in Windows Explorer e, se appropriato, che supporti l'indicizzazione del contenuto del file.

Il verificatore del tipo di file verifica quanto segue:

-   [Gestori di anteprima](building-preview-handlers.md)
-   [Gestori di anteprime](building-thumbnail-providers.md)
-   [Gestori delle proprietà](../search/-search-3x-wds-extidx-propertyhandlers.md)
-   [Gestori di verbi](fa-verbs.md)
-   [Filtri (IFilter)](../search/-search-3x-wds-extidx-filters.md)
-   [Associazioni di tipi](../properties/building-property-handlers-user-friendly-kind-names.md)
-   [Tipi percepiti](fa-perceivedtypes.md)
-   [Proprietà importanti](../search/-shell-systemdefinedpropertiesforfileformats.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Come usare il verificatore del tipo di file](how-to-use-the-file-type-verifier.md)
</dt> <dt>

[Registrazione dell'applicazione](app-registration.md)
</dt> <dt>

[Tipi di file](fa-file-types.md)
</dt> <dt>

[Funzionamento delle associazioni di file](fa-how-work.md)
</dt> <dt>

[Visualizzazione contenuto per tipo o tipo di file](prophand-content-view.md)
</dt> <dt>

[Gestori dei tipi di file](fa-file-extensions.md)
</dt> <dt>

[Identificatori a livello di codice](fa-progids.md)
</dt> <dt>

[Tipi percepiti](fa-perceivedtypes.md)
</dt> <dt>

[Matrici di associazioni](fa-associationarray.md)
</dt> </dl>

 

 
