---
title: Registrazione di un callback in Visual Basic
description: L'aggiunta di un callback in Visual Basic è diversa dal metodo utilizzato in VBScript.
ms.assetid: 6aebb855-cf5b-4134-b7f6-3a8b404b7ae8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa754235458820a3c16eea73eec247aed90a103f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118159"
---
# <a name="registering-a-callback-in-visual-basic"></a><span data-ttu-id="c19a0-103">Registrazione di un callback in Visual Basic</span><span class="sxs-lookup"><span data-stu-id="c19a0-103">Registering a Callback in Visual Basic</span></span>

<span data-ttu-id="c19a0-104">L'aggiunta di un callback in Visual Basic è diversa dal metodo utilizzato in VBScript.</span><span class="sxs-lookup"><span data-stu-id="c19a0-104">Adding a callback in Visual Basic is different from the method used in VBScript.</span></span> <span data-ttu-id="c19a0-105">La funzione **GetRef** utilizzata in VBScript è diversa da quella utilizzata in Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="c19a0-105">The **GetRef** function used in VBScript is different than the one used in Visual Basic.</span></span> <span data-ttu-id="c19a0-106">Pertanto, uno sviluppatore deve creare un oggetto [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con la funzione di callback come metodo predefinito.</span><span class="sxs-lookup"><span data-stu-id="c19a0-106">Therefore, a developer must create an [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) object that has the callback function as the default method.</span></span> <span data-ttu-id="c19a0-107">In questo argomento vengono fornite le informazioni necessarie per sviluppare applicazioni Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="c19a0-107">This topic provides the necessary information to develop Visual Basic applications.</span></span>

<span data-ttu-id="c19a0-108">**Per implementare questo callback in un'applicazione**</span><span class="sxs-lookup"><span data-stu-id="c19a0-108">**To implement this callback in an application**</span></span>

1.  <span data-ttu-id="c19a0-109">Aggiungere riferimenti a due librerie di oggetti: TLBTypes. olb e VboostTypes6. olb.</span><span class="sxs-lookup"><span data-stu-id="c19a0-109">Add references to two object libraries: TLBTypes.olb and VboostTypes6.olb.</span></span> <span data-ttu-id="c19a0-110">Queste librerie di oggetti vengono fornite con il codice di esempio del punto di controllo.</span><span class="sxs-lookup"><span data-stu-id="c19a0-110">These object libraries are provided with the Control Point sample code.</span></span>
2.  <span data-ttu-id="c19a0-111">Aggiungere un riferimento a Cbklib. tlb.</span><span class="sxs-lookup"><span data-stu-id="c19a0-111">Add a reference to Cbklib.tlb.</span></span> <span data-ttu-id="c19a0-112">Questo file definisce la struttura della funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="c19a0-112">This file defines the structure of the callback function.</span></span>

    <span data-ttu-id="c19a0-113">Cbklib. tlb viene creato usando il file cbklib. idl incluso come parte del codice di esempio del punto di controllo.</span><span class="sxs-lookup"><span data-stu-id="c19a0-113">The cbklib.tlb is created using the cbklib.idl file that is included as part of the Control Point sample code.</span></span> <span data-ttu-id="c19a0-114">Si consiglia di modificare il nome di questo file per le funzioni di callback che differiscono nella struttura dei rispettivi parametri.</span><span class="sxs-lookup"><span data-stu-id="c19a0-114">It is recommended that the name of this file change for callback functions that differ in the structure of their parameters.</span></span> <span data-ttu-id="c19a0-115">Questo esempio USA MIDL per creare il file della libreria dei tipi.</span><span class="sxs-lookup"><span data-stu-id="c19a0-115">This example uses MIDL to create the type library file.</span></span>

3.  <span data-ttu-id="c19a0-116">Scrivere la funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="c19a0-116">Write the callback function.</span></span> <span data-ttu-id="c19a0-117">I parametri sono identici a quelli dell'esempio VBScript per la [registrazione di un callback](registering-a-callback.md).</span><span class="sxs-lookup"><span data-stu-id="c19a0-117">The parameters are the same as in the VBScript example in [Registering a Callback](registering-a-callback.md).</span></span> <span data-ttu-id="c19a0-118">In questo esempio viene stampata una stringa ogni volta che arriva un evento.</span><span class="sxs-lookup"><span data-stu-id="c19a0-118">This example prints a string whenever an event arrives.</span></span>
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

    

4.  <span data-ttu-id="c19a0-119">Aggiungere la funzione di callback all'oggetto [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) , come illustrato nell'esempio seguente, o in un altro oggetto, ad esempio [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder), utilizzando la libreria dei tipi di callback appropriata (cbklib. tbl).</span><span class="sxs-lookup"><span data-stu-id="c19a0-119">Add the callback function to the [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) object, as shown in the following example, or in another object such as [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder), using the appropriate callback type library (cbklib.tbl).</span></span>
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

    

