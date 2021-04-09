---
description: Impossibile impostare le sottoscrizioni temporanee utilizzando lo strumento di amministrazione Servizi componenti. Per creare o aggiornare una sottoscrizione temporanea, è necessario utilizzare le interfacce amministrative COM+.
ms.assetid: 28d48d59-abb2-4682-ab54-60b6aa7b31b1
title: Registrazione di una sottoscrizione temporanea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3fc85f189d14fbe6220d6f3760509e1ba0248a4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126705"
---
# <a name="registering-a-transient-subscription"></a>Registrazione di una sottoscrizione temporanea

Le sottoscrizioni temporanee richiedono un evento per un oggetto Sottoscrittore specifico già esistente. Le sottoscrizioni temporanee vengono archiviate nel catalogo COM+, ma la sottoscrizione viene eliminata se il sistema operativo o il sistema operativo viene arrestato. Diversamente dalle sottoscrizioni permanenti, le sottoscrizioni temporanee sono associate a un determinato oggetto e vengono archiviate solo nel sistema di eventi. Se si verifica un problema con il sistema di eventi o il sistema operativo, la sottoscrizione scompare. Le sottoscrizioni temporanee possono essere più efficienti rispetto alle sottoscrizioni persistenti, ma è necessario gestire i cicli di vita degli oggetti.

Impossibile impostare le sottoscrizioni temporanee utilizzando lo strumento di amministrazione Servizi componenti. Per creare o aggiornare una sottoscrizione temporanea, è necessario utilizzare le interfacce amministrative COM+.

## <a name="visual-basic"></a>Visual Basic

Nella procedura seguente viene descritto come creare una sottoscrizione temporanea utilizzando Microsoft Visual Basic:

1.  Specificare una sottoscrizione come temporanea aggiungendo una nuova voce alla raccolta [**TransientSubscriptions**](transientsubscriptions.md) e impostando la proprietà SubscriberInterface sull'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) dell'oggetto Subscriber. Gli eventi COM+ non creano una nuova istanza dell'oggetto Sottoscrittore durante la generazione di un evento, ma utilizzano invece l'istanza specificata. Gli eventi COM+ contengono un conteggio dei riferimenti per l'oggetto Sottoscrittore fino a quando la sottoscrizione non viene rimossa dal sistema.
2.  Creare un'applicazione server COM+ (un file con estensione exe, dll o ocx) con un oggetto che implementa le interfacce o i metodi a cui si desidera eseguire la sottoscrizione.
3.  Creare la sottoscrizione temporanea usando il codice seguente, passando il CLSID dell'oggetto classe di [evento](the-com--event-class-object.md) e l'istanza dell'oggetto Sottoscrittore. Utilizzando lo strumento di amministrazione Servizi componenti, è possibile ottenere la proprietà EventCLSID facendo clic con il pulsante destro del mouse sul componente COM+, selezionando **Proprietà** e selezionando la scheda **generale** .

    ``` syntax
    Public Function CreateTransientSubscription( _
      ByVal clsid As String, ByVal objref As Object) As String 
        Dim oCOMAdminCatalog As COMAdmin.COMAdminCatalog
        Dim oTSCol As COMAdminCatalogCollection
        Dim oSubscription As ICatalogObject
        Dim objvar As Variant
        On Error GoTo CreateTransientSubscriptionError
        Set oCOMAdminCatalog = CreateObject("COMAdmin.COMAdminCatalog")
        'Gets the TransientSubscriptions collection
        Set oTSCol = oCOMAdminCatalog.GetCollection( _
          "TransientSubscriptions")
        Set oSubscription = oTSCol.Add
        Set objvar = objref
        oSubscription.Value("SubscriberInterface") = objref
        oSubscription.Value("EventCLSID") = clsid
        oSubscription.Value("Name") = "TransientSubscription"
        oTSCol.SaveChanges
        CreateTransientSubscription = oSubscription.Value("ID")
        Set oSubscription = Nothing
        Set oTSCol = Nothing
        Set oCOMAdminCatalog = Nothing
        Set objvar = Nothing
        Exit Function
    CreateTransientSubscriptionError:
        CreateTransientSubscription = ""
        Err.Raise Err.Number, "[CreateTransientSubscription]" & _
          Err.Source, Err.Description
    End Function
    ```

Nell'esempio seguente viene illustrato come chiamare la funzione CreateTransientSubscription per sottoscrivere un'interfaccia denominata IStockTicker, che dispone di un metodo denominato UpdateStock.

1.  Creare una classe di evento che supporta l'interfaccia IStockTicker, che ha un metodo, UpdateStock.
2.  Nel progetto Sottoscrittore aggiungere una classe che implementi l'interfaccia IStockTicker.
3.  Quando si vuole sottoscrivere, eseguire il codice seguente:

    ``` syntax
    Dim oMyTicker As Object
    Dim sSubscriptionID As String
    Set oMyTicker = CreateObject("TheProject.CMyTicker")
    sSubscriptionID = CreateTransientSubscription( _
      "{..CLSID for the Event Class..}", oMyTicker)
    ```

La funzione CreateTransientSubscription restituisce una stringa, ovvero un GUID che può essere utilizzato come handle o cookie per revocare la sottoscrizione in un secondo momento. Per rimuovere la sottoscrizione, chiamare il metodo [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) di [**COMAdminCatalogCollection**](comadmincatalogcollection.md) sulla raccolta [**TransientSubscriptions**](transientsubscriptions.md) , passando l'indice corrispondente alla sottoscrizione con il GUID ricevuto in precedenza.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione di una sottoscrizione](registering-a-subscription.md)
</dt> </dl>

 

 
