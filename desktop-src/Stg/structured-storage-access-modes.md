---
title: Modalità di accesso all'archiviazione strutturata
description: I meccanismi di controllo dell'accesso simultaneo a un oggetto, da parte di più processi e utenti, sono essenziali.
ms.assetid: 2d524c2b-f2b4-49f2-9be8-2037846eb9e9
keywords:
- Archiviazione strutturata Strctd STG, nozioni fondamentali, funzioni API, flag per l'accesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2e46a231cb5168d15564f0b86b064c8bfd19e38
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297843"
---
# <a name="structured-storage-access-modes"></a>Modalità di accesso all'archiviazione strutturata

I meccanismi di controllo dell'accesso simultaneo a un oggetto, da parte di più processi e utenti, sono essenziali. COM fornisce questi meccanismi definendo le modalità di accesso per gli oggetti di archiviazione e di flusso. La modalità di accesso specificata per un oggetto di archiviazione padre viene ereditata dai relativi elementi figlio, sebbene sia possibile inserire restrizioni aggiuntive sul flusso o sull'archiviazione figlio. Un oggetto di archiviazione o flusso annidato può essere aperto nella stessa modalità o in una modalità più limitata rispetto a quello del relativo elemento padre, ma non può essere aperto in modalità meno limitata rispetto a quello del relativo padre.

Per specificare le modalità di accesso, è possibile usare i valori elencati in [**costanti STGM**](stgm-constants.md). Questi valori vengono usati come flag per essere passati come argomenti ai metodi nell'interfaccia [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) e alle funzioni API associate. In genere, diversi flag vengono combinati nel parametro *grfMode*, usando un'operazione **o** un valore booleano.

I flag rientrano in sei gruppi. È possibile specificare solo un flag di ogni gruppo alla volta:

-   [Flag di transazione](transaction-flags.md)
-   [Flag di creazione archiviazione](storage-creation-flags.md)
-   [Flag di creazione temporanei](temporary-creation-flags.md)
-   [Flag di priorità](priority-flags.md)
-   [Flag di autorizzazione di accesso](access-permission-flags.md)
-   [Flag di accesso condiviso](shared-access-flags.md)

 

 




