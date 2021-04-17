---
title: Accesso agli attributi con ADSI
description: I metodi IADs. Get e IADs. GetEx vengono usati per recuperare i valori degli attributi denominati.
ms.assetid: 8aa139e1-6b20-4745-92f1-d2f352071f33
ms.tgt_platform: multiple
keywords:
- Attributi, accesso con ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4ee6990483b45e335bb6b830cef85e482f30e00
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300425"
---
# <a name="accessing-attributes-with-adsi"></a><span data-ttu-id="fd994-104">Accesso agli attributi con ADSI</span><span class="sxs-lookup"><span data-stu-id="fd994-104">Accessing Attributes with ADSI</span></span>

<span data-ttu-id="fd994-105">I metodi [**IADs. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) e [**IADs. GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) vengono usati per recuperare i valori degli attributi denominati.</span><span class="sxs-lookup"><span data-stu-id="fd994-105">The [**IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) and [**IADs.GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) methods are used to retrieve named attribute values.</span></span> <span data-ttu-id="fd994-106">Entrambi i metodi restituiscono un valore [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) .</span><span class="sxs-lookup"><span data-stu-id="fd994-106">Both methods return a [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) value.</span></span> <span data-ttu-id="fd994-107">Questi metodi sono disponibili solo per le directory che supportano uno schema.</span><span class="sxs-lookup"><span data-stu-id="fd994-107">These methods are available only for directories that support a schema.</span></span> <span data-ttu-id="fd994-108">Quando si accede a oggetti in una directory senza uno schema, è necessario utilizzare le interfacce [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry) e [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) per modificare i valori degli attributi.</span><span class="sxs-lookup"><span data-stu-id="fd994-108">When accessing objects in a directory without a schema, the [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry) and [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) interfaces must be used to manipulate attribute values.</span></span>

<span data-ttu-id="fd994-109">I metodi [**IADs. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) e [**IADs. GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) restituiscono una [**variante**](/windows/win32/api/oaidl/ns-oaidl-variant) che può, o meno, essere una matrice **Variant** a seconda del numero di valori restituiti dal server.</span><span class="sxs-lookup"><span data-stu-id="fd994-109">The [**IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) and [**IADs.GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) methods return a [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) which may, or may not, be a **VARIANT** array depending on the number of values returned by the server.</span></span> <span data-ttu-id="fd994-110">Se, ad esempio, dal server viene restituito un solo valore, indipendentemente dal fatto che si tratti di un attributo singolo o multivalore, il metodo restituisce una singola **variante**.</span><span class="sxs-lookup"><span data-stu-id="fd994-110">For example, if only one value is returned from the server, regardless of whether it is a single or multi-valued attribute, the method returns a single **VARIANT**.</span></span> <span data-ttu-id="fd994-111">Viceversa, se vengono restituiti più valori, viene restituita una matrice **Variant** .</span><span class="sxs-lookup"><span data-stu-id="fd994-111">Conversely, if multiple values are returned, a **VARIANT** array is returned.</span></span> <span data-ttu-id="fd994-112">Se viene restituita una matrice **Variant** , il membro **VT** della struttura **Variant** contiene i flag **VT \_ Variant/vbVariant** e **VT \_ Array/VBArray** .</span><span class="sxs-lookup"><span data-stu-id="fd994-112">If a **VARIANT** array is returned, the **vt** member of the **VARIANT** structure contains the **VT\_VARIANT/vbVariant** and **VT\_ARRAY/vbArray** flags.</span></span>

