---
title: Oggetto Enumerator (WSManDisp. h)
description: Rappresenta un flusso di risultati restituiti dalle operazioni, ad esempio un'operazione pull.
ms.assetid: 8d8b461d-06a7-4600-8b68-2faf741a394b
ms.tgt_platform: multiple
keywords:
- Gestione remota Windows oggetto enumeratore
- Enumeratore Gestione remota Windows oggetto, descritto
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
ms.openlocfilehash: 6ad2395ae0ba17b1f221cd0a6dc0f7517a89db71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048682"
---
# <a name="enumerator-object"></a>Enumerator (oggetto)

Rappresenta un flusso di risultati restituiti dalle operazioni, ad esempio un'operazione pull. Ad esempio, il metodo [**Session. enumerate**](session-enumerate.md) restituisce più risultati.

## <a name="members"></a>Membri

L'oggetto **enumeratore** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'oggetto **enumeratore** ha questi metodi.



| Metodo                                  | Descrizione                                                                                   |
|:----------------------------------------|:----------------------------------------------------------------------------------------------|
| [**ReadItem**](enumerator-readitem.md) | Recupera un elemento dalla risorsa e restituisce una rappresentazione XML dell'elemento.<br/> |



 

### <a name="properties"></a>Proprietà

L'oggetto **enumeratore** dispone di queste proprietà.



| Proprietà                                                     | Descrizione                                                                                    |
|:-------------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [**AtEndOfStream**](enumerator-atendofstream.md)<br/> | Ottiene un valore booleano che indica se sono presenti più elementi nella raccolta.<br/> |
| [**Errore**](enumerator-error.md)<br/>                 | Ottiene una rappresentazione XML di informazioni aggiuntive sull'errore.<br/>                         |



 

## <a name="remarks"></a>Commenti

Per avviare un'enumerazione, utilizzare [**Session. enumerate**](session-enumerate.md). Per eseguire un'operazione [*WS-Enumeration:*](windows-remote-management-glossary.md)[*pull*](windows-remote-management-glossary.md) che continua a leggere gli elementi nell'enumerazione, usare [**Enumerator. ReadItem**](enumerator-readitem.md).

L'oggetto **enumeratore** corrisponde all'interfaccia [**IWSManEnumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator) .

## <a name="examples"></a>Esempio

Nell'esempio di codice VBScript seguente vengono enumerati tutti i dischi in un computer remoto specificato dal nome di dominio completo (servername.domain.com). La subroutine DiplayOutput formatta l'output dei dati in modo analogo allo strumento WinRM. cmd.


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
| Intestazione<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[API di scripting WinRM](winrm-scripting-api.md)
</dt> <dt>

[Enumerazione o elenco di tutte le istanze di una risorsa](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> <dt>

[Creazione di script in Gestione remota Windows](scripting-in-windows-remote-management.md)
</dt> </dl>

 

 





