---
description: È possibile dichiarare un'istanza di base di una classe nel servizio di gestione Windows utilizzando Managed Object Format (MOF). È inoltre possibile eseguire l'override dei valori predefiniti per un'istanza di. Per ulteriori informazioni, vedere Impostazione di un valore della proprietà dell'istanza.
ms.assetid: 12eda062-9614-455d-ae99-7706c685137b
ms.tgt_platform: multiple
title: Creazione di un'istanza mediante MOF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5078c5fcddaab4e8437a33e8cb3210d515360fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310392"
---
# <a name="creating-an-instance-using-mof"></a><span data-ttu-id="67e37-105">Creazione di un'istanza mediante MOF</span><span class="sxs-lookup"><span data-stu-id="67e37-105">Creating an Instance Using MOF</span></span>

<span data-ttu-id="67e37-106">È possibile dichiarare un'istanza di base di una classe nel servizio di gestione Windows utilizzando Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="67e37-106">You can declare a basic instance of a class in the Windows Management service using Managed Object Format (MOF).</span></span> <span data-ttu-id="67e37-107">È inoltre possibile eseguire l'override dei valori predefiniti per un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="67e37-107">You can also override the default values for an instance.</span></span> <span data-ttu-id="67e37-108">Per ulteriori informazioni, vedere [impostazione di un valore della proprietà dell'istanza](#setting-an-instance-property-value).</span><span class="sxs-lookup"><span data-stu-id="67e37-108">For more information, see [Setting an Instance Property Value](#setting-an-instance-property-value).</span></span>

<span data-ttu-id="67e37-109">Nella procedura riportata di seguito viene descritto come dichiarare un'istanza di base di una classe utilizzando il codice MOF.</span><span class="sxs-lookup"><span data-stu-id="67e37-109">The following procedure describes how to declare a basic instance of a class using MOF code.</span></span>

<span data-ttu-id="67e37-110">**Per dichiarare un'istanza di base di una classe usando il codice MOF**</span><span class="sxs-lookup"><span data-stu-id="67e37-110">**To declare a basic instance of a class using MOF code**</span></span>

1.  <span data-ttu-id="67e37-111">Utilizzare l' **istanza di** parole chiave seguite dal nome della classe, dalle parentesi graffe e da un punto e virgola.</span><span class="sxs-lookup"><span data-stu-id="67e37-111">Use the **Instance of** keywords followed by the class name, curly braces, and a semicolon.</span></span>

    <span data-ttu-id="67e37-112">Nell'esempio di codice riportato di seguito viene illustrato come dichiarare un'istanza di una classe.</span><span class="sxs-lookup"><span data-stu-id="67e37-112">The following code example shows how to declare an instance of a class.</span></span>

    ```mof
    instance of ClassName
    {
    };
    ```

    

2.  <span data-ttu-id="67e37-113">Al termine, inserire il codice MOF nel repository WMI utilizzando il compilatore MOF.</span><span class="sxs-lookup"><span data-stu-id="67e37-113">When finished, insert your MOF code into the WMI repository using the MOF compiler.</span></span>

    <span data-ttu-id="67e37-114">Per ulteriori informazioni, vedere [compilazione di file MOF](compiling-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="67e37-114">For more information, see [Compiling MOF Files](compiling-mof-files.md).</span></span>

<span data-ttu-id="67e37-115">Un'istanza di una classe include tutte le proprietà della classe.</span><span class="sxs-lookup"><span data-stu-id="67e37-115">An instance of a class includes all of the properties of the class.</span></span> <span data-ttu-id="67e37-116">Se la classe è una classe derivata, le istanze includono le proprietà che appartengono a tutte le classi di livello superiore nella gerarchia.</span><span class="sxs-lookup"><span data-stu-id="67e37-116">If the class is a derived class, instances include the properties belonging to all of the classes higher in the hierarchy.</span></span> <span data-ttu-id="67e37-117">Ogni classe da cui viene creata un'istanza ha una o più proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="67e37-117">Each class that an instance is created from has one or more key properties.</span></span> <span data-ttu-id="67e37-118">Non è possibile creare un'istanza con più di 256 di chiavi.</span><span class="sxs-lookup"><span data-stu-id="67e37-118">You cannot create an instance with more than 256 keys.</span></span>

## <a name="setting-an-instance-property-value"></a><span data-ttu-id="67e37-119">Impostazione del valore della proprietà di un'istanza</span><span class="sxs-lookup"><span data-stu-id="67e37-119">Setting an Instance Property Value</span></span>

<span data-ttu-id="67e37-120">Poiché WMI esegue fortemente la tipizzazione delle proprietà, non è possibile modificare i tipi di proprietà.</span><span class="sxs-lookup"><span data-stu-id="67e37-120">Because WMI strongly types properties, you cannot modify property types.</span></span> <span data-ttu-id="67e37-121">È tuttavia possibile impostare i valori delle proprietà nelle istanze di.</span><span class="sxs-lookup"><span data-stu-id="67e37-121">You can, however, set property values in instances.</span></span> <span data-ttu-id="67e37-122">Quando una classe assegna un valore predefinito a una proprietà, WMI assegna il valore predefinito a ogni istanza.</span><span class="sxs-lookup"><span data-stu-id="67e37-122">When a class assigns a default value to a property, WMI assigns the default value to each instance.</span></span> <span data-ttu-id="67e37-123">È possibile eseguire l'override di questo valore nella dichiarazione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="67e37-123">You can override this value in your instance declaration.</span></span>

<span data-ttu-id="67e37-124">Nella procedura riportata di seguito viene descritto come impostare un valore di proprietà o sovrascrivere un valore predefinito utilizzando il codice MOF.</span><span class="sxs-lookup"><span data-stu-id="67e37-124">The following procedure describes how to set a property value or overwrite a default value using MOF code.</span></span>

<span data-ttu-id="67e37-125">**Per impostare un valore di proprietà o sovrascrivere un valore predefinito utilizzando il codice MOF**</span><span class="sxs-lookup"><span data-stu-id="67e37-125">**To set a property value or overwrite a default value using MOF code**</span></span>

1.  <span data-ttu-id="67e37-126">Inserire un'istruzione di assegnazione tra le parentesi graffe della dichiarazione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="67e37-126">Place an assignment statement between the curly braces of the instance declaration.</span></span>

    <span data-ttu-id="67e37-127">Nell'esempio di codice riportato di seguito viene illustrato come impostare un valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="67e37-127">The following code example shows how to set a property value.</span></span>

    ``` syntax
    instance of ClassName
    {
        Prop = "value";
    };
    ```

    <span data-ttu-id="67e37-128">WMI non richiede l'impostazione di alcuna proprietà durante la creazione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="67e37-128">WMI does not require that you set any property during instance creation.</span></span> <span data-ttu-id="67e37-129">L'eccezione è rappresentata da qualsiasi proprietà contrassegnata con il qualificatore della [**chiave**](key-qualifier.md) .</span><span class="sxs-lookup"><span data-stu-id="67e37-129">The exception is any property marked with the [**Key**](key-qualifier.md) qualifier.</span></span> <span data-ttu-id="67e37-130">Poiché WMI utilizza proprietà chiave per identificare in modo univoco le istanze, è necessario impostare tutte le proprietà chiave quando vengono rilevate.</span><span class="sxs-lookup"><span data-stu-id="67e37-130">Because WMI uses key properties to uniquely identify instances, you must set all key properties as you encounter them.</span></span> <span data-ttu-id="67e37-131">Non è invece necessario impostare una proprietà di sistema in una dichiarazione di istanza.</span><span class="sxs-lookup"><span data-stu-id="67e37-131">In contrast, you must not set a system property in an instance declaration.</span></span> <span data-ttu-id="67e37-132">Al contrario, WMI assegna i valori appropriati a una proprietà di sistema, se necessario.</span><span class="sxs-lookup"><span data-stu-id="67e37-132">Instead, WMI assigns the appropriate values to a system property when necessary.</span></span>

2.  <span data-ttu-id="67e37-133">Al termine, inserire il codice MOF nel repository WMI con una chiamata al compilatore MOF.</span><span class="sxs-lookup"><span data-stu-id="67e37-133">When finished, insert your MOF code into the WMI repository with a call to the MOF compiler.</span></span>

    <span data-ttu-id="67e37-134">Per ulteriori informazioni, vedere [compilazione di file MOF](compiling-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="67e37-134">For more information, see [Compiling MOF Files](compiling-mof-files.md).</span></span>

<span data-ttu-id="67e37-135">Negli esempi di codice seguenti viene illustrato il modo in cui un'istanza specifica i dati per le proprietà definite da una classe.</span><span class="sxs-lookup"><span data-stu-id="67e37-135">The following code examples show how an instance specifies data for properties defined by a class.</span></span>

``` syntax
class MyClass 
{
    [key] string   strProp;
    sint32   dwProp1;
    uint32       dwProp2;
};

instance of MyClass 
{
    strProp = "hello";
    dwProp1 = -1;
    dwProp2 = 0xffffffff;
};
```

<span data-ttu-id="67e37-136">Nell'esempio precedente la classe definisce tre proprietà: una stringa di caratteri, un Signed Integer a 32 bit e un Unsigned Integer a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="67e37-136">In the preceding example, the class defines three properties: a character string, a 32-bit signed integer, and a 32-bit unsigned integer.</span></span> <span data-ttu-id="67e37-137">L'istanza fornisce i valori dei dati per ognuna di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="67e37-137">The instance provides data values for each of these properties.</span></span>

 

 



