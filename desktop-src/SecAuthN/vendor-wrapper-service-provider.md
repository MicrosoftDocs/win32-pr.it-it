---
description: Lo scopo del wrapper del fornitore è incapsulare e usare le interfacce COM di basso livello (fornite dai produttori di smart card) per un particolare smart card. Queste interfacce non vengono fornite da Microsoft.
ms.assetid: 7bc26f7b-c355-448a-9f23-4ccfffea2fef
title: Provider di servizi wrapper del fornitore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aeec4a8a5125e8fe19201a6c810eb87705eb7b5614b49fb455e8a96af63c8d26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785846"
---
# <a name="vendor-wrapper-service-provider"></a>Provider di servizi wrapper del fornitore

Lo scopo del wrapper del fornitore è incapsulare e usare le interfacce COM di basso livello (fornite dai produttori di smart card) per un particolare smart card. Queste interfacce non vengono fornite da Microsoft.

![wrapper del fornitore](images/scspart1.png)

Come descritto nella parte 6 della specifica di interoperabilità per *ICC* e Personal Computer Systems (vedere le specifiche in ), la funzionalità esposta da questo wrapper è più facile da usare rispetto alla funzionalità di quattro provider di servizi [https://www.pcscworkgroup.com/](https://www.pcscworkgroup.com/) separati. Le funzionalità del wrapper possono essere suddivise in quattro aree principali:

-   Servizi di autenticazione con smart card, ad esempio l'autenticazione basata su richiesta e l'autenticazione con smart card.
-   Accesso ai file della smart card o file system, ad esempio apertura, chiusura, lettura e scrittura.
-   Gestione delle smart card, ad esempio collegamento e scollegamento.
-   Servizi di verifica delle smart card, ad esempio la verifica e la modifica del codice.

> [!Note]  
> Questa specifica potrebbe non essere disponibile in alcune lingue e paesi o aree geografiche.

 

La funzionalità è specifica per il tipo di scheda usata (che funziona la scheda supporta, protocolli e così via) e sarà diversa per ogni scheda.

Il wrapper di esempio Microsoft SCardCOM usa la libreria COM ATL per implementare un wrapper semplice e impostare un modello per altri wrapper. Implementa le interfacce seguenti.



| Interfaccia o oggetto                                     | Descrizione                         |
|---------------------------------------------------------|-------------------------------------|
| [**ISCardAuth**](iscardauth.md)<br/>             | Servizi di autenticazione.<br/> |
| [**ISCardFileAccess**](iscardfileaccess.md)<br/> | Servizi del file system.<br/>    |
| [**ISCardManage**](iscardmanage.md)<br/>         | Servizi di gestione.<br/>     |
| [**ISCardVerify**](iscardverify.md)<br/>         | Servizi di verifica.<br/>   |



 

> [!Note]  
> L'esempio SCardCOM viene fornito solo come esempio di implementazione delle interfacce wrapper. Per evitare conflitti di nomi DLL con altri fornitori, non è necessario usare SCardCOM.dll come nome delle DLL create.

 

Di seguito è riportato un uso tipico del wrapper del fornitore. In questo esempio viene utilizzata [**l'interfaccia ISCardManage**](iscardmanage.md) per creare istanze delle interfacce di cui verrà eseguito il wrapping nel provider di servizi e l'interfaccia [**ISCardVerify**](iscardverify.md) per verificarne l'operazione.

**Per compilare un provider di servizi wrapper**

1.  Creare un'istanza [**dell'interfaccia ISCardManage.**](iscardmanage.md) Usare questa interfaccia per creare un'istanza delle interfacce necessarie, ad esempio [**ISCardFileAccess**](iscardfileaccess.md) o [**ISCardVerify**](iscardverify.md). Quando si creano queste interfacce, vengono create anche le interfacce COM di basso livello corrispondenti.
2.  Collegare/connettersi a una scheda tramite il metodo [**ISCardManage**](iscardmanage.md) appropriato.
3.  Eseguire le operazioni necessarie tramite il metodo [**ISCardVerify**](iscardverify.md) appropriato (che può chiamare più interfacce e metodi COM di basso livello per il completamento).
4.  Ripetere l'operazione per altre operazioni.
5.  Al termine, rilasciare .

Il nome dell'interfaccia COM e l'identificatore di interfaccia (GUID) non devono cambiare da quelli usati nel codice o nel wrapper di esempio. Tuttavia, è necessario modificare il GUID della classe, ovvero la posizione in cui risiede un'implementazione effettiva di un'interfaccia, rispetto a quelli usati. Ciò è particolarmente importante quando si implementa un wrapper del fornitore. Un esempio è l'uso di più wrapper del fornitore in un computer specifico. Questi wrapper devono implementare le stesse interfacce COM, ma useranno sempre strategie di implementazione diverse. Di conseguenza, sono necessarie classi diverse (e ID di classe).

 

 