<span data-ttu-id="c19a0-120">Nell'esempio seguente, l'oggetto [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) viene passato alla funzione.</span><span class="sxs-lookup"><span data-stu-id="c19a0-120">In the following example, the [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) object is passed to the function.</span></span> <span data-ttu-id="c19a0-121">La funzione di callback viene quindi aggiunta come parametro.</span><span class="sxs-lookup"><span data-stu-id="c19a0-121">The callback function is then added as the parameter.</span></span>


```VB
    Dim device as UPnPDevice
    Dim svcObj as UpnPService

    ' Initialize the device using the FindByType or using other methods of finding the devices
    Set svcObj = device.Services("appropriateService")
    Call AddCbFunction(svcObj)
```



## <a name="object-libraries-used-in-the-sample-code"></a><span data-ttu-id="c19a0-122">Librerie di oggetti utilizzate nel codice di esempio</span><span class="sxs-lookup"><span data-stu-id="c19a0-122">Object Libraries Used in the Sample Code</span></span>

<span data-ttu-id="c19a0-123">Gli esempi precedenti e il codice di esempio del punto di controllo usano alcune delle librerie di oggetti seguenti:</span><span class="sxs-lookup"><span data-stu-id="c19a0-123">The previous examples and the Control Point sample code use some of the following object libraries:</span></span>

1.  <span data-ttu-id="c19a0-124">TLBTypes. olb: questa libreria definisce alcuni tipi di librerie dei tipi e le interfacce usate nel codice di esempio.</span><span class="sxs-lookup"><span data-stu-id="c19a0-124">TLBTypes.olb — This library defines some of the type library types and interfaces that are used in the sample code.</span></span> <span data-ttu-id="c19a0-125">Definisce alcune delle funzioni da usare in Visual Basic, ad esempio [**LoadTypeLibEx**](/windows/win32/api/oleauto/nf-oleauto-loadtypelibex), che sono già disponibili in C o C++.</span><span class="sxs-lookup"><span data-stu-id="c19a0-125">It defines some of the functions to be used in Visual Basic, such as [**LoadTypeLibEx**](/windows/win32/api/oleauto/nf-oleauto-loadtypelibex), that are already available in C or C++.</span></span>
2.  <span data-ttu-id="c19a0-126">VboostTypes6. olb: questa libreria definisce alcuni tipi di base usati in TLBTypes. olb e FunctionDelegator. bas. Altre informazioni su TLBTypes sono disponibili nel libro *Advanced Visual Basic 6: Power Techniques for Everyday programs* di Matthew Curland (Addison-Wesley, luglio 2000, ISBN: 0-201-70712-8).</span><span class="sxs-lookup"><span data-stu-id="c19a0-126">VboostTypes6.olb — This library defines some base types which are used in TLBTypes.olb and FunctionDelegator.bas. Further information regarding TLBTypes can be found in the book *Advanced Visual Basic 6: Power Techniques for Everyday Programs*, by Matthew Curland (Addison-Wesley, July 2000, ISBN: 0-201-70712-8).</span></span> <span data-ttu-id="c19a0-127">(Questo libro potrebbe non essere disponibile in alcune lingue e paesi).</span><span class="sxs-lookup"><span data-stu-id="c19a0-127">(This book may not be available in some languages and countries.)</span></span>

<span data-ttu-id="c19a0-128">Il codice di esempio del punto di controllo e le librerie seguenti sono correlati a questa sezione e sono necessari per implementare questo callback.</span><span class="sxs-lookup"><span data-stu-id="c19a0-128">The Control Point sample code and the following libraries are related to this section and are needed to implement this callback.</span></span> <span data-ttu-id="c19a0-129">Sono reperibili con il codice di esempio del punto di controllo:</span><span class="sxs-lookup"><span data-stu-id="c19a0-129">They can be found with the Control Point sample code:</span></span>

-   <span data-ttu-id="c19a0-130">Cbklib. idl</span><span class="sxs-lookup"><span data-stu-id="c19a0-130">Cbklib.idl</span></span>
-   <span data-ttu-id="c19a0-131">Cbklib. tlb</span><span class="sxs-lookup"><span data-stu-id="c19a0-131">Cbklib.tlb</span></span>
-   <span data-ttu-id="c19a0-132">VboostTypes6. olb</span><span class="sxs-lookup"><span data-stu-id="c19a0-132">VboostTypes6.olb</span></span>
-   <span data-ttu-id="c19a0-133">TLBTypes. olb</span><span class="sxs-lookup"><span data-stu-id="c19a0-133">TLBTypes.olb</span></span>
-   <span data-ttu-id="c19a0-134">FunctionDelegator. Bas</span><span class="sxs-lookup"><span data-stu-id="c19a0-134">FunctionDelegator.bas</span></span>

 

 