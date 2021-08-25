---
description: Panoramica del modello a cascata per la classe RealTimeStylus.
ms.assetid: f4c377a7-979d-4a06-a8de-31b8e67d74f8
title: Modello Cascaded RealTimeStylus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf848f1382a8c6a54f58fb6db864ece165c7cff2
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467998"
---
# <a name="the-cascaded-realtimestylus-model"></a>Modello Cascaded RealTimeStylus

Il modello [**RealTimeStylus**](realtimestylus-class.md) a catena consente di usare due oggetti **RealTimeStylus,** ognuno in esecuzione in un thread diverso. Con questo modello si collega un oggetto **RealTimeStylus secondario** a un **oggetto RealTimeStylus** primario. **L'oggetto RealTimeStylus** secondario è collegato come unico plug-in asincrono nella raccolta di plug-in asincroni dell'oggetto **RealTimeStylus** primario.

Il modello [**RealTimeStylus**](realtimestylus-class.md) a catena può essere utile negli scenari seguenti.

-   È possibile aggiungere determinate attività che possono essere impegnative dal punto di vista del calcolo ma che richiedono comunque l'accesso in tempo reale al flusso di dati della penna del tablet, ad esempio il riconoscimento del movimento a più sequenze, alla raccolta di plug-in sincroni dell'oggetto [**RealTimeStylus**](realtimestylus-class.md) secondario.
-   È possibile distribuire il carico di calcolo dei plug-in sincroni su due thread, riducendo i ritardi nella raccolta input penna in alcuni TABLET.

Il diagramma seguente illustra il flusso dei dati della penna del tablet attraverso due oggetti [**RealTimeStylus**](realtimestylus-class.md) a catena e le relative raccolte di plug-in.

![illustrazione che mostra il flusso di dati realtimestylus a cascata](images/72ca1999-e078-49f8-a336-3b4d0157a472.gif)

In questo diagramma il cerchio con lettera "A" rappresenta i dati della penna del tablet che sono già stati elaborati dagli oggetti [**RealTimeStylus**](realtimestylus-class.md) primario e secondario ed è stato inserito nella coda di output dell'oggetto **RealTimeStylus secondario.** Il cerchio con lettera "B" rappresenta i dati della penna del tablet che sono già stati elaborati dall'oggetto **RealTimeStylus primario** e aggiunti alla coda di output dell'oggetto **RealTimeStylus primario** e non sono ancora stati inviati all'oggetto **RealTimeStylus secondario.** La lettera circolare "C" rappresenta i dati della penna del tablet attualmente in **elaborazione dall'oggetto RealTimeStylus** primario. Viene inviato alla raccolta di plug-in sincroni e inserito nella coda di output. Il cerchio vuoto rappresenta la posizione nella coda di output in cui vengono aggiunti i futuri dati della penna del tablet.

## <a name="constraints"></a>Vincoli

Se si usa il costruttore [**Predefinito RealTimeStylus,**](realtimestylus-class.md) si crea un oggetto **RealTimeStylus** che può accettare solo l'input da un **altro oggetto RealTimeStylus.**

Nell'elenco seguente vengono descritti i vincoli associati all'utilizzo del modello [**RealTimeStylus a**](realtimestylus-class.md) catena.

-   È possibile usare solo due oggetti [**RealTimeStylus,**](realtimestylus-class.md) un oggetto **RealTimeStylus primario** e un oggetto **RealTimeStylus** secondario.
-   [**L'oggetto RealTimeStylus primario**](realtimestylus-class.md) deve essere creato con un costruttore che usa **il parametro attachedControl** *o handle.* **L'oggetto RealTimeStylus secondario** deve essere creato con il costruttore senza argomenti.
-   [**L'oggetto RealTimeStylus secondario**](realtimestylus-class.md) deve essere l'unico plug-in asincrono nella raccolta di plug-in asincroni dell'oggetto **RealTimeStylus** primario.
-   Un oggetto [**RealTimeStylus secondario**](realtimestylus-class.md) può essere collegato solo a un oggetto **RealTimeStylus** primario alla volta. Se viene aggiunto a un secondo oggetto **RealTimeStylus** primario, il metodo [Add](/previous-versions/ms824814(v=msdn.10)) genera un'eccezione e l'oggetto **RealTimeStylus** secondario non è collegato al secondo oggetto **RealTimeStylus primario.**
-   Il comportamento di alcuni membri dell'oggetto [**RealTimeStylus secondario**](realtimestylus-class.md) viene modificato. Nella tabella seguente viene descritto il comportamento modificato di questi membri.

    

    
| Membro | Comportamento | 
|--------|----------|
| <a href="/previous-versions/ms825905(v=msdn.10)">GetDesiredPacketDescription</a> | Questo metodo restituisce le informazioni <a href="realtimestylus-class.md"><strong>dall'oggetto RealTimeStylus</strong></a> primario.<br /> Se <a href="realtimestylus-class.md"><strong>l'oggetto Secondario RealTimeStylus</strong></a> non è collegato a un oggetto <strong>RealTimeStylus primario,</strong> questo metodo restituisce il valore predefinito.<br /> | 
| <a href="/previous-versions/ms826041(v=msdn.10)">SetDesiredPacketDescription</a> | Questo metodo genera <a href="/dotnet/api/system.invalidoperationexception">un'eccezione InvalidOperationException.</a><br /> | 
| <a href="/previous-versions/ms825913(v=msdn.10)">GetStyluses</a> | Questo metodo restituisce le informazioni <a href="realtimestylus-class.md"><strong>dall'oggetto RealTimeStylus</strong></a> primario.<br /> Se <a href="realtimestylus-class.md"><strong>l'oggetto Secondario RealTimeStylus</strong></a> non è collegato a un <strong>oggetto RealTimeStylus primario,</strong> questo metodo restituisce una matrice vuota.<br /> | 
| <a href="/previous-versions/ms824832(v=msdn.10)">Enabled</a> | Il recupero di questa proprietà restituisce le informazioni <a href="realtimestylus-class.md"><strong>dall'oggetto RealTimeStylus</strong></a> primario.<br /> Se <a href="realtimestylus-class.md"><strong>l'oggetto Secondario RealTimeStylus</strong></a> non è collegato a un oggetto <strong>RealTimeStylus primario,</strong> il recupero di questa proprietà restituisce il valore predefinito.<br /><blockquote>    [!Note]<br />    L'impostazione di questa proprietà genera <a href="/dotnet/api/system.invalidoperationexception">un'eccezione InvalidOperationException.</a>    </blockquote><br /> | 
| <a href="/previous-versions/ms824834(v=msdn.10)">WindowInputRectangle</a> | Il recupero di questa proprietà restituisce le informazioni <a href="realtimestylus-class.md"><strong>dall'oggetto RealTimeStylus</strong></a> primario.<br /> Se <a href="realtimestylus-class.md"><strong>l'oggetto Secondario RealTimeStylus</strong></a> non è collegato a un oggetto <strong>RealTimeStylus primario,</strong> il recupero di questa proprietà restituisce il valore predefinito.<br /><blockquote>    [!Note]<br />    L'impostazione di questa proprietà genera <a href="/dotnet/api/system.invalidoperationexception">un'eccezione InvalidOperationException.</a>    </blockquote><br /> | 


    

     

-   È previsto [**che l'oggetto RealTimeStylus**](realtimestylus-class.md) padre smetta di funzionare quando l'oggetto **Figlio RealTimeStylus** è Disposed.

 

 
