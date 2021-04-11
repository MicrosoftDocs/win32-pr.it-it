---
description: Modalità di modifica dei valori restituiti da COM+
ms.assetid: a6997f02-8456-45b5-9f40-4b9094ee4626
title: Modalità di modifica dei valori restituiti da COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2aa8270e41f1a1a96df0c17ccc1b98530fba4347
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127034"
---
# <a name="how-com-modifies-return-values"></a>Modalità di modifica dei valori restituiti da COM+

COM+ non modifica mai il valore restituito di un valore **HRESULT** che indica un errore, ad esempio e ha \_ \_ esito negativo. Tuttavia, quando un oggetto che utilizza la funzionalità COM+ restituisce un valore **HRESULT** che indica l'esito positivo (ad esempio \_ , S OK, s \_ false o NOERROR), com+ talvolta converte il valore **HRESULT** in un codice di errore com+ prima che venga restituito al chiamante.

Ad esempio, quando un'applicazione restituisce \_ OK dopo la chiamata a [**IObjectContext:: Tocomplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete), se l'oggetto è la radice di una transazione di cui non è stato eseguito il commit, **HRESULT** viene convertito nel contesto \_ E \_ interrotto.

Quando COM+ converte un valore **HRESULT** , cancella tutti i parametri di output del metodo. I riferimenti restituiti vengono rilasciati e i valori dei puntatori a oggetti restituiti vengono impostati su **null**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Criteri di isolamento degli errori e FailFast](fault-isolation-and-failfast-policy.md)
</dt> <dt>

[Individuazione dell'origine di un errore](finding-the-source-of-an-error.md)
</dt> <dt>

[Interpretazione dei codici di errore](interpreting-error-codes.md)
</dt> <dt>

[Strategie per la gestione degli errori in COM+](strategies-for-handling-errors-in-com-.md)
</dt> <dt>

[Risoluzione dei problemi](troubleshooting-the-com--crm.md)
</dt> </dl>

 

 



