---
description: Questi provider di servizi forniscono le funzionalità di smart card di base.
ms.assetid: 1d887c4c-095c-4e1e-8b9a-7761acda2cbf
title: Provider di servizi di base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d07fab7f7406b4932ed5c08ab2c8743f8ebde57893aed4564f8fdf40758b5af4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883571"
---
# <a name="base-service-providers"></a>Provider di servizi di base

Questi [*provider di servizi*](/windows/desktop/SecGloss/c-gly) forniscono le funzionalità di smart card di base. [](/windows/desktop/SecGloss/s-gly) Possono essere usati per accedere a una singola smart card, oppure le interfacce COM possono essere combinate per fornire diverse funzionalità all'interno di un singolo provider di servizi. Questi provider di servizi sono i blocchi predefiniti per lo sviluppo di funzionalità aggiuntive per altri provider di servizi.

Le attività seguenti possono essere eseguite dalle interfacce del provider di servizi di base fornite da Smart Card SDK.



| Attività                                                                                                                   | Interfacce del provider di servizi di base         | DLL      |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------|----------|
| Connessione a un smart card, implementare transazioni, chiudere le connessioni e così via.                                         | [**ISCard**](iscard.md)                 | SCardSSP |
| Mantenere un comando APDU e [*rispondere a APDU*](/windows/desktop/SecGloss/r-gly).          | [**ISCardCmd**](iscardcmd.md)           | SCardSSP |
| Eseguire una query [*smart card database .*](/windows/desktop/SecGloss/s-gly) | [**ISCardDatabase**](iscarddatabase.md) | SCardSSP |
| Individuare un smart card o un lettore.                                                                                         | [**ISCardLocate**](iscardlocate.md)     | SCardSSP |
| Compilare un comando APDU ISO7816-4.                                                                                       | [**ISCardISO7816**](iscardiso7816.md)   | SCardSSP |
| Eseguire il wrapping di un buffer Istream usando Visual Basic tipi compatibili.                                                         | [**IByteBuffer**](ibytebuffer.md)       | SCardSSP |



 

La procedura seguente illustra un uso tipico di queste interfacce del provider di servizi di base. In questo esempio le [**interfacce ISCard**](iscard.md), [**ISCardISO7816**](iscardiso7816.md)e [**ISCardCmd**](iscardcmd.md) vengono usate per eseguire una transazione.

**Per eseguire una transazione**

1.  Creare un'istanza per tutte le interfacce del provider di servizi di base necessarie , ad esempio [**ISCard**](iscard.md), [**ISCardISO7816**](iscardiso7816.md)e [**ISCardCmd**](iscardcmd.md).
2.  Connessione a un particolare smart card usando i metodi [**nell'interfaccia ISCard.**](iscard.md)
3.  Usando [**ISCardISO7816**](iscardiso7816.md) e un oggetto [**ISCardCmd,**](iscardcmd.md) compilare un comando ISO 7816-4 chiamando il **metodo ISCardISO7816.** Il comando è contenuto in **ISCardCmd** come comando APDU.
4.  Eseguire una transazione con la scheda chiamando il metodo di transazione [**ISCard**](iscard.md) e passando [**l'oggetto ISCardCmd**](iscardcmd.md) creato. Al termine della transazione, i risultati vengono archiviati nell'APDU di risposta **ISCardCmd.**
5.  Interpretare [**l'APDU di risposta ISCardCmd**](iscardcmd.md) e ripetere l'operazione.
6.  Rilasciare tutte le interfacce al termine delle operazioni.

Per informazioni sul comando APDU compilato all'interno delle DLL, vedere Compilazione di un [comando APDU ISO7816-4](building-an-iso7816-4-apdu-command.md).

 

 
