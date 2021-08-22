---
title: Esecuzione di query per istanze specifiche di una risorsa
description: La chiamata a Session.Enumerate ha parametri facoltativi che restringeno l'enumerazione in una query.
ms.assetid: 69d2fe79-9aad-4c8c-a65e-c6bb0e51c063
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f757b6392ec26f809004d599f6c5603629d23e8eb7a7f4b08a4f3a4ef18791a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119642851"
---
# <a name="querying-for-specific-instances-of-a-resource"></a>Esecuzione di query per istanze specifiche di una risorsa

La chiamata a [**Session.Enumerate ha**](session-enumerate.md) parametri facoltativi che restringeno l'enumerazione in una query. Poiché l'API di [scripting WinRM](winrm-scripting-api.md) e l'API [C++ WinRM](winrm-c---api.md) sono strettamente modellate sul protocollo WS-Management sottostante, i parametri usano la stessa terminologia per l'esecuzione di query del *protocollo,* ovvero il filtro e il dialetto di filtro *.*

È possibile usare i parametri di filtro e dialetto di [**Session.Enumerate**](session-enumerate.md) oppure è possibile costruire e fornire un oggetto [**ResourceLocator**](resourcelocator.md) e il metodo [**AddSelector,**](resourcelocator-addselector.md) ma non è possibile eseguire entrambe le operazioni.

Questa procedura esegue una query per le schede di rete che hanno TCP/IP associato e abilitato. La query richiede tutte le istanze di [**Win32 \_ NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration) con la **proprietà IpEnabled** impostata su **True.** Ad eccezione dell'aggiunta del *filtro e* del *dialetto*, la query viene gestita come una semplice enumerazione.

In questo esempio il nome della risorsa per la costante Resource è rappresentato da un asterisco " " perché il nome della \* [**classe, Win32 \_ NetworkAdapterConfiguration,**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration)è già indicato nella stringa *strFilter.*

**Per eseguire una query per istanze specifiche di una risorsa**

1.  Per semplificare la lettura, definire gli URI come costanti.

    ```VB
    Const RemoteComputer = "servername.domain.com"
    Const Resource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/*"
    Const Dialect = "http://schemas.microsoft.com/wbem/wsman/1/WQL"
    ```

    

2.  Crea una sessione.

    ```VB
    Set objWsman = CreateObject("Wsman.Automation")
    Set objSession = objWsman.CreateSession("https://" & RemoteComputer)
    ```

    

3.  Costruire la stringa di filtro. Windows Gestione remota supporta [WQL](/windows/desktop/WmiSdk/wql-sql-for-wmi) come dialetto di filtro.

    ```VB
    strFilter = "SELECT * FROM Win32_NetworkAdapterConfiguration WHERE IpEnabled=TRUE"
    ```

    

4.  Impostare le costanti [**di enumerazione necessarie**](enumeration-constants.md) nel parametro *flags.*

    Tenere presente che se [](enumeration-constants.md) i flag includono le costanti di enumerazione **WSManFlagHierarchyDeepBasePropsOnly** o **WSManFlagHierarchyShallow,** il servizio WinRM restituisce il codice di errore **ERROR \_ WSMAN \_ POLYMORPHISM \_ MODE \_ UNSUPPORTED**.

5.  Chiamare il [**metodo Session.Enumerate.**](session-enumerate.md) Questa chiamata avvia un'enumerazione. Il **metodo Session.Enumerate** stabilisce un contesto WS-Management di enumerazione del protocollo, mantenuto nell'oggetto [**Enumerator.**](enumerator.md)

    ```VB
    Set objResultSet = objSession.Enumerate(Resource, strFilter, Dialect)
    ```

    

6.  Chiamare il [**metodo Enumerator.ReadItem**](enumerator-readitem.md) per ottenere l'elemento successivo dei risultati. In WS-Management protocollo corrisponde all'operazione pull. Usare il [**metodo Enumerator.AtEndOfStream**](enumerator-atendofstream.md) come controllo per sapere quando interrompere la lettura.

    ```VB
    While Not objResultSet.AtEndOfStream
        DisplayOutput(objResultSet.ReadItem)
    Wend
    ```

    

Nell'esempio di codice VBScript seguente viene illustrato lo script completo.


```VB
Const RemoteComputer = "servername.domain.com"
Const Resource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/*"
Const Dialect = "http://schemas.microsoft.com/wbem/wsman/1/WQL"

Set objWsman = CreateObject("Wsman.Automation")
Set objSession = objWsman.CreateSession("https://" & RemoteComputer)

strFilter = "SELECT * FROM Win32_NetworkAdapterConfiguration WHERE IpEnabled=TRUE"

Set objResultSet = objSession.Enumerate(Resource, strFilter, Dialect)

While Not objResultSet.AtEndOfStream
    DisplayOutput(objResultSet.ReadItem)
Wend

'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************
Sub DisplayOutput(strWinRMXml)
    Dim xmlFile, xslFile
    Set xmlFile = CreateObject("MSXml2.DOMDocument.3.0") 
    Set xslFile = CreateObject("MSXml2.DOMDocument.3.0")
    xmlFile.LoadXml(strWinRMXml)
    xslFile.Load("WsmTxt.xsl")
    Wscript.Echo xmlFile.TransformNode(xslFile) 
End Sub
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso Windows gestione remota](using-windows-remote-management.md)
</dt> <dt>

[Enumerazione o elenco di tutte le istanze di una risorsa](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> <dt>

[**ResourceLocator**](resourcelocator.md)
</dt> </dl>

 

 