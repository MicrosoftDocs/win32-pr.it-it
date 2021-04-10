---
description: Il metodo consigliato per creare una nuova classe di base WMI per un provider WMI è in un file di Managed Object Format (MOF).
ms.assetid: d46060aa-77c3-4f51-b4a7-2c3612f2bc5c
ms.tgt_platform: multiple
title: Creazione di una classe di base WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebdcbe6995a7782d854a4d0950db841f23a30b45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968369"
---
# <a name="creating-a-wmi-base-class"></a><span data-ttu-id="90271-103">Creazione di una classe di base WMI</span><span class="sxs-lookup"><span data-stu-id="90271-103">Creating a WMI Base Class</span></span>

<span data-ttu-id="90271-104">Il metodo consigliato per creare una nuova classe di base WMI per un provider WMI è in un file di Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="90271-104">The recommended way to create a new WMI base class for a WMI provider is in a Managed Object Format (MOF) file.</span></span> <span data-ttu-id="90271-105">È inoltre possibile creare una classe di base utilizzando l' [API com per WMI](com-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="90271-105">You can also create a base class using the [COM API for WMI](com-api-for-wmi.md).</span></span> <span data-ttu-id="90271-106">Sebbene sia possibile creare una classe base o derivata nello script, senza che un provider fornisca dati alla classe e alle relative sottoclassi, la classe non è utile.</span><span class="sxs-lookup"><span data-stu-id="90271-106">While you can create a base or derived class in script, without a provider supplying data to the class and its subclasses, the class is not useful.</span></span>