<span data-ttu-id="fd994-113">I metodi [**IADs. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) e [**IADs. GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) possono anche restituire un oggetto com usando l'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="fd994-113">The [**IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) and [**IADs.GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) methods can also return a COM object using the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="fd994-114">In questo caso, il membro **VT** della struttura [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) contiene il flag **di \_ invio/vbObject del VT** .</span><span class="sxs-lookup"><span data-stu-id="fd994-114">In this case, the **vt** member of the [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) structure contains the **VT\_DISPATCH/vbObject** flag.</span></span> <span data-ttu-id="fd994-115">Per accedere all'oggetto COM, chiamare il metodo [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sull'interfaccia **IDispatch** per ottenere l'interfaccia desiderata.</span><span class="sxs-lookup"><span data-stu-id="fd994-115">To access the COM object, call the [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method on the **IDispatch** interface to obtain the desired interface.</span></span>

<span data-ttu-id="fd994-116">Un altro tipo di dati restituito dai metodi [**IADs. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) e [**IADs. GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) è dati binari.</span><span class="sxs-lookup"><span data-stu-id="fd994-116">Another data type returned by the [**IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) and [**IADs.GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) methods is binary data.</span></span> <span data-ttu-id="fd994-117">In questo caso, i dati vengono forniti come matrice contigua di byte e il membro **VT** della struttura [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) conterrà i flag **VT \_ Ui1/vbByte** e **VT \_ Array/VBArray** .</span><span class="sxs-lookup"><span data-stu-id="fd994-117">In this case, the data is supplied as a contiguous array of bytes and the **vt** member of the [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) structure will contain the **VT\_UI1/vbByte** and **VT\_ARRAY/vbArray** flags.</span></span>

> [!Note]  
> <span data-ttu-id="fd994-118">Microsoft Visual Basic, Scripting Edition supporta solo [](/windows/win32/api/oaidl/ns-oaidl-variant) matrici Variant **e Variant.**</span><span class="sxs-lookup"><span data-stu-id="fd994-118">Microsoft Visual Basic, Scripting Edition only supports [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) and **VARIANT** arrays.</span></span> <span data-ttu-id="fd994-119">Per questo motivo, non è possibile usare VBScript per leggere i valori delle proprietà binarie.</span><span class="sxs-lookup"><span data-stu-id="fd994-119">Because of this, VBScript cannot be used to read binary property values.</span></span>

 

<span data-ttu-id="fd994-120">Molte interfacce ADSI definiscono proprietà specifiche dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="fd994-120">Many ADSI interfaces define interface-specific properties.</span></span> <span data-ttu-id="fd994-121">Ad esempio, l'interfaccia [**IADsComputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer) definisce la proprietà [**location**](iadscomputer-property-methods.md) .</span><span class="sxs-lookup"><span data-stu-id="fd994-121">For example, the [**IADsComputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer) interface defines the [**Location**](iadscomputer-property-methods.md) property.</span></span> <span data-ttu-id="fd994-122">Queste proprietà definite dall'interfaccia possono contenere dati identici a uno degli attributi denominati, ma le proprietà sono specifiche per il tipo di oggetto a cui fa riferimento l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="fd994-122">These interface-defined properties may contain data that is identical to one of the named attributes, but the properties are specific to the type of object the interface refers to.</span></span> <span data-ttu-id="fd994-123">Nei linguaggi che supportano l'automazione, è possibile accedere a queste proprietà definite dall'interfaccia usando la notazione del punto, come illustrato nell'esempio di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="fd994-123">In languages that support automation, these interface-defined properties can be accessed using the dot notation as shown in the following code example.</span></span>

## <a name="examples"></a><span data-ttu-id="fd994-124">Esempio</span><span class="sxs-lookup"><span data-stu-id="fd994-124">Examples</span></span>

<span data-ttu-id="fd994-125">Nell'esempio di codice seguente viene illustrato come accedere alla proprietà ADsPath nell'interfaccia IADs.</span><span class="sxs-lookup"><span data-stu-id="fd994-125">The following code example shows how to access the ADsPath property on the IADs interface.</span></span>


```VB
Dim oUser as IADs
Dim Path as String
 
' Bind to a specific user object.
set oUser = GetObject(
            "LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
 
' Get property.
Path = MyUser.ADsPath
```



<span data-ttu-id="fd994-126">Nei linguaggi non di automazione, è necessario utilizzare i metodi di accesso alle proprietà per accedere alle proprietà definite dall'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="fd994-126">In non-automation languages, the property access methods must be used to access the interface-defined properties.</span></span> <span data-ttu-id="fd994-127">Ad esempio, il metodo [**IADsComputer:: Get \_ location**](iadscomputer-property-methods.md) viene usato per recuperare la proprietà **IADSComputer. location** .</span><span class="sxs-lookup"><span data-stu-id="fd994-127">For example, the [**IADsComputer::get\_Location**](iadscomputer-property-methods.md) method is used to retrieve the **IADsComputer.Location** property.</span></span>

<span data-ttu-id="fd994-128">Nell'esempio di codice C++ riportato di seguito viene illustrato come utilizzare il metodo di accesso alle proprietà in C++ per recuperare il ADsPath di un utente.</span><span class="sxs-lookup"><span data-stu-id="fd994-128">The following C++ code example demonstrates how to use the property access method in C++ to retrieve the ADsPath of a user.</span></span>


```C++
HRESULT hr;
IADs *pUser; 
 
// Bind to user object.
hr = ADsGetObject(
     L"LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com", 
     IID_IADs, 
     (void**)&pUser);
if(SUCCEEDED(hr)) 
{
    BSTR bstrName;

    // Get property.
    hr = pUser->get_Name(&bstrName);
    if(SUCCEEDED(hr)) 
    {
        wprintf(bstrName);
 
        SysFreeString(bstrName);
    }

    pUser->Release();
}
```



<span data-ttu-id="fd994-129">Per ulteriori informazioni sull'accesso agli attributi con ADSI, vedere:</span><span class="sxs-lookup"><span data-stu-id="fd994-129">For more information about accessing attributes with ADSI, see:</span></span>

-   [<span data-ttu-id="fd994-130">Metodo Get</span><span class="sxs-lookup"><span data-stu-id="fd994-130">The Get Method</span></span>](the-get-method.md)
-   [<span data-ttu-id="fd994-131">Metodo GetEx</span><span class="sxs-lookup"><span data-stu-id="fd994-131">The GetEx Method</span></span>](the-getex-method.md)
-   [<span data-ttu-id="fd994-132">Metodo GetInfo</span><span class="sxs-lookup"><span data-stu-id="fd994-132">The GetInfo Method</span></span>](the-getinfo-method.md)
-   [<span data-ttu-id="fd994-133">Ottimizzazione con GetInfoEx</span><span class="sxs-lookup"><span data-stu-id="fd994-133">Optimization Using GetInfoEx</span></span>](optimization-using-getinfoex.md)
-   [<span data-ttu-id="fd994-134">Accesso agli attributi con l'interfaccia IDirectoryObject</span><span class="sxs-lookup"><span data-stu-id="fd994-134">Accessing Attributes with the IDirectoryObject Interface</span></span>](accessing-attributes-with-the-idirectoryobject-interface.md)
-   [<span data-ttu-id="fd994-135">Codice di esempio per la lettura degli attributi</span><span class="sxs-lookup"><span data-stu-id="fd994-135">Example Code for Reading Attributes</span></span>](example-code-for-reading-attributes.md)

 

 