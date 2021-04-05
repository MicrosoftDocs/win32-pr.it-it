---
title: Metodo Session. enumerate (WSManDisp. h)
description: Enumera una tabella, una raccolta dati o una risorsa di log.
ms.assetid: ed8ad3ad-d033-45cb-b681-995c5f73b12e
ms.tgt_platform: multiple
keywords:
- Enumera il metodo Gestione remota Windows
- Enumerazione Gestione remota Windows metodo, oggetto Session
- Gestione remota Windows oggetto sessione, metodo enumerate
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
ms.openlocfilehash: ca6b66b910251c641832cde3ddd93d6479f66be7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048135"
---
# <a name="sessionenumerate-method"></a>Metodo Session. enumerate

Enumera una tabella, una raccolta dati o una risorsa di log. Per creare una query, includere un parametro di *filtro* e un parametro *dialetto* in un'enumerazione. È anche possibile usare un oggetto [**resourceLocator**](resourcelocator.md) per creare query. Per ulteriori informazioni, vedere [enumerazione o visualizzazione di un elenco di tutte le istanze di una risorsa](enumerating-or-listing-all-instances-of-a-resource.md).

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

*resourceUri* \[ in\]
</dt> <dd>

Identificatore della risorsa da recuperare.

Questo parametro può contenere uno dei seguenti elementi:

-   URI della risorsa.

    ```VB
    strResourceUri = "http://schemas.microsoft.com/" _ 
        & "wbem/wsman/1/wmi/root/cimv2/Win32_Service"
    ```

    

-   Oggetto [**resourceLocator**](resourcelocator.md) .
-   Riferimento all'endpoint di [*WS-Addressing*](windows-remote-management-glossary.md) come descritto nello standard del protocollo WS-Management. Per ulteriori informazioni sulla specifica pubblica per [protocollo WS-Management](ws-management-protocol.md), vedere la [pagina](/previous-versions/dotnet/articles/ms951267(v=msdn.10))relativa all'indice delle specifiche di gestione.

</dd> <dt>

*filtro* \[ di in, facoltativo\]
</dt> <dd>

Filtro che definisce quali elementi della risorsa vengono restituiti dall'enumerazione. Quando la risorsa viene enumerata, vengono restituiti solo gli elementi che corrispondono ai criteri di filtro. L'inclusione di un parametro di *filtro* e di un parametro *dialetto* in un'enumerazione converte l'enumerazione in una query. Per un esempio, vedere [esecuzione di query per istanze specifiche di una risorsa](querying-for-specific-instances-of-a-resource.md).

Se si dispone di un oggetto [**resourceLocator**](resourcelocator.md) per il parametro *resourceUri* , questo parametro non deve essere utilizzato.

</dd> <dt>

*dialetto* \[ in, facoltativo\]
</dt> <dd>

Lingua utilizzata dal filtro. [WQL](/windows/desktop/WmiSdk/wql-sql-for-wmi), un subset di SQL utilizzato da WMI, è l'unico linguaggio supportato.

Se si dispone di un oggetto [**resourceLocator**](resourcelocator.md) per il parametro *resourceUri* , questo parametro non deve essere utilizzato.

</dd> <dt>

*flag* \[ in, facoltativo\]
</dt> <dd>

Parametro che deve contenere un flag nell'enumerazione **\_ \_ WSManEnumFlags** . Per altre informazioni, vedere [costanti di enumerazione](enumeration-constants.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Oggetto [**enumeratore**](enumerator.md) che contiene i risultati dell'enumerazione.

## <a name="remarks"></a>Commenti

Per ulteriori informazioni sulla limitazione delle chiamate di rete durante un'enumerazione, vedere la proprietà [**BatchItems**](session-batchitems.md) .

Tenere presente che se i flag includono le [**costanti di enumerazione**](enumeration-constants.md) **WSManFlagHierarchyDeepBasePropsOnly** o **WSManFlagHierarchyShallow** , gestione remota Windows servizio restituisce il codice di errore **errore \_ WSMan modalità di \_ polimorfismo non \_ \_ supportata**.

Se viene specificato un filtro, è necessario che sia un documento valido rispetto allo schema della risorsa. Il parametro Dialect è facoltativo. Tuttavia, se la stringa di filtro inizia con <, ma non è un frammento XML, includere il parametro *dialect* o impostare il flag **WSManFlagNonXmlText** nel parametro *Flags* . Per altre informazioni, vedere [**costanti di enumerazione**](enumeration-constants.md).

Il metodo C++ corrispondente è [**IWSManSession:: enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).

## <a name="examples"></a>Esempio

Nell'esempio di codice VBScript riportato di seguito vengono enumerate le istanze [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) in un computer remoto specificato dal nome di dominio completo (servername.Domain.com). Tenere presente che liberare l'oggetto di enumerazione Cancella le richieste di enumerazione in sospeso. La subroutine DiplayOutput usa il file di trasformazione XML dello strumento da riga di comando WinRM (WsmTxt. Xsl) per restituire i dati in formato tabulare.


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
| Intestazione<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
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

 

