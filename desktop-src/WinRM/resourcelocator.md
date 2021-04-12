---
title: Oggetto ResourceLocator (WSManDisp. h)
description: Fornisce il percorso di una risorsa. È possibile usare un oggetto ResourceLocator anziché un URI di risorsa nelle operazioni dell'oggetto sessione, ad esempio Session. Get, Session. put o Session. enumerate.
ms.assetid: 0904b7eb-d4ce-46a7-bf58-452e7c0d41e9
ms.tgt_platform: multiple
keywords:
- Gestione remota Windows oggetto ResourceLocator
- Oggetto ResourceLocator Gestione remota Windows, descritto
topic_type:
- apiref
api_name:
- ResourceLocator
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd110b94d3174134e6410428843de76e809d5e22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119183"
---
# <a name="resourcelocator-object"></a>Oggetto ResourceLocator

Oggetto che fornisce il percorso di una risorsa. È possibile usare un oggetto **resourceLocator** anziché un [*URI di risorsa*](windows-remote-management-glossary.md) nelle operazioni dell'oggetto [**sessione**](session.md) , ad esempio [**Session. Get**](session-get.md), [**Session. Put**](session-put.md)o [**Session. enumerate**](session-enumerate.md).

Questo oggetto consente di:

-   Aggiungere uno o più [*selettori*](windows-remote-management-glossary.md) che identifichino una particolare istanza di una risorsa. Equivale a fornire un valore di chiave nell'URI della risorsa per una risorsa che usa chiavi. Per ulteriori informazioni, vedere [**resourceLocator. AddSelector**](resourcelocator-addselector.md). È possibile eseguire un'operazione simile utilizzando il parametro *Filter* in una chiamata a [**Session. enumerate**](session-enumerate.md).
-   Specificare un percorso e un dialetto del [*frammento*](windows-remote-management-glossary.md) per ottenere solo una proprietà di una risorsa. È inoltre possibile specificare uno o tutti gli elementi di una proprietà di matrice fornendo l'indice della matrice. Per ulteriori informazioni, vedere [**resourceLocator. FragmentPath**](resourcelocator-fragmentpath.md).
-   Aggiungere una o più [*Opzioni*](windows-remote-management-glossary.md) che un'origine dati può richiedere per elaborare una richiesta. Per ulteriori informazioni, vedere [**resourceLocator. AddOption**](resourcelocator-addoption.md).

Per altre informazioni, vedere [esecuzione di query per istanze specifiche di una risorsa](querying-for-specific-instances-of-a-resource.md).

## <a name="members"></a>Membri

L'oggetto **resourceLocator** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'oggetto **resourceLocator** dispone di questi metodi.



| Metodo                                                   | Descrizione                                                                                                                        |
|:---------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [**AddOption**](resourcelocator-addoption.md)           | Aggiunge dati aggiuntivi necessari per elaborare la richiesta.<br/>                                                                   |
| [**AddSelector**](resourcelocator-addselector.md)       | Aggiunge un [*selettore*](windows-remote-management-glossary.md) all'oggetto **resourceLocator** .<br/>     |
| [**ClearOptions**](resourcelocator-clearoptions.md)     | Rimuove tutte le [*Opzioni*](windows-remote-management-glossary.md) dall'oggetto **resourceLocator** .<br/> |
| [**ClearSelectors**](resourcelocator-clearselectors.md) | Rimuove tutti i selettori da un oggetto **resourceLocator** .<br/>                                                            |



 

### <a name="properties"></a>Proprietà

L'oggetto **resourceLocator** dispone di queste proprietà.



| Proprietà                                                                          | Tipo di accesso           | Descrizione                                                                                                                                                                                             |
|:----------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**FragmentDialect**](resourcelocator-fragmentdialect.md)<br/>             | Lettura/Scrittura<br/> | Ottiene o imposta il dialetto del linguaggio per un [*frammento*](windows-remote-management-glossary.md)di [*risorsa*](windows-remote-management-glossary.md) .<br/> |
| [**FragmentPath**](resourcelocator-fragmentpath.md)<br/>                   | Lettura/Scrittura<br/> | Ottiene o imposta il percorso di una proprietà o di un [*frammento*](windows-remote-management-glossary.md) di [*risorsa*](windows-remote-management-glossary.md) .<br/> |
| [**MustUnderstandOptions**](resourcelocator-mustunderstandoptions.md)<br/> | Lettura/Scrittura<br/> | Ottiene o imposta il valore **MustUnderstandOptions** per l'oggetto **resourceLocator** .<br/>                                                                                                         |
| [**ResourceURI**](resourcelocator-resourceuri.md)<br/>                     | Lettura/Scrittura<br/> | Ottiene o imposta l' [*URI della risorsa*](windows-remote-management-glossary.md) in un oggetto **resourceLocator** .<br/>                                                          |



 

## <a name="remarks"></a>Commenti

L'oggetto **resourceLocator** corrisponde all'interfaccia **IWSManResourceLocator** .

## <a name="examples"></a>Esempio

Nell'esempio di codice VBScript seguente vengono ottenute le proprietà **NumberOfLogicalProcessors** e **NumberOfCores** da un'istanza specifica del [**\_ processore Win32**](/windows/desktop/CIMWin32Prov/win32-processor).


```VB
Option Explicit
Dim strUri
strUri = "http://schemas.microsoft.com/wbem/wsman/1/" _
    & "wmi/root/cimv2/Win32_Processor"
Const FragmentDialect = _
    "https://www.w3.org/TR/1999/REC-xpath-19991116"

Dim WSMan
Set WSMan = CreateObject("WSMan.Automation")

Dim Session
Set Session = WSMan.CreateSession

Dim Locator
Set Locator = WSMan.CreateResourceLocator(strUri)

Locator.AddSelector "DeviceID", "CPU0"

Dim NumberOfCores_XML
Locator.FragmentPath = "NumberOfCores"
Locator.FragmentDialect = FragmentDialect
NumberOfCores_XML = Session.Get(Locator)
DisplayOutput NumberOfCores_XML

Dim NumberOfLogicalProcessors_XML
Locator.FragmentPath = "NumberOfLogicalProcessors"
Locator.FragmentDialect = FragmentDialect
NumberOfLogicalProcessors_XML = Session.Get(Locator)

DisplayOutput NumberOfLogicalProcessors_XML

'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************

Sub DisplayOutput( strWinRMXml )
    Dim xmlFile, xslFile
    Set xmlFile = CreateObject( "MSXml2.DOMDocument.3.0" )    
    Set xslFile = CreateObject( "MSXml2.DOMDocument.3.0" )
    xmlFile.LoadXml( strWinRMXml )
    xslFile.Load( "WsmTxt.xsl" )
    Wscript.Echo xmlFile.TransformNode( xslFile )           
End Sub
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                 |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[API di scripting WinRM](winrm-scripting-api.md)
</dt> </dl>

 