<span data-ttu-id="90271-107">Le sezioni seguenti sono illustrate in questo argomento:</span><span class="sxs-lookup"><span data-stu-id="90271-107">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="90271-108">Creazione di una classe di base utilizzando MOF</span><span class="sxs-lookup"><span data-stu-id="90271-108">Creating a Base Class Using MOF</span></span>](#creating-a-base-class-using-mof)
-   [<span data-ttu-id="90271-109">Creazione di una classe base con C++</span><span class="sxs-lookup"><span data-stu-id="90271-109">Creating a Base Class with C++</span></span>](#creating-a-base-class-with-c)
-   [<span data-ttu-id="90271-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="90271-110">Related topics</span></span>](#related-topics)

## <a name="creating-a-base-class-using-mof"></a><span data-ttu-id="90271-111">Creazione di una classe di base utilizzando MOF</span><span class="sxs-lookup"><span data-stu-id="90271-111">Creating a Base Class Using MOF</span></span>

<span data-ttu-id="90271-112">Le classi WMI si basano in genere sull'ereditarietà.</span><span class="sxs-lookup"><span data-stu-id="90271-112">WMI classes usually rely on inheritance.</span></span> <span data-ttu-id="90271-113">Prima di creare una classe di base, controllare le classi Common Information Model (CIM) disponibili da Distributed Management Task Force ([DMTF](https://www.dmtf.org/)).</span><span class="sxs-lookup"><span data-stu-id="90271-113">Before creating a base class, check the Common Information Model (CIM) classes available from the Distributed Management Task Force ([DMTF](https://www.dmtf.org/)).</span></span>

<span data-ttu-id="90271-114">Se molte classi derivate utilizzeranno le stesse proprietà, inserire queste proprietà e questi metodi nella classe di base.</span><span class="sxs-lookup"><span data-stu-id="90271-114">If many derived classes will use the same properties, put these properties and methods in your base class.</span></span> <span data-ttu-id="90271-115">Il numero massimo di proprietà che è possibile definire in una classe WMI è 1024.</span><span class="sxs-lookup"><span data-stu-id="90271-115">The maximum number of properties you can define in a WMI class is 1024.</span></span>

<span data-ttu-id="90271-116">Quando si crea una classe base, osservare l'elenco seguente di linee guida per i nomi delle classi:</span><span class="sxs-lookup"><span data-stu-id="90271-116">When creating a base class, observe the following list of guidelines for class names:</span></span>

-   <span data-ttu-id="90271-117">Usare lettere maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="90271-117">Use both uppercase and lowercase letters.</span></span>
-   <span data-ttu-id="90271-118">Inizia un nome di classe con una lettera.</span><span class="sxs-lookup"><span data-stu-id="90271-118">Begin a class name with a letter.</span></span>
-   <span data-ttu-id="90271-119">Non usare un carattere di sottolineatura iniziali o finali.</span><span class="sxs-lookup"><span data-stu-id="90271-119">Do not use either a leading or trailing underscore.</span></span>
-   <span data-ttu-id="90271-120">Definire tutti i caratteri rimanenti come lettere, cifre o caratteri di sottolineatura.</span><span class="sxs-lookup"><span data-stu-id="90271-120">Define all remaining characters as letters, digits, or underscores.</span></span>
-   <span data-ttu-id="90271-121">Usare una convenzione di denominazione coerente.</span><span class="sxs-lookup"><span data-stu-id="90271-121">Use a consistent naming convention.</span></span>

    <span data-ttu-id="90271-122">Sebbene non sia necessario, una convenzione di denominazione corretta per una classe è due componenti Uniti da un carattere di sottolineatura.</span><span class="sxs-lookup"><span data-stu-id="90271-122">While not necessary, a good naming convention for a class is two components joined by an underscore.</span></span> <span data-ttu-id="90271-123">Quando possibile, un nome di fornitore deve costituire la prima metà del nome e un nome di classe descrittivo deve essere la seconda parte.</span><span class="sxs-lookup"><span data-stu-id="90271-123">When possible, a vendor name should make up the first half of the name, and a descriptive class name should be the second part.</span></span>

> [!Note]  
> <span data-ttu-id="90271-124">Non è possibile modificare le classi durante l'esecuzione dei provider.</span><span class="sxs-lookup"><span data-stu-id="90271-124">Classes cannot be changed during execution of providers.</span></span> <span data-ttu-id="90271-125">È necessario arrestare l'attività, modificare la classe e quindi riavviare il servizio di gestione Windows.</span><span class="sxs-lookup"><span data-stu-id="90271-125">You must stop the activity, change the class, and then restart the Windows Management service.</span></span> <span data-ttu-id="90271-126">Il rilevamento di una modifica di classe non è attualmente possibile.</span><span class="sxs-lookup"><span data-stu-id="90271-126">Detecting a class change is currently not possible.</span></span>

 

<span data-ttu-id="90271-127">In MOF creare una classe base chiamandola con la parola chiave **Class** , ma non indicando una classe padre.</span><span class="sxs-lookup"><span data-stu-id="90271-127">In MOF, create a base class by naming it with the **class** keyword, but not indicating a parent class.</span></span>

<span data-ttu-id="90271-128">**Per creare una classe di base utilizzando il codice MOF**</span><span class="sxs-lookup"><span data-stu-id="90271-128">**To create a base class using MOF code**</span></span>

1.  <span data-ttu-id="90271-129">Usare la parola chiave **Class** con il nome della nuova classe, seguita da una coppia di parentesi graffe e da un punto e virgola.</span><span class="sxs-lookup"><span data-stu-id="90271-129">Use the **class** keyword with the name of the new class, followed by a pair of curly braces and a semicolon.</span></span> <span data-ttu-id="90271-130">Aggiungere le proprietà e i metodi per la classe tra parentesi graffe.</span><span class="sxs-lookup"><span data-stu-id="90271-130">Add properties and methods for the class between the curly braces.</span></span> <span data-ttu-id="90271-131">Viene fornito l'esempio di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="90271-131">The following code example is provided.</span></span>

    <span data-ttu-id="90271-132">Nell'esempio di codice riportato di seguito viene illustrato come definire una classe di base.</span><span class="sxs-lookup"><span data-stu-id="90271-132">The following code example shows how a base class should be defined.</span></span>

    ``` syntax
    class MyClass_BaseDisk
    {
    };
    ```

    <span data-ttu-id="90271-133">Nell'esempio di codice seguente viene illustrata una definizione non corretta di una classe di base.</span><span class="sxs-lookup"><span data-stu-id="90271-133">The following code example shows an incorrect definition of a base class.</span></span>

    ``` syntax
    class MyClass_BaseDisk : CIM_LogicalDisk
    {
    };
    ```

2.  <span data-ttu-id="90271-134">Aggiungere i [*qualificatori*](gloss-q.md) di classe prima della parola chiave Class per modificare la modalità di utilizzo della classe.</span><span class="sxs-lookup"><span data-stu-id="90271-134">Add any class [*qualifiers*](gloss-q.md) before the class keyword to modify the way the class is used.</span></span> <span data-ttu-id="90271-135">Posizionare i qualificatori tra parentesi quadre.</span><span class="sxs-lookup"><span data-stu-id="90271-135">Place the qualifiers between square brackets.</span></span> <span data-ttu-id="90271-136">Per ulteriori informazioni sui qualificatori per la modifica delle classi, vedere [qualificatori WMI](wmi-qualifiers.md).</span><span class="sxs-lookup"><span data-stu-id="90271-136">For more information about qualifiers for modifying classes, see [WMI Qualifiers](wmi-qualifiers.md).</span></span> <span data-ttu-id="90271-137">Utilizzare il qualificatore **astratto** per indicare che non è possibile creare direttamente un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="90271-137">Use the **Abstract** qualifier to indicate that you cannot create an instance of this class directly.</span></span> <span data-ttu-id="90271-138">Le classi astratte vengono spesso usate per definire le proprietà o i metodi che verranno usati da diverse classi derivate.</span><span class="sxs-lookup"><span data-stu-id="90271-138">Abstract classes are often used to define properties or methods that will be used by several derived classes.</span></span> <span data-ttu-id="90271-139">Per ulteriori informazioni, vedere [creazione di una classe derivata](creating-a-derived-class.md).</span><span class="sxs-lookup"><span data-stu-id="90271-139">For more information, see [Creating a Derived Class](creating-a-derived-class.md).</span></span>

    <span data-ttu-id="90271-140">Nell'esempio di codice seguente viene definita la classe come astratta e viene definito il provider che fornirà i dati.</span><span class="sxs-lookup"><span data-stu-id="90271-140">The following code example defines the class as abstract and defines the provider that will supply the data.</span></span> <span data-ttu-id="90271-141">La versione del qualificatore **ToClass** indica che le informazioni [*nel qualificatore*](gloss-f.md) del **provider** sono ereditate dalle classi derivate.</span><span class="sxs-lookup"><span data-stu-id="90271-141">The **ToSubClass** qualifier [*flavor*](gloss-f.md) indicates that the information in the **Provider** qualifier is inherited by derived classes.</span></span>

    ``` syntax
    [Abstract, Provider("MyProvider") : ToSubClass]
    class MyClass_BaseDisk
    {
    };
    ```

3.  <span data-ttu-id="90271-142">Aggiungere le proprietà e i metodi della classe all'interno di parentesi quadre prima del nome della proprietà o del metodo.</span><span class="sxs-lookup"><span data-stu-id="90271-142">Add the properties and methods for the class inside square brackets before the property or method name.</span></span> <span data-ttu-id="90271-143">Per ulteriori informazioni, vedere [aggiunta di una proprietà](adding-a-property.md) e [creazione di un metodo](creating-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="90271-143">For more information, see [Adding a Property](adding-a-property.md) and [Creating a Method](creating-a-method.md).</span></span> <span data-ttu-id="90271-144">È possibile modificare queste proprietà e metodi usando i qualificatori MOF.</span><span class="sxs-lookup"><span data-stu-id="90271-144">You can modify these properties and methods using MOF qualifiers.</span></span> <span data-ttu-id="90271-145">Per ulteriori informazioni, vedere [aggiunta di un qualificatore](adding-a-qualifier.md).</span><span class="sxs-lookup"><span data-stu-id="90271-145">For more information, see [Adding a Qualifier](adding-a-qualifier.md).</span></span>

    <span data-ttu-id="90271-146">Nell'esempio di codice riportato di seguito viene illustrato come modificare proprietà e metodi con qualificatori MOF.</span><span class="sxs-lookup"><span data-stu-id="90271-146">The following code example shows how to modify properties and methods with MOF qualifiers.</span></span>

    ``` syntax
    [read : ToSubClass, key : ToSubClass ] string DeviceID;
      [read : ToSubClass] uint32 State;
      [read : ToSubclass, write : ToSubClass] uint64 LimitUsers;
    ```

4.  <span data-ttu-id="90271-147">Salvare il file MOF con estensione MOF.</span><span class="sxs-lookup"><span data-stu-id="90271-147">Save the MOF file with an extension of .mof.</span></span>
5.  <span data-ttu-id="90271-148">Registrare la classe con WMI eseguendo [**Mofcomp.exe**](mofcomp.md) sul file.</span><span class="sxs-lookup"><span data-stu-id="90271-148">Register the class with WMI by running [**Mofcomp.exe**](mofcomp.md) on the file.</span></span>

    <span data-ttu-id="90271-149">**mofcomp.exe** *newmof. mof*</span><span class="sxs-lookup"><span data-stu-id="90271-149">**mofcomp.exe** *newmof.mof*</span></span>

    <span data-ttu-id="90271-150">Se non si usa l'opzione **-N** o lo \# [**spazio dei nomi pragma**](pragma-namespace.md) del comando per il preprocessore per specificare uno spazio dei nomi, le classi MOF compilate verranno archiviate nello \\ spazio dei nomi predefinito radice nel repository.</span><span class="sxs-lookup"><span data-stu-id="90271-150">If you do not use the **-N** switch or the preprocessor command \#[**pragma namespace**](pragma-namespace.md) to specify a namespace, the compiled MOF classes will be stored in the root\\default namespace in the repository.</span></span> <span data-ttu-id="90271-151">Per ulteriori informazioni, vedere [**mofcomp**](mofcomp.md).</span><span class="sxs-lookup"><span data-stu-id="90271-151">For more information, see [**mofcomp**](mofcomp.md).</span></span>

<span data-ttu-id="90271-152">Nell'esempio di codice seguente vengono combinati gli esempi di codice MOF descritti nella procedura precedente e viene illustrato come creare una classe di base nello \\ spazio dei nomi CIMV2 radice utilizzando MOF.</span><span class="sxs-lookup"><span data-stu-id="90271-152">The following code example combines the MOF code examples discussed in the previous procedure and shows how to create a base class in the root\\cimv2 namespace using MOF.</span></span>

``` syntax
#pragma namespace("\\\\.\\Root\\cimv2")

[Abstract, Provider("MyProvider") : ToSubClass]
class MyClass_BaseDisk
{
  [read : ToSubClass, key : ToSubClass ] string DeviceID;
  [read : ToSubClass] uint32 State;
  [read : ToSubClass, write : ToSubClass] uint64 LimitUsers;
};
```

<span data-ttu-id="90271-153">Per ulteriori informazioni, vedere [creazione di una classe derivata](creating-a-derived-class.md) per un esempio di classe dinamica derivata da questa classe di base.</span><span class="sxs-lookup"><span data-stu-id="90271-153">For more information, see [Creating a Derived Class](creating-a-derived-class.md) for an example of a dynamic class derived from this base class.</span></span>

## <a name="creating-a-base-class-with-c"></a><span data-ttu-id="90271-154">Creazione di una classe base con C++</span><span class="sxs-lookup"><span data-stu-id="90271-154">Creating a Base Class with C++</span></span>

<span data-ttu-id="90271-155">La creazione di una classe di base tramite l'API WMI è principalmente una serie di comandi put che definiscono la classe e registrano la classe con WMI.</span><span class="sxs-lookup"><span data-stu-id="90271-155">Creating a base class using the WMI API is mainly a series of Put commands that define the class and register the class with WMI.</span></span> <span data-ttu-id="90271-156">Lo scopo principale di questa API è quello di consentire alle applicazioni client di creare classi di base.</span><span class="sxs-lookup"><span data-stu-id="90271-156">The main purpose of this API is to enable client applications to create base classes.</span></span> <span data-ttu-id="90271-157">Tuttavia, è anche possibile fare in modo che un provider usi questa API per creare una classe di base.</span><span class="sxs-lookup"><span data-stu-id="90271-157">However, you can also have a provider use this API to create a base class.</span></span> <span data-ttu-id="90271-158">Se, ad esempio, si ritiene che il codice MOF per il provider non verrà installato correttamente, è possibile indicare al provider di creare automaticamente le classi corrette nel repository WMI.</span><span class="sxs-lookup"><span data-stu-id="90271-158">For example, if you believe that the MOF code for your provider will not be installed properly, you can instruct your provider to automatically create the correct classes in the WMI repository.</span></span> <span data-ttu-id="90271-159">Per ulteriori informazioni sui provider, vedere [scrittura di un provider di classi](writing-a-class-provider.md).</span><span class="sxs-lookup"><span data-stu-id="90271-159">For more information about providers, see [Writing a Class Provider](writing-a-class-provider.md).</span></span>

> [!Note]  
> <span data-ttu-id="90271-160">Non è possibile modificare le classi durante l'esecuzione dei provider.</span><span class="sxs-lookup"><span data-stu-id="90271-160">Classes cannot be changed during execution of providers.</span></span> <span data-ttu-id="90271-161">È necessario arrestare l'attività, modificare la classe e quindi riavviare il servizio di gestione Windows.</span><span class="sxs-lookup"><span data-stu-id="90271-161">You must stop the activity, change the class, and then restart the Windows Management service.</span></span> <span data-ttu-id="90271-162">Il rilevamento di una modifica di classe non è attualmente possibile.</span><span class="sxs-lookup"><span data-stu-id="90271-162">Detecting a class change is currently not possible.</span></span>

 

<span data-ttu-id="90271-163">Il codice richiede che il riferimento seguente venga compilato correttamente.</span><span class="sxs-lookup"><span data-stu-id="90271-163">The code requires the following reference to compile correctly.</span></span>


```C++
#include <wbemidl.h>
```



<span data-ttu-id="90271-164">È possibile creare una nuova classe di base a livello di codice usando l' [API com per WMI](com-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="90271-164">You can create a new base class programmatically using the [COM API for WMI](com-api-for-wmi.md).</span></span>

<span data-ttu-id="90271-165">**Per creare una nuova classe base con l'API WMI**</span><span class="sxs-lookup"><span data-stu-id="90271-165">**To create a new base class with the WMI API**</span></span>

1.  <span data-ttu-id="90271-166">Recuperare una definizione per la nuova classe chiamando il metodo [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) con il parametro *strObjectPath* impostato su un valore **null** .</span><span class="sxs-lookup"><span data-stu-id="90271-166">Retrieve a definition for the new class by calling the [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) method with the *strObjectPath* parameter set to a **null** value.</span></span>

    <span data-ttu-id="90271-167">Nell'esempio di codice seguente viene illustrato come recuperare una definizione per una nuova classe.</span><span class="sxs-lookup"><span data-stu-id="90271-167">The following code example shows how to retrieve a definition for a new class.</span></span>

    ```C++
    IWbemServices* pSvc = 0;
    IWbemContext* pCtx = 0;
    IWbemClassObject* pNewClass = 0;
    IWbemCallResult* pResult = 0;
    HRESULT hRes = pSvc->GetObject(0, 0, pCtx, &pNewClass, &pResult);
    ```

    

2.  <span data-ttu-id="90271-168">Definire un nome per la classe impostando la proprietà di sistema della **\_ \_ classe** con una chiamata al metodo [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) .</span><span class="sxs-lookup"><span data-stu-id="90271-168">Establish a name for the class by setting the **\_\_CLASS** system property with a call to the [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) method.</span></span>

    <span data-ttu-id="90271-169">Nell'esempio di codice seguente viene illustrato come assegnare un nome alla classe impostando la proprietà di sistema della **\_ \_ classe** .</span><span class="sxs-lookup"><span data-stu-id="90271-169">The following code example shows how to name the class by setting the **\_\_CLASS** system property.</span></span>

    ```C++
    VARIANT v;
    VariantInit(&v);
    V_VT(&v) = VT_BSTR;

    V_BSTR(&v) = SysAllocString(L"Example");
    BSTR Class = SysAllocString(L"__CLASS");
    pNewClass->Put(Class, 0, &v, 0);
    SysFreeString(Class);
    VariantClear(&v);
    ```

    

3.  <span data-ttu-id="90271-170">Creare la proprietà o le proprietà chiave chiamando [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span><span class="sxs-lookup"><span data-stu-id="90271-170">Create the key property or properties by calling [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span></span>

    <span data-ttu-id="90271-171">Nell'esempio di codice riportato di seguito viene illustrato come creare la proprietà [**index**](swbemrefreshableitem-index.md) , etichettata come proprietà chiave nel passaggio 4.</span><span class="sxs-lookup"><span data-stu-id="90271-171">The following code example describes how to create the [**Index**](swbemrefreshableitem-index.md) property, which is labeled as a key property in Step 4.</span></span>

    ```C++
      BSTR KeyProp = SysAllocString(L"Index");
      pNewClass->Put(KeyProp, 0, NULL, CIM_STRING);
    ```

    

4.  <span data-ttu-id="90271-172">Alleghi il qualificatore standard della [**chiave**](standard-qualifiers.md) alla proprietà chiave chiamando prima il metodo [**IWbemClassObject:: GetPropertyQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getpropertyqualifierset) e quindi il metodo [**IWbemQualifierSet::P UT**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemqualifierset-put) .</span><span class="sxs-lookup"><span data-stu-id="90271-172">Attach the [**Key**](standard-qualifiers.md) standard qualifier to the key property by first calling the [**IWbemClassObject::GetPropertyQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getpropertyqualifierset) method and then the [**IWbemQualifierSet::Put**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemqualifierset-put) method.</span></span>

    <span data-ttu-id="90271-173">Nell'esempio di codice seguente viene illustrato come aggiungere il qualificatore standard della [**chiave**](standard-qualifiers.md) alla proprietà della chiave.</span><span class="sxs-lookup"><span data-stu-id="90271-173">The following code example shows how to attach the [**Key**](standard-qualifiers.md) standard qualifier to the key property.</span></span>

    ```C++
      IWbemQualifierSet *pQual = 0;
      pNewClass->GetPropertyQualifierSet(KeyProp, &pQual);
      SysFreeString(KeyProp);

      V_VT(&v) = VT_BOOL;
      V_BOOL(&v) = VARIANT_TRUE;
      BSTR Key = SysAllocString(L"Key");

      pQual->Put(Key, &v, 0);   // Flavors not required for Key 
      SysFreeString(Key);

      // No longer need the qualifier set for "Index"
      pQual->Release();   
      VariantClear(&v);
    ```

    

5.  <span data-ttu-id="90271-174">Creare altre proprietà della classe con [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span><span class="sxs-lookup"><span data-stu-id="90271-174">Create other properties of the class with [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span></span>

    <span data-ttu-id="90271-175">Nell'esempio di codice seguente viene descritto come creare proprietà aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="90271-175">The following code example describes how to create additional properties.</span></span>

    ```C++
      V_VT(&v) = VT_BSTR;
      V_BSTR(&v) = SysAllocString(L"<default>");
      BSTR OtherProp = SysAllocString(L"OtherInfo");
      pNewClass->Put(OtherProp, 0, &v, CIM_STRING);
      SysFreeString(OtherProp);
      VariantClear(&v);

      OtherProp = SysAllocString(L"IntVal");
      pNewClass->Put(OtherProp, 0, NULL, CIM_SINT32); // NULL is default
      SysFreeString(OtherProp);
    ```

    

6.  <span data-ttu-id="90271-176">Registrare la nuova classe chiamando [**IWbemServices::P utclass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass).</span><span class="sxs-lookup"><span data-stu-id="90271-176">Register the new class by calling [**IWbemServices::PutClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass).</span></span>

    <span data-ttu-id="90271-177">Poiché non è possibile definire chiavi e indici dopo la registrazione di una nuova classe, verificare di aver definito tutte le proprietà prima di chiamare [**PutClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass).</span><span class="sxs-lookup"><span data-stu-id="90271-177">Because you cannot define keys and indices after you register a new class, ensure that you have defined all of your properties before calling [**PutClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass).</span></span>

    <span data-ttu-id="90271-178">Nell'esempio di codice seguente viene illustrato come registrare una nuova classe.</span><span class="sxs-lookup"><span data-stu-id="90271-178">The following code example describes how to register a new class.</span></span>

    ```C++
      hRes = pSvc->PutClass(pNewClass, 0, pCtx, &pResult);
      pNewClass->Release();
    ```

    

<span data-ttu-id="90271-179">Nell'esempio di codice seguente vengono combinati gli esempi di codice illustrati nella procedura precedente e viene illustrato come creare una classe di base utilizzando l'API WMI.</span><span class="sxs-lookup"><span data-stu-id="90271-179">The following code example combines the code examples discussed in the previous procedure and shows how to create a base class using the WMI API.</span></span>


```C++
void CreateClass(IWbemServices *pSvc)
{
  IWbemClassObject *pNewClass = 0;
  IWbemContext *pCtx = 0;
  IWbemCallResult *pResult = 0;

  // Get a class definition. 
  // ============================
  HRESULT hRes = pSvc->GetObject(0, 0, pCtx, &pNewClass, &pResult);
  VARIANT v;
  VariantInit(&v);

  // Create the class name.
  // ============================
  V_VT(&v) = VT_BSTR;
  V_BSTR(&v) = SysAllocString(L"Example");
  BSTR Class = SysAllocString(L"__CLASS");
  pNewClass->Put(Class, 0, &v, 0);
  SysFreeString(Class);
  VariantClear(&v);

  // Create the key property. 
  // ============================
  BSTR KeyProp = SysAllocString(L"Index");
  pNewClass->Put(KeyProp, 0, NULL, CIM_STRING);

  // Attach Key qualifier to mark the "Index" property as the key.
  // ============================
  IWbemQualifierSet *pQual = 0;
  pNewClass->GetPropertyQualifierSet(KeyProp, &pQual);
  SysFreeString(KeyProp);

  V_VT(&v) = VT_BOOL;
  V_BOOL(&v) = VARIANT_TRUE;
  BSTR Key = SysAllocString(L"Key");

  pQual->Put(Key, &v, 0);   // Flavors not required for Key 
  SysFreeString(Key);

  // No longer need the qualifier set for "Index"
  pQual->Release();     
  VariantClear(&v);

  // Create other properties.
  // ============================
  V_VT(&v) = VT_BSTR;
  V_BSTR(&v) = SysAllocString(L"<default>");
  BSTR OtherProp = SysAllocString(L"OtherInfo");
  pNewClass->Put(OtherProp, 0, &v, CIM_STRING);
  SysFreeString(OtherProp);
  VariantClear(&v);

  OtherProp = SysAllocString(L"IntVal");
  pNewClass->Put(OtherProp, 0, NULL, CIM_SINT32); // NULL is default
  SysFreeString(OtherProp);
  
  // Register the class with WMI
  // ============================
  hRes = pSvc->PutClass(pNewClass, 0, pCtx, &pResult);
  pNewClass->Release();
}
```



## <a name="related-topics"></a><span data-ttu-id="90271-180">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="90271-180">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90271-181">Creazione di una classe</span><span class="sxs-lookup"><span data-stu-id="90271-181">Creating a Class</span></span>](creating-a-class.md)
</dt> </dl>

 

 



