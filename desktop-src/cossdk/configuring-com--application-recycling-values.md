---
description: È possibile utilizzare i metodi seguenti per configurare i valori di riciclo delle applicazioni per l'applicazione COM+.
ms.assetid: 8f6a4879-cf4c-4171-8448-bc07371e038c
title: Configurazione dei valori di riciclo delle applicazioni COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b34c989d81f2e3486adb1d12ec76859a1d28f090
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127559"
---
# <a name="configuring-com-application-recycling-values"></a><span data-ttu-id="bebf7-103">Configurazione dei valori di riciclo delle applicazioni COM+</span><span class="sxs-lookup"><span data-stu-id="bebf7-103">Configuring COM+ Application Recycling Values</span></span>

<span data-ttu-id="bebf7-104">È possibile utilizzare i metodi seguenti per configurare i valori di riciclo delle applicazioni per l'applicazione COM+.</span><span class="sxs-lookup"><span data-stu-id="bebf7-104">You can use the following methods to configure application recycling values for your COM+ application.</span></span>

> [!Note]  
> <span data-ttu-id="bebf7-105">Non è possibile riciclare un'applicazione COM+ configurata per l'esecuzione come servizio Windows.</span><span class="sxs-lookup"><span data-stu-id="bebf7-105">You cannot recycle a COM+ application that has been configured to run as a Windows service.</span></span> <span data-ttu-id="bebf7-106">Inoltre, le applicazioni di libreria dispongono delle proprietà di riciclo e pool del processo host.</span><span class="sxs-lookup"><span data-stu-id="bebf7-106">Also, library applications have the recycling and pooling properties of their host process.</span></span>

 

## <a name="component-services-administrative-tool"></a><span data-ttu-id="bebf7-107">Strumento di amministrazione Servizi componenti</span><span class="sxs-lookup"><span data-stu-id="bebf7-107">Component Services Administrative Tool</span></span>

<span data-ttu-id="bebf7-108">Per configurare il riciclo dell'applicazione per un'applicazione COM+, attenersi alla procedura seguente:</span><span class="sxs-lookup"><span data-stu-id="bebf7-108">To configure application recycling for a COM+ application, use the following steps:</span></span>

1.  <span data-ttu-id="bebf7-109">Nell'albero della console dello strumento di amministrazione Servizi componenti fare clic con il pulsante destro del mouse sull'applicazione server COM+ che si desidera riciclare, quindi scegliere **Proprietà**.</span><span class="sxs-lookup"><span data-stu-id="bebf7-109">In the console tree of the Component Services administrative tool, right-click the COM+ server application you want to be recycled and then click **Properties**.</span></span>

