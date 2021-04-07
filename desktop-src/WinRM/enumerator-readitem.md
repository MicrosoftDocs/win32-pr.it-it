---
title: Metodo Enumerator. ReadItem (WSManDisp. h)
description: Recupera un elemento dalla risorsa e restituisce una rappresentazione XML dell'elemento.
ms.assetid: 4280ecb8-2449-41bd-868a-785e8ac3b3d5
ms.tgt_platform: multiple
keywords:
- Gestione remota Windows del metodo ReadItem
- Metodo ReadItem Gestione remota Windows, oggetto Enumerator
- Enumeratore Gestione remota Windows oggetto, metodo ReadItem
topic_type:
- apiref
api_name:
- Enumerator.ReadItem
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7fda1b31cbc14d4a7474d4de55b572df82a8aaf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048136"
---
# <a name="enumeratorreaditem-method"></a>Enumerator. ReadItem, metodo

Recupera un elemento dalla risorsa e restituisce una rappresentazione XML dell'elemento.

## <a name="syntax"></a>Sintassi


```VB
Enumerator.ReadItem( _
  ByVal resource _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*risorse* 
</dt> <dd>

URI dell'elemento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Rappresentazione XML dell'elemento.

## <a name="remarks"></a>Commenti

Per limitare il numero di elementi letti, impostare la proprietà [**Session.BatchItems**](session-batchitems.md) .

Si noti che la liberazione dell'oggetto di enumerazione pulisce tutte le richieste di enumerazione in sospeso.

Il metodo [**Session. enumerate**](session-enumerate.md) non ottiene una raccolta nello stesso modo in cui una [query WMI](/windows/desktop/WmiSdk/querying-wmi), ad esempio `SELECT * from Win32_LogicalDisk` , restituisce una raccolta in un [**SWbemObjectSet**](/windows/desktop/WmiSdk/swbemobjectset). Per leggere un file come flusso di testo, creare l'oggetto scripting [TextStream](/previous-versions//312a5kbt(v=vs.85)) e chiamare il metodo [TextStream. ReadLine](/previous-versions//h7se9d4f(v=vs.85)) per leggere ogni riga del file. In modo analogo, si chiama il metodo **Session. enumerate** per ottenere un oggetto [**enumeratore**](enumerator.md) e quindi si chiama il metodo **Enumerator. ReadItem** . Come per la lettura dal file di testo, è possibile controllare la proprietà [**Enumerator. AtEndOfStream**](enumerator-atendofstream.md) per verificare se è stata raggiunta la fine degli elementi di dati.

## <a name="examples"></a>Esempio

Nell'esempio VBScript seguente viene chiamato il metodo [**Session. enumerate**](session-enumerate.md) per ottenere un elenco di processi pianificati. La subroutine DiplayOutput usa il file di trasformazione XML dello strumento da riga di comando WinRM (WsmTxt. Xsl) per restituire i dati in formato tabulare.


```VB
Const RemoteComputer = "servername.domain.com"

Set objWsman = CreateObject( "WSMan.Automation" )
Set objSession = objWsman.CreateSession( "https://" & RemoteComputer )

strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
              "wmi/root/cimv2/Win32_ScheduledJob"

Set objResultSet = objSession.Enumerate( strResource )
NumOfJobs = 0

While Not objResultSet.AtEndOfStream
    NumOfJobs = NumOfJobs + 1
    DisplayOutput( objResultSet.ReadItem ) 
Wend

Wscript.Echo "There are " & NumOfJobs & " jobs scheduled."

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

[**Enumeratore**](enumerator.md)
</dt> <dt>

[Enumerazione o elenco di tutte le istanze di una risorsa](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> </dl>

 

