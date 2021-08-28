---
title: Modalità di accesso Archiviazione strutturate
description: I meccanismi per controllare l'accesso simultaneo a un oggetto, da parte di più processi e utenti, sono essenziali.
ms.assetid: 2d524c2b-f2b4-49f2-9be8-2037846eb9e9
keywords:
- Structured Archiviazione Strctd Stg , nozioni fondamentali, funzioni API, flag per l'accesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b7d1dda6605bb16a8c2fd4897a2b10670eb0877f49090a4994a004a0fd6d411
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117960085"
---
# <a name="structured-storage-access-modes"></a>Modalità di accesso Archiviazione strutturate

I meccanismi per controllare l'accesso simultaneo a un oggetto, da parte di più processi e utenti, sono essenziali. COM fornisce questi meccanismi definendo le modalità di accesso per gli oggetti di archiviazione e di flusso. La modalità di accesso specificata per un oggetto di archiviazione padre viene ereditata dai relativi elementi figlio, anche se è possibile applicare restrizioni aggiuntive all'archiviazione o al flusso figlio. Un oggetto di archiviazione o flusso annidato può essere aperto nella stessa modalità o in una modalità più limitata rispetto a quella dell'elemento padre, ma non può essere aperto in una modalità meno limitata rispetto a quella dell'elemento padre.

È possibile specificare le modalità di accesso usando i valori elencati in [**StGM Constants**](stgm-constants.md). Questi valori fungono da flag da passare come argomenti ai metodi [**nell'interfaccia IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) e nelle funzioni API associate. In genere, diversi flag vengono combinati nel parametro *grfMode*, usando **un'operazione OR booleana.**

I flag rientrano in sei gruppi. È possibile specificare un solo flag per volta per ogni gruppo:

-   [Flag di transazione](transaction-flags.md)
-   [Archiviazione Flag di creazione](storage-creation-flags.md)
-   [Flag di creazione temporanei](temporary-creation-flags.md)
-   [Flag di priorità](priority-flags.md)
-   [Flag di autorizzazione di accesso](access-permission-flags.md)
-   [Flag di accesso condiviso](shared-access-flags.md)

 

 




