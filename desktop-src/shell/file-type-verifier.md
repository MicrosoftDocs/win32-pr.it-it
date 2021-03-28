---
description: Il tipo di file Verifier è uno strumento che consente ai fornitori di software indipendenti (ISV) di verificare che i tipi di file univoci siano implementati correttamente.
ms.assetid: 1BD7452B-2DF5-44e9-9B09-C29ABFFA5F93
title: Tipo di file Verifier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8e4a588e4889241762a9d8e0567d4a4542c0255
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881593"
---
# <a name="file-type-verifier"></a>Tipo di file Verifier

Il tipo di file Verifier è uno strumento che consente ai fornitori di software indipendenti (ISV) di verificare che i tipi di file univoci siano implementati correttamente. Le implementazioni di qualità elevata dei gestori di tipi di file sono fondamentali per un'esperienza utente ottimale perché gli utenti interagiscono con il formato di file in molti modi in Esplora risorse. Gli utenti possono eseguire ricerche full-text, ordinare in base a metadati personalizzati o visualizzare anteprime e anteprime avanzate del formato di file.

Per istruzioni sull'utilizzo del verificatore del tipo di file, vedere [come utilizzare il tipo di file Verifier](how-to-use-the-file-type-verifier.md).

## <a name="about-the-file-type-verifier-tool"></a>Informazioni sullo strumento File Type Verifier

Il tipo di file Verifier è un programma disponibile come parte di [Windows 7 SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx). È progettato per aiutare gli sviluppatori che creano tipi di [file](fa-file-types.md) Windows personalizzati per rilevare potenziali problemi con i tipi di file. Sebbene il verificatore del tipo di file venga eseguito solo in Windows 7 e versioni successive, le regole applicate dal Verifier del tipo di file si applicano a tutte le versioni di Windows in cui sono disponibili le funzionalità che controlla.

Il tipo di file Verifier esegue diversi test sul tipo di file per verificare che sia correttamente registrato e che fornisca i [gestori dei tipi di file](fa-file-extensions.md) appropriati per visualizzare il tipo di file correttamente in Esplora risorse e, quando appropriato, supporta l'indicizzazione del contenuto del file.

Il tipo di file Verifier Verifica gli elementi seguenti:

-   [Gestori di anteprime](building-preview-handlers.md)
-   [Gestori di anteprime](building-thumbnail-providers.md)
-   [Gestori di proprietà](../search/-search-3x-wds-extidx-propertyhandlers.md)
-   [Gestori di verbi](fa-verbs.md)
-   [Filtri (IFilter)](../search/-search-3x-wds-extidx-filters.md)
-   [Associazioni di tipo](../properties/building-property-handlers-user-friendly-kind-names.md)
-   [Tipi percepiti](fa-perceivedtypes.md)
-   [Proprietà importanti](../search/-shell-systemdefinedpropertiesforfileformats.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Come utilizzare il tipo di file Verifier](how-to-use-the-file-type-verifier.md)
</dt> <dt>

[Registrazione dell'applicazione](app-registration.md)
</dt> <dt>

[Tipi di file](fa-file-types.md)
</dt> <dt>

[Funzionamento delle associazioni di file](fa-how-work.md)
</dt> <dt>

[Visualizzazione contenuto per tipo di file o tipo](prophand-content-view.md)
</dt> <dt>

[Gestori di tipi di file](fa-file-extensions.md)
</dt> <dt>

[Identificatori a livello di codice](fa-progids.md)
</dt> <dt>

[Tipi percepiti](fa-perceivedtypes.md)
</dt> <dt>

[Matrici di associazione](fa-associationarray.md)
</dt> </dl>

 

 
