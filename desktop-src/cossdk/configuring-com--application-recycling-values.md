---
description: È possibile usare i metodi seguenti per configurare i valori di riciclo delle applicazioni per l'applicazione COM+.
ms.assetid: 8f6a4879-cf4c-4171-8448-bc07371e038c
title: Configurazione dei valori di riciclo delle applicazioni COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2613fb6f063a49d53baa90fad6f7dac862b848c6abf95fddcc36ace25e3d6b5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118548642"
---
# <a name="configuring-com-application-recycling-values"></a>Configurazione dei valori di riciclo delle applicazioni COM+

È possibile usare i metodi seguenti per configurare i valori di riciclo delle applicazioni per l'applicazione COM+.

> [!Note]  
> Non è possibile riciclare un'applicazione COM+ configurata per l'esecuzione come Windows servizio. Inoltre, le applicazioni di libreria hanno le proprietà di riciclo e pooling del processo host.

 

## <a name="component-services-administrative-tool"></a>Strumento amministrativo servizi componenti

Per configurare il riciclo delle applicazioni per un'applicazione COM+, seguire questa procedura:

1.  Nell'albero della console dello strumento amministrativo Servizi componenti fare clic con il pulsante destro del mouse sull'applicazione server COM+ da riciclare e quindi scegliere **Proprietà**.

2.  Nella scheda **Pooling & Recycling** immettere i valori per Lifetime **Limit (minutes)**, Memory **Limit (KB)**, **Expiration Timeout (minutes)**, **Call Limit** e **Activation Limit**, a seconda dei criteri da usare.

    -   **Limite di** durata indica il numero massimo di minuti che un processo può eseguire prima di essere riciclato. L'intervallo valido è compreso tra 0 e 30.240 minuti (21 giorni). Il numero predefinito di minuti è 0.
    -   **Limite di** memoria indica la quantità massima di utilizzo della memoria del processo (in kilobyte) prima del riciclo del processo. Se l'utilizzo della memoria del processo supera il numero specificato per più di un minuto, il processo viene riciclato. L'intervallo valido è compreso tra 0 e 1.048.576 KB e la quantità predefinita di utilizzo della memoria è 0 KB.
    -   **Timeout scadenza** indica il numero di minuti di attesa, prima dell'arresto forzato, per il rilascio di tutti i riferimenti esterni agli oggetti nel processo. L'intervallo valido è compreso tra 1 e 1440 minuti (24 ore) e il timeout di scadenza predefinito è di 15 minuti. Questo valore viene usato solo quando è già stato determinato che un processo verrà riciclato in base agli altri criteri.
    -   **Limite chiamate** indica il numero massimo di chiamate che gli oggetti applicazione possono accettare prima di riciclare il processo. L'intervallo valido è compreso tra 0 e 1.048.576 chiamate e il numero predefinito di chiamate è 0.
    -   **Limite di** attivazione indica il numero massimo di attivazioni di oggetti applicazione da accettare prima del riciclo del processo. L'intervallo valido è compreso tra 0 e 1.048.576 attivazioni e il numero predefinito di attivazioni è 0.

    > [!Note]  
    > Quando il valore **limite di** **durata,** limite di memoria,  **limite** di chiamate o limite di attivazione è impostato su 0 (valore predefinito), il riciclo dell'applicazione per tale criterio è disabilitato. Quando tutti e quattro questi criteri sono impostati su 0, il riciclo delle applicazioni è disabilitato per l'applicazione selezionata.

     

3.  Fare clic su **OK**.

## <a name="visual-basic"></a>Visual Basic

La funzione seguente in Microsoft Visual Basic illustra come è possibile impostare i valori di riciclo dell'applicazione per qualsiasi applicazione server COM+ scelta. Per usarlo da Visual Basic, aggiungere un riferimento alla libreria dei tipi di amministrazione COM+.


```VB
Function SetMyApplicationRecycling( _
  strApplicationName As String, _
  lngLifetimeLimit As Long, _
  lngMemoryLimit As Long, _
  lngCallLimit As Long, _
  lngActivationLimit As Long, _
  lngExpirationTimeout As Long _
) As Boolean  ' Return False if any errors occur.

    SetMyApplicationRecycling = False  ' Initialize the function.
    On Error GoTo My_Error_Handler  ' Initialize error handling.

    Dim objCatalog As COMAdmin.COMAdminCatalog
    Dim objAppCollection As COMAdmin.COMAdminCatalogCollection
    Dim objApplication As COMAdmin.COMAdminCatalogObject
    Set objCatalog = CreateObject("COMAdmin.COMAdminCatalog")
    Set objAppCollection = objCatalog.GetCollection("Applications")
    objAppCollection.Populate
    For Each objApplication In objAppCollection
        With objApplication
            If .Name = strApplicationName Then
                .Value("RecycleLifetimeLimit") = lngLifetimeLimit
                .Value("RecycleMemoryLimit") = lngMemoryLimit
                .Value("RecycleCallLimit") = lngCallLimit
                .Value("RecycleActivationLimit") = lngActivationLimit
                .Value("RecycleExpirationTimeout") = lngExpirationTimeout
                MsgBox strApplicationName & _
                  " recycling values are now set to the following: " & _
                  vbNewLine & vbNewLine & _
                  "Lifetime Limit = " & lngLifetimeLimit & vbNewLine & _
                  "Memory Limit = " & lngMemoryLimit & vbNewLine & _
                  "Call Limit = " & lngCallLimit & vbNewLine & _
                  "Activation Limit = " & lngActivationLimit & vbNewLine _
                  & "Expiration Timeout = " & lngExpirationTimeout
                Exit For
            End If
        End With
    Next
    objAppCollection.SaveChanges
    Set objApplication = Nothing
    Set objAppCollection = Nothing
    Set objCatalog = Nothing
    SetMyApplicationRecycling = True  ' Successful end to procedure
    Exit Function
    
My_Error_Handler:  ' Replace with specific error handling.
    MsgBox "Error # " & Err.Number & " (Hex: " & Hex(Err.Number) _
      & ")" & vbNewLine & Err.Description
    Set objApplication = Nothing
    Set objAppCollection = Nothing
    Set objCatalog = Nothing
End Function

```



Per usare la funzione , specificare un valore stringa per il nome dell'applicazione e valori interi per le impostazioni di riciclo dell'applicazione desiderate. Il codice Visual Basic seguente illustra come impostare il valore **RecycleLifetimeLimit** su 5, il valore **RecycleMemoryLimit** su 10, il **valore RecycleCallLimit** su 9, il valore **RecycleActivationLimit** su 100 e il valore **RecycleExpirationTimeout** su 15.


```VB
Sub Main()
    If Not SetMyApplicationRecycling("MyApp", 5, 10, 9, 100, 15) Then
        MsgBox "SetMyApplicationRecycling failed."
    End If
End Sub

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti relativi al riciclo delle applicazioni COM+](com--application-recycling-concepts.md)
</dt> </dl>

 

 



