---
description: È possibile creare un'istanza di in C++ tramite l'interfaccia IWbemServices.
ms.assetid: ee54c1ef-bc91-4771-8c11-9ee3aacd8112
ms.tgt_platform: multiple
title: Creazione e dichiarazione di un'istanza con C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd316975c68625383a9d2a2d1fe2fc389d30494a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316571"
---
# <a name="creating-and-declaring-an-instance-using-c"></a><span data-ttu-id="de1f2-103">Creazione e dichiarazione di un'istanza con C++</span><span class="sxs-lookup"><span data-stu-id="de1f2-103">Creating and Declaring an Instance Using C++</span></span>

<span data-ttu-id="de1f2-104">È possibile creare un'istanza di in C++ tramite l'interfaccia [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) .</span><span class="sxs-lookup"><span data-stu-id="de1f2-104">You can create an instance in C++ through the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interface.</span></span>

<span data-ttu-id="de1f2-105">Gli esempi di codice in questo argomento richiedono la \# compilazione corretta dell'istruzione include seguente.</span><span class="sxs-lookup"><span data-stu-id="de1f2-105">The code examples in this topic require the following \#include statement to compile correctly.</span></span>


```C++
#include <wbemidl.h>
```



<span data-ttu-id="de1f2-106">Nella procedura riportata di seguito viene descritto come creare un'istanza di una classe esistente.</span><span class="sxs-lookup"><span data-stu-id="de1f2-106">The following procedure describes how to create an instance of an existing class.</span></span>

<span data-ttu-id="de1f2-107">**Per creare un'istanza di una classe esistente**</span><span class="sxs-lookup"><span data-stu-id="de1f2-107">**To create an instance of an existing class**</span></span>

1.  <span data-ttu-id="de1f2-108">Recuperare la definizione della classe esistente chiamando il metodo [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) o [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) .</span><span class="sxs-lookup"><span data-stu-id="de1f2-108">Retrieve the definition of the existing class by calling the [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) or [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) methods.</span></span>

    <span data-ttu-id="de1f2-109">Nell'esempio di codice seguente viene illustrato come utilizzare i metodi [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) e [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) per ottenere un puntatore all'interfaccia [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) che fornisce l'accesso alla definizione della classe.</span><span class="sxs-lookup"><span data-stu-id="de1f2-109">The following code example shows how to use the [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) and [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) methods to get a pointer to the [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) interface that provides access to the class definition.</span></span>

    ```C++
    // The pSv variable is of type IWbemServices *

    IWbemClassObject *pNewInstance = 0;
    IWbemClassObject *pExampleClass = 0;
    IWbemContext *pCtx = 0;
    IWbemCallResult *pResult = 0;

    BSTR PathToClass = SysAllocString(L"Example");
    HRESULT hRes = pSvc->GetObject(PathToClass, 0, pCtx, 
                  &pExampleClass, &pResult);
    SysFreeString(PathToClass);
    ```

    

2.  <span data-ttu-id="de1f2-110">Creare la nuova istanza di chiamando il metodo [**IWbemClassObject:: SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance) .</span><span class="sxs-lookup"><span data-stu-id="de1f2-110">Create the new instance by calling the [**IWbemClassObject::SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance) method.</span></span>

    <span data-ttu-id="de1f2-111">Nell'esempio di codice seguente viene illustrato come creare una nuova istanza di e quindi rilasciare la classe.</span><span class="sxs-lookup"><span data-stu-id="de1f2-111">The following code example shows how to create a new instance and then release the class.</span></span>

    ```C++
    pExampleClass->SpawnInstance(0, &pNewInstance);
    pExampleClass->Release();  // Don't need the class any more
    ```

    