2.  <span data-ttu-id="bebf7-110">Nella scheda **pooling & riciclo** immettere i valori per **limite di durata (minuti)**, **limite di memoria (KB)**, **timeout scadenza (minuti)**, **limite di chiamate** e **limite di attivazione**, a seconda dei criteri che si desidera utilizzare.</span><span class="sxs-lookup"><span data-stu-id="bebf7-110">On the **Pooling & Recycling** tab, enter values for **Lifetime Limit (minutes)**, **Memory Limit (KB)**, **Expiration Timeout (minutes)**, **Call Limit**, and **Activation Limit**, depending on the criteria you want to use.</span></span>

    -   <span data-ttu-id="bebf7-111">**Limite durata** indica il numero massimo di minuti per cui un processo può essere eseguito prima di essere riciclato.</span><span class="sxs-lookup"><span data-stu-id="bebf7-111">**Lifetime Limit** indicates the maximum number of minutes a process can run before it's recycled.</span></span> <span data-ttu-id="bebf7-112">L'intervallo valido è compreso tra 0 e 30.240 minuti (21 giorni).</span><span class="sxs-lookup"><span data-stu-id="bebf7-112">The valid range is 0 through 30,240 minutes (21 days).</span></span> <span data-ttu-id="bebf7-113">Il numero predefinito di minuti è 0.</span><span class="sxs-lookup"><span data-stu-id="bebf7-113">The default number of minutes is 0.</span></span>
    -   <span data-ttu-id="bebf7-114">**Limite di memoria** indica la quantità massima di utilizzo della memoria del processo (espressa in kilobyte) prima del riciclo del processo.</span><span class="sxs-lookup"><span data-stu-id="bebf7-114">**Memory Limit** indicates the maximum amount of process memory usage (in kilobytes) before recycling the process.</span></span> <span data-ttu-id="bebf7-115">Se l'utilizzo della memoria del processo supera il numero specificato per più di un minuto, il processo viene riciclato.</span><span class="sxs-lookup"><span data-stu-id="bebf7-115">If the process's memory usage exceeds the specified number for longer than one minute, the process is recycled.</span></span> <span data-ttu-id="bebf7-116">L'intervallo valido è compreso tra 0 e 1.048.576 KB e la quantità predefinita di utilizzo della memoria è 0 KB.</span><span class="sxs-lookup"><span data-stu-id="bebf7-116">The valid range is 0 through 1,048,576 KB, and the default amount of memory usage is 0 KB.</span></span>
    -   <span data-ttu-id="bebf7-117">**Timeout scadenza** indica il numero di minuti di attesa, prima che venga arrestato forzatamente, per il rilascio di tutti i riferimenti esterni agli oggetti nel processo.</span><span class="sxs-lookup"><span data-stu-id="bebf7-117">**Expiration Timeout** indicates the number of minutes to wait, before being forcibly shut down, for the release of all external references to objects in the process.</span></span> <span data-ttu-id="bebf7-118">L'intervallo valido è compreso tra 1 e 1440 minuti (24 ore) e il timeout di scadenza predefinito è 15 minuti.</span><span class="sxs-lookup"><span data-stu-id="bebf7-118">The valid range is 1 through 1440 minutes (24 hours), and the default expiration time-out is 15 minutes.</span></span> <span data-ttu-id="bebf7-119">Questo valore viene utilizzato solo se è già stato determinato che un processo verrà riciclato in base agli altri criteri.</span><span class="sxs-lookup"><span data-stu-id="bebf7-119">This value is used only when it is already determined that a process will be recycled based on the other criteria.</span></span>
    -   <span data-ttu-id="bebf7-120">**Limite chiamate** indica il numero massimo di chiamate che gli oggetti applicazione possono accettare prima di riciclare il processo.</span><span class="sxs-lookup"><span data-stu-id="bebf7-120">**Call Limit** indicates the maximum number of calls that application objects can accept before recycling the process.</span></span> <span data-ttu-id="bebf7-121">L'intervallo valido è compreso tra 0 e 1.048.576 chiamate e il numero predefinito di chiamate è 0.</span><span class="sxs-lookup"><span data-stu-id="bebf7-121">The valid range is 0 through 1,048,576 calls, and the default number of calls is 0.</span></span>
    -   <span data-ttu-id="bebf7-122">**Limite di attivazione** indica il numero massimo di attivazioni di oggetti applicazione da accettare prima del riciclo del processo.</span><span class="sxs-lookup"><span data-stu-id="bebf7-122">**Activation Limit** indicates the maximum number of application object activations to accept before recycling the process.</span></span> <span data-ttu-id="bebf7-123">L'intervallo valido è compreso tra 0 e 1.048.576 attivazioni e il numero predefinito di attivazioni è 0.</span><span class="sxs-lookup"><span data-stu-id="bebf7-123">The valid range is 0 through 1,048,576 activations, and the default number of activations is 0.</span></span>

    > [!Note]  
    > <span data-ttu-id="bebf7-124">Quando il **limite di durata**, il limite di **memoria**, il **limite di chiamata** o il valore del limite di **attivazione** è impostato su 0 (valore predefinito), il riciclo delle applicazioni per quel criterio è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="bebf7-124">When the **Lifetime Limit**, **Memory Limit**, **Call Limit**, or **Activation Limit** value is set to 0 (the default value), application recycling for that criterion is disabled.</span></span> <span data-ttu-id="bebf7-125">Quando tutti e quattro questi criteri sono impostati su 0, il riciclo delle applicazioni è disabilitato per l'applicazione selezionata.</span><span class="sxs-lookup"><span data-stu-id="bebf7-125">When all four of these criteria are set to 0, application recycling is disabled for the selected application.</span></span>

     

3.  <span data-ttu-id="bebf7-126">Fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="bebf7-126">Click **OK**.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="bebf7-127">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="bebf7-127">Visual Basic</span></span>

<span data-ttu-id="bebf7-128">La funzione seguente in Microsoft Visual Basic illustra come è possibile impostare i valori di riciclo dell'applicazione per qualsiasi applicazione server COM+ scelta.</span><span class="sxs-lookup"><span data-stu-id="bebf7-128">The following function in Microsoft Visual Basic demonstrates how you can set the application recycling values for any COM+ server application that you choose.</span></span> <span data-ttu-id="bebf7-129">Per usarlo da Visual Basic, aggiungere un riferimento alla libreria dei tipi di amministrazione COM+.</span><span class="sxs-lookup"><span data-stu-id="bebf7-129">To use it from Visual Basic, add a reference to the COM+ Admin Type Library.</span></span>


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



<span data-ttu-id="bebf7-130">Per usare la funzione, fornire un valore stringa per il nome dell'applicazione e i valori integer per le impostazioni di riciclo delle applicazioni desiderate.</span><span class="sxs-lookup"><span data-stu-id="bebf7-130">To use the function, provide a string value for the application name and integer values for the desired application recycling settings.</span></span> <span data-ttu-id="bebf7-131">Il codice di Visual Basic seguente mostra come impostare il valore **RecycleLifetimeLimit** su 5, il valore **RecycleMemoryLimit** su 10, il valore **RecycleCallLimit** su 9, il valore **RecycleActivationLimit** su 100 e il valore **RecycleExpirationTimeout** su 15.</span><span class="sxs-lookup"><span data-stu-id="bebf7-131">The following Visual Basic code shows how to set the **RecycleLifetimeLimit** value to 5, the **RecycleMemoryLimit** value to 10, the **RecycleCallLimit** value to 9, the **RecycleActivationLimit** value to 100, and the **RecycleExpirationTimeout** value to 15.</span></span>


```VB
Sub Main()
    If Not SetMyApplicationRecycling("MyApp", 5, 10, 9, 100, 15) Then
        MsgBox "SetMyApplicationRecycling failed."
    End If
End Sub

```



## <a name="related-topics"></a><span data-ttu-id="bebf7-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bebf7-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bebf7-133">Concetti relativi al riciclo delle applicazioni COM+</span><span class="sxs-lookup"><span data-stu-id="bebf7-133">COM+ Application Recycling Concepts</span></span>](com--application-recycling-concepts.md)
</dt> </dl>

 

 



