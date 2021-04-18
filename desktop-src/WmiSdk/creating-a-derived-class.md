---
description: La creazione di una classe derivata in WMI è molto simile alla creazione di una classe di base. Come per una classe base, è innanzitutto necessario definire la classe derivata e quindi registrare la classe derivata con WMI.
ms.assetid: 8dd483b8-8bc2-4a5c-b981-6c2ffaccdb95
ms.tgt_platform: multiple
title: Creazione di una classe derivata WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b65079d206cb7a0a490622018f6d2e2df98867d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310400"
---
# <a name="creating-a-wmi-derived-class"></a><span data-ttu-id="6a11c-104">Creazione di una classe derivata WMI</span><span class="sxs-lookup"><span data-stu-id="6a11c-104">Creating a WMI Derived Class</span></span>

<span data-ttu-id="6a11c-105">La creazione di una classe derivata in WMI è molto simile alla creazione di una classe di base.</span><span class="sxs-lookup"><span data-stu-id="6a11c-105">Creating a derived class in WMI is very similar to creating a base class.</span></span> <span data-ttu-id="6a11c-106">Come per una classe base, è innanzitutto necessario definire la classe derivata e quindi registrare la classe derivata con WMI.</span><span class="sxs-lookup"><span data-stu-id="6a11c-106">As with a base class, you must first define the derived class and then register the derived class with WMI.</span></span> <span data-ttu-id="6a11c-107">La differenza principale consiste nel fatto che è necessario innanzitutto individuare la classe padre da cui si desidera eseguire la derivazione.</span><span class="sxs-lookup"><span data-stu-id="6a11c-107">The main difference is that you must first locate the parent class from which you wish to derive.</span></span> <span data-ttu-id="6a11c-108">Per ulteriori informazioni, vedere [scrittura di un provider di classi](writing-a-class-provider.md) e [scrittura di un provider di istanze](writing-an-instance-provider.md).</span><span class="sxs-lookup"><span data-stu-id="6a11c-108">For more information, see [Writing a Class Provider](writing-a-class-provider.md) and [Writing an Instance Provider](writing-an-instance-provider.md).</span></span>

<span data-ttu-id="6a11c-109">Il metodo consigliato per creare classi per un provider è nei file Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="6a11c-109">The recommended way to create classes for a provider is in Managed Object Format (MOF) files.</span></span> <span data-ttu-id="6a11c-110">Diverse classi derivate che sono correlate tra loro devono essere raggruppate in un file MOF, insieme a tutte le classi di base da cui derivano le proprietà o i metodi.</span><span class="sxs-lookup"><span data-stu-id="6a11c-110">Several derived classes that are related to each other should be grouped into a MOF file, along with any base classes from which they derive properties or methods.</span></span> <span data-ttu-id="6a11c-111">Se si posiziona ogni classe in un file MOF separato, è necessario compilare ogni file prima che il provider possa funzionare correttamente.</span><span class="sxs-lookup"><span data-stu-id="6a11c-111">If you place each class in a separate MOF file then each file must be compiled before the provider can work properly.</span></span>

<span data-ttu-id="6a11c-112">Dopo aver creato la classe, è necessario eliminare tutte le istanze della classe prima di poter eseguire una delle attività seguenti sulla classe derivata:</span><span class="sxs-lookup"><span data-stu-id="6a11c-112">After you create your class, you must delete all instances of your class before you can perform any of the following activities on your derived class:</span></span>

