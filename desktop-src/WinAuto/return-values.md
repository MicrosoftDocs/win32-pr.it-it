---
title: Valori restituiti (funzionalità di accessibilità di Windows)
description: In questo argomento vengono descritti i valori restituiti più comuni e altri valori restituiti che potrebbero essere visualizzati meno frequentemente.
ms.assetid: e6deca92-42da-41ab-bfdb-75cbce3022bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd0f073c401682eb78d9fdf9270709a84ed77ae2
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443992"
---
# <a name="return-values-windows-accessibility-features"></a>Valori restituiti (funzionalità di accessibilità di Windows)

In questo argomento vengono descritti i valori restituiti più comuni e altri valori restituiti che potrebbero essere visualizzati meno frequentemente.

## <a name="common-return-values"></a>Valori restituiti comuni

I [**metodi IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) restituiscono uno dei valori seguenti, definiti in winerror.h, o un altro codice di errore Component Object Model (COM) standard:



|   Valore                      |   Descrizione                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| S \_ OK                   | Il metodo è riuscito.                                                                                                                                                                                                                                                                                                                                                                     |
| S \_ FALSE                | Il metodo ha avuto esito positivo in parte. Ciò si verifica quando il metodo ha esito positivo, ma le informazioni richieste non sono disponibili. Ad esempio, Microsoft Active Accessibility restituisce S FALSE se si chiama \_ [**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) per recuperare un oggetto figlio in un determinato punto e il punto specificato non si trova all'interno dell'oggetto o dell'oggetto figlio dell'oggetto. |
| DISP \_ E \_ MEMBERNOTFOUND | L'oggetto non supporta la proprietà o l'azione richiesta. Ad esempio, un pulsante di comando restituisce questo valore se si richiede la proprietà [Value](value-property.md), perché non dispone di una proprietà Value.                                                                                                                                                                           |
| E \_ NOTIMPL              | Il metodo non è implementato. Questo valore si verifica quando un client chiama un metodo non ancora supportato in tale sistema operativo.                                                                                                                                                                                                                                                         |
| E \_ INVALIDARG           | Uno o più argomenti non sono validi. Questo errore si verifica quando il chiamante tenta di identificare un oggetto figlio utilizzando un identificatore non riconosciuto dal server. Questo errore si verifica anche quando un client tenta di identificare un oggetto figlio all'interno di un oggetto senza elementi figlio.                                                                                                      |
| E \_ OUTOFMEMORY          | Il metodo non è stato in grado di allocare la memoria necessaria per completare un'operazione fondamentale per l'esito positivo.                                                                                                                                                                                                                                                                                        |
| E \_ FAIL                 | Si è verificato un errore sconosciuto o generico.                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="additional-return-values"></a>Valori restituiti aggiuntivi

Di seguito sono riportati i valori [**restituiti che i metodi IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) potrebbero restituire. Questi valori restituiti non sono comuni come quelli precedenti, ma è necessario conoscerli.



|    Valore                    |    Descrizione                                                                                  |
|------------------------|--------------------------------------------------------------------------------------|
| E \_ ACCESSO NEGATO        | Viene restituito quando si chiama get \_ accValue per ottenere il valore di un controllo password. |
| ECCEZIONE DISP \_ E \_     |                                                                                      |
| CO \_ E \_ OBJNOTCONNECTED |                                                                                      |



 

 

 




