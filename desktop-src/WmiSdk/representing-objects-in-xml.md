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
# <a name="representing-objects-in-xml"></a>Rappresentazione di oggetti in XML

Il componente codificatore XML in WMI genera rappresentazioni XML di oggetti.

In C++ è possibile avviare il codificatore XML con una chiamata al metodo [**IWbemObjectTextSrc. GetText**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) , specificando l'oggetto che deve essere rappresentato in XML e il formato di testo da utilizzare nella rappresentazione. Per ulteriori informazioni e un esempio di codice, vedere per codificare un oggetto in XML utilizzando C/C++.

In VBScript o Visual Basic per codificare i dati per un'istanza XML, chiamare [**SWbemObjectEx. GetText**](swbemobjectex-gettext-.md). Per ulteriori informazioni e un esempio di codice, vedere per codificare un oggetto in XML tramite VBScript.

Le sezioni seguenti sono illustrate in questo argomento:

-   [Codificare un oggetto con C o C++](#encode-an-object-using-c-or-c)
-   [Codificare un oggetto tramite VBScript](#encode-an-object-using-vbscript)
-   [Argomenti correlati](#related-topics)

## <a name="encode-an-object-using-c-or-c"></a>Codificare un oggetto con C o C++

<span id="to_encode_an_object_in_xml_using_c_c_"></span><span id="TO_ENCODE_AN_OBJECT_IN_XML_USING_C_C_"></span>

Nella procedura riportata di seguito viene descritto come codificare un oggetto in XML utilizzando C o C++.

**Per codificare un oggetto in XML utilizzando C o C++**

1.  Configurare il programma per accedere ai dati WMI.

    Poiché WMI è basato sulla tecnologia COM, è necessario eseguire le chiamate necessarie alle funzioni [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) e [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) per accedere a WMI. Per ulteriori informazioni, vedere [inizializzazione di com per un'applicazione WMI](initializing-com-for-a-wmi-application.md).

2.  Facoltativamente, creare un oggetto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) e inizializzarlo.

    Non è necessario creare l'oggetto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) , a meno che non sia necessario modificare l'operazione predefinita. L'oggetto context viene utilizzato dal codificatore XML per controllare la quantità di informazioni incluse nella rappresentazione XML dell'oggetto.

    Nella tabella seguente sono elencati i valori facoltativi che è possibile specificare per l'oggetto context.

    

    <table>
    <thead>
    <tr class="header">
    <th>Valore/tipo</th>
    <th>Significato</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>&quot;&quot; <strong>VT_BOOL</strong> LocalOnly</td>
    <td>Se è <strong>true</strong>, solo le proprietà e i metodi definiti localmente nella classe sono presenti nel codice XML risultante. Il valore predefinito è <strong>false</strong>.</td>
    </tr>
    <tr class="even">
    <td>&quot;&quot; <strong>VT_BOOL</strong> IncludeQualifiers</td>
    <td>Se <strong>true</strong>, le classi, le istanze, le proprietà e i qualificatori di metodo sono inclusi nel codice XML risultante. Il valore predefinito è <strong>false</strong>.</td>
    </tr>
    <tr class="odd">
    <td>&quot;&quot; <strong>VT_BOOL</strong> ExcludeSystemProperties</td>
    <td>Se è <strong>true</strong>, le proprietà di sistema WMI vengono filtrate dall'output. Il valore predefinito è <strong>false</strong>.</td>
    </tr>
    <tr class="even">
    <td>&quot;&quot; <strong>VT_I4</strong> PathLevel</td>
    <td><dl> 0 = <CLASS> <INSTANCE> viene generato un elemento o.<br />
1 = <VALUE.NAMEDOBJECT> viene generato un elemento.<br />
2 = <VALUE.OBJECTWITHLOCALPATH> viene generato un elemento.<br />
3 = <VALUE.OBJECTWITHPATH> viene generato un.<br />
    </dl> Il valore predefinito è 0 (zero).<br/></td>
    </tr>
    </tbody>
    </table>

    

     

    Nell'esempio di codice riportato di seguito viene illustrato come inizializzare l'oggetto Context per includere qualificatori ed escludere le proprietà di sistema.

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

    Dopo l'inizializzazione di COM e la connessione a WMI, chiamare [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) per recuperare un riferimento alla classe o all'istanza specificata. Se è stato usato un BSTR per specificare la classe o l'istanza, chiamare [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) per liberare la memoria allocata da [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring).

    Nell'esempio di codice seguente viene recuperato un riferimento a un'istanza di [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .

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

    

4.  Creare un oggetto [**IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) .

    Dopo aver creato un riferimento a un oggetto, è necessario creare l'oggetto [**IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) con una chiamata a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance). L'oggetto **IWbemObjectTextSrc** viene utilizzato per generare il testo XML effettivo.

    Nell'esempio di codice seguente viene illustrato come creare un oggetto [**IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) chiamando [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).

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

    

5.  Richiamare il metodo [**IWbemObjectTextSrc. GetText**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) per ottenere una rappresentazione XML di un oggetto.

    Dopo aver impostato il contesto per la rappresentazione dell'oggetto, ottenendo un riferimento all'oggetto e creando un oggetto [**IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) , si è pronti per generare una rappresentazione XML dell'oggetto specificato chiamando il metodo [**IWbemObjectTextSrc. GetText**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) .

    Il codice di esempio C++ seguente genera una rappresentazione XML dell'oggetto a cui fa riferimento *pClass*. La rappresentazione XML viene restituita in *strText*. Il terzo parametro di [**gettext**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) specifica il formato di testo da utilizzare per il codice XML e deve essere WMI \_ obj \_ Text \_ CIM \_ DTD \_ 2 \_ 0 (0x1) o WMI \_ obj \_ Text \_ WMI \_ DTD \_ 2 \_ 0 (0x2). Per ulteriori informazioni su questi valori, vedere [**IWbemObjectTextSrc:: GetText**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) parameter values.

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

    

Il codice di esempio C++ riportato di seguito include tutti i passaggi della procedura precedente e codifica la classe [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) in XML, inclusi i qualificatori di classi, proprietà e metodi ed escludendo le proprietà di sistema.


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



## <a name="encode-an-object-using-vbscript"></a>Codificare un oggetto tramite VBScript

<span id="to_encode_an_object_in_xml_using_vbscript"></span><span id="TO_ENCODE_AN_OBJECT_IN_XML_USING_VBSCRIPT"></span>

Nella procedura riportata di seguito viene descritto come codificare un oggetto in XML utilizzando VBScript.

**Per codificare un oggetto in XML tramite VBScript**

1.  Facoltativamente, creare un oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) e inizializzarlo in modo da impostare i valori di contesto richiesti per la rappresentazione XML.

    Nell'esempio di codice seguente viene illustrato il modo in cui i valori indicano al codificatore XML di generare un valore <. OBJECTWITHLOCALPATH> elemento, inclusi tutti i qualificatori ed escludendo le proprietà di sistema quando viene costruita la rappresentazione XML dell'oggetto.

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

    Nell'esempio di codice seguente viene recuperata un'istanza dell'oggetto.

    ```VB
    ' Retrieve the object/class to be represented in XML
    set myObj = GetObject("winmgmts:\\.\root\cimv2:win32_LogicalDisk")
    ```

    

3.  Richiamare il metodo [**gettext \_**](swbemobjectex-gettext-.md) dell'istanza di creata nel passaggio precedente, usando 1 come parametro per specificare il formato di testo che corrisponde alla dtd CIM versione 2,0 o 2 per specificare il formato di testo che corrisponde alla dtd WMI versione 2,0. Se è stato creato l'oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) nel passaggio 1, includerlo nell'elenco dei parametri come terzo parametro.

    Nell'esempio di codice riportato di seguito viene illustrato come richiamare il metodo [**gettext \_**](swbemobjectex-gettext-.md) dell'istanza di.

    ```VB
    ' Get the XML representation of the object
    strText = myObj.GetText_(2,,context)

    ' If you have not used a SWbemNamedValueSet object
    ' enter the following line.
    strText = myObj.GetText_(2)
    ```

    

4.  Facoltativamente, verificare che il codice XML generato nel passaggio 3 sia un codice XML ben formato, creando e inizializzando un oggetto XML Document Object Model (DOM) e quindi caricarvi il testo XML.

    Nell'esempio di codice seguente viene illustrato come creare e inizializzare un oggetto DOM XML e come caricarvi il testo XML.

    ```VB
    ' Create an XMLDOM object
    set xml = CreateObject("Microsoft.xmldom")

    ' Initialize the XMLDOM object so results are returned synchronously
    xml.async = false

    ' Load the XML into the XMLDOM object
    xml.loadxml strText
    ```

    

5.  Output della rappresentazione XML dell'oggetto.

    Nell'esempio di codice riportato di seguito viene illustrato come utilizzare WScript per restituire il codice XML.

    ```VB
    wscript.echo strText
    ```

    

    Se si sceglie di utilizzare il modello DOM XML per verificare che l'XML generato sia in formato corretto, sostituire la riga precedente con il codice seguente.

    ```VB
    wscript.echo xml.xml
    ```

    

Nell'esempio di codice VBScript seguente sono inclusi tutti i passaggi della procedura precedente e viene codificata la classe [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) in XML, inclusi i qualificatori di classi, proprietà e metodi ed escluse le proprietà di sistema.


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

[Utilizzo di WMI](using-wmi.md)
</dt> </dl>

 

