---
description: Per creare un metodo WMI, definire i parametri di input e output per il metodo.
ms.assetid: 71cbecde-33c4-4bf1-9793-bef6d823dcac
ms.tgt_platform: multiple
title: Creazione di un metodo WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2489a5dd4e97ed6c8d26eeb292c45fa66901cbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233469"
---
# <a name="creating-a-wmi-method"></a><span data-ttu-id="51c60-103">Creazione di un metodo WMI</span><span class="sxs-lookup"><span data-stu-id="51c60-103">Creating a WMI Method</span></span>

<span data-ttu-id="51c60-104">Per creare un metodo WMI, definire i parametri di input e output per il metodo.</span><span class="sxs-lookup"><span data-stu-id="51c60-104">To create a WMI method, define the input and output parameters for the method.</span></span> <span data-ttu-id="51c60-105">I parametri di input e output sono rappresentati da uno speciale [**\_ \_ parametro**](--parameters.md)della classe di sistema WMI.</span><span class="sxs-lookup"><span data-stu-id="51c60-105">The input and output parameters are represented by a special WMI system class [**\_\_PARAMETERS**](--parameters.md).</span></span> <span data-ttu-id="51c60-106">Per ulteriori informazioni, vedere la pagina relativa alla [chiamata a un metodo](calling-a-method.md) e alla [scrittura di un provider di metodi](writing-a-method-provider.md).</span><span class="sxs-lookup"><span data-stu-id="51c60-106">For more information, see [Calling a Method](calling-a-method.md) and [Writing a Method Provider](writing-a-method-provider.md).</span></span>

