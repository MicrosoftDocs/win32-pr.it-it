---
title: Metodo Session.Enumerate (WSManDisp.h)
description: Enumera una tabella, una raccolta dati o una risorsa di log.
ms.assetid: ed8ad3ad-d033-45cb-b681-995c5f73b12e
ms.tgt_platform: multiple
keywords:
- Enumerare il metodo Windows gestione remota
- Enumerare il metodo Windows gestione remota , oggetto Session
- Metodo Di enumerazione Windows oggetto Sessione di Gestione remota
topic_type:
- apiref
api_name:
- Session.Enumerate
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dc40a45cc28179acd8e5dc9fff17df8b8accddd8dffda3ea299571e11d46564
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119642631"
---
# <a name="sessionenumerate-method"></a>Metodo Session.Enumerate

Enumera una tabella, una raccolta dati o una risorsa di log. Per creare una query, includere un *parametro di filtro* e un parametro *dialetto* in un'enumerazione. È anche possibile usare un [**oggetto ResourceLocator**](resourcelocator.md) per creare query. Per altre informazioni, vedere [Enumerazione o elenco di tutte le istanze di una risorsa](enumerating-or-listing-all-instances-of-a-resource.md).

## <a name="syntax"></a>Sintassi


```VB
Session.Enumerate( _
  ByVal resourceUri, _
  [ ByVal filter ], _
  [ ByVal dialect ], _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*resourceUri* \[ Pollici\]
</dt> <dd>

Identificatore della risorsa da recuperare.

Questo parametro può contenere uno degli elementi seguenti:

-   URI della risorsa.

    ```VB
    strResourceUri = "http://schemas.microsoft.com/" _ 
        & "wbem/wsman/1/wmi/root/cimv2/Win32_Service"
    ```

    

-   Oggetto [**ResourceLocator.**](resourcelocator.md)
-   Informazioni [*di riferimento sull'endpoint WS-Addressing,*](windows-remote-management-glossary.md) come descritto nello standard WS-Management protocollo. Per altre informazioni sulla specifica pubblica per protocollo WS-Management [,](ws-management-protocol.md)vedere [Pagina dell'indice](/previous-versions/dotnet/articles/ms951267(v=msdn.10))delle specifiche di gestione .

</dd> <dt>

*filtro* \[ in, facoltativo\]
</dt> <dd>

Filtro che definisce gli elementi della risorsa restituiti dall'enumerazione . Quando la risorsa viene enumerata, vengono restituiti solo gli elementi che corrispondono ai criteri di filtro. *L'inclusione di un* parametro di filtro e di un parametro *dialetto* in un'enumerazione converte l'enumerazione in una query. Per un esempio, vedere [Esecuzione di query per istanze specifiche di una risorsa](querying-for-specific-instances-of-a-resource.md).

Se si dispone di [**un oggetto ResourceLocator**](resourcelocator.md) per il *parametro resourceURI,* questo parametro non deve essere usato.

</dd> <dt>

*dialetto* \[ in, facoltativo\]
</dt> <dd>

Lingua utilizzata dal filtro. [WQL,](/windows/desktop/WmiSdk/wql-sql-for-wmi)un subset di SQL usato da WMI, è l'unico linguaggio supportato.

Se si dispone di [**un oggetto ResourceLocator**](resourcelocator.md) per il *parametro resourceURI,* questo parametro non deve essere usato.

</dd> <dt>

*flag* \[ in, facoltativo\]
</dt> <dd>

Parametro che deve contenere un flag **\_ \_ nell'enumerazione WSManEnumFlags.** Per altre informazioni, vedere [Costanti di enumerazione](enumeration-constants.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Oggetto [**Enumerator**](enumerator.md) che contiene i risultati dell'enumerazione .

## <a name="remarks"></a>Commenti

Per altre informazioni sulla limitazione delle chiamate di rete durante un'enumerazione, vedere la [**proprietà BatchItems.**](session-batchitems.md)

Tenere presente che se [](enumeration-constants.md) i flag includono le costanti di enumerazione **WSManFlagHierarchyDeepBasePropsOnly** o **WSManFlagHierarchyShallow,** il servizio di gestione remota Windows restituisce il codice di errore **ERROR \_ WSMAN \_ POLYMORPHISM \_ MODE \_ UNSUPPORTED**.

Se viene specificato un filtro, deve essere un documento valido rispetto allo schema della risorsa. Il parametro dialetto è facoltativo. Tuttavia, se la stringa di filtro inizia con <, ma non è un frammento XML, includere il parametro *dialetto* o impostare il flag **WSManFlagNonXmlText** nel parametro *flags.* Per altre informazioni, vedere [**Costanti di enumerazione**](enumeration-constants.md).

Il metodo C++ corrispondente è [**IWSManSession::Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).

## <a name="examples"></a>Esempio

Nell'esempio di codice VBScript seguente vengono enumerate le istanze [**\_ di LogicalDisk Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) in un computer remoto specificato dal nome di dominio completo (servername.domain.com). Tenere presente che la liberatura dell'oggetto di enumerazione cancella le richieste di enumerazione in sospeso. La subroutine DisplayOutput usa il file di trasformazione XML dello strumento da riga di comando Winrm (WsmTxt.xsl) per l'output dei dati in formato tabulare.


```VB
Const RemoteComputer = "servername.domain.com"
Set objWsman = CreateObject( "WSMan.Automation" )

Set objSession = objWsman.CreateSession( "https://" & REMOTECOMPUTER )

strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
              "wmi/root/cimv2/Win32_LogicalDisk"

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

[**Sessione**](session.md)
</dt> <dt>

[Esecuzione di query per istanze specifiche di una risorsa](querying-for-specific-instances-of-a-resource.md)
</dt> <dt>

[**BatchItems**](session-batchitems.md)
</dt> <dt>

[**ResourceLocator**](resourcelocator.md)
</dt> </dl>

 

