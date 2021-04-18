---
description: Panoramica del modello a cascata per la classe RealTimeStylus.
ms.assetid: f4c377a7-979d-4a06-a8de-31b8e67d74f8
title: Modello di RealTimeStylus a cascata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd2f61ea3cd44753d1d91fb2662226a716ee5590
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104550372"
---
# <a name="the-cascaded-realtimestylus-model"></a>Modello di RealTimeStylus a cascata

Il modello di tipo [**RealTimeStylus**](realtimestylus-class.md) a cascata consente di usare due oggetti **RealTimeStylus** , ognuno in esecuzione su un thread diverso. Con questo modello si associa un oggetto **RealTimeStylus** secondario a un oggetto **RealTimeStylus** primario. L'oggetto **RealTimeStylus** secondario è associato come unico plug-in asincrono nella raccolta di plug-in asincrona dell'oggetto **RealTimeStylus** primario.

Il modello di [**RealTimeStylus**](realtimestylus-class.md) a cascata può essere utile negli scenari seguenti.

-   È possibile aggiungere determinate attività che possono essere richieste dal punto di vista del calcolo, pur continuando a richiedere l'accesso in tempo reale al flusso di dati della penna del tablet, ad esempio il riconoscimento dei movimenti a più tratti, alla raccolta di plug-in sincrona dell'oggetto [**RealTimeStylus**](realtimestylus-class.md) secondario.
-   È possibile distribuire il carico di calcolo dei plug-in sincroni su due thread, riducendo i ritardi nella raccolta di input penna in alcuni Tablet PC.

Il diagramma seguente illustra il flusso dei dati della penna del Tablet PC tramite due oggetti [**RealTimeStylus**](realtimestylus-class.md) a cascata e le relative raccolte di plug-in.

![illustrazione che mostra il flusso di dati RealTimeStylus a cascata](images/72ca1999-e078-49f8-a336-3b4d0157a472.gif)

In questo diagramma il cerchio con lettera "A" rappresenta i dati della penna del tablet che sono già stati elaborati dagli oggetti [**RealTimeStylus**](realtimestylus-class.md) primari e secondari ed è stato inserito nella coda di output dell'oggetto **RealTimeStylus** secondario. La lettera "B" del cerchio rappresenta i dati della penna del tablet che sono già stati elaborati dall'oggetto **RealTimeStylus** primario e aggiunti alla coda di output dell'oggetto **RealTimeStylus** primario e che non sono ancora stati inviati all'oggetto **RealTimeStylus** secondario. La lettera "C" del cerchio rappresenta i dati della penna del tablet attualmente elaborati dall'oggetto **RealTimeStylus** primario. Viene inviato alla raccolta di plug-in sincrono e inserito nella coda di output. Il cerchio vuoto rappresenta la posizione nella coda di output in cui vengono aggiunti i dati futuri della penna del tablet.

## <a name="constraints"></a>Vincoli

Se si usa il costruttore [**RealTimeStylus**](realtimestylus-class.md) predefinito, si crea un oggetto **RealTimeStylus** che può accettare solo input da un altro oggetto **RealTimeStylus** .

Nell'elenco seguente vengono descritti i vincoli associati all'utilizzo del modello [**RealTimeStylus**](realtimestylus-class.md) a cascata.

-   È possibile utilizzare solo due oggetti [**RealTimeStylus**](realtimestylus-class.md) , un oggetto **RealTimeStylus** primario e un oggetto **RealTimeStylus** secondario.
-   È necessario creare l'oggetto [**RealTimeStylus**](realtimestylus-class.md) primario con un costruttore che utilizza il parametro **attachedControl** o *handle* . L'oggetto **RealTimeStylus** secondario deve essere creato con il costruttore senza argomenti.
-   L'oggetto [**RealTimeStylus**](realtimestylus-class.md) secondario deve essere l'unico plug-in asincrono nella raccolta di plug-in asincrona dell'oggetto **RealTimeStylus** primario.
-   Un oggetto [**RealTimeStylus**](realtimestylus-class.md) secondario può essere associato a un solo oggetto **RealTimeStylus** primario alla volta. Se viene aggiunto a un secondo oggetto **RealTimeStylus** primario, il metodo [Add](/previous-versions/ms824814(v=msdn.10)) genera un'eccezione e l'oggetto **RealTimeStylus** secondario non è associato al secondo oggetto **RealTimeStylus** primario.
-   Il comportamento di alcuni membri dell'oggetto [**RealTimeStylus**](realtimestylus-class.md) secondario viene modificato. Nella tabella seguente viene descritto il comportamento modificato di questi membri.

    

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Membro</th>
    <th>Comportamento</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><a href="/previous-versions/ms825905(v=msdn.10)">GetDesiredPacketDescription</a></td>
    <td>Questo metodo restituisce le informazioni dall'oggetto <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> primario.<br/> Se il metodo <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> secondario non è collegato a un oggetto <strong>RealTimeStylus</strong> primario, questo metodo restituisce il valore predefinito.<br/></td>
    </tr>
    <tr class="even">
    <td><a href="/previous-versions/ms826041(v=msdn.10)">SetDesiredPacketDescription</a></td>
    <td>Questo metodo genera un'eccezione <a href="/dotnet/api/system.invalidoperationexception">InvalidOperationException</a> .<br/></td>
    </tr>
    <tr class="odd">
    <td><a href="/previous-versions/ms825913(v=msdn.10)">GetStyluses</a></td>
    <td>Questo metodo restituisce le informazioni dall'oggetto <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> primario.<br/> Se il metodo <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> secondario non è collegato a un oggetto <strong>RealTimeStylus</strong> primario, questo metodo restituisce una matrice vuota.<br/></td>
    </tr>
    <tr class="even">
    <td><a href="/previous-versions/ms824832(v=msdn.10)">Enabled</a></td>
    <td>Se si recupera questa proprietà, le informazioni vengono restituite dall'oggetto <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> primario.<br/> Se il metodo <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> secondario non è collegato a un oggetto <strong>RealTimeStylus</strong> primario, il recupero di questa proprietà restituisce il valore predefinito.<br/>
    <blockquote>
    [!Note]<br />
L'impostazione di questa proprietà genera un'eccezione <a href="/dotnet/api/system.invalidoperationexception">InvalidOperationException</a> .
    </blockquote>
    <br/></td>
    </tr>
    <tr class="odd">
    <td><a href="/previous-versions/ms824834(v=msdn.10)">WindowInputRectangle</a></td>
    <td>Se si recupera questa proprietà, le informazioni vengono restituite dall'oggetto <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> primario.<br/> Se il metodo <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> secondario non è collegato a un oggetto <strong>RealTimeStylus</strong> primario, il recupero di questa proprietà restituisce il valore predefinito.<br/>
    <blockquote>
    [!Note]<br />
L'impostazione di questa proprietà genera un'eccezione <a href="/dotnet/api/system.invalidoperationexception">InvalidOperationException</a> .
    </blockquote>
    <br/></td>
    </tr>
    </tbody>
    </table>

    

     

-   Si prevede che l'oggetto [**RealTimeStylus**](realtimestylus-class.md) padre smetta di funzionare quando viene eliminato il metodo **RealTimeStylus** figlio.

 

 