<span data-ttu-id="51c60-107">Le sezioni seguenti sono illustrate in questo argomento:</span><span class="sxs-lookup"><span data-stu-id="51c60-107">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="51c60-108">Creazione di un metodo di classe WMI in MOF</span><span class="sxs-lookup"><span data-stu-id="51c60-108">Creating a WMI Class Method in MOF</span></span>](#creating-a-wmi-class-method-in-mof)
-   [<span data-ttu-id="51c60-109">Creazione di un metodo di classe WMI in C++</span><span class="sxs-lookup"><span data-stu-id="51c60-109">Creating a WMI Class Method in C++</span></span>](#creating-a-wmi-class-method-in-c)
-   [<span data-ttu-id="51c60-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="51c60-110">Related topics</span></span>](#related-topics)

## <a name="creating-a-wmi-class-method-in-mof"></a><span data-ttu-id="51c60-111">Creazione di un metodo di classe WMI in MOF</span><span class="sxs-lookup"><span data-stu-id="51c60-111">Creating a WMI Class Method in MOF</span></span>

<span data-ttu-id="51c60-112">In WMI i metodi del provider sono in genere azioni distinte correlate all'oggetto rappresentato dalla classe.</span><span class="sxs-lookup"><span data-stu-id="51c60-112">In WMI, provider methods are generally distinct actions related to the object that the class represents.</span></span> <span data-ttu-id="51c60-113">Anziché modificare il valore di una proprietà per eseguire un'azione, è necessario creare un metodo.</span><span class="sxs-lookup"><span data-stu-id="51c60-113">Rather than change the value of a property to execute an action, a method should be created.</span></span> <span data-ttu-id="51c60-114">Ad esempio, è possibile abilitare o disabilitare un Network Information Center (NIC) rappresentato da [**Win32 \_ NetworkAdapter**](/windows/desktop/CIMWin32Prov/win32-networkadapter) usando i metodi [**Enable**](/windows/desktop/CIMWin32Prov/enable-method-in-class-win32-networkadapter) e [**Disable**](/windows/desktop/CIMWin32Prov/disable-method-in-class-win32-networkadapter) .</span><span class="sxs-lookup"><span data-stu-id="51c60-114">For example, you can enable or disable a network information center (NIC) that is represented by [**Win32\_NetworkAdapter**](/windows/desktop/CIMWin32Prov/win32-networkadapter) by using the [**Enable**](/windows/desktop/CIMWin32Prov/enable-method-in-class-win32-networkadapter) and [**Disable**](/windows/desktop/CIMWin32Prov/disable-method-in-class-win32-networkadapter) methods.</span></span> <span data-ttu-id="51c60-115">Anche se queste azioni possono essere rappresentate come proprietà di lettura/scrittura, la progettazione consigliata consiste nel creare un metodo.</span><span class="sxs-lookup"><span data-stu-id="51c60-115">While these actions can be represented as a read/write property, the recommended design is to create a method.</span></span> <span data-ttu-id="51c60-116">In alternativa, se si desidera rendere visibile uno stato o un valore per la classe, l'approccio consigliato consiste nel creare una proprietà di lettura/scrittura anziché un metodo.</span><span class="sxs-lookup"><span data-stu-id="51c60-116">Alternatively, if you want to make a state or value visible for the class, then the recommended approach is to create a read/write property rather than a method.</span></span> <span data-ttu-id="51c60-117">In **Win32 \_ NetworkAdapter** la proprietà **NetEnabled** rende visibile lo stato dell'adapter, ma le modifiche tra gli Stati vengono eseguite dai metodi **Enable** o **Disable** .</span><span class="sxs-lookup"><span data-stu-id="51c60-117">In **Win32\_NetworkAdapter**, the **NetEnabled** property makes the state of the adapter visible but changes between states are executed by the **Enable** or **Disable** methods.</span></span>

<span data-ttu-id="51c60-118">Le dichiarazioni di classe possono includere la dichiarazione di uno o più metodi.</span><span class="sxs-lookup"><span data-stu-id="51c60-118">Class declarations can include the declaration of one or more methods.</span></span> <span data-ttu-id="51c60-119">È possibile scegliere di ereditare i metodi di una classe padre o implementarne uno personalizzato.</span><span class="sxs-lookup"><span data-stu-id="51c60-119">You can either choose to inherit the methods of a parent class, or implement your own.</span></span> <span data-ttu-id="51c60-120">Se si sceglie di implementare metodi personalizzati, è necessario dichiarare il metodo e contrassegnare il metodo con tag di qualificatore specifici.</span><span class="sxs-lookup"><span data-stu-id="51c60-120">If you choose to implement your own methods, you must declare the method and mark the method with specific qualifier tags.</span></span>

<span data-ttu-id="51c60-121">Nella procedura riportata di seguito viene descritto come dichiarare un metodo in una classe che non eredita da una classe base.</span><span class="sxs-lookup"><span data-stu-id="51c60-121">The following procedure describes how to declare a method in a class that does not inherit from a base class.</span></span>

<span data-ttu-id="51c60-122">**Per dichiarare un metodo**</span><span class="sxs-lookup"><span data-stu-id="51c60-122">**To declare a method**</span></span>

1.  <span data-ttu-id="51c60-123">Definire il nome del metodo tra le parentesi graffe di una dichiarazione di classe, seguito da tutti i qualificatori.</span><span class="sxs-lookup"><span data-stu-id="51c60-123">Define the name of your method between the curly braces of a class declaration, followed by any qualifiers.</span></span>

    <span data-ttu-id="51c60-124">Nell'esempio di codice seguente viene illustrata la sintassi di un metodo.</span><span class="sxs-lookup"><span data-stu-id="51c60-124">The following code example describes the syntax for a method.</span></span>

    ``` syntax
    [Dynamic, Provider ("ProviderName")]
    class ClassName
    {
        [Implemented] <ReturnType> <MethodName>
            ([ParameterDirection, IDQualifier] 
            <ParameterType> <ParameterName>);
    };
    ```

2.  <span data-ttu-id="51c60-125">Al termine, inserire il codice di Managed Object Format (MOF) nel repository WMI con una chiamata al compilatore MOF.</span><span class="sxs-lookup"><span data-stu-id="51c60-125">When finished, insert your Managed Object Format (MOF) code into the WMI repository with a call to the MOF compiler.</span></span>

    <span data-ttu-id="51c60-126">Per ulteriori informazioni, vedere [compilazione di file MOF](compiling-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="51c60-126">For more information, see [Compiling MOF Files](compiling-mof-files.md).</span></span>

<span data-ttu-id="51c60-127">Nell'elenco seguente vengono definiti gli elementi della dichiarazione di metodo.</span><span class="sxs-lookup"><span data-stu-id="51c60-127">The following list defines the elements of the method declaration.</span></span>

<dl> <dt>

<span data-ttu-id="51c60-128"><span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>[**Provider**](/windows/desktop/api/Provider/nl-provider-provider)</span><span class="sxs-lookup"><span data-stu-id="51c60-128"><span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>[**Provider**](/windows/desktop/api/Provider/nl-provider-provider)</span></span>
</dt> <dd>

<span data-ttu-id="51c60-129">Collega un provider specifico alla descrizione della classe.</span><span class="sxs-lookup"><span data-stu-id="51c60-129">Links a specific provider to your class description.</span></span> <span data-ttu-id="51c60-130">Il valore del qualificatore del [**provider**](/windows/desktop/api/Provider/nl-provider-provider) è il nome del provider, che indica a WMI dove risiede il codice che supporta il metodo.</span><span class="sxs-lookup"><span data-stu-id="51c60-130">The value of the [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifier is the name of the provider, which tells WMI where the code that supports your method resides.</span></span> <span data-ttu-id="51c60-131">Un provider deve inoltre contrassegnare con il qualificatore **dinamico** qualsiasi classe che dispone di istanze dinamiche.</span><span class="sxs-lookup"><span data-stu-id="51c60-131">A provider should also mark with the **Dynamic** qualifier any class that has dynamic instances.</span></span> <span data-ttu-id="51c60-132">Al contrario, non usare il qualificatore **dinamico** per contrassegnare una classe che contiene un'istanza statica con i metodi **implementati** .</span><span class="sxs-lookup"><span data-stu-id="51c60-132">In contrast, do not use the **Dynamic** qualifier to mark a class that contains a static instance with **Implemented** methods.</span></span>

</dd> <dt>

<span data-ttu-id="51c60-133"><span id="Implemented"></span><span id="implemented"></span><span id="IMPLEMENTED"></span>**Implementato**</span><span class="sxs-lookup"><span data-stu-id="51c60-133"><span id="Implemented"></span><span id="implemented"></span><span id="IMPLEMENTED"></span>**Implemented**</span></span>
</dt> <dd>

<span data-ttu-id="51c60-134">Dichiara che viene implementato un metodo, anziché ereditare l'implementazione del metodo dalla classe padre.</span><span class="sxs-lookup"><span data-stu-id="51c60-134">Declares that you will implement a method, rather than inherit the method implementation from the parent class.</span></span> <span data-ttu-id="51c60-135">Per impostazione predefinita, WMI propaga l'implementazione della classe padre a una classe derivata a meno che la classe derivata non fornisca un'implementazione.</span><span class="sxs-lookup"><span data-stu-id="51c60-135">By default, WMI propagates the implementation of the parent class to a derived class unless the derived class provides an implementation.</span></span> <span data-ttu-id="51c60-136">L'omissione del qualificatore **implementato** indica che il metodo non dispone di alcuna implementazione in tale classe.</span><span class="sxs-lookup"><span data-stu-id="51c60-136">Omitting the **Implemented** qualifier indicates that the method has no implementation in that class.</span></span> <span data-ttu-id="51c60-137">Se si dichiara di nuovo un metodo senza il qualificatore **implementato** , WMI presuppone comunque che non si implementi il metodo e richiama l'implementazione del metodo della classe padre quando viene chiamato.</span><span class="sxs-lookup"><span data-stu-id="51c60-137">If you redeclare a method without the **Implemented** qualifier, WMI still assumes that you are not going to implement that method, and invokes the parent class method implementation when called.</span></span> <span data-ttu-id="51c60-138">Di conseguenza, la ridichiarazione di un metodo in una classe derivata senza l'associazione del qualificatore **implementato** risulta utile solo quando si aggiunge o rimuove un qualificatore a o dal metodo.</span><span class="sxs-lookup"><span data-stu-id="51c60-138">As such, redeclaring a method in a derived class without attaching the **Implemented** qualifier is useful only when you add or remove a qualifier to or from the method.</span></span>

</dd> <dt>

<span data-ttu-id="51c60-139"><span id="ReturnType"></span><span id="returntype"></span><span id="RETURNTYPE"></span>ReturnType</span><span class="sxs-lookup"><span data-stu-id="51c60-139"><span id="ReturnType"></span><span id="returntype"></span><span id="RETURNTYPE"></span>ReturnType</span></span>
</dt> <dd>

<span data-ttu-id="51c60-140">Descrive il valore restituito dal metodo.</span><span class="sxs-lookup"><span data-stu-id="51c60-140">Describes what value the method returns.</span></span> <span data-ttu-id="51c60-141">Il valore restituito per un metodo deve essere un oggetto booleano, numerico, **char**, **String**, [DateTime](datetime.md)o schema.</span><span class="sxs-lookup"><span data-stu-id="51c60-141">The return value for a method must be a Boolean, numeric, **CHAR**, **STRING**, [DATETIME](datetime.md), or schema object.</span></span> <span data-ttu-id="51c60-142">È anche possibile dichiarare il tipo restituito come [void](void.md), a indicare che il metodo non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="51c60-142">You can also declare the return type as [VOID](void.md), indicating that the method returns nothing.</span></span> <span data-ttu-id="51c60-143">Tuttavia, non è possibile dichiarare una matrice come tipo di valore restituito.</span><span class="sxs-lookup"><span data-stu-id="51c60-143">However, you cannot declare an array as a return value type.</span></span>

</dd> <dt>

<span data-ttu-id="51c60-144"><span id="MethodName"></span><span id="methodname"></span><span id="METHODNAME"></span>MethodName</span><span class="sxs-lookup"><span data-stu-id="51c60-144"><span id="MethodName"></span><span id="methodname"></span><span id="METHODNAME"></span>MethodName</span></span>
</dt> <dd>

<span data-ttu-id="51c60-145">Definisce il nome del metodo.</span><span class="sxs-lookup"><span data-stu-id="51c60-145">Defines the name of the method.</span></span> <span data-ttu-id="51c60-146">Ogni metodo deve avere un nome univoco.</span><span class="sxs-lookup"><span data-stu-id="51c60-146">Every method must have a unique name.</span></span> <span data-ttu-id="51c60-147">WMI non consente l'esistenza di due metodi con lo stesso nome e firme diverse in una classe o in una gerarchia di classi.</span><span class="sxs-lookup"><span data-stu-id="51c60-147">WMI does not allow two methods with the same name and different signatures to exist in one class or within a class hierarchy.</span></span> <span data-ttu-id="51c60-148">Di conseguenza, non è possibile eseguire l'overload di un metodo.</span><span class="sxs-lookup"><span data-stu-id="51c60-148">As such, you also cannot overload a method.</span></span>

</dd> <dt>

<span data-ttu-id="51c60-149"><span id="ParameterDirection"></span><span id="parameterdirection"></span><span id="PARAMETERDIRECTION"></span>ParameterDirection</span><span class="sxs-lookup"><span data-stu-id="51c60-149"><span id="ParameterDirection"></span><span id="parameterdirection"></span><span id="PARAMETERDIRECTION"></span>ParameterDirection</span></span>
</dt> <dd>

<span data-ttu-id="51c60-150">Contiene qualificatori che descrivono se un parametro è un parametro di input, un parametro di output o entrambi.</span><span class="sxs-lookup"><span data-stu-id="51c60-150">Contains qualifiers that describe if a parameter is an input parameter, output parameter, or both.</span></span> <span data-ttu-id="51c60-151">Non usare lo stesso nome di parametro più di una volta come parametro di input o più di una volta come parametro di output.</span><span class="sxs-lookup"><span data-stu-id="51c60-151">Do not use the same parameter name more than one time as an input parameter or more than one time as an output parameter.</span></span> <span data-ttu-id="51c60-152">Se viene visualizzato lo stesso nome di parametro con i qualificatori [**in**](standard-qualifiers.md) e **out** , la funzionalità è concettualmente analoga all'uso di qualificatori **in**, **out** per un singolo parametro.</span><span class="sxs-lookup"><span data-stu-id="51c60-152">If the same parameter name appears with both the [**In**](standard-qualifiers.md) and an **Out** qualifiers, the functionality is conceptually the same as using the **In**, **Out** qualifiers on a single parameter.</span></span> <span data-ttu-id="51c60-153">Tuttavia, quando si usano dichiarazioni separate, i parametri di input e di output devono essere esattamente gli stessi in tutti gli altri aspetti, inclusi il numero e il tipo di qualificatori [**ID**](standard-wmi-qualifiers.md) , e il qualificatore deve essere lo stesso e dichiarato in modo esplicito per entrambi.</span><span class="sxs-lookup"><span data-stu-id="51c60-153">However, when using separate declarations, the input and output parameters must be exactly the same in all other respects, including the number and type of [**ID**](standard-wmi-qualifiers.md) qualifiers, and the qualifier must be the same and explicitly declared for both.</span></span> <span data-ttu-id="51c60-154">Si consiglia vivamente di utilizzare i qualificatori **in**, **out** all'interno di una singola dichiarazione di parametro.</span><span class="sxs-lookup"><span data-stu-id="51c60-154">It is strongly recommended to use the **In**, **Out** qualifiers within a single parameter declaration.</span></span>

</dd> <dt>

<span data-ttu-id="51c60-155"><span id="IDQualifier"></span><span id="idqualifier"></span><span id="IDQUALIFIER"></span>**IDQualifier**</span><span class="sxs-lookup"><span data-stu-id="51c60-155"><span id="IDQualifier"></span><span id="idqualifier"></span><span id="IDQUALIFIER"></span>**IDQualifier**</span></span>
</dt> <dd>

<span data-ttu-id="51c60-156">Contiene il qualificatore [**ID**](standard-wmi-qualifiers.md) che identifica in modo univoco la posizione di ogni parametro all'interno della sequenza di parametri nel metodo.</span><span class="sxs-lookup"><span data-stu-id="51c60-156">Contains the [**ID**](standard-wmi-qualifiers.md) qualifier that uniquely identifies the position of each parameter within the sequence of parameters in the method.</span></span> <span data-ttu-id="51c60-157">Per impostazione predefinita, il compilatore MOF contrassegna automaticamente i parametri con un qualificatore **ID** .</span><span class="sxs-lookup"><span data-stu-id="51c60-157">By default, the MOF compiler automatically marks parameters with an **ID** qualifier.</span></span> <span data-ttu-id="51c60-158">Il compilatore contrassegna il primo parametro con un valore pari a 0 (zero), il secondo parametro un valore 1 (uno) e così via.</span><span class="sxs-lookup"><span data-stu-id="51c60-158">The compiler marks the first parameter with a value of 0 (zero), the second parameter a value of 1 (one), and so on.</span></span> <span data-ttu-id="51c60-159">Se necessario, è possibile dichiarare in modo esplicito la sequenza di ID nel codice MOF.</span><span class="sxs-lookup"><span data-stu-id="51c60-159">If necessary, you can explicitly state the ID sequence in your MOF code.</span></span>

</dd> <dt>

<span data-ttu-id="51c60-160"><span id="ParameterType"></span><span id="parametertype"></span><span id="PARAMETERTYPE"></span>ParameterType</span><span class="sxs-lookup"><span data-stu-id="51c60-160"><span id="ParameterType"></span><span id="parametertype"></span><span id="PARAMETERTYPE"></span>ParameterType</span></span>
</dt> <dd>

<span data-ttu-id="51c60-161">Descrive il tipo di dati che il metodo può accettare.</span><span class="sxs-lookup"><span data-stu-id="51c60-161">Describes what data type the method can accept.</span></span> <span data-ttu-id="51c60-162">È possibile definire un tipo di parametro come qualsiasi valore di dati MOF, tra cui una matrice, un oggetto dello schema o un riferimento.</span><span class="sxs-lookup"><span data-stu-id="51c60-162">You can define a parameter type as any MOF data value, including an array, schema object, or reference.</span></span> <span data-ttu-id="51c60-163">Quando si usa una matrice come parametro, usare la matrice come Unbound o con dimensioni esplicite.</span><span class="sxs-lookup"><span data-stu-id="51c60-163">When using an array as a parameter, use the array as unbound or with an explicit size.</span></span>

</dd> <dt>

<span data-ttu-id="51c60-164"><span id="ParameterName"></span><span id="parametername"></span><span id="PARAMETERNAME"></span>ParameterName</span><span class="sxs-lookup"><span data-stu-id="51c60-164"><span id="ParameterName"></span><span id="parametername"></span><span id="PARAMETERNAME"></span>ParameterName</span></span>
</dt> <dd>

<span data-ttu-id="51c60-165">Contiene il nome del parametro.</span><span class="sxs-lookup"><span data-stu-id="51c60-165">Contains the name of the parameter.</span></span> <span data-ttu-id="51c60-166">A questo punto è anche possibile scegliere di definire il valore predefinito del parametro.</span><span class="sxs-lookup"><span data-stu-id="51c60-166">You can also choose to define the default value of the parameter at this point.</span></span> <span data-ttu-id="51c60-167">I parametri privi di valori iniziali rimangono non assegnati.</span><span class="sxs-lookup"><span data-stu-id="51c60-167">Parameters lacking initial values remain unassigned.</span></span>

</dd> </dl>

<span data-ttu-id="51c60-168">Nell'esempio di codice seguente vengono descritti i qualificatori e l'elenco dei parametri.</span><span class="sxs-lookup"><span data-stu-id="51c60-168">The following code example describes parameter listing and qualifiers.</span></span>

``` syntax
[Dynamic, Provider ("ProviderX")]
class MyClass
{
    [Implemented] 
    sint32 MyMethod1 ([in, id(0)] sint32 InParam);
    [Implemented] 
    void MyMethod2 ([in, id(0)] sint32 InParam, 
       [out, id(1)] sint32 OutParam);
    [Implemented] 
    sint32 MyMethod3 ([in, out, id(0)] sint32 InOutParam);
};
```

<span data-ttu-id="51c60-169">Nell'esempio di codice riportato di seguito viene illustrato come utilizzare una matrice in un parametro MOF.</span><span class="sxs-lookup"><span data-stu-id="51c60-169">The following code example describes how to use an array in a MOF parameter.</span></span>

``` syntax
[Dynamic, Provider ("ProviderX")]
class MyClass
{
    [Implemented] 
    sint32 MyMethod1 ([in, id(0)] Win32_LogicalDisk DiskParam[]);
    [Implemented] 
    sint32 MyMethod2 ([in, id(0)] Win32_LogicalDisk DiskParam[32]);
};
```

<span data-ttu-id="51c60-170">Nell'esempio di codice riportato di seguito viene descritto l'utilizzo di un oggetto dello schema come parametro e valore restituito.</span><span class="sxs-lookup"><span data-stu-id="51c60-170">The following code example describes using a schema object as both a parameter and return value.</span></span>

``` syntax
[Dynamic, Provider ("ProviderX")]
class MyClass
{
    [Implemented] sint32 MyMethod1 ([in, id(0)] Win32_LogicalDisk 
        DiskParam);
    [Implemented] 
    Win32_LogicalDisk MyMethod2 ([in, id(0)] string DiskVolLabel);
};
```

<span data-ttu-id="51c60-171">Nell'esempio di codice seguente viene descritto come includere due riferimenti: uno a un'istanza della classe [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) e l'altro a un'istanza di un tipo di oggetto sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="51c60-171">The following code example describes how to include two references: one to an instance of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class and the other to an instance of an unknown object type.</span></span>

``` syntax
[Dynamic, Provider("ProviderX")]
class MyClass
{
    [Implemented] 
    sint32 MyMethod1 ([in, id(0)] Win32_LogicalDisk ref DiskRef);
    [Implemented] 
    sint32 MyMethod2 ([in, id(0)] object ref AnyObject);
};
```

## <a name="creating-a-wmi-class-method-in-c"></a><span data-ttu-id="51c60-172">Creazione di un metodo di classe WMI in C++</span><span class="sxs-lookup"><span data-stu-id="51c60-172">Creating a WMI Class Method in C++</span></span>

<span data-ttu-id="51c60-173">Nella procedura seguente viene descritto come creare un metodo di classe WMI a livello di programmazione.</span><span class="sxs-lookup"><span data-stu-id="51c60-173">The following procedure describes how to create a WMI class method programmatically.</span></span>

<span data-ttu-id="51c60-174">**Per creare un metodo di classe WMI a livello di codice**</span><span class="sxs-lookup"><span data-stu-id="51c60-174">**To create a WMI class method programmatically**</span></span>

1.  <span data-ttu-id="51c60-175">Creare la classe a cui apparterrà il metodo.</span><span class="sxs-lookup"><span data-stu-id="51c60-175">Create the class to which the method will belong.</span></span>

    <span data-ttu-id="51c60-176">Prima di creare il metodo, è necessario innanzitutto disporre di una classe in cui inserire il metodo.</span><span class="sxs-lookup"><span data-stu-id="51c60-176">You must first have a class to place the method in before you create the method.</span></span>

2.  <span data-ttu-id="51c60-177">Recuperare due classi figlio della classe di sistema [**\_ \_ Parameters**](--parameters.md) usando [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) o [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="51c60-177">Retrieve two child classes of the [**\_\_PARAMETERS**](--parameters.md) system class using either [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) or [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>

    <span data-ttu-id="51c60-178">Usare la prima classe figlio per descrivere i parametri in e la seconda per descrivere i parametri out.</span><span class="sxs-lookup"><span data-stu-id="51c60-178">Use the first child class to describe the in-parameters, and the second to describe the out-parameters.</span></span> <span data-ttu-id="51c60-179">Se necessario, è possibile eseguire un singolo recupero seguito da una chiamata al metodo [**IWbemClassObject:: Clone**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-clone) .</span><span class="sxs-lookup"><span data-stu-id="51c60-179">If necessary, you can perform a single retrieval followed by a call to the [**IWbemClassObject::Clone**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-clone) method.</span></span>

3.  <span data-ttu-id="51c60-180">Scrivere i parametri in nella prima classe e i parametri out per la seconda classe, usando una o più chiamate a [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span><span class="sxs-lookup"><span data-stu-id="51c60-180">Write the in-parameters to the first class, and the out-parameters to the second class, using one or more calls to [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span></span>

    <span data-ttu-id="51c60-181">Quando si descrivono i parametri per un metodo, osservare le regole e le restrizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="51c60-181">When describing parameters to a method, observe the following rules and restrictions:</span></span>

    -   <span data-ttu-id="51c60-182">Trattare i \[ parametri in, out \] come voci separate, uno nell'oggetto che contiene i parametri in e uno nell'oggetto che contiene i parametri out.</span><span class="sxs-lookup"><span data-stu-id="51c60-182">Treat the \[in, out\] parameters as separate entries, one in the object that contains the in-parameters and one in the object that contains the out-parameters.</span></span>
    -   <span data-ttu-id="51c60-183">Ad eccezione di, i qualificatori \[ \] rimanenti devono essere esattamente gli stessi.</span><span class="sxs-lookup"><span data-stu-id="51c60-183">Other than the \[in, out\] qualifiers, the remaining qualifiers must be exactly the same.</span></span>
    -   <span data-ttu-id="51c60-184">Specificare i qualificatori [**ID**](standard-wmi-qualifiers.md) , a partire da 0 (zero), uno per ogni parametro.</span><span class="sxs-lookup"><span data-stu-id="51c60-184">Specify the [**ID**](standard-wmi-qualifiers.md) qualifiers, starting at 0 (zero), one for each parameter.</span></span>

        <span data-ttu-id="51c60-185">L'ordine dei parametri di input o output viene stabilito dal valore del qualificatore [**ID**](standard-wmi-qualifiers.md) per ogni parametro.</span><span class="sxs-lookup"><span data-stu-id="51c60-185">The order of the input or output parameters is established by the value of the [**ID**](standard-wmi-qualifiers.md) qualifier on each parameter.</span></span> <span data-ttu-id="51c60-186">Tutti gli argomenti di input devono precedere qualsiasi argomento di output.</span><span class="sxs-lookup"><span data-stu-id="51c60-186">All input arguments must precede any output arguments.</span></span> <span data-ttu-id="51c60-187">La modifica dell'ordine dei parametri di input e output del metodo durante l'aggiornamento di un provider di metodi esistente può causare errori nelle applicazioni che chiamano il metodo.</span><span class="sxs-lookup"><span data-stu-id="51c60-187">Changing the order of method input and output parameters when updating an existing method provider can cause applications that call the method to fail.</span></span> <span data-ttu-id="51c60-188">Aggiungere nuovi parametri di input alla fine dei parametri esistenti anziché inserirli nella sequenza già stabilita.</span><span class="sxs-lookup"><span data-stu-id="51c60-188">Add new input parameters at the end of the existing parameters rather than inserting them in the sequence that is already established.</span></span>

        <span data-ttu-id="51c60-189">Assicurarsi di non lasciare vuoti nella sequenza di qualificatore [**ID**](standard-wmi-qualifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="51c60-189">Make sure to leave no gaps in the [**ID**](standard-wmi-qualifiers.md) qualifier sequence.</span></span>

    -   <span data-ttu-id="51c60-190">Inserire il valore restituito nella classe out-parameters come proprietà denominata **returnValue**.</span><span class="sxs-lookup"><span data-stu-id="51c60-190">Place the return value in the out-parameters class as a property named **ReturnValue**.</span></span>

        <span data-ttu-id="51c60-191">Identifica la proprietà come valore restituito del metodo.</span><span class="sxs-lookup"><span data-stu-id="51c60-191">This identifies the property as the return value of the method.</span></span> <span data-ttu-id="51c60-192">Il tipo CIM di questa proprietà è il tipo restituito del metodo.</span><span class="sxs-lookup"><span data-stu-id="51c60-192">The CIM type of this property is the return type of the method.</span></span> <span data-ttu-id="51c60-193">Se il metodo ha un tipo restituito void, non deve essere presente alcuna proprietà **returnValue** .</span><span class="sxs-lookup"><span data-stu-id="51c60-193">If the method has a return type of void, then do not have a **ReturnValue** property at all.</span></span> <span data-ttu-id="51c60-194">Inoltre, la proprietà **returnValue** non può avere un qualificatore [**ID**](standard-wmi-qualifiers.md) come gli argomenti del metodo.</span><span class="sxs-lookup"><span data-stu-id="51c60-194">Also, the **ReturnValue** property cannot have an [**ID**](standard-wmi-qualifiers.md) qualifier like the arguments of the method.</span></span> <span data-ttu-id="51c60-195">L'assegnazione di un qualificatore **ID** alla proprietà **returnValue** genera un errore WMI.</span><span class="sxs-lookup"><span data-stu-id="51c60-195">Assigning an **ID** qualifier to the **ReturnValue** property produces a WMI error.</span></span>

    -   <span data-ttu-id="51c60-196">Esprimere tutti i valori di parametro predefiniti per la proprietà nella classe.</span><span class="sxs-lookup"><span data-stu-id="51c60-196">Express any default parameter values for the property in the class.</span></span>

4.  <span data-ttu-id="51c60-197">Inserire entrambi gli oggetti [**\_ \_ Parameters**](--parameters.md) nella classe padre con una chiamata a [**IWbemClassObject::P utmethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).</span><span class="sxs-lookup"><span data-stu-id="51c60-197">Place both [**\_\_PARAMETERS**](--parameters.md) objects into the parent class with a call to [**IWbemClassObject::PutMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).</span></span>

    <span data-ttu-id="51c60-198">Una singola chiamata a [**PutMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod) può inserire entrambi gli oggetti [**\_ \_ Parameters**](--parameters.md) nella classe.</span><span class="sxs-lookup"><span data-stu-id="51c60-198">A single call to [**PutMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod) can place both [**\_\_PARAMETERS**](--parameters.md) objects into the class.</span></span>

## <a name="related-topics"></a><span data-ttu-id="51c60-199">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="51c60-199">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="51c60-200">Creazione di una classe</span><span class="sxs-lookup"><span data-stu-id="51c60-200">Creating a Class</span></span>](creating-a-class.md)
</dt> </dl>

 

 
