---
title: Oggetto Enumerator (WSManDisp.h)
description: Rappresenta un flusso di risultati restituiti da operazioni, ad esempio un'operazione pull.
ms.assetid: 8d8b461d-06a7-4600-8b68-2faf741a394b
ms.tgt_platform: multiple
keywords:
- Oggetto Enumeratore Windows gestione remota
- Enumeratore - Windows gestione remota , descritto
topic_type:
- apiref
api_name:
- Enumerator
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83799c4c67ad0b0f7c1ad89c77c3abab5989f1231508757c47dfe4c1705d7e20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051829"
---
# <a name="enumerator-object"></a>Enumerator (oggetto)

Rappresenta un flusso di risultati restituiti da operazioni, ad esempio un'operazione pull. Ad esempio, il [**metodo Session.Enumerate**](session-enumerate.md) restituisce più risultati.

## <a name="members"></a>Membri

**L'oggetto Enumerator** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'oggetto Enumerator** dispone di questi metodi.



| Metodo                                  | Descrizione                                                                                   |
|:----------------------------------------|:----------------------------------------------------------------------------------------------|
| [**ReadItem**](enumerator-readitem.md) | Recupera un elemento dalla risorsa e restituisce una rappresentazione XML dell'elemento.<br/> |



 

### <a name="properties"></a>Proprietà

**L'oggetto Enumerator** dispone di queste proprietà.



| Proprietà                                                     | Descrizione                                                                                    |
|:-------------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [**AtEndOfStream**](enumerator-atendofstream.md)<br/> | Ottiene un valore booleano che indica se sono presenti più elementi nell'insieme.<br/> |
| [**Errore**](enumerator-error.md)<br/>                 | Ottiene una rappresentazione XML di informazioni aggiuntive sull'errore.<br/>                         |



 

## <a name="remarks"></a>Commenti

Per avviare un'enumerazione, usare [**Session.Enumerate.**](session-enumerate.md) Per eseguire [*un'operazione WS-Enumeration:*](windows-remote-management-glossary.md)[*Pull*](windows-remote-management-glossary.md) che continua la lettura degli elementi nell'enumerazione, usare [**Enumerator.ReadItem**](enumerator-readitem.md).

**L'oggetto Enumerator** corrisponde all'interfaccia [**IWSManEnumerator.**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator)

## <a name="examples"></a>Esempio

Nell'esempio di codice VBScript seguente vengono enumerati tutti i dischi in un computer remoto specificato dal nome di dominio completo (servername.domain.com). La subroutine DisplayOutput formatta l'output dei dati nello stesso modo dello strumento WinRM.cmd.


```VB
Option Explicit

Const RemoteComputer = "MIG50-64D.mig.net"

Dim objWsman, objSession, strResource
Dim objResultSet

Set objWsman = CreateObject( "WSMan.Automation" )
Set objSession = objWsman.CreateSession( "https://" _
    & RemoteComputer )
strResource = "http://schemas.microsoft.com/wbem/wsman/1/" _
     & "wmi/root/cimv2/Win32_OperatingSystem"
Dim iFlag
iFlag = objWsman.EnumerationFlagReturnObjectAndEPR or _
    objWsman.EnumerationFlagHierarchyDeep
Set objResultSet = _
    objSession.Enumerate( strResource, "", "",  iFlag)
While Not objResultSet.AtEndOfStream
    DisplayOutput( objResultSet.ReadItem ) 
Wend


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
</dt> <dt>

[Enumerazione o elenco di tutte le istanze di una risorsa](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> <dt>

[Esecuzione di script Windows gestione remota](scripting-in-windows-remote-management.md)
</dt> </dl>

 

 





