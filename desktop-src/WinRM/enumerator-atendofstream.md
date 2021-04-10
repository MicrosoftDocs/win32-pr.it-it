---
title: Proprietà Enumerator. AtEndOfStream (WSManDisp. h)
description: Ottiene un valore booleano che indica se sono presenti altri elementi nella raccolta.
ms.assetid: 5e80674a-7889-4753-b0dd-4d7b44eba00a
ms.tgt_platform: multiple
keywords:
- Gestione remota Windows proprietà AtEndOfStream
- Gestione remota Windows proprietà AtEndOfStream, oggetto enumeratore
- Enumeratore Gestione remota Windows oggetto, proprietà AtEndOfStream
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
ms.openlocfilehash: 023798f6c868e434218dd1a4dbdf1928bf4526a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119371"
---
# <a name="enumeratoratendofstream-property"></a>Proprietà Enumerator. AtEndOfStream

Ottiene un valore booleano che indica se sono presenti altri elementi nella raccolta.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```VB
Enumerator.AtEndOfStream As BOOLEAN
```



## <a name="property-value"></a>Valore proprietà

<dt>

<span id="True"></span><span id="true"></span><span id="TRUE"></span>

<span id="True"></span><span id="true"></span><span id="TRUE"></span>**True**


</dt> <dd>

Non sono presenti altri elementi nella raccolta.

</dd> <dt>

<span id="False"></span><span id="false"></span><span id="FALSE"></span>

<span id="False"></span><span id="false"></span><span id="FALSE"></span>**False**


</dt> <dd>

Sono disponibili altri elementi.

</dd> </dl>

## <a name="remarks"></a>Commenti

Se si libera l'oggetto [**enumeratore**](enumerator.md) dopo avere ottenuto tutti i dati necessari, eventuali richieste di enumerazione in sospeso verranno rimosse. Per ulteriori informazioni, vedere [enumerazione o visualizzazione di un elenco di tutte le istanze di una risorsa](enumerating-or-listing-all-instances-of-a-resource.md).

## <a name="examples"></a>Esempio

Nell'esempio VBScript seguente vengono enumerate le istanze del sistema operativo. Si noti che la liberazione dell'oggetto di enumerazione pulisce tutte le richieste di enumerazione in sospeso. La subroutine DiplayOutput formatta l'output dei dati in modo analogo allo strumento WinRM. cmd.


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

 

 





