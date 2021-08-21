---
description: Modalità di modifica dei valori restituiti da COM+
ms.assetid: a6997f02-8456-45b5-9f40-4b9094ee4626
title: Modalità di modifica dei valori restituiti da COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ba2b8a9761c7bb669982b47d94b7d522298fa6d557d197d24ea4cb5e56a0df9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118813822"
---
# <a name="how-com-modifies-return-values"></a>Modalità di modifica dei valori restituiti da COM+

COM+ non modifica mai il valore restituito di **un HRESULT** che indica un errore, ad esempio E \_ UNEXPECTED o E \_ FAIL. Tuttavia, quando un oggetto che usa la funzionalità COM+ restituisce un valore **HRESULT** che indica l'esito positivo (ad esempio S OK, S FALSE o \_ NOERROR), COM+ a volte converte \_ **il valore HRESULT** in un codice di errore COM+ prima che venga restituito al chiamante.

Ad esempio, quando un'applicazione restituisce S OK dopo aver chiamato \_ [**IObjectContext::SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete), se l'oggetto è la radice di una transazione di cui non viene eseguito il commit, **HRESULT** viene convertito in CONTEXT \_ E \_ ABORTED.

Quando COM+ converte un **valore HRESULT,** cancella tutti i parametri di output del metodo. I riferimenti restituiti vengono rilasciati e i valori dei puntatori agli oggetti restituiti vengono impostati su **NULL.**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Isolamento degli errori e criteri failfast](fault-isolation-and-failfast-policy.md)
</dt> <dt>

[Ricerca dell'origine di un errore](finding-the-source-of-an-error.md)
</dt> <dt>

[Interpretazione dei codici di errore](interpreting-error-codes.md)
</dt> <dt>

[Strategie per la gestione degli errori in COM+](strategies-for-handling-errors-in-com-.md)
</dt> <dt>

[Risoluzione dei problemi](troubleshooting-the-com--crm.md)
</dt> </dl>

 

 



