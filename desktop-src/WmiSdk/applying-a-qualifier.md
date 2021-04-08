---
description: Analogamente a molte altre tecniche in Managed Object Format (MOF), l'applicazione di un qualificatore al codice è un processo relativamente semplice.
ms.assetid: aaa5c921-bdcd-40e6-ab4b-9441a1957e5b
ms.tgt_platform: multiple
title: Applicazione di un qualificatore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 042a3cdbf7236dc838735ce0cbf18a6315dd02e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760778"
---
# <a name="applying-a-qualifier"></a><span data-ttu-id="721e3-103">Applicazione di un qualificatore</span><span class="sxs-lookup"><span data-stu-id="721e3-103">Applying a Qualifier</span></span>

<span data-ttu-id="721e3-104">Analogamente a molte altre tecniche in Managed Object Format (MOF), l'applicazione di un qualificatore al codice è un processo relativamente semplice.</span><span class="sxs-lookup"><span data-stu-id="721e3-104">Like many other techniques in Managed Object Format (MOF), applying a qualifier to your code is a relatively simple process.</span></span>

<span data-ttu-id="721e3-105">Le convenzioni di denominazione applicate da WMI sono le seguenti:</span><span class="sxs-lookup"><span data-stu-id="721e3-105">The only real challenges are the following restrictions in naming conventions that WMI enforces:</span></span>

-   <span data-ttu-id="721e3-106">Un qualificatore può descrivere una classe, un'istanza, una proprietà, un metodo o un parametro del metodo.</span><span class="sxs-lookup"><span data-stu-id="721e3-106">A qualifier can describe a class, instance, property, method, or method parameter.</span></span>
-   <span data-ttu-id="721e3-107">I nomi dei qualificatori non possono contenere caratteri di sottolineatura iniziali o finali.</span><span class="sxs-lookup"><span data-stu-id="721e3-107">Qualifier names cannot have either leading or trailing underscores.</span></span>
-   <span data-ttu-id="721e3-108">Un nome di qualificatore non può iniziare con una cifra.</span><span class="sxs-lookup"><span data-stu-id="721e3-108">A qualifier name cannot begin with a digit.</span></span>
-   <span data-ttu-id="721e3-109">Un nome qualificatore non può contenere caratteri speciali, ad esempio & \* @!</span><span class="sxs-lookup"><span data-stu-id="721e3-109">A qualifier name cannot contain special characters such as & \* @ !</span></span><span data-ttu-id="721e3-110"> ~ \\ /.</span><span class="sxs-lookup"><span data-stu-id="721e3-110"> ~ \\ /.</span></span>
-   <span data-ttu-id="721e3-111">Tutti i nomi dei qualificatori non fanno distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="721e3-111">All qualifier names are case-insensitive.</span></span>
-   <span data-ttu-id="721e3-112">Non è possibile ridefinire i qualificatori WMI standard o i qualificatori descritti nella specifica DMTF CIM.</span><span class="sxs-lookup"><span data-stu-id="721e3-112">You cannot redefine the standard WMI qualifiers or any qualifiers described in the DMTF CIM specification.</span></span>
-   <span data-ttu-id="721e3-113">I tipi qualificatore non sono dichiarati in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="721e3-113">Qualifier types are not explicitly declared.</span></span>

    <span data-ttu-id="721e3-114">Se non si dichiara un tipo di qualificatore, WMI presuppone che il tipo sia booleano con un valore **true**.</span><span class="sxs-lookup"><span data-stu-id="721e3-114">If you do not declare a qualifier type, WMI assumes the type as Boolean with a value of **TRUE**.</span></span> <span data-ttu-id="721e3-115">In caso contrario, i qualificatori dei tipi WMI sono basati sui valori del qualificatore dichiarati.</span><span class="sxs-lookup"><span data-stu-id="721e3-115">Otherwise, WMI types qualifiers based on the qualifier values you declare.</span></span>

-   <span data-ttu-id="721e3-116">Quando si creano i propri qualificatori, è necessario anteporre al nome del qualificatore il nome dello schema.</span><span class="sxs-lookup"><span data-stu-id="721e3-116">When creating your own qualifiers, you should prefix your schema name to your qualifier name.</span></span>

    <span data-ttu-id="721e3-117">Lo scopo di questa regola è evitare confusione con i nuovi qualificatori.</span><span class="sxs-lookup"><span data-stu-id="721e3-117">The purpose of this rule is to avoid confusion with new qualifiers.</span></span>

