---
description: Passaggio di oggetti come parametri
ms.assetid: 174847c8-4545-4f61-ae13-42bdec1405e7
title: Passaggio di oggetti come parametri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c47669d3e3e5af572b6dfd50dcbbefacf5c008971f276408fa87b37ccbed9a1b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070381"
---
# <a name="passing-objects-as-parameters"></a>Passaggio di oggetti come parametri

Il servizio componenti in coda COM+ non abilita l'accodamento per ogni componente COM esistente. Esistono restrizioni sui tipi di metodi che possono essere accodati. A causa dei vincoli di messaggistica, i metodi devono rispettare le regole seguenti:

-   Devono contenere solo parametri di input.
-   Non devono restituire risultati specifici dell'applicazione.

Esistono inoltre restrizioni sui tipi di parametri di input che possono essere passati a un componente in coda. In fase di esecuzione, il servizio componenti in coda esegue il pacchetto degli argomenti nel client e li passa al componente server tramite [Accodamento messaggi](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)). È possibile effettuare facilmente il marshalling di tipi semplici, ad esempio numeri interi e booleani. Non è possibile effettuare il marshalling di tipi più complessi senza assistenza.

Nel caso di passaggio di un oggetto tramite la chiamata al metodo di un componente in coda come parametro, il client passa l'oggetto al registratore. Il registratore effettua il marshalling dell'oggetto in un messaggio di Accodamento messaggi e lo passa al listener. Dopo che il listener ha ricevuto il messaggio e lo ha passato al lettore, il lettore deve creare un'istanza dell'oggetto per inviare il messaggio alla chiamata al metodo specificata dal client. In base alla durata del client e del server in un ambiente in coda, l'implicazione è che questi oggetti devono essere in grado di eseguire il marshalling in base al valore. Poiché COM+ non fornisce semantica pass-by-value per gli oggetti COM standard, il registratore e il lettore devono essere aiutati dal componente per effettuare il marshalling e l'unmarshal dell'oggetto.

I riferimenti agli oggetti che [**supportano IPersistStream**](/windows/desktop/api/objidl/nn-objidl-ipersiststream) possono essere usati come parametri per le chiamate ai metodi nei componenti in coda. L'oggetto non può fare supposizioni su quando verrà creata un'istanza. Ad esempio, il server potrebbe non essere disponibile o il componente server potrebbe non essere avviato fino a un secondo momento del giorno. Gli oggetti che non **supportano IPersistStream** restituiranno un errore.

## <a name="visual-basic-persistable-objects"></a>Visual Basic Oggetti persistenti

Microsoft Visual Basic 6 consente la creazione di oggetti persistenti. Questi oggetti [**supportano IPersistStream**](/windows/desktop/api/objidl/nn-objidl-ipersiststream) e possono essere passati come parametri alle chiamate al metodo del componente in coda. Prima di Visual Basic a un componente in coda, è necessario inizializzare l'oggetto persistente. Questa operazione può essere eseguita in uno dei due modi seguenti:

-   Se l'applicazione che crea l'oggetto persistente viene scritta in Visual Basic, il runtime Visual Basic gestisce automaticamente l'inizializzazione dell'oggetto.
-   Se l'applicazione che crea l'oggetto persistente Visual Basic viene scritta in un linguaggio diverso da Visual Basic, ad esempio Microsoft Visual C++, l'applicazione deve inizializzare in modo esplicito il componente tramite una query per l'interfaccia [**IPersistStream**](/windows/desktop/api/objidl/nn-objidl-ipersiststream) dell'oggetto persistente o chiamando il metodo [**IPersistStreamInit::InitNew**](/windows/desktop/api/ocidl/nf-ocidl-ipersiststreaminit-initnew)o [**IPersistStream::Load.**](/windows/desktop/api/objidl/nf-objidl-ipersiststream-load)

## <a name="ado-recordsets-and-ole-db-rowsets"></a>Recordset ADO e set OLE DB set di righe

Il passaggio di **oggetti Recordset** ADO OLE DB set di righe tra componenti consente a un componente di elaborare i risultati delle query eseguite da un altro componente. Ciò è utile quando si distribuisce un'applicazione in più computer. **Gli** oggetti Recordset e rowset possono essere passati come parametri del metodo ai componenti in coda, con le restrizioni seguenti:

-   Non è possibile effettuare il marshalling di oggetti **Recordset** sul lato server [**tramite IPersistStream**](/windows/desktop/api/objidl/nn-objidl-ipersiststream). Solo gli oggetti **Recordset** sul lato client possono essere passati come parametri a una chiamata al metodo del componente in coda.
-   Se si lavora direttamente con OLE DB, OLE DB set di righe deve essere definito come set di righe sul lato client.

 

 
