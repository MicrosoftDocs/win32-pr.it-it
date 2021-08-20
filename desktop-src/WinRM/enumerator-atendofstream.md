---
title: Proprietà Enumerator.AtEndOfStream (WSManDisp.h)
description: Ottiene un valore booleano che indica se sono presenti altri elementi nell'insieme.
ms.assetid: 5e80674a-7889-4753-b0dd-4d7b44eba00a
ms.tgt_platform: multiple
keywords:
- Proprietà AtEndOfStream Windows gestione remota
- Proprietà AtEndOfStream Windows, oggetto Enumeratore di Gestione remota
- Oggetto Enumerator Windows gestione remota, proprietà AtEndOfStream
topic_type:
- apiref
api_name:
- Enumerator.AtEndOfStream
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1077837f82d650b57dfea0316ef15094b18749eefdb6957e62e6afd92cfe672
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118113202"
---
# <a name="enumeratoratendofstream-property"></a>Enumerator.AtEndOfStream - proprietà

Ottiene un valore booleano che indica se sono presenti altri elementi nell'insieme.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```VB
Enumerator.AtEndOfStream As BOOLEAN
```



## <a name="property-value"></a>Valore proprietà

<dt>

<span id="True"></span><span id="true"></span><span id="TRUE"></span>

<span id="True"></span><span id="true"></span><span id="TRUE"></span>**Vero**


</dt> <dd>

Nella raccolta non sono presenti altri elementi.

</dd> <dt>

<span id="False"></span><span id="false"></span><span id="FALSE"></span>

<span id="False"></span><span id="false"></span><span id="FALSE"></span>**False**


</dt> <dd>

Sono disponibili altri elementi.

</dd> </dl>

## <a name="remarks"></a>Commenti

Se si libera [**l'oggetto Enumerator**](enumerator.md) dopo aver ottenuto tutti i dati necessari, le eventuali richieste di enumerazione in sospeso vengono rimosse. Per altre informazioni, vedere [Enumerazione o elenco di tutte le istanze di una risorsa.](enumerating-or-listing-all-instances-of-a-resource.md)

## <a name="examples"></a>Esempio

Nell'esempio di VBScript seguente vengono enumerate le istanze del sistema operativo. Si noti che la rimozione dell'oggetto enumerazione elimina tutte le richieste di enumerazione in sospeso. La subroutine DisplayOutput formatta l'output dei dati nello stesso modo dello strumento WinRM.cmd.


```VB
Const RemoteComputer = "servername.domain.com"

Set objWsman = CreateObject( "WSMan.Automation" )
Set objSession = objWsman.CreateSession( "https://" & _
    RemoteComputer )

strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
    "wmi/root/cimv2/Win32_OperatingSystem"

Set objResultSet = objSession.Enumerate( strResource )

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

[**Enumeratore**](enumerator.md)
</dt> <dt>

[Enumerazione o elenco di tutte le istanze di una risorsa](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> </dl>

 

 





