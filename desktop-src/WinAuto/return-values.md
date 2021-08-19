---
title: Valori restituiti (Windows accessibilità)
description: Questo argomento descrive i valori restituiti più comuni e altri valori restituiti che potrebbero essere visualizzati meno frequentemente.
ms.assetid: e6deca92-42da-41ab-bfdb-75cbce3022bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71595f7a21d932ee961f9fa5f2a9443cf4d63e38de42f3d5b8c89fa8e9f84e83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122061"
---
# <a name="return-values-windows-accessibility-features"></a>Valori restituiti (Windows accessibilità)

Questo argomento descrive i valori restituiti più comuni e altri valori restituiti che potrebbero essere visualizzati meno frequentemente.

## <a name="common-return-values"></a>Valori restituiti comuni

I [**metodi IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) restituiscono uno dei valori seguenti, definiti in winerror.h, o un altro codice di errore Component Object Model (COM) standard:



|   Valore                      |   Descrizione                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| S \_ OK                   | Il metodo è riuscito.                                                                                                                                                                                                                                                                                                                                                                     |
| S \_ FALSE                | Il metodo è riuscito in parte. Ciò si verifica quando il metodo ha esito positivo, ma le informazioni richieste non sono disponibili. Ad esempio, Microsoft Active Accessibility restituisce S FALSE se si chiama \_ [**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) per recuperare un oggetto figlio in un determinato punto e il punto specificato non si trova all'interno dell'oggetto o dell'oggetto figlio dell'oggetto. |
| MEMBRO \_ DISP \_ ENOTFOUND | L'oggetto non supporta la proprietà o l'azione richiesta. Ad esempio, un pulsante di push restituisce questo valore se si richiede la relativa proprietà [Value](value-property.md), perché non dispone di una proprietà Value.                                                                                                                                                                           |
| E \_ NOTIMPL              | Il metodo non è implementato. Questo valore si verifica quando un client chiama un metodo non ancora supportato in tale sistema operativo.                                                                                                                                                                                                                                                         |
| E \_ INVALIDARG           | Uno o più argomenti non sono validi. Questo errore si verifica quando il chiamante tenta di identificare un oggetto figlio usando un identificatore non riconosciuto dal server. Questo errore si verifica anche quando un client tenta di identificare un oggetto figlio all'interno di un oggetto senza elementi figlio.                                                                                                      |
| E \_ OUTOFMEMORY          | Il metodo non è stato in grado di allocare la memoria necessaria per completare un'operazione fondamentale per il suo esito positivo.                                                                                                                                                                                                                                                                                        |
| E \_ FAIL                 | Si è verificato un errore sconosciuto o generico.                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="additional-return-values"></a>Valori restituiti aggiuntivi

Di seguito sono riportati i valori [**restituiti che i metodi IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) potrebbero restituire. Questi valori restituiti non sono comuni come quelli precedenti, ma è necessario conoscerli.



|    Valore                    |    Descrizione                                                                                  |
|------------------------|--------------------------------------------------------------------------------------|
| E \_ ACCESSO NEGATO        | Viene restituito quando si chiama get \_ accValue per ottenere il valore di un controllo password. |
| ECCEZIONE \_ DISP E \_     |                                                                                      |
| CO \_ E \_ OBJNOTCONNECTED |                                                                                      |



 

 

 




