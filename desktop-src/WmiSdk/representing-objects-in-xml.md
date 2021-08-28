---
description: Genera rappresentazioni XML di oggetti .
ms.assetid: 06d2b532-7ab2-489d-9021-27b5187c8f2b
ms.tgt_platform: multiple
title: Rappresentazione di oggetti in XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68bcbc47a0e5466b69775b4ff9a6c09ce20bae6f
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122879653"
---
# <a name="representing-objects-in-xml"></a>Rappresentazione di oggetti in XML

Il componente codificatore XML in WMI genera rappresentazioni XML di oggetti.

In C++ è possibile avviare il codificatore XML con una chiamata al metodo [**IWbemObjectTextSrc.GetText,**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) specificando l'oggetto da rappresentare in XML e il formato testo da usare nella rappresentazione. Per altre informazioni e un esempio di codice, vedere Per codificare un oggetto in XML usando C/C++.

In VBScript o Visual Basic codificare i dati per un'istanza XML, chiamare [**SWbemObjectEx.GetText**](swbemobjectex-gettext-.md). Per altre informazioni e un esempio di codice, vedere Per codificare un oggetto in XML usando VBScript.

In questo argomento vengono illustrate le sezioni seguenti:

-   [Codificare un oggetto usando C o C++](#encode-an-object-using-c-or-c)
-   [Codificare un oggetto usando VBScript](#encode-an-object-using-vbscript)
-   [Argomenti correlati](#related-topics)

## <a name="encode-an-object-using-c-or-c"></a>Codificare un oggetto usando C o C++

<span id="to_encode_an_object_in_xml_using_c_c_"></span><span id="TO_ENCODE_AN_OBJECT_IN_XML_USING_C_C_"></span>

La procedura seguente descrive come codificare un oggetto in XML usando C o C++.

**Per codificare un oggetto in XML usando C o C++**

1.  Configurare il programma per l'accesso ai dati WMI.

    Poiché WMI è basato sulla tecnologia COM, è necessario eseguire le chiamate richieste alle funzioni [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) e [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) per accedere a WMI. Per altre informazioni, vedere [Inizializzazione di COM per un'applicazione WMI.](initializing-com-for-a-wmi-application.md)

2.  Facoltativamente, creare un [**oggetto IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) e inizializzarlo.

    Non è necessario creare l'oggetto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) a meno che non sia necessario modificare l'operazione predefinita. L'oggetto contesto viene usato dal codificatore XML per controllare la quantità di informazioni incluse nella rappresentazione XML dell'oggetto.

    Nella tabella seguente sono elencati i valori facoltativi che è possibile specificare per l'oggetto contesto.

    

    <table>
    <thead>
    <tr class="header">
    <th>Valore/tipo</th>
    <th>Significato</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>&quot;LocalOnly &quot; <strong>VT_BOOL</strong></td>
    <td>Se <strong>TRUE,</strong>solo le proprietà e i metodi definiti in locale nella classe sono presenti nel codice XML risultante. Il valore predefinito è <strong>FALSE.</strong></td>
    </tr>
    <tr class="even">
    <td>&quot;IncludeQualifiers &quot; <strong>VT_BOOL</strong></td>
    <td>Quando <strong>TRUE,</strong>classe, istanza, proprietà e qualificatori di metodo vengono inclusi nel codice XML risultante. Il valore predefinito è <strong>FALSE.</strong></td>
    </tr>
    <tr class="odd">
    <td>&quot;ExcludeSystemProperties &quot; <strong>VT_BOOL</strong></td>
    <td>Se <strong>TRUE,</strong>le proprietà di sistema WMI vengono filtrate dall'output. Il valore predefinito è <strong>FALSE.</strong></td>
    </tr>
    <tr class="even">
    <td>&quot;PathLevel &quot; <strong>VT_I4</strong></td>
    <td><dl> 0 = Viene &lt; generata una classe o un &gt; <INSTANCE> elemento.<br />
1 = Viene <VALUE.NAMEDOBJECT> generato un elemento.<br />
2 = Viene <VALUE.OBJECTWITHLOCALPATH> generato un elemento.<br />
3 = Viene <VALUE.OBJECTWITHPATH> generato un oggetto .<br />
    </dl> Il valore predefinito è 0 (zero).<br/></td>
    </tr>
    </tbody>
    </table>

    

     

    Nell'esempio di codice seguente viene illustrato come inizializzare l'oggetto di contesto per includere qualificatori ed escludere le proprietà di sistema.

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

    

3.  Ottenere un riferimento alla classe o all'istanza da codificare in XML.

    Dopo aver inizializzato COM e essere connessi a WMI, chiamare [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) per recuperare un riferimento alla classe o all'istanza specificata. Se è stato usato un BSTR per specificare la classe o l'istanza, chiamare [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) per liberare la memoria allocata [**da SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring).

    Nell'esempio di codice seguente viene recuperato un riferimento a [**un'istanza \_ di LogicalDisk Win32.**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)

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

    

4.  Creare un [**oggetto IWbemObjectTextSrc.**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc)

    Dopo aver creato un riferimento a un oggetto, è necessario creare [**l'oggetto IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) con una chiamata a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance). **L'oggetto IWbemObjectTextSrc** viene usato per generare il testo XML effettivo.

    Nell'esempio di codice seguente viene illustrato come creare un [**oggetto IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) chiamando [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).

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

    

5.  Richiamare il [**metodo IWbemObjectTextSrc.GetText**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) per ottenere una rappresentazione XML di un oggetto.

    Dopo aver impostato il contesto per la rappresentazione dell'oggetto, aver creato un riferimento all'oggetto e aver creato un oggetto [**IWbemObjectTextSrc,**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) è possibile generare una rappresentazione XML dell'oggetto specificato chiamando il metodo [**IWbemObjectTextSrc.GetText.**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext)

    Il codice di esempio C++ seguente genera una rappresentazione XML dell'oggetto a cui fa riferimento *pClass*. La rappresentazione XML viene restituita in *strText*. Il terzo parametro di [**GetText**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) specifica il formato di testo da usare per xml e deve essere WMI \_ OBJ \_ TEXT \_ CIM \_ DTD \_ 2 \_ 0 (0x1) o WMI \_ OBJ \_ TEXT WMI \_ \_ DTD \_ 2 \_ 0 (0x2). Per altre informazioni su questi valori, vedere Valori dei parametri [**IWbemObjectTextSrc::GetText.**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext)

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

    

Il codice di esempio C++ seguente include tutti i passaggi della procedura precedente e codifica la classe [**\_ LogicalDisk Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) in XML, inclusi i qualificatori di classe, proprietà e metodo ed escludendo le proprietà di sistema.


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



## <a name="encode-an-object-using-vbscript"></a>Codificare un oggetto usando VBScript

<span id="to_encode_an_object_in_xml_using_vbscript"></span><span id="TO_ENCODE_AN_OBJECT_IN_XML_USING_VBSCRIPT"></span>

La procedura seguente descrive come codificare un oggetto in XML usando VBScript.

**Per codificare un oggetto in XML usando VBScript**

1.  Facoltativamente, creare un [**oggetto SWbemNamedValueSet**](swbemnamedvalueset.md) e inizializzarlo in modo da impostare i valori di contesto necessari per la rappresentazione XML.

    Nell'esempio di codice seguente viene illustrato come i valori indicano al codificatore XML di generare un <VALUE. OBJECTWITHLOCALPATH>, inclusi tutti i qualificatori ed escludendo le proprietà di sistema quando costruisce la rappresentazione XML dell'oggetto.

    ```VB
    ' Create an optional SWbemNamedValueSet object
    set context = CreateObject("wbemscripting.SWbemNamedValueSet")

    ' Initialize the value set object to set the context
    ' Generate a <VALUE.OBJECTWITHLOCALPATH> element
    context.add "PathLevel", 2 
    context.add "IncludeQualifiers", true 
    context.add "ExcludeSystemProperties", true '
    ```

    

2.  Recuperare un'istanza dell'oggetto o della classe da rappresentare in XML.

    Nell'esempio di codice seguente viene recuperata un'istanza dell'oggetto .

    ```VB
    ' Retrieve the object/class to be represented in XML
    set myObj = GetObject("winmgmts:\\.\root\cimv2:win32_LogicalDisk")
    ```

    

3.  Richiamare il metodo [**GetText \_**](swbemobjectex-gettext-.md) dell'istanza creata nel passaggio precedente, usando 1 come parametro per specificare il formato di testo corrispondente a CIM DTD versione 2.0 o 2 per specificare il formato di testo corrispondente a WMI DTD versione 2.0. Se [**l'oggetto SWbemNamedValueSet**](swbemnamedvalueset.md) è stato creato nel passaggio 1, includerlo nell'elenco di parametri come terzo parametro.

    Nell'esempio di codice seguente viene illustrato come richiamare il [**metodo GetText \_**](swbemobjectex-gettext-.md) dell'istanza di .

    ```VB
    ' Get the XML representation of the object
    strText = myObj.GetText_(2,,context)

    ' If you have not used a SWbemNamedValueSet object
    ' enter the following line.
    strText = myObj.GetText_(2)
    ```

    

4.  Facoltativamente, verificare che il codice XML generato nel passaggio 3 sia xml ben formato, creando e inizializzando un oggetto DOM (XML Document Object Model) e quindi caricando il testo XML.

    Nell'esempio di codice seguente viene illustrato come creare e inizializzare un oggetto DOM XML e caricarne il testo XML.

    ```VB
    ' Create an XMLDOM object
    set xml = CreateObject("Microsoft.xmldom")

    ' Initialize the XMLDOM object so results are returned synchronously
    xml.async = false

    ' Load the XML into the XMLDOM object
    xml.loadxml strText
    ```

    

5.  Restituisce la rappresentazione XML dell'oggetto .

    Nell'esempio di codice seguente viene illustrato come usare wscript per l'output del codice XML.

    ```VB
    wscript.echo strText
    ```

    

    Se si è scelto di usare IL DOM XML per verificare che il formato del codice XML generato sia corretto, sostituire la riga precedente con la seguente.

    ```VB
    wscript.echo xml.xml
    ```

    

L'esempio di codice VBScript seguente include tutti i passaggi della procedura precedente e codifica la classe [**\_ LogicalDisk Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) in XML, inclusi i qualificatori di classe, proprietà e metodo ed escludendo le proprietà di sistema.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di WMI](using-wmi.md)
</dt> </dl>

 

