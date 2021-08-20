---
title: Registrazione di un callback in Visual Basic
description: L'aggiunta di un callback Visual Basic è diversa dal metodo usato in VBScript.
ms.assetid: 6aebb855-cf5b-4134-b7f6-3a8b404b7ae8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7145a6c6ef80ede3ea2fdb1fd62a2661142fb6f0a85454389fe1c09c117e5b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118126224"
---
# <a name="registering-a-callback-in-visual-basic"></a>Registrazione di un callback in Visual Basic

L'aggiunta di un callback Visual Basic è diversa dal metodo usato in VBScript. La **funzione GetRef** usata in VBScript è diversa da quella usata in Visual Basic. Pertanto, uno sviluppatore deve creare un [**oggetto IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con la funzione di callback come metodo predefinito. In questo argomento vengono fornite le informazioni necessarie per sviluppare Visual Basic applicazioni.

**Per implementare questo callback in un'applicazione**

1.  Aggiungere riferimenti a due librerie di oggetti: TLBTypes.olb e VboostTypes6.olb. Queste librerie di oggetti vengono fornite con il codice di esempio del punto di controllo.
2.  Aggiungere un riferimento a Cbklib.tlb. Questo file definisce la struttura della funzione di callback.

    Il file cbklib.tlb viene creato usando il file cbklib.idl incluso nel codice di esempio del punto di controllo. È consigliabile modificare il nome di questo file per le funzioni di callback che differiscono nella struttura dei relativi parametri. In questo esempio viene utilizzato MIDL per creare il file della libreria dei tipi.

3.  Scrivere la funzione di callback. I parametri sono gli stessi dell'esempio VBScript in [Registrazione di un callback](registering-a-callback.md). In questo esempio viene stampata una stringa ogni volta che arriva un evento.
    ```VB
    Function eventHandler(ByVal callbackType As Variant, _
    ByVal svcObj As Variant, ByVal varName As Variant, _
    ByVal value As Variant) As Long

        On Error GoTo Error
        'Write some interesting code to do actual work here

        MsgBox "Event Handler Called"
        Exit Function

    Error:
        With Err
            If .Number > 0 Then
                eventHandler = .Number Or &H800A0000
            Else
                eventHandler = .Number
            End If
        End With
    End Function
    ```

    

4.  Aggiungere la funzione di callback all'oggetto [**IUPnPService,**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) come illustrato nell'esempio seguente, o in un altro oggetto, ad esempio [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder), usando la libreria dei tipi di callback appropriata (cbklib.tbl).
    ```VB
    Public Sub AddCbFunction(upnpSvc As UPnPService)

        Dim X As CallbackIUnknownLib.CallBackInterface
        Dim obj As Object
        Dim ptinfo As ITypeInfo
        Dim ptcomp As ITypeComp

        With LoadTypeLibEx(App.Path & "\cbklib.tlb", _
          REGKIND_NONE).GetTypeComp
            .BindType "CallBackInterface", 0, ptinfo, ptcomp
        End With

        'NewDelegator is defined in FunctionDelegator.bas
        Set X = NewDelegator(AddressOf eventHandler) 
        Set obj = CreateStdDispatch(Nothing, ObjPtr(X), ptinfo)
        upnpSvc.AddCallback obj
    End Sub
    ```

    

Nell'esempio seguente [**l'oggetto IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) viene passato alla funzione . La funzione di callback viene quindi aggiunta come parametro .


```VB
    Dim device as UPnPDevice
    Dim svcObj as UpnPService

    ' Initialize the device using the FindByType or using other methods of finding the devices
    Set svcObj = device.Services("appropriateService")
    Call AddCbFunction(svcObj)
```



## <a name="object-libraries-used-in-the-sample-code"></a>Librerie di oggetti usate nel codice di esempio

Gli esempi precedenti e il codice di esempio del punto di controllo usano alcune delle librerie di oggetti seguenti:

1.  TLBTypes.olb: questa libreria definisce alcuni dei tipi e delle interfacce della libreria dei tipi usati nel codice di esempio. Definisce alcune delle funzioni da usare in Visual Basic, ad esempio [**LoadTypeLibEx**](/windows/win32/api/oleauto/nf-oleauto-loadtypelibex), che sono già disponibili in C o C++.
2.  VboostTypes6.olb: questa libreria definisce alcuni tipi di base usati in TLBTypes.olb e FunctionDelegator.bas. Per altre informazioni su TLBTypes, vedere il libro *Advanced Visual Basic 6: Power Techniques for Everyday Programs* di Mattia Curland (Addison-Wesley, luglio 2000, ISBN: 0-201-70712-8). Questo libro potrebbe non essere disponibile in alcune lingue e paesi.

Il codice di esempio del punto di controllo e le librerie seguenti sono correlati a questa sezione e sono necessari per implementare questo callback. Sono disponibili con il codice di esempio del punto di controllo:

-   Cbklib.idl
-   Cbklib.tlb
-   VboostTypes6.olb
-   TLBTypes.olb
-   FunctionDelegator.bas

 

 