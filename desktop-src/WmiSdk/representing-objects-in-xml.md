---
description: Genera rappresentazioni XML di oggetti.
ms.assetid: 06d2b532-7ab2-489d-9021-27b5187c8f2b
ms.tgt_platform: multiple
title: Rappresentazione di oggetti in XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9698c54eeff61517a1389ceea14bc2415727f085
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309906"
---
# <a name="representing-objects-in-xml"></a><span data-ttu-id="e74f7-103">Rappresentazione di oggetti in XML</span><span class="sxs-lookup"><span data-stu-id="e74f7-103">Representing Objects in XML</span></span>

<span data-ttu-id="e74f7-104">Il componente codificatore XML in WMI genera rappresentazioni XML di oggetti.</span><span class="sxs-lookup"><span data-stu-id="e74f7-104">The XML encoder component in WMI generates XML representations of objects.</span></span>

<span data-ttu-id="e74f7-105">In C++ è possibile avviare il codificatore XML con una chiamata al metodo [**IWbemObjectTextSrc. GetText**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) , specificando l'oggetto che deve essere rappresentato in XML e il formato di testo da utilizzare nella rappresentazione.</span><span class="sxs-lookup"><span data-stu-id="e74f7-105">In C++, you can start the XML encoder with a call to the [**IWbemObjectTextSrc.GetText**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) method, specifying the object to be represented in XML and the text format to use in the representation.</span></span> <span data-ttu-id="e74f7-106">Per ulteriori informazioni e un esempio di codice, vedere per codificare un oggetto in XML utilizzando C/C++.</span><span class="sxs-lookup"><span data-stu-id="e74f7-106">For more information and a code example, see To encode an object in XML using C/C++.</span></span>

<span data-ttu-id="e74f7-107">In VBScript o Visual Basic per codificare i dati per un'istanza XML, chiamare [**SWbemObjectEx. GetText**](swbemobjectex-gettext-.md).</span><span class="sxs-lookup"><span data-stu-id="e74f7-107">In VBScript or Visual Basic, to encode data for an XML instance, call [**SWbemObjectEx.GetText**](swbemobjectex-gettext-.md).</span></span> <span data-ttu-id="e74f7-108">Per ulteriori informazioni e un esempio di codice, vedere per codificare un oggetto in XML tramite VBScript.</span><span class="sxs-lookup"><span data-stu-id="e74f7-108">For more information and a code example, see To encode an object in XML using VBScript.</span></span>