3.  <span data-ttu-id="de1f2-112">Impostare i valori per tutte le proprietà che non ereditano i valori definiti per la classe chiamando il metodo [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) .</span><span class="sxs-lookup"><span data-stu-id="de1f2-112">Set values for any properties that do not inherit the values defined for the class by calling the [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) method.</span></span>

    <span data-ttu-id="de1f2-113">Ogni istanza di una classe eredita tutte le proprietà definite per la classe.</span><span class="sxs-lookup"><span data-stu-id="de1f2-113">Each instance of a class inherits all of the properties that are defined for the class.</span></span> <span data-ttu-id="de1f2-114">Tuttavia, se si sceglie, è possibile specificare valori di proprietà diversi.</span><span class="sxs-lookup"><span data-stu-id="de1f2-114">However, you can specify different property values if you choose.</span></span>

    <span data-ttu-id="de1f2-115">Se la classe esistente ha una proprietà chiave, è necessario impostare la proprietà su **null** o su un valore univoco garantito.</span><span class="sxs-lookup"><span data-stu-id="de1f2-115">If the existing class has a key property, you should set the property either to **NULL** or a guaranteed unique value.</span></span> <span data-ttu-id="de1f2-116">Se si imposta la chiave su **null** e la chiave è una stringa, [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) o [**PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) genera internamente e assegna un GUID alla chiave.</span><span class="sxs-lookup"><span data-stu-id="de1f2-116">If you set the key to **NULL** and the key is a string, then [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) or [**PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) internally generates and assigns a GUID to the key.</span></span> <span data-ttu-id="de1f2-117">In questo modo, se si specifica **null** per una proprietà chiave, è possibile creare un'istanza univoca che non sovrascrive alcuna istanza precedente.</span><span class="sxs-lookup"><span data-stu-id="de1f2-117">This way, specifying **NULL** for a key property lets you create a unique instance that will not overwrite any previous instance.</span></span>

    <span data-ttu-id="de1f2-118">Nell'esempio di codice seguente viene illustrato come impostare il valore della proprietà [**index**](swbemrefreshableitem-index.md) della classe di istanza di esempio.</span><span class="sxs-lookup"><span data-stu-id="de1f2-118">The following code example shows how to set the [**Index**](swbemrefreshableitem-index.md) property value of the example instance class.</span></span>

    ```C++
    VARIANT v;
    VariantInit(&v);

    V_VT(&v) = VT_BSTR;
    V_BSTR(&v) = SysAllocString(L"IX100");

    BSTR KeyProp = SysAllocString(L"Index");
    pNewInstance->Put(KeyProp, 0, &v, 0);
    SysFreeString(KeyProp);
    VariantClear(&v);
    ```

    

4.  <span data-ttu-id="de1f2-119">Impostare i valori per i qualificatori rilevanti tramite una chiamata a [**IWbemClassObject:: GetQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getqualifierset).</span><span class="sxs-lookup"><span data-stu-id="de1f2-119">Set the values for any relevant qualifiers through a call to [**IWbemClassObject::GetQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getqualifierset).</span></span>

    <span data-ttu-id="de1f2-120">Il metodo [**GetQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getqualifierset) restituisce un puntatore a un'interfaccia [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) , che usa per accedere ai qualificatori per una classe o un'istanza.</span><span class="sxs-lookup"><span data-stu-id="de1f2-120">The [**GetQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getqualifierset) method returns a pointer to an [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) interface, which use to access the qualifiers for a class or instance.</span></span> <span data-ttu-id="de1f2-121">È possibile specificare valori diversi per un qualificatore definito per la classe se la versione del qualificatore di classe è **EnableOverride**.</span><span class="sxs-lookup"><span data-stu-id="de1f2-121">You can specify different values for a qualifier defined for the class if the class qualifier flavor is **EnableOverride**.</span></span> <span data-ttu-id="de1f2-122">Non è possibile modificare o eliminare un qualificatore di classe con la versione di Flavor impostata su **DisableOverride**.</span><span class="sxs-lookup"><span data-stu-id="de1f2-122">You cannot modify or delete a class qualifier with the flavor set to **DisableOverride**.</span></span> <span data-ttu-id="de1f2-123">Per altre informazioni, vedere [tipi di qualificatori](qualifier-flavors.md).</span><span class="sxs-lookup"><span data-stu-id="de1f2-123">For more information, see [Qualifier Flavors](qualifier-flavors.md).</span></span>

    <span data-ttu-id="de1f2-124">Facoltativamente, è anche possibile definire qualificatori aggiuntivi per la classe dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="de1f2-124">As an option, you can also define additional qualifiers for your instance class.</span></span> <span data-ttu-id="de1f2-125">È possibile definire qualificatori aggiuntivi per la proprietà dell'istanza o dell'istanza che non devono essere visualizzati nella dichiarazione della classe.</span><span class="sxs-lookup"><span data-stu-id="de1f2-125">You can define additional qualifiers for the instance or instance property which do not need to appear in the class declaration.</span></span>

5.  <span data-ttu-id="de1f2-126">Salvare l'istanza chiamando il metodo [**IWbemServices::P utinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) o [**IWbemServices::P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) .</span><span class="sxs-lookup"><span data-stu-id="de1f2-126">Save the instance by calling the [**IWbemServices::PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) or [**IWbemServices::PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) method.</span></span>

    <span data-ttu-id="de1f2-127">WMI Salva l'istanza nello spazio dei nomi WMI corrente.</span><span class="sxs-lookup"><span data-stu-id="de1f2-127">WMI saves the instance in the current WMI namespace.</span></span> <span data-ttu-id="de1f2-128">Di conseguenza, il percorso completo dell'istanza dipende dallo spazio dei nomi, che in genere è l' \\ impostazione predefinita radice.</span><span class="sxs-lookup"><span data-stu-id="de1f2-128">As such, the full path of the instance is dependent on the namespace, which is typically root\\default.</span></span> <span data-ttu-id="de1f2-129">Per questo esempio di codice, il nome del percorso completo sarà \\ \\ . \\ \\impostazione predefinita radice: example. index = "IX100".</span><span class="sxs-lookup"><span data-stu-id="de1f2-129">For this code example, the full path name would be \\\\.\\root\\default:Example.Index="IX100".</span></span>

    <span data-ttu-id="de1f2-130">Nell'esempio di codice seguente viene illustrato come salvare un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="de1f2-130">The following code example shows how to save an instance.</span></span>

    ```C++
        hRes = pSvc->PutInstance(pNewInstance, 0, pCtx, &pResult);
        pNewInstance->Release();
    ```

    