-   <span data-ttu-id="721e3-118">È possibile creare matrici omogenee di qualificatori.</span><span class="sxs-lookup"><span data-stu-id="721e3-118">You can create homogeneous arrays of qualifiers.</span></span>

    <span data-ttu-id="721e3-119">Nell'esempio di codice riportato di seguito viene illustrato come specificare matrici di qualificatori con parentesi graffe che racchiudono i valori.</span><span class="sxs-lookup"><span data-stu-id="721e3-119">The following code example shows how qualifier arrays are specified with curly braces that surround the values.</span></span>

    ``` syntax
    [StringArray{"hello", "there"}, SingleElementArray{3}]
    ```

-   <span data-ttu-id="721e3-120">WMI non supporta i tipi di automazione non elencati nel riferimento, ad esempio VT \_ null.</span><span class="sxs-lookup"><span data-stu-id="721e3-120">WMI does not support automation types not listed in the reference, such as VT\_NULL.</span></span> <span data-ttu-id="721e3-121">Per ulteriori informazioni, vedere [tipi di dati MOF](mof-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="721e3-121">For more information, see [MOF Data Types](mof-data-types.md).</span></span>

<span data-ttu-id="721e3-122">La procedura seguente consente di usare C++ per aggiungere un qualificatore a una proprietà.</span><span class="sxs-lookup"><span data-stu-id="721e3-122">The following procedure helps you to use C++ to add a qualifier to a property.</span></span>

<span data-ttu-id="721e3-123">**Per applicare un qualificatore mediante C++**</span><span class="sxs-lookup"><span data-stu-id="721e3-123">**To apply a qualifier using C++**</span></span>

-   <span data-ttu-id="721e3-124">Applicare il qualificatore con una chiamata al metodo [**IWbemQualifierSet::P UT**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemqualifierset-put) .</span><span class="sxs-lookup"><span data-stu-id="721e3-124">Apply the qualifier with a call to the [**IWbemQualifierSet::Put**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemqualifierset-put) method.</span></span>

    <span data-ttu-id="721e3-125">È possibile utilizzare altri metodi di [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) per recuperare o eliminare i qualificatori esistenti.</span><span class="sxs-lookup"><span data-stu-id="721e3-125">You can use other methods of [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) to retrieve or delete existing qualifiers.</span></span>

<span data-ttu-id="721e3-126">La procedura seguente consente di applicare un qualificatore nei file MOF.</span><span class="sxs-lookup"><span data-stu-id="721e3-126">The following procedure helps you to apply a qualifier in MOF files.</span></span>

<span data-ttu-id="721e3-127">**Per descrivere una parola chiave o un identificatore con un qualificatore usando MOF**</span><span class="sxs-lookup"><span data-stu-id="721e3-127">**To describe a keyword or identifier with a qualifier using MOF**</span></span>

-   <span data-ttu-id="721e3-128">Posizionare un qualificatore tra parentesi quadre prima della parola chiave o dell'identificatore descritto dal qualificatore.</span><span class="sxs-lookup"><span data-stu-id="721e3-128">Place a qualifier in brackets before the keyword or identifier described by the qualifier.</span></span>

    <span data-ttu-id="721e3-129">Nell'esempio di codice seguente viene illustrato come vengono utilizzati i qualificatori.</span><span class="sxs-lookup"><span data-stu-id="721e3-129">The following code example shows how qualifiers are used.</span></span>

    ``` syntax
    [qualifiers...]
    class StdDisk
    {
      [qualifiers...]  uint32 dwNumCylinders;
      [qualifiers...]  uint32 dwNumHeads;
      [qualifiers...]  sint32 Method1();
      sint32 Method2([qualifiers...] Parameter1);
    };
    ```

    <span data-ttu-id="721e3-130">Nell'esempio seguente viene descritto il posizionamento appropriato dei qualificatori.</span><span class="sxs-lookup"><span data-stu-id="721e3-130">The following example describes the proper placement of qualifiers.</span></span>

    ``` syntax
    [Abstract]
    class MyClass
    {
        [Amendment, InstanceOf]  uint32 dwNumber;
        sint32 MyMethod ([in] sint32 Param);
    };
    ```

 

 



