---
title: Valori restituiti (funzionalità di accessibilità di Windows)
description: In questo argomento vengono descritti i valori restituiti più comuni e altri valori restituiti che potrebbero essere visualizzati con minore frequenza.
ms.assetid: e6deca92-42da-41ab-bfdb-75cbce3022bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cae2ccaf8bc74b1802be7569bc9e783cde4e11f9
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104474771"
---
# <a name="return-values-windows-accessibility-features"></a>Valori restituiti (funzionalità di accessibilità di Windows)

In questo argomento vengono descritti i valori restituiti più comuni e altri valori restituiti che potrebbero essere visualizzati con minore frequenza.

## <a name="common-return-values"></a>Valori restituiti comuni

I metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) restituiscono uno dei valori seguenti, definiti in Winerror. h, o un altro codice di errore Component Object Model standard (com):



|                         |                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_OK                   | Il metodo è riuscito.                                                                                                                                                                                                                                                                                                                                                                     |
| S \_ false                | Il metodo è riuscito in parte. Questo errore si verifica quando il metodo ha esito positivo, ma le informazioni richieste non sono disponibili. Ad esempio, Microsoft Active Accessibility restituisce \_ false se si chiama [**IAccessible:: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) per recuperare un oggetto figlio in un determinato punto e il punto specificato non si trova all'interno dell'oggetto o dell'oggetto figlio. |
| DISP \_ E \_ MEMBERNOTFOUND | L'oggetto non supporta la proprietà o l'azione richiesta. Un pulsante di push, ad esempio, restituisce questo valore se si richiede la relativa [proprietà Value](value-property.md), perché non dispone di una proprietà Value.                                                                                                                                                                           |
| E \_ NOTIMPL              | Il metodo non è implementato. Questo valore si verifica quando un client chiama un metodo non ancora supportato in quel sistema operativo.                                                                                                                                                                                                                                                         |
| E \_ INVALIDARG           | Uno o più argomenti non sono validi. Questo errore si verifica quando il chiamante tenta di identificare un oggetto figlio utilizzando un identificatore non riconosciuto dal server. Questo errore si verifica anche quando un client tenta di identificare un oggetto figlio all'interno di un oggetto privo di elementi figlio.                                                                                                      |
| E \_ OutOfMemory          | Il metodo non è riuscito ad allocare la memoria necessaria per completare un'operazione cruciale per il suo esito positivo.                                                                                                                                                                                                                                                                                        |
| E \_ non riescono                 | Si è verificato un errore sconosciuto o generico.                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="additional-return-values"></a>Valori restituiti aggiuntivi

Di seguito sono riportati i valori restituiti che possono essere restituiti dai metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) . Questi valori restituiti non sono comuni come quelli precedenti, ma è necessario conoscerli.



|                        |                                                                                      |
|------------------------|--------------------------------------------------------------------------------------|
| E \_ AccessDenied        | Viene restituito quando si chiama Get \_ accValue per ottenere il valore di un controllo password. |
| \_eccezione disp E \_     |                                                                                      |
| CO \_ E \_ OBJNOTCONNECTED |                                                                                      |



 

 

 




