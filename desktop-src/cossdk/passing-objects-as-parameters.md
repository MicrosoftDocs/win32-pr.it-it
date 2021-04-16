---
description: Passaggio di oggetti come parametri
ms.assetid: 174847c8-4545-4f61-ae13-42bdec1405e7
title: Passaggio di oggetti come parametri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a58e012138bc65cec481f714ac216bb8227fb924
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524042"
---
# <a name="passing-objects-as-parameters"></a>Passaggio di oggetti come parametri

Il servizio componenti in coda COM+ non Abilita l'accodamento per ogni componente COM esistente. Esistono restrizioni sui tipi di metodi che possono essere accodati. A causa dei vincoli di messaggistica, i metodi devono rispettare le regole seguenti:

-   Devono contenere solo parametri di input.
-   Non devono restituire risultati specifici dell'applicazione.

Esistono inoltre restrizioni sui tipi di parametri di input che possono essere passati a un componente in coda. In fase di esecuzione, il servizio componenti in coda crea il pacchetto degli argomenti nel client e li passa al componente server utilizzando [Accodamento messaggi](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)). È possibile eseguire facilmente il marshalling di tipi semplici, ad esempio numeri interi e booleani. i tipi più complessi non possono essere sottoposti a marshalling senza guida.

Nel caso di passaggio di un oggetto tramite la chiamata al metodo di un componente in coda come parametro, il client passa l'oggetto al registratore. Il registratore esegue il marshalling dell'oggetto in un messaggio di Accodamento messaggi e lo passa al listener. Quando il listener preleva il messaggio e lo passa al lettore, il lettore deve creare una nuova istanza dell'oggetto per inviarlo alla chiamata al metodo specificata dal client. In base alla durata del client e del server in un ambiente in coda, l'implicazione è che questi oggetti devono essere in grado di effettuare il marshalling in base al valore. Poiché COM+ non fornisce la semantica pass-by-value per gli oggetti COM standard, il registratore e il lettore necessitano di assistenza dal componente per eseguire il marshalling e l'unmarshalling dell'oggetto.

I riferimenti agli oggetti che supportano [**IPersistStream**](/windows/desktop/api/objidl/nn-objidl-ipersiststream) possono essere usati come parametri per le chiamate ai metodi sui componenti in coda. L'oggetto non può fare supposizioni su quando verrà ricreata la nuova istanza. È ad esempio possibile che il server non sia disponibile o che il componente server non venga avviato solo in un secondo momento. Gli oggetti che non supportano **IPersistStream** restituiranno un errore.

## <a name="visual-basic-persistable-objects"></a>Visual Basic di oggetti resi permanente

Microsoft Visual Basic 6 consente la creazione di oggetti salvati in modo permanente. Questi oggetti supportano [**IPersistStream**](/windows/desktop/api/objidl/nn-objidl-ipersiststream) e possono essere passati come parametri alle chiamate al metodo del componente in coda. Prima che un oggetto Visual Basic possa essere passato a un componente in coda, è necessario inizializzare l'oggetto permanente. Questa operazione può essere eseguita in uno dei due modi seguenti:

-   Se l'applicazione che crea l'oggetto permanente viene scritta in Visual Basic, il runtime di Visual Basic gestisce automaticamente l'inizializzazione dell'oggetto.
-   Se l'applicazione che crea il Visual Basic oggetto permanente viene scritta in una lingua diversa da Visual Basic, ad esempio Microsoft Visual C++, l'applicazione deve inizializzare in modo esplicito il componente eseguendo una query per l'interfaccia [**IPersistStream**](/windows/desktop/api/objidl/nn-objidl-ipersiststream) dell'oggetto permanente oppure chiamando il metodo [**IPersistStreamInit:: InitNew**](/windows/desktop/api/ocidl/nf-ocidl-ipersiststreaminit-initnew)o [**IPersistStream:: Load**](/windows/desktop/api/objidl/nf-objidl-ipersiststream-load) .

## <a name="ado-recordsets-and-ole-db-rowsets"></a>Recordset ADO e set di righe OLE DB

Il passaggio di oggetti **Recordset** ADO o OLE DB set di righe tra componenti consente a un componente di elaborare i risultati delle query eseguite da un altro componente. Questa operazione è utile quando si distribuisce un'applicazione in più computer. Gli oggetti **Recordset** e set di righe possono essere passati come parametri del metodo ai componenti in coda, con le restrizioni seguenti:

-   Impossibile effettuare il marshalling degli oggetti **Recordset** sul lato server utilizzando [**IPersistStream**](/windows/desktop/api/objidl/nn-objidl-ipersiststream). Solo gli oggetti **Recordset** lato client possono essere passati come parametri a una chiamata al metodo del componente in coda.
-   Se si lavora direttamente con OLE DB, il set di righe OLE DB deve essere definito come set di righe lato client.

 

 
