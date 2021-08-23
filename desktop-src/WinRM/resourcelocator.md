---
title: Oggetto ResourceLocator (WSManDisp.h)
description: Specifica il percorso di una risorsa. È possibile usare un oggetto ResourceLocator anziché un URI di risorsa nelle operazioni dell'oggetto Session, ad esempio Session.Get, Session.Put o Session.Enumerate.
ms.assetid: 0904b7eb-d4ce-46a7-bf58-452e7c0d41e9
ms.tgt_platform: multiple
keywords:
- Oggetto ResourceLocator Windows gestione remota
- Oggetto ResourceLocator Windows Gestione remota , descritto
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
ms.openlocfilehash: 26d3287c02949326b672f550271ba3472e6cb16abb6748efb4a80de425c40e57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119642871"
---
# <a name="resourcelocator-object"></a>Oggetto ResourceLocator

Oggetto che fornisce il percorso di una risorsa. È possibile usare un **oggetto ResourceLocator** anziché un [*URI*](windows-remote-management-glossary.md) di risorsa nelle operazioni dell'oggetto [**Session,**](session.md) ad esempio [**Session.Get**](session-get.md), [**Session.Put**](session-put.md)o [**Session.Enumerate**](session-enumerate.md).

Questo oggetto consente di:

-   Aggiungere uno o più [*selettori che*](windows-remote-management-glossary.md) identificano una particolare istanza di una risorsa. Questo è lo stesso di fornire un valore di chiave nell'URI della risorsa per una risorsa che usa le chiavi. Per altre informazioni, vedere [**ResourceLocator.AddSelector**](resourcelocator-addselector.md). È possibile eseguire un'operazione simile usando il *parametro filter* in una chiamata a [**Session.Enumerate**](session-enumerate.md).
-   Specificare un [*percorso di*](windows-remote-management-glossary.md) frammento e un dialetto per ottenere solo una proprietà di una risorsa. È anche possibile specificare uno o tutti gli elementi di una proprietà di matrice specificando l'indice della matrice. Per altre informazioni, vedere [**ResourceLocator.FragmentPath.**](resourcelocator-fragmentpath.md)
-   Aggiungere una o più [*opzioni che*](windows-remote-management-glossary.md) un'origine dati potrebbe richiedere per elaborare una richiesta. Per altre informazioni, vedere [**ResourceLocator.AddOption.**](resourcelocator-addoption.md)

Per altre informazioni, vedere [Esecuzione di query per istanze specifiche di una risorsa.](querying-for-specific-instances-of-a-resource.md)

## <a name="members"></a>Membri

**L'oggetto ResourceLocator** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'oggetto ResourceLocator** dispone di questi metodi.



| Metodo                                                   | Descrizione                                                                                                                        |
|:---------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [**AddOption**](resourcelocator-addoption.md)           | Aggiunge dati aggiuntivi necessari per elaborare la richiesta.<br/>                                                                   |
| [**AddSelector**](resourcelocator-addselector.md)       | Aggiunge un [*selettore*](windows-remote-management-glossary.md) **all'oggetto ResourceLocator.**<br/>     |
| [**ClearOptions**](resourcelocator-clearoptions.md)     | Rimuove tutte [*le opzioni*](windows-remote-management-glossary.md) **dall'oggetto ResourceLocator.**<br/> |
| [**ClearSelectors**](resourcelocator-clearselectors.md) | Rimuove tutti i selettori da un **oggetto ResourceLocator.**<br/>                                                            |



 

### <a name="properties"></a>Proprietà

**L'oggetto ResourceLocator** ha queste proprietà.



| Proprietà                                                                          | Tipo di accesso           | Descrizione                                                                                                                                                                                             |
|:----------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**FrammentoDialect**](resourcelocator-fragmentdialect.md)<br/>             | Lettura/Scrittura<br/> | Ottiene o imposta il dialetto della lingua per un [*frammento di*](windows-remote-management-glossary.md) [*risorsa.*](windows-remote-management-glossary.md)<br/> |
| [**FragmentPath**](resourcelocator-fragmentpath.md)<br/>                   | Lettura/Scrittura<br/> | Ottiene o imposta il percorso per un [*frammento di*](windows-remote-management-glossary.md) [*risorsa*](windows-remote-management-glossary.md) o una proprietà.<br/> |
| [**MustUnderstandOptions**](resourcelocator-mustunderstandoptions.md)<br/> | Lettura/Scrittura<br/> | Ottiene o imposta il **valore MustUnderstandOptions** per **l'oggetto ResourceLocator.**<br/>                                                                                                         |
| [**ResourceURI**](resourcelocator-resourceuri.md)<br/>                     | Lettura/Scrittura<br/> | Ottiene o imposta [*l'URI della risorsa*](windows-remote-management-glossary.md) in **un oggetto ResourceLocator.**<br/>                                                          |



 

## <a name="remarks"></a>Commenti

**L'oggetto ResourceLocator** corrisponde all'interfaccia **IWSManResourceLocator.**

## <a name="examples"></a>Esempio

L'esempio di codice VBScript seguente ottiene le **proprietà NumberOfLogicalProcessors** e **NumberOfCores** da un'istanza specifica del processore [**Win32. \_**](/windows/desktop/CIMWin32Prov/win32-processor)


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
| Intestazione<br/>                   | <dl> <dt>WSManDisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WSManDisp.idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>WSManDisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[WinRM Scripting API](winrm-scripting-api.md)
</dt> </dl>

 