-   <span data-ttu-id="6a11c-113">Modificare la classe padre della classe derivata.</span><span class="sxs-lookup"><span data-stu-id="6a11c-113">Change the parent class of your derived class.</span></span>
-   <span data-ttu-id="6a11c-114">Aggiungere o rimuovere proprietà.</span><span class="sxs-lookup"><span data-stu-id="6a11c-114">Add or remove properties.</span></span>
-   <span data-ttu-id="6a11c-115">Modificare i tipi di proprietà.</span><span class="sxs-lookup"><span data-stu-id="6a11c-115">Change property types.</span></span>
-   <span data-ttu-id="6a11c-116">Aggiungere o rimuovere la [**chiave**](key-qualifier.md) o i qualificatori **indicizzati** .</span><span class="sxs-lookup"><span data-stu-id="6a11c-116">Add or remove [**Key**](key-qualifier.md) or **Indexed** qualifiers.</span></span>
-   <span data-ttu-id="6a11c-117">Aggiungere o rimuovere qualificatori [**singleton**](standard-wmi-qualifiers.md), **dinamici** o [**astratti**](standard-qualifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="6a11c-117">Add or remove [**Singleton**](standard-wmi-qualifiers.md), **Dynamic**, or [**Abstract**](standard-qualifiers.md) qualifiers.</span></span>

> [!Note]  
> <span data-ttu-id="6a11c-118">Per aggiungere, rimuovere o modificare una proprietà o un qualificatore, chiamare [**IWbemServices::P utclass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass) o [**SWbemObject. \_ put**](swbemobject-put-.md) e impostare il parametro del flag su "Force Mode".</span><span class="sxs-lookup"><span data-stu-id="6a11c-118">To add, remove, or modify a property or qualifier, call [**IWbemServices::PutClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass) or [**SWbemObject.Put\_**](swbemobject-put-.md) and set the flag parameter to "force mode".</span></span> <span data-ttu-id="6a11c-119">Il qualificatore [**astratto**](standard-qualifiers.md) può essere utilizzato solo se la classe padre è astratta.</span><span class="sxs-lookup"><span data-stu-id="6a11c-119">The [**Abstract**](standard-qualifiers.md) qualifier can be used only if the parent class is abstract.</span></span>

 

<span data-ttu-id="6a11c-120">Quando si dichiara la classe derivata, osservare le regole e le restrizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="6a11c-120">When you declare your derived class, observe the following rules and restrictions:</span></span>

-   <span data-ttu-id="6a11c-121">La classe padre della classe derivata deve esistere già.</span><span class="sxs-lookup"><span data-stu-id="6a11c-121">The parent class of the derived class must already exist.</span></span>

    <span data-ttu-id="6a11c-122">La dichiarazione della classe padre può comparire nello stesso file MOF della classe derivata o in un file diverso.</span><span class="sxs-lookup"><span data-stu-id="6a11c-122">The declaration of the parent class can appear in the same MOF file as the derived class or in a different file.</span></span> <span data-ttu-id="6a11c-123">Se la classe padre è sconosciuta, il compilatore genera un errore di run-time.</span><span class="sxs-lookup"><span data-stu-id="6a11c-123">If the parent class is unknown, the compiler generates a run-time error.</span></span>

-   <span data-ttu-id="6a11c-124">Una classe derivata può avere una sola classe padre.</span><span class="sxs-lookup"><span data-stu-id="6a11c-124">A derived class can have only a single parent class.</span></span>

    <span data-ttu-id="6a11c-125">WMI non supporta l'ereditarietà multipla.</span><span class="sxs-lookup"><span data-stu-id="6a11c-125">WMI does not support multiple inheritance.</span></span> <span data-ttu-id="6a11c-126">Tuttavia, una classe padre può avere molte classi derivate.</span><span class="sxs-lookup"><span data-stu-id="6a11c-126">However, a parent class can have many derived classes.</span></span>

-   <span data-ttu-id="6a11c-127">È possibile definire gli indici per le classi derivate, ma WMI non utilizza questi indici.</span><span class="sxs-lookup"><span data-stu-id="6a11c-127">You can define indices for derived classes, but WMI does not use these indices.</span></span>

    <span data-ttu-id="6a11c-128">Pertanto, la specifica di un indice in una classe derivata non migliora le prestazioni delle query per le istanze della classe derivata.</span><span class="sxs-lookup"><span data-stu-id="6a11c-128">Therefore, specifying an index on a derived class does not improve the performance of queries for instances of the derived class.</span></span> <span data-ttu-id="6a11c-129">È possibile migliorare le prestazioni di una query su una classe derivata specificando le proprietà indicizzate per la classe padre della classe derivata.</span><span class="sxs-lookup"><span data-stu-id="6a11c-129">You can improve the performance of a query on a derived class by specifying indexed properties for the parent class of the derived class.</span></span>

-   <span data-ttu-id="6a11c-130">Le definizioni delle classi derivate possono essere più complesse e possono includere caratteristiche quali alias, qualificatori e versioni di qualificatori.</span><span class="sxs-lookup"><span data-stu-id="6a11c-130">Derived class definitions can be more complex, and can include such features as aliases, qualifiers, and qualifier flavors.</span></span>

    <span data-ttu-id="6a11c-131">Per ulteriori informazioni, vedere [creazione di un alias](creating-an-alias.md) e [aggiunta di un qualificatore](adding-a-qualifier.md).</span><span class="sxs-lookup"><span data-stu-id="6a11c-131">For more information, see [Creating an Alias](creating-an-alias.md) and [Adding a Qualifier](adding-a-qualifier.md).</span></span>

-   <span data-ttu-id="6a11c-132">Se si desidera modificare un qualificatore, modificare il valore predefinito di una proprietà della classe base o digitare più fortemente un riferimento o una proprietà dell'oggetto incorporato di una classe di base, è necessario dichiarare di nuovo l'intera classe di base.</span><span class="sxs-lookup"><span data-stu-id="6a11c-132">If you wish to change a qualifier, change the default value of a base class property, or more strongly type a reference or embedded object property of a base class, you must declare the entire base class again.</span></span>
-   <span data-ttu-id="6a11c-133">Il numero massimo di proprietà che è possibile definire in una classe WMI è 1024.</span><span class="sxs-lookup"><span data-stu-id="6a11c-133">The maximum number of properties you can define in a WMI class is 1024.</span></span>

> [!Note]  
> <span data-ttu-id="6a11c-134">Non è possibile modificare le classi durante l'esecuzione dei provider.</span><span class="sxs-lookup"><span data-stu-id="6a11c-134">Classes cannot be changed during execution of providers.</span></span> <span data-ttu-id="6a11c-135">È necessario arrestare l'attività, modificare la classe e quindi riavviare il servizio di gestione Windows.</span><span class="sxs-lookup"><span data-stu-id="6a11c-135">You must stop the activity, change the class, and then restart the Windows Management service.</span></span> <span data-ttu-id="6a11c-136">Il rilevamento di una modifica di classe non è attualmente possibile.</span><span class="sxs-lookup"><span data-stu-id="6a11c-136">Detecting a class change is currently not possible.</span></span>

 

<span data-ttu-id="6a11c-137">Come per la classe di base, l'uso più comune di questa tecnica è costituito dalle applicazioni client.</span><span class="sxs-lookup"><span data-stu-id="6a11c-137">As with the base class, the most common use of this technique will be by client applications.</span></span> <span data-ttu-id="6a11c-138">Tuttavia, un provider può anche creare una classe derivata.</span><span class="sxs-lookup"><span data-stu-id="6a11c-138">However, a provider can also create a derived class.</span></span> <span data-ttu-id="6a11c-139">Per ulteriori informazioni, vedere [creazione di una classe di base](creating-a-base-class.md) e [scrittura di un provider di classi](writing-a-class-provider.md).</span><span class="sxs-lookup"><span data-stu-id="6a11c-139">For more information, see [Creating a Base Class](creating-a-base-class.md) and [Writing a Class Provider](writing-a-class-provider.md).</span></span>

<span data-ttu-id="6a11c-140">Nell'esempio di codice in questo argomento è richiesta la \# compilazione corretta dell'istruzione include seguente.</span><span class="sxs-lookup"><span data-stu-id="6a11c-140">The code example in this topic requires the following \#include statement to compile correctly.</span></span>


```C++
#include <wbemidl.h>
```



<span data-ttu-id="6a11c-141">Nella procedura riportata di seguito viene descritto come creare una classe derivata mediante C++.</span><span class="sxs-lookup"><span data-stu-id="6a11c-141">The following procedure describes how to create a derived class using C++.</span></span>

<span data-ttu-id="6a11c-142">**Per creare una classe derivata con C++**</span><span class="sxs-lookup"><span data-stu-id="6a11c-142">**To create a derived class using C++**</span></span>

1.  <span data-ttu-id="6a11c-143">Individuare la classe di base con una chiamata a [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).</span><span class="sxs-lookup"><span data-stu-id="6a11c-143">Locate the base class with a call to [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).</span></span>

    <span data-ttu-id="6a11c-144">Nell'esempio di codice riportato di seguito viene illustrato come individuare la classe base di esempio.</span><span class="sxs-lookup"><span data-stu-id="6a11c-144">The following code example shows how to locate the Example base class.</span></span>

    ```C++
    // The pSv variable is of type IWbemServices *

    IWbemClassObject *pNewDerivedClass = 0;
    IWbemClassObject *pExampleClass = 0;
    IWbemContext *pCtx = 0;
    IWbemCallResult *pResult = 0;

    BSTR PathToClass = SysAllocString(L"Example");
    HRESULT hRes = pSvc->GetObject(PathToClass, 0, pCtx, &pExampleClass, &pResult);
    SysFreeString(PathToClass);
    ```

    

2.  <span data-ttu-id="6a11c-145">Creare un oggetto derivato dalla classe base con una chiamata a [**IWbemClassObject:: SpawnDerivedClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawnderivedclass).</span><span class="sxs-lookup"><span data-stu-id="6a11c-145">Create a derived object from the base class with a call to [**IWbemClassObject::SpawnDerivedClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawnderivedclass).</span></span>

    <span data-ttu-id="6a11c-146">Nell'esempio di codice seguente viene illustrato come creare un oggetto di classe derivata.</span><span class="sxs-lookup"><span data-stu-id="6a11c-146">The following code example shows how to create a derived class object.</span></span>

    ```C++
    pExampleClass->SpawnDerivedClass(0, &pNewDerivedClass);
    pExampleClass->Release();  // Don't need the parent class any more
    ```

    

3.  <span data-ttu-id="6a11c-147">Definire un nome per la classe impostando la proprietà di sistema della **\_ \_ classe** con una chiamata al metodo [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) .</span><span class="sxs-lookup"><span data-stu-id="6a11c-147">Establish a name for the class by setting the **\_\_CLASS** system property with a call to the [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) method.</span></span>

    <span data-ttu-id="6a11c-148">Nell'esempio di codice seguente viene illustrato come assegnare un nome alla classe derivata.</span><span class="sxs-lookup"><span data-stu-id="6a11c-148">The following code example shows how to assign a name to the derived class.</span></span>

    ```C++
    VARIANT v;
    VariantInit(&v);

    V_VT(&v) = VT_BSTR;
    V_BSTR(&v) = SysAllocString(L"Example2");
    BSTR Class = SysAllocString(L"__CLASS");
    pNewDerivedClass->Put(Class, 0, &v, 0);
    SysFreeString(Class);
    VariantClear(&v);
    ```

    

4.  <span data-ttu-id="6a11c-149">Creare proprietà aggiuntive con [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span><span class="sxs-lookup"><span data-stu-id="6a11c-149">Create additional properties with [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span></span>

    <span data-ttu-id="6a11c-150">Nell'esempio di codice seguente viene illustrato come creare proprietà aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="6a11c-150">The following code example shows how to create additional properties.</span></span>

    ```C++
    BSTR OtherProp = SysAllocString(L"OtherInfo2");
    pNewDerivedClass->Put(OtherProp, 0, NULL, CIM_STRING); 
    SysFreeString(OtherProp);
    ```

    

5.  <span data-ttu-id="6a11c-151">Salvare la nuova classe chiamando [**IWbemServices::P utclass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass).</span><span class="sxs-lookup"><span data-stu-id="6a11c-151">Save the new class by calling [**IWbemServices::PutClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass).</span></span>

    <span data-ttu-id="6a11c-152">Nell'esempio di codice seguente viene illustrato come salvare la nuova classe derivata.</span><span class="sxs-lookup"><span data-stu-id="6a11c-152">The following code example shows how to save the new derived class.</span></span>

    ```C++
    hRes = pSvc->PutClass(pNewDerivedClass, 0, pCtx, &pResult);
    pNewDerivedClass->Release();
    ```

    

<span data-ttu-id="6a11c-153">Nell'esempio di codice seguente vengono combinati gli esempi di codice illustrati nella procedura precedente per descrivere come creare una classe derivata utilizzando l'API WMI.</span><span class="sxs-lookup"><span data-stu-id="6a11c-153">The following code example combines the code examples discussed in the previous procedure to describe how to create a derived class using the WMI API.</span></span>


```C++
void CreateDerivedClass(IWbemServices *pSvc)
{
  IWbemClassObject *pNewDerivedClass = 0;
  IWbemClassObject *pExampleClass = 0;
  IWbemContext *pCtx = 0;
  IWbemCallResult *pResult = 0;

  BSTR PathToClass = SysAllocString(L"Example");
  HRESULT hRes = pSvc->GetObject(PathToClass, 0, pCtx, 
    &pExampleClass, &pResult);
  SysFreeString(PathToClass);

  if (hRes != 0)
    return;

  pExampleClass->SpawnDerivedClass(0, &pNewDerivedClass);
  pExampleClass->Release();  // The parent class is no longer needed

  VARIANT v;
  VariantInit(&v);

  // Create the class name.
  // =====================

  V_VT(&v) = VT_BSTR;
  V_BSTR(&v) = SysAllocString(L"Example2");
  BSTR Class = SysAllocString(L"__CLASS");
  pNewDerivedClass->Put(Class, 0, &v, 0);
  SysFreeString(Class);
  VariantClear(&v);

  // Create another property.
  // =======================
  BSTR OtherProp = SysAllocString(L"OtherInfo2");
  // No default value
  pNewDerivedClass->Put(OtherProp, 0, NULL, CIM_STRING); 
  SysFreeString(OtherProp);
  
  // Register the class with WMI. 
  // ============================
  hRes = pSvc->PutClass(pNewDerivedClass, 0, pCtx, &pResult);
  pNewDerivedClass->Release();
}
```



<span data-ttu-id="6a11c-154">Nella procedura riportata di seguito viene descritto come definire una classe derivata utilizzando il codice MOF.</span><span class="sxs-lookup"><span data-stu-id="6a11c-154">The following procedure describes how to define a derived class using MOF code.</span></span>

<span data-ttu-id="6a11c-155">**Per definire una classe derivata utilizzando il codice MOF**</span><span class="sxs-lookup"><span data-stu-id="6a11c-155">**To define a derived class using MOF code**</span></span>

1.  <span data-ttu-id="6a11c-156">Definire la classe derivata con la parola chiave **Class** , seguita dal nome della classe derivata e il nome della classe padre separata da due punti.</span><span class="sxs-lookup"><span data-stu-id="6a11c-156">Define your derived class with the **Class** keyword, followed by the name of your derived class, and the name of the parent class separated by a colon.</span></span>

    <span data-ttu-id="6a11c-157">Nell'esempio di codice seguente viene descritta un'implementazione di una classe derivata.</span><span class="sxs-lookup"><span data-stu-id="6a11c-157">The following code example describes an implementation of a derived class.</span></span>

    ``` syntax
    class MyClass 
    {
        [key] string   strProp;
        sint32   dwProp1;
        uint32       dwProp2;
    };

    class MyDerivedClass : MyClass
    {
        string   strDerivedProp;
        sint32   dwDerivedProp;
    };
    ```

2.  <span data-ttu-id="6a11c-158">Al termine, compilare il codice MOF con il compilatore MOF.</span><span class="sxs-lookup"><span data-stu-id="6a11c-158">When complete, compile your MOF code with the MOF compiler.</span></span>

    <span data-ttu-id="6a11c-159">Per ulteriori informazioni, vedere [compilazione di file MOF](compiling-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="6a11c-159">For more information, see [Compiling MOF Files](compiling-mof-files.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6a11c-160">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6a11c-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a11c-161">Creazione di una classe</span><span class="sxs-lookup"><span data-stu-id="6a11c-161">Creating a Class</span></span>](creating-a-class.md)
</dt> </dl>

 

 



