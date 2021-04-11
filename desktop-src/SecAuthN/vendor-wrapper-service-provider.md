---
description: Lo scopo del wrapper fornitore è incapsulare e utilizzare le interfacce COM di basso livello (fornite dai produttori di smart card) per una particolare smart card. Queste interfacce non vengono fornite da Microsoft.
ms.assetid: 7bc26f7b-c355-448a-9f23-4ccfffea2fef
title: Provider di servizi wrapper fornitore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37b7d22fea8e450111e1611f2ec069697c229a32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128906"
---
# <a name="vendor-wrapper-service-provider"></a>Provider di servizi wrapper fornitore

Lo scopo del wrapper fornitore è incapsulare e utilizzare le interfacce COM di basso livello (fornite dai produttori di smart card) per una particolare smart card. Queste interfacce non vengono fornite da Microsoft.

![wrapper fornitore](images/scspart1.png)

Come descritto nella parte 6 della *specifica di interoperabilità per i sistemi ICCS e personal computer* (vedere le specifiche all'indirizzo [https://www.pcscworkgroup.com/](https://www.pcscworkgroup.com/) ), la funzionalità esposta da questo wrapper è più semplice da usare rispetto alla funzionalità di quattro provider di servizi distinti. Le funzionalità del wrapper possono essere divise in quattro aree principali:

-   Servizi di autenticazione con smart card, ad esempio richiedere l'autenticazione della carta e della richiesta.
-   Accesso ai file di smart card o file system servizi, ad esempio apertura, chiusura, lettura e scrittura.
-   Gestione delle smart card, ad esempio collegamento e scollegamento.
-   Servizi di verifica della smart card, ad esempio la verifica e la modifica del codice.

> [!Note]  
> Questa specifica potrebbe non essere disponibile in alcune lingue e paesi o aree geografiche.

 

La funzionalità è specifica per il tipo di scheda usato (le funzioni supportate dalla scheda, i protocolli e così via) e saranno diverse per ogni scheda.

Il wrapper di esempio Microsoft SCardCOM utilizza la libreria COM ATL per implementare un wrapper semplice e il layout di un modello per altri wrapper. Implementa le interfacce seguenti.



| Interfaccia o oggetto                                     | Descrizione                         |
|---------------------------------------------------------|-------------------------------------|
| [**ISCardAuth**](iscardauth.md)<br/>             | Servizi di autenticazione.<br/> |
| [**ISCardFileAccess**](iscardfileaccess.md)<br/> | Servizi del file System.<br/>    |
| [**ISCardManage**](iscardmanage.md)<br/>         | Servizi di gestione.<br/>     |
| [**ISCardVerify**](iscardverify.md)<br/>         | Servizi di verifica.<br/>   |



 

> [!Note]  
> L'esempio SCardCOM viene fornito solo come esempio di implementazione delle interfacce wrapper. Per evitare conflitti tra i nomi di DLL e altri fornitori, non è necessario usare SCardCOM.dll come nome di qualsiasi DLL creata.

 

Di seguito è riportato un tipico utilizzo del wrapper fornitore. In questo esempio viene utilizzata l'interfaccia [**ISCardManage**](iscardmanage.md) per creare istanze delle interfacce che verranno incapsulate nel provider di servizi e nell'interfaccia [**ISCardVerify**](iscardverify.md) per verificarne il funzionamento.

**Per compilare un provider di servizi wrapper**

1.  Creare un'istanza dell'interfaccia [**ISCardManage**](iscardmanage.md) . Usare questa interfaccia per creare un'istanza di interfacce obbligatorie (ad esempio, [**ISCardFileAccess**](iscardfileaccess.md) o [**ISCardVerify**](iscardverify.md)). Quando si creano queste interfacce, verranno create anche le interfacce COM di basso livello corrispondenti.
2.  Collegare/connettersi a una scheda tramite il metodo [**ISCardManage**](iscardmanage.md) appropriato.
3.  Eseguire le operazioni necessarie tramite il metodo [**ISCardVerify**](iscardverify.md) appropriato, che può chiamare più metodi e interfacce com di basso livello per il completamento.
4.  Ripetere l'operazione per altre operazioni.
5.  Rilasciare al termine.

Il nome dell'interfaccia COM e l'identificatore di interfaccia (GUID) non devono essere modificati rispetto a quelli usati nel codice o nel wrapper di esempio. Tuttavia, il GUID della classe (ovvero, in cui risiede un'implementazione effettiva di un'interfaccia) deve essere modificato da quelli utilizzati. Questa operazione è particolarmente importante quando si implementa un wrapper fornitore. Un esempio potrebbe essere l'utilizzo di più wrapper fornitore in un particolare computer. Questi wrapper devono implementare le stesse interfacce COM, ma utilizzeranno sempre strategie di implementazione diverse. Sono pertanto necessarie classi diverse (e ID di classe).

 

 




