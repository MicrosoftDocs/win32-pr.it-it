---
description: Le sottoscrizioni temporanee non possono essere impostate tramite lo strumento di amministrazione Servizi componenti. È necessario usare le interfacce amministrative COM+ per creare o aggiornare una sottoscrizione temporanea.
ms.assetid: 28d48d59-abb2-4682-ab54-60b6aa7b31b1
title: Registrazione di una sottoscrizione temporanea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f93b543a4602b0b4ed7ed4177133f3eb8f543a0db02750af8657ab36f310993
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990441"
---
# <a name="registering-a-transient-subscription"></a>Registrazione di una sottoscrizione temporanea

Le sottoscrizioni temporanee richiedono un evento per un oggetto sottoscrittore specifico già esistente. Le sottoscrizioni temporanee vengono archiviate nel catalogo COM+, ma la sottoscrizione viene eliminata se il sistema operativo o il sistema operativo viene arrestato. A differenza delle sottoscrizioni permanenti, le sottoscrizioni temporanee sono collegate a un determinato oggetto e vengono archiviate solo nel sistema di eventi. Se si verifica un problema con il sistema operativo o il sistema operativo degli eventi, la sottoscrizione scompare. Le sottoscrizioni temporanee possono essere più efficienti delle sottoscrizioni permanenti, ma è necessario gestirne i cicli di vita degli oggetti.

Le sottoscrizioni temporanee non possono essere impostate tramite lo strumento di amministrazione Servizi componenti. È necessario usare le interfacce amministrative COM+ per creare o aggiornare una sottoscrizione temporanea.

## <a name="visual-basic"></a>Visual Basic

La procedura seguente descrive come creare una sottoscrizione temporanea usando Microsoft Visual Basic:

1.  Specificare una sottoscrizione come temporanea aggiungendo una nuova voce alla raccolta [**TransientSubscriptions**](transientsubscriptions.md) e impostando la proprietà SubscriberInterface [**sull'interfaccia IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) dell'oggetto sottoscrittore. Eventi COM+ non crea una nuova istanza dell'oggetto sottoscrittore quando si genera un evento, ma usa l'istanza specificata. Eventi COM+ contiene un conteggio dei riferimenti per l'oggetto sottoscrittore fino a quando la sottoscrizione non viene rimossa dal sistema.
2.  Creare un'applicazione server COM+ (un .exe, un .dll o un file con estensione ocx) con un oggetto che implementa le interfacce o i metodi a cui si vuole eseguire la sottoscrizione.
3.  Creare la sottoscrizione temporanea usando il codice seguente, passando il CLSID dell'oggetto della classe [di](the-com--event-class-object.md) evento e l'istanza dell'oggetto sottoscrittore. Con lo strumento di amministrazione Servizi componenti è possibile ottenere la proprietà EventCLSID facendo clic con il pulsante destro del mouse sul componente COM+, scegliendo **Proprietà** e selezionando la **scheda** Generale.

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

L'esempio seguente illustra come chiamare la funzione CreateTransientSubscription per sottoscrivere un'interfaccia denominata IStockTicker, che ha un metodo denominato UpdateStock.

1.  Creare una classe di evento che supporta l'interfaccia IStockTicker, che ha un solo metodo, UpdateStock.
2.  Nel progetto sottoscrittore aggiungere una classe che implementa l'interfaccia IStockTicker.
3.  Quando si vuole eseguire la sottoscrizione, eseguire il codice seguente:

    ``` syntax
    Dim oMyTicker As Object
    Dim sSubscriptionID As String
    Set oMyTicker = CreateObject("TheProject.CMyTicker")
    sSubscriptionID = CreateTransientSubscription( _
      "{..CLSID for the Event Class..}", oMyTicker)
    ```

La funzione CreateTransientSubscription restituisce una stringa, ovvero un GUID che può essere usato come handle o cookie per revocare la sottoscrizione in un secondo momento. Per rimuovere la sottoscrizione, chiamare il metodo [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) di [**COMAdminCatalogCollection**](comadmincatalogcollection.md) nella raccolta [**TransientSubscriptions,**](transientsubscriptions.md) passando l'indice corrispondente alla sottoscrizione con il GUID ricevuto in precedenza.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione di una sottoscrizione](registering-a-subscription.md)
</dt> </dl>

 

 
