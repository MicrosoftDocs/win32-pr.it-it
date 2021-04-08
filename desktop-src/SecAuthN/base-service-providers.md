---
description: Questi provider di servizi forniscono le funzionalità di base delle smart card.
ms.assetid: 1d887c4c-095c-4e1e-8b9a-7761acda2cbf
title: Provider di servizi di base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25dfa6c190e7a09ed4dfceafb983878906e8e3b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967719"
---
# <a name="base-service-providers"></a>Provider di servizi di base

Questi [*provider di servizi*](/windows/desktop/SecGloss/c-gly) forniscono le funzionalità di base delle [*Smart Card*](/windows/desktop/SecGloss/s-gly) . Possono essere usati per accedere a una singola funzionalità di smart card o per combinare le interfacce COM per fornire diverse funzionalità all'interno di un singolo provider di servizi. Questi provider di servizi sono i blocchi predefiniti per lo sviluppo di funzionalità aggiuntive per altri provider di servizi.

Le attività seguenti possono essere eseguite dalle interfacce del provider di servizi di base fornite da Smart Card SDK.



| Attività                                                                                                                   | Interfacce del provider di servizi di base         | DLL      |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------|----------|
| Connettersi a una smart card, implementare transazioni, chiudere connessioni e così via.                                         | [**Scheda di**](iscard.md)                 | SCardSSP |
| Mantenere un comando APDU e [*Reply APDU*](/windows/desktop/SecGloss/r-gly).          | [**ISCardCmd**](iscardcmd.md)           | SCardSSP |
| Eseguire una query sul [*database delle smart card*](/windows/desktop/SecGloss/s-gly). | [**ISCardDatabase**](iscarddatabase.md) | SCardSSP |
| Individuare una smart card o un lettore.                                                                                         | [**ISCardLocate**](iscardlocate.md)     | SCardSSP |
| Compilare un comando ISO7816-4 APDU.                                                                                       | [**ISCardISO7816**](iscardiso7816.md)   | SCardSSP |
| Eseguire il wrapping di un buffer IStream utilizzando tipi compatibili con Visual Basic.                                                         | [**IByteBuffer**](ibytebuffer.md)       | SCardSSP |



 

Nella procedura riportata di seguito viene illustrato un utilizzo tipico di queste interfacce del provider di servizi di base. In questo [**esempio le interfacce**](iscard.md) [**ISCardISO7816**](iscardiso7816.md)e [**ISCardCmd**](iscardcmd.md) vengono usate per eseguire una transazione.

**Per eseguire una transazione**

1.  Creare un'istanza per tutte le interfacce del provider di servizi di base necessarie (ad [**esempio,**](iscard.md) [**ISCardISO7816**](iscardiso7816.md)e [**ISCardCmd**](iscardcmd.md)).
2.  Connettersi a una smart card specifica utilizzando i metodi nell'interfaccia della [**scheda**](iscard.md) .
3.  Utilizzando [**ISCardISO7816**](iscardiso7816.md) e un oggetto [**ISCardCmd**](iscardcmd.md) , compilare un comando ISO 7816-4 chiamando il metodo **ISCardISO7816** . Il comando è contenuto in **ISCardCmd** come APDU comando.
4.  Eseguire una transazione con la scheda chiamando il metodo di transazione della [**scheda**](iscard.md) e passando l'oggetto [**ISCardCmd**](iscardcmd.md) creato. Al termine della transazione, i risultati vengono archiviati in **ISCardCmd** Reply APDU.
5.  Interpretare il [**ISCardCmd**](iscardcmd.md) Reply APDU e REPEAT.
6.  Rilascia tutte le interfacce quando le operazioni vengono completate.

Per informazioni sul comando APDU compilato all'interno delle dll, vedere [compilazione di un comando ISO7816-4 APDU](building-an-iso7816-4-apdu-command.md).

 

 