<span data-ttu-id="de1f2-131">Il salvataggio dell'istanza in WMI blocca diverse proprietà dell'istanza di.</span><span class="sxs-lookup"><span data-stu-id="de1f2-131">Saving the instance to WMI locks down several of the properties of the instance.</span></span>

<span data-ttu-id="de1f2-132">In particolare, non è possibile eseguire le operazioni seguenti tramite l'API WMI dopo l'esistenza di un'istanza nell'infrastruttura WMI:</span><span class="sxs-lookup"><span data-stu-id="de1f2-132">Specifically, you cannot perform any of the following operations through the WMI API after an instance exists within the WMI infrastructure:</span></span>

-   <span data-ttu-id="de1f2-133">Modificare la classe padre della classe a cui appartiene l'istanza.</span><span class="sxs-lookup"><span data-stu-id="de1f2-133">Change the parent class of the class to which the instance belongs.</span></span>
-   <span data-ttu-id="de1f2-134">Aggiungere o rimuovere proprietà.</span><span class="sxs-lookup"><span data-stu-id="de1f2-134">Add or remove properties.</span></span>
-   <span data-ttu-id="de1f2-135">Modificare i tipi di proprietà.</span><span class="sxs-lookup"><span data-stu-id="de1f2-135">Change property types.</span></span>
-   <span data-ttu-id="de1f2-136">Aggiungere o rimuovere la [**chiave**](standard-qualifiers.md) o i qualificatori **indicizzati** .</span><span class="sxs-lookup"><span data-stu-id="de1f2-136">Add or remove [**Key**](standard-qualifiers.md) or **Indexed** qualifiers.</span></span>
-   <span data-ttu-id="de1f2-137">Aggiungere o rimuovere qualificatori [**singleton**](standard-wmi-qualifiers.md), **dinamici** o [**astratti**](standard-qualifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="de1f2-137">Add or remove [**Singleton**](standard-wmi-qualifiers.md), **Dynamic**, or [**Abstract**](standard-qualifiers.md) qualifiers.</span></span>

<span data-ttu-id="de1f2-138">Nell'esempio di codice seguente vengono combinati gli esempi di codice illustrati nella procedura precedente per illustrare come creare un'istanza di tramite l'API WMI.</span><span class="sxs-lookup"><span data-stu-id="de1f2-138">The following code example combines the code examples discussed in the previous procedure to show how to create an instance using the WMI API.</span></span>


```C++
void CreateInstance (IWbemServices *pSvc)
{
    IWbemClassObject *pNewInstance = 0;
    IWbemClassObject *pExampleClass = 0;
    IWbemContext *pCtx = 0;
    IWbemCallResult *pResult = 0;

    // Get the class definition.
    BSTR PathToClass = SysAllocString(L"Example");
    HRESULT hRes = pSvc->GetObject(PathToClass, 0, pCtx, 
                 &pExampleClass, &pResult);
    SysFreeString(PathToClass);

    if (hRes != 0)
       return;

    // Create a new instance.
    pExampleClass->SpawnInstance(0, &pNewInstance);
    pExampleClass->Release();  // Don't need the class any more

    VARIANT v;
    VariantInit(&v);

    // Set the Index property (the key).
    V_VT(&v) = VT_BSTR;
    V_BSTR(&v) = SysAllocString(L"IX100");

    BSTR KeyProp = SysAllocString(L"Index");
    pNewInstance->Put(KeyProp, 0, &v, 0);
    SysFreeString(KeyProp);
    VariantClear(&v);

    // Set the IntVal property.
    V_VT(&v) = VT_I4;
    V_I4(&v) = 1001;  
    
    BSTR Prop = SysAllocString(L"IntVal");
    pNewInstance->Put(Prop, 0, &v, 0);
    SysFreeString(Prop);
    VariantClear(&v);    
    
    // Other properties acquire the 'default' value specified
    // in the class definition unless otherwise modified here.

    // Write the instance to WMI. 
    hRes = pSvc->PutInstance(pNewInstance, 0, pCtx, &pResult);
    pNewInstance->Release();
}
```



 

 