<span data-ttu-id="e74f7-109">Le sezioni seguenti sono illustrate in questo argomento:</span><span class="sxs-lookup"><span data-stu-id="e74f7-109">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="e74f7-110">Codificare un oggetto con C o C++</span><span class="sxs-lookup"><span data-stu-id="e74f7-110">Encode an Object Using C or C++</span></span>](#encode-an-object-using-c-or-c)
-   [<span data-ttu-id="e74f7-111">Codificare un oggetto tramite VBScript</span><span class="sxs-lookup"><span data-stu-id="e74f7-111">Encode an Object Using VBScript</span></span>](#encode-an-object-using-vbscript)
-   [<span data-ttu-id="e74f7-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e74f7-112">Related topics</span></span>](#related-topics)

## <a name="encode-an-object-using-c-or-c"></a><span data-ttu-id="e74f7-113">Codificare un oggetto con C o C++</span><span class="sxs-lookup"><span data-stu-id="e74f7-113">Encode an Object Using C or C++</span></span>

<span id="to_encode_an_object_in_xml_using_c_c_"></span><span id="TO_ENCODE_AN_OBJECT_IN_XML_USING_C_C_"></span>

<span data-ttu-id="e74f7-114">Nella procedura riportata di seguito viene descritto come codificare un oggetto in XML utilizzando C o C++.</span><span class="sxs-lookup"><span data-stu-id="e74f7-114">The following procedure describes how to encode an object in XML using C or C++.</span></span>

<span data-ttu-id="e74f7-115">**Per codificare un oggetto in XML utilizzando C o C++**</span><span class="sxs-lookup"><span data-stu-id="e74f7-115">**To encode an object in XML using C or C++**</span></span>

1.  <span data-ttu-id="e74f7-116">Configurare il programma per accedere ai dati WMI.</span><span class="sxs-lookup"><span data-stu-id="e74f7-116">Set up your program to access WMI data.</span></span>

    <span data-ttu-id="e74f7-117">Poiché WMI è basato sulla tecnologia COM, è necessario eseguire le chiamate necessarie alle funzioni [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) e [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) per accedere a WMI.</span><span class="sxs-lookup"><span data-stu-id="e74f7-117">Because WMI is based on COM technology, you must perform the requisite calls to the [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) and [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) functions to access WMI.</span></span> <span data-ttu-id="e74f7-118">Per ulteriori informazioni, vedere [inizializzazione di com per un'applicazione WMI](initializing-com-for-a-wmi-application.md).</span><span class="sxs-lookup"><span data-stu-id="e74f7-118">For more information, see [Initializing COM for a WMI Application](initializing-com-for-a-wmi-application.md).</span></span>

2.  <span data-ttu-id="e74f7-119">Facoltativamente, creare un oggetto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) e inizializzarlo.</span><span class="sxs-lookup"><span data-stu-id="e74f7-119">Optionally, create an [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object and initialize it.</span></span>

    <span data-ttu-id="e74f7-120">Non è necessario creare l'oggetto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) , a meno che non sia necessario modificare l'operazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="e74f7-120">You do not need to create the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object unless you need to change the default operation.</span></span> <span data-ttu-id="e74f7-121">L'oggetto context viene utilizzato dal codificatore XML per controllare la quantità di informazioni incluse nella rappresentazione XML dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e74f7-121">The context object is used by the XML encoder to control the amount of information included in the object's XML representation.</span></span>

    <span data-ttu-id="e74f7-122">Nella tabella seguente sono elencati i valori facoltativi che è possibile specificare per l'oggetto context.</span><span class="sxs-lookup"><span data-stu-id="e74f7-122">The following table lists the optional values that can be specified for the context object.</span></span>

    

    <table>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="e74f7-123">Valore/tipo</span><span class="sxs-lookup"><span data-stu-id="e74f7-123">Value/type</span></span></th>
    <th><span data-ttu-id="e74f7-124">Significato</span><span class="sxs-lookup"><span data-stu-id="e74f7-124">Meaning</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="e74f7-125">&quot;&quot; <strong>VT_BOOL</strong> LocalOnly</span><span class="sxs-lookup"><span data-stu-id="e74f7-125">&quot;LocalOnly&quot; <strong>VT_BOOL</strong></span></span></td>
    <td><span data-ttu-id="e74f7-126">Se è <strong>true</strong>, solo le proprietà e i metodi definiti localmente nella classe sono presenti nel codice XML risultante.</span><span class="sxs-lookup"><span data-stu-id="e74f7-126">When <strong>TRUE</strong>, only properties and methods defined locally in the class are present in the resulting XML.</span></span> <span data-ttu-id="e74f7-127">Il valore predefinito è <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="e74f7-127">The default value is <strong>FALSE</strong>.</span></span></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="e74f7-128">&quot;&quot; <strong>VT_BOOL</strong> IncludeQualifiers</span><span class="sxs-lookup"><span data-stu-id="e74f7-128">&quot;IncludeQualifiers&quot; <strong>VT_BOOL</strong></span></span></td>
    <td><span data-ttu-id="e74f7-129">Se <strong>true</strong>, le classi, le istanze, le proprietà e i qualificatori di metodo sono inclusi nel codice XML risultante.</span><span class="sxs-lookup"><span data-stu-id="e74f7-129">When <strong>TRUE</strong>, class, instance, properties, and method qualifiers are included in the resulting XML.</span></span> <span data-ttu-id="e74f7-130">Il valore predefinito è <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="e74f7-130">The default value is <strong>FALSE</strong>.</span></span></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="e74f7-131">&quot;&quot; <strong>VT_BOOL</strong> ExcludeSystemProperties</span><span class="sxs-lookup"><span data-stu-id="e74f7-131">&quot;ExcludeSystemProperties&quot; <strong>VT_BOOL</strong></span></span></td>
    <td><span data-ttu-id="e74f7-132">Se è <strong>true</strong>, le proprietà di sistema WMI vengono filtrate dall'output.</span><span class="sxs-lookup"><span data-stu-id="e74f7-132">When <strong>TRUE</strong>, WMI system properties are filtered out of the output.</span></span> <span data-ttu-id="e74f7-133">Il valore predefinito è <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="e74f7-133">The default value is <strong>FALSE</strong>.</span></span></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="e74f7-134">&quot;&quot; <strong>VT_I4</strong> PathLevel</span><span class="sxs-lookup"><span data-stu-id="e74f7-134">&quot;PathLevel&quot; <strong>VT_I4</strong></span></span></td>
    <td><dl> <span data-ttu-id="e74f7-135">0 = <CLASS> <INSTANCE> viene generato un elemento o.</span><span class="sxs-lookup"><span data-stu-id="e74f7-135">0 = A <CLASS> or <INSTANCE> element is generated.</span></span><br />
<span data-ttu-id="e74f7-136">1 = <VALUE.NAMEDOBJECT> viene generato un elemento.</span><span class="sxs-lookup"><span data-stu-id="e74f7-136">1 = A <VALUE.NAMEDOBJECT> element is generated.</span></span><br />
<span data-ttu-id="e74f7-137">2 = <VALUE.OBJECTWITHLOCALPATH> viene generato un elemento.</span><span class="sxs-lookup"><span data-stu-id="e74f7-137">2 = A <VALUE.OBJECTWITHLOCALPATH> element is generated.</span></span><br />
<span data-ttu-id="e74f7-138">3 = <VALUE.OBJECTWITHPATH> viene generato un.</span><span class="sxs-lookup"><span data-stu-id="e74f7-138">3 = A <VALUE.OBJECTWITHPATH> is generated.</span></span><br />
    </dl> <span data-ttu-id="e74f7-139">Il valore predefinito è 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="e74f7-139">The default is 0 (zero).</span></span><br/></td>
    </tr>
    </tbody>
    </table>

    

     

    <span data-ttu-id="e74f7-140">Nell'esempio di codice riportato di seguito viene illustrato come inizializzare l'oggetto Context per includere qualificatori ed escludere le proprietà di sistema.</span><span class="sxs-lookup"><span data-stu-id="e74f7-140">The following code example shows how the context object is initialized to include qualifiers and exclude system properties.</span></span>

    ```C++
    VARIANT vValue;
    IWbemContext *pContext = NULL;
    HRESULT hr = CoCreateInstance (CLSID_WbemContext, 
                           NULL, 
                           CLSCTX_INPROC_SERVER,
                           IID_IWbemContext, 
                           (void**) &pContext);
    if (FAILED(hr))
    {
      printf("Create context failed with %x\n", hr);
      return hr;
    }

    // Generate a <VALUE.OBJECTWITHLOCALPATH> element
    VariantInit(&vValue);
    vValue.vt = VT_I4;
    vValue.lVal = 2;
    pContext->SetValue(L"PathLevel", 0, &vValue);
    VariantClear(&vValue);

    // Include qualifiers
    VariantInit(&vValue);
    vValue.vt = VT_BOOL;
    vValue.boolVal = VARIANT_TRUE;
    pContext->SetValue(L"IncludeQualifiers", 0, &vValue);
    VariantClear(&vValue);

    // Exclude system properties
    VariantInit(&vValue);
    vValue.vt = VT_BOOL;
    vValue.boolVal = VARIANT_TRUE;
    pContext->SetValue(L"ExcludeSystemProperties", 0, &vValue);
    VariantClear(&vValue);
    ```

    

3.  <span data-ttu-id="e74f7-141">Ottenere un riferimento alla classe o all'istanza da codificare in XML.</span><span class="sxs-lookup"><span data-stu-id="e74f7-141">Get a reference to the class or instance to encode in XML.</span></span>

    <span data-ttu-id="e74f7-142">Dopo l'inizializzazione di COM e la connessione a WMI, chiamare [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) per recuperare un riferimento alla classe o all'istanza specificata.</span><span class="sxs-lookup"><span data-stu-id="e74f7-142">After you have initialized COM and are connected to WMI, call [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) to retrieve a reference to the specified class or instance.</span></span> <span data-ttu-id="e74f7-143">Se è stato usato un BSTR per specificare la classe o l'istanza, chiamare [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) per liberare la memoria allocata da [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring).</span><span class="sxs-lookup"><span data-stu-id="e74f7-143">If you used a BSTR to specify the class or instance, call [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free up the memory allocated by [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring).</span></span>

    <span data-ttu-id="e74f7-144">Nell'esempio di codice seguente viene recuperato un riferimento a un'istanza di [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .</span><span class="sxs-lookup"><span data-stu-id="e74f7-144">The following code example retrieves a reference to an [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) instance.</span></span>

    ```C++
    HRESULT hr = NULL;
    IWbemClassObject *pClass = NULL;
    BSTR strObj = SysAllocString(L"Win32_LogicalDisk");

    hr = pConnection->GetObject(strObj, 
                                0, 
                                NULL, 
                                &pClass, 
                                NULL);

    SysFreeString(strObj);
    if (FAILED(hr))
    {
      printf("GetObject failed with %x\n",hr)
      return hr;
    }
    ```

    

4.  <span data-ttu-id="e74f7-145">Creare un oggetto [**IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) .</span><span class="sxs-lookup"><span data-stu-id="e74f7-145">Create an [**IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) object.</span></span>

    <span data-ttu-id="e74f7-146">Dopo aver creato un riferimento a un oggetto, è necessario creare l'oggetto [**IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) con una chiamata a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="e74f7-146">After you have a reference to an object you must create the [**IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) object with a call to [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span> <span data-ttu-id="e74f7-147">L'oggetto **IWbemObjectTextSrc** viene utilizzato per generare il testo XML effettivo.</span><span class="sxs-lookup"><span data-stu-id="e74f7-147">The **IWbemObjectTextSrc** object is used to generate the actual XML text.</span></span>

    <span data-ttu-id="e74f7-148">Nell'esempio di codice seguente viene illustrato come creare un oggetto [**IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) chiamando [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="e74f7-148">The following code example shows how to create an [**IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) object by calling [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

    ```C++
    HRESULT hr = NULL;
    IWbemObjectTextSrc *pSrc = NULL;

    hr = CoCreateInstance (CLSID_WbemObjectTextSrc, 
                           NULL,
                           CLSCTX_INPROC_SERVER,
                           IID_IWbemObjectTextSrc, 
                           (void**) &pSrc);

    if (FAILED(hr))
    {
        printf("CoCreateInstance of IWbemObjectTextSrc failed %x\n",hr);
        return hr;
    }
    ```

    

5.  <span data-ttu-id="e74f7-149">Richiamare il metodo [**IWbemObjectTextSrc. GetText**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) per ottenere una rappresentazione XML di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="e74f7-149">Invoke the [**IWbemObjectTextSrc.GetText**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) method to get an XML representation of an object.</span></span>

    <span data-ttu-id="e74f7-150">Dopo aver impostato il contesto per la rappresentazione dell'oggetto, ottenendo un riferimento all'oggetto e creando un oggetto [**IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) , si è pronti per generare una rappresentazione XML dell'oggetto specificato chiamando il metodo [**IWbemObjectTextSrc. GetText**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) .</span><span class="sxs-lookup"><span data-stu-id="e74f7-150">After setting the context for the object's representation, getting a reference to the object, and creating an [**IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) object, you are ready to generate an XML representation of the specified object by calling the [**IWbemObjectTextSrc.GetText**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) method.</span></span>

    <span data-ttu-id="e74f7-151">Il codice di esempio C++ seguente genera una rappresentazione XML dell'oggetto a cui fa riferimento *pClass*.</span><span class="sxs-lookup"><span data-stu-id="e74f7-151">The following C++ example code generates an XML representation of the object referenced by *pClass*.</span></span> <span data-ttu-id="e74f7-152">La rappresentazione XML viene restituita in *strText*.</span><span class="sxs-lookup"><span data-stu-id="e74f7-152">The XML representation is returned in *strText*.</span></span> <span data-ttu-id="e74f7-153">Il terzo parametro di [**gettext**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) specifica il formato di testo da utilizzare per il codice XML e deve essere WMI \_ obj \_ Text \_ CIM \_ DTD \_ 2 \_ 0 (0x1) o WMI \_ obj \_ Text \_ WMI \_ DTD \_ 2 \_ 0 (0x2).</span><span class="sxs-lookup"><span data-stu-id="e74f7-153">The third parameter of [**GetText**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) specifies the text format to be used for the XML and must be either WMI\_OBJ\_TEXT\_CIM\_DTD\_2\_0 (0x1) or WMI\_OBJ\_TEXT\_WMI\_DTD\_2\_0 (0x2).</span></span> <span data-ttu-id="e74f7-154">Per ulteriori informazioni su questi valori, vedere [**IWbemObjectTextSrc:: GetText**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) parameter values.</span><span class="sxs-lookup"><span data-stu-id="e74f7-154">For more information about these values, see [**IWbemObjectTextSrc::GetText**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) Parameter Values.</span></span>

    ```C++
    HRESULT hr = NULL;
    BSTR strText = NULL;
    hr = pSrc->GetText(0, 
                       pClass, 
                       WMI_OBJ_TEXT_CIM_DTD_2_0,
                       pContext, 
                       &strText);

    // Perform a task with strText
    SysFreeString(strText);

    if (FAILED(hr))
    {
      printf("GetText failed with %x\n", hr);
      return hr;
    }
    ```

    

<span data-ttu-id="e74f7-155">Il codice di esempio C++ riportato di seguito include tutti i passaggi della procedura precedente e codifica la classe [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) in XML, inclusi i qualificatori di classi, proprietà e metodi ed escludendo le proprietà di sistema.</span><span class="sxs-lookup"><span data-stu-id="e74f7-155">The following C++ example code includes all of the steps in the previous procedure and encodes the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class in XML including class, property, and method qualifiers and excluding system properties.</span></span>


```C++
// The following #define statement is needed so that 
// the proper values are loaded by the #include files.
#define _WIN32_WINNT 0x0500

#include <stdio.h>
#include <wbemcli.h>
#pragma comment(lib, "wbemuuid.lib")

// Initialize the context object
// ---------------------------------------------
void FillUpContext(IWbemContext *pContext)
{
  VARIANT vValue;

  // IncludeQualifiers
  VariantInit(&vValue);
  vValue.vt = VT_BOOL;
  vValue.boolVal = VARIANT_FALSE;
  pContext->SetValue(L"IncludeQualifiers", 0, &vValue);
  VariantClear(&vValue);

  VariantInit(&vValue);
  vValue.vt = VT_I4;
  vValue.lVal = 0;
  pContext->SetValue(L"PathLevel", 0, &vValue);
  VariantClear(&vValue);

  // ExcludeSystemProperties
  VariantInit(&vValue);
  vValue.vt = VT_BOOL;
  vValue.boolVal = VARIANT_TRUE;
  pContext->SetValue(L"ExcludeSystemProperties", 0, &vValue);
  VariantClear(&vValue);
}

// Main method ... drives the program
// ---------------------------------------------
int _cdecl main(int argc, char * argv[])
{
  BSTR strNs = NULL;
  BSTR strObj = NULL;
  BSTR strText = NULL;

  if(FAILED(CoInitialize(NULL)))
    return 1;
  HRESULT hr = E_FAIL;
  IWbemObjectTextSrc *pSrc = NULL;

  IWbemLocator *pL = NULL;
  if(SUCCEEDED(hr = CoCreateInstance (CLSID_WbemLocator, 
                                      NULL, 
                                      CLSCTX_INPROC_SERVER,
                                      IID_IWbemLocator, 
                                      (void**) &pL)))
  {
    // Create a context object
    IWbemContext *pContext = NULL;
    if(SUCCEEDED(hr = CoCreateInstance (CLSID_WbemContext, 
                                        NULL, 
                                        CLSCTX_INPROC_SERVER,
                                        IID_IWbemContext, 
                                        (void**) &pContext)))
    {
      FillUpContext(pContext);
      IWbemServices *pConnection = NULL;
      strNs = SysAllocString(L"root\\cimv2");
      strText = NULL;
      if(SUCCEEDED(hr = pL->ConnectServer(strNs, 
                                          NULL, 
                                          NULL, 
                                          NULL, 
                                          0, 
                                          NULL, 
                                          NULL, 
                                          &pConnection)))
      {
        IWbemClassObject *pClass = NULL;
        strObj = SysAllocString(L"Win32_LogicalDisk");

        if(SUCCEEDED(hr = CoCreateInstance (CLSID_WbemObjectTextSrc, 
                                            NULL,
                                            CLSCTX_INPROC_SERVER,
                                            IID_IWbemObjectTextSrc, 
                                            (void**) &pSrc)))
        {
          // Test for GetObject
          if(SUCCEEDED(hr = pConnection->GetObject(strObj, 
                                                   0, 
                                                   NULL, 
                                                   &pClass, 
                                                   NULL)))
          {
            if(SUCCEEDED(hr = pSrc->GetText(0, 
                                            pClass, 
                                            WMI_OBJ_TEXT_CIM_DTD_2_0,
                                            pContext, 
                                            &strText)))
            {
              printf("GETOBJECT SUCCEEDED\n");
              printf("==========================================\n");
              wprintf(strText);
              pContext->Release();
              pClass->Release();
            }
            else
            {
              printf("GetText failed with %x\n", hr);
              // Free up the object
              pContext->Release();
              pClass->Release();
            }
          }
          else
            printf("GetObject failed with %x\n", hr);
        }
        else
          printf("CoCreateInstance on WbemObjectTextSrc failed with %x\n", hr);
      }
      else
        printf("ConnectServer on root\\cimv2 failed with %x\n", hr);
    }
    else
      printf("CoCreateInstance on Context failed with %x\n", hr);
  }
  else
    printf("CoCreateInstance on Locator failed with %x\n", hr);

// Clean up memory
  if (strNs != NULL)
    SysFreeString(strNs);
  if (strObj != NULL)
    SysFreeString(strObj);
  if (strText != NULL)
    SysFreeString(strText);
  if (pSrc != NULL)
    pSrc->Release();
  if (pL != NULL)
    pL->Release();
  return 0;
}
```



## <a name="encode-an-object-using-vbscript"></a><span data-ttu-id="e74f7-156">Codificare un oggetto tramite VBScript</span><span class="sxs-lookup"><span data-stu-id="e74f7-156">Encode an Object Using VBScript</span></span>

<span id="to_encode_an_object_in_xml_using_vbscript"></span><span id="TO_ENCODE_AN_OBJECT_IN_XML_USING_VBSCRIPT"></span>

<span data-ttu-id="e74f7-157">Nella procedura riportata di seguito viene descritto come codificare un oggetto in XML utilizzando VBScript.</span><span class="sxs-lookup"><span data-stu-id="e74f7-157">The following procedure describes how to encode an object in XML using VBScript.</span></span>

<span data-ttu-id="e74f7-158">**Per codificare un oggetto in XML tramite VBScript**</span><span class="sxs-lookup"><span data-stu-id="e74f7-158">**To encode an object in XML using VBScript**</span></span>

1.  <span data-ttu-id="e74f7-159">Facoltativamente, creare un oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) e inizializzarlo in modo da impostare i valori di contesto richiesti per la rappresentazione XML.</span><span class="sxs-lookup"><span data-stu-id="e74f7-159">Optionally, create an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object and initialize it so as to set the context values required for the XML representation.</span></span>

    <span data-ttu-id="e74f7-160">Nell'esempio di codice seguente viene illustrato il modo in cui i valori indicano al codificatore XML di generare un valore <. OBJECTWITHLOCALPATH> elemento, inclusi tutti i qualificatori ed escludendo le proprietà di sistema quando viene costruita la rappresentazione XML dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e74f7-160">The following code example shows how the values instruct the XML encoder to generate a <VALUE.OBJECTWITHLOCALPATH> element, including all of the qualifiers and excluding system properties when it constructs the XML representation of the object.</span></span>

    ```VB
    ' Create an optional SWbemNamedValueSet object
    set context = CreateObject("wbemscripting.SWbemNamedValueSet")

    ' Initialize the value set object to set the context
    ' Generate a <VALUE.OBJECTWITHLOCALPATH> element
    context.add "PathLevel", 2 
    context.add "IncludeQualifiers", true 
    context.add "ExcludeSystemProperties", true '
    ```

    

2.  <span data-ttu-id="e74f7-161">Recuperare un'istanza dell'oggetto o della classe da rappresentare in XML.</span><span class="sxs-lookup"><span data-stu-id="e74f7-161">Retrieve an instance of the object or class to represent in XML.</span></span>

    <span data-ttu-id="e74f7-162">Nell'esempio di codice seguente viene recuperata un'istanza dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e74f7-162">The following code example retrieves an instance of the object.</span></span>

    ```VB
    ' Retrieve the object/class to be represented in XML
    set myObj = GetObject("winmgmts:\\.\root\cimv2:win32_LogicalDisk")
    ```

    

3.  <span data-ttu-id="e74f7-163">Richiamare il metodo [**gettext \_**](swbemobjectex-gettext-.md) dell'istanza di creata nel passaggio precedente, usando 1 come parametro per specificare il formato di testo che corrisponde alla dtd CIM versione 2,0 o 2 per specificare il formato di testo che corrisponde alla dtd WMI versione 2,0.</span><span class="sxs-lookup"><span data-stu-id="e74f7-163">Invoke the [**GetText\_**](swbemobjectex-gettext-.md) method of the instance created in the preceding step, using 1 as the parameter to specify the text format that corresponds to CIM DTD version 2.0, or 2 to specify the text format that corresponds to WMI DTD version 2.0.</span></span> <span data-ttu-id="e74f7-164">Se è stato creato l'oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) nel passaggio 1, includerlo nell'elenco dei parametri come terzo parametro.</span><span class="sxs-lookup"><span data-stu-id="e74f7-164">If you created the [**SWbemNamedValueSet**](swbemnamedvalueset.md) object in Step 1, include it in the parameter list as the third parameter.</span></span>

    <span data-ttu-id="e74f7-165">Nell'esempio di codice riportato di seguito viene illustrato come richiamare il metodo [**gettext \_**](swbemobjectex-gettext-.md) dell'istanza di.</span><span class="sxs-lookup"><span data-stu-id="e74f7-165">The following code example shows how to invoke the [**GetText\_**](swbemobjectex-gettext-.md) method of the instance.</span></span>

    ```VB
    ' Get the XML representation of the object
    strText = myObj.GetText_(2,,context)

    ' If you have not used a SWbemNamedValueSet object
    ' enter the following line.
    strText = myObj.GetText_(2)
    ```

    

4.  <span data-ttu-id="e74f7-166">Facoltativamente, verificare che il codice XML generato nel passaggio 3 sia un codice XML ben formato, creando e inizializzando un oggetto XML Document Object Model (DOM) e quindi caricarvi il testo XML.</span><span class="sxs-lookup"><span data-stu-id="e74f7-166">Optionally, validate that the XML generated in Step 3 is well-formed XML, by creating and initializing an XML Document Object Model (DOM) object and then load the XML text into it.</span></span>

    <span data-ttu-id="e74f7-167">Nell'esempio di codice seguente viene illustrato come creare e inizializzare un oggetto DOM XML e come caricarvi il testo XML.</span><span class="sxs-lookup"><span data-stu-id="e74f7-167">The following code example shows how to create and initialize an XML DOM object and load the XML text into it.</span></span>

    ```VB
    ' Create an XMLDOM object
    set xml = CreateObject("Microsoft.xmldom")

    ' Initialize the XMLDOM object so results are returned synchronously
    xml.async = false

    ' Load the XML into the XMLDOM object
    xml.loadxml strText
    ```

    

5.  <span data-ttu-id="e74f7-168">Output della rappresentazione XML dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e74f7-168">Output the XML representation of the object.</span></span>

    <span data-ttu-id="e74f7-169">Nell'esempio di codice riportato di seguito viene illustrato come utilizzare WScript per restituire il codice XML.</span><span class="sxs-lookup"><span data-stu-id="e74f7-169">The following code example shows how to use wscript to output the XML.</span></span>

    ```VB
    wscript.echo strText
    ```

    

    <span data-ttu-id="e74f7-170">Se si sceglie di utilizzare il modello DOM XML per verificare che l'XML generato sia in formato corretto, sostituire la riga precedente con il codice seguente.</span><span class="sxs-lookup"><span data-stu-id="e74f7-170">If you chose to use XML DOM to verify that the XML generated is well-formed, replace the previous line with the following.</span></span>

    ```VB
    wscript.echo xml.xml
    ```

    

<span data-ttu-id="e74f7-171">Nell'esempio di codice VBScript seguente sono inclusi tutti i passaggi della procedura precedente e viene codificata la classe [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) in XML, inclusi i qualificatori di classi, proprietà e metodi ed escluse le proprietà di sistema.</span><span class="sxs-lookup"><span data-stu-id="e74f7-171">The following VBScript code example includes all of the steps in the preceding procedure and encodes the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class in XML, including class, property, and method qualifiers and excluding system properties.</span></span>


```VB
' Create optional SWbemNamedValueSet object
set context = CreateObject("Wbemscripting.SWbemNamedValueSet")

' Initialize the context object
context.add "PathLevel", 2
context.add "IncludeQualifiers", true
context.add "ExcludeSystemProperties", true

' Retrieve the object/class to be represented in XML
set myObj = GetObject("winmgmts:\\.\root\cimv2:Win32_LogicalDisk")

' Get the XML representation of the object
strText = myObj.GetText_(2,,context)
' If you have not used a SWbemNamedValueSet object 
'   use the following line
'   strText = myObj.GetText(2)

' Print the XML representation
wscript.echo strText

' If you choose to use the XML DOM to verify 
'   that the XML generated is well-formed, replace the last
'   line in the above code example with the following lines:

' Create an XMLDOM object
set xml = CreateObject("Microsoft.xmldom")

' Initialize the XMLDOM object so results are 
'   returned synchronously
xml.async = false

' Load the XML into the XMLDOM object
xml.loadxml strText

' Print the XML representation
wscript.echo xml.xml
```



## <a name="related-topics"></a><span data-ttu-id="e74f7-172">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e74f7-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e74f7-173">Utilizzo di WMI</span><span class="sxs-lookup"><span data-stu-id="e74f7-173">Using WMI</span></span>](using-wmi.md)
</dt> </dl>

 

