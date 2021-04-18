---
title: Esecuzione di query per istanze specifiche di una risorsa
description: La chiamata a Session. enumerate dispone di parametri facoltativi che limitano l'enumerazione in una query.
ms.assetid: 69d2fe79-9aad-4c8c-a65e-c6bb0e51c063
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 30ae068c712dd04ba892220657ad64820a890040
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299818"
---
# <a name="querying-for-specific-instances-of-a-resource"></a>Esecuzione di query per istanze specifiche di una risorsa

La chiamata a [**Session. enumerate**](session-enumerate.md) dispone di parametri facoltativi che limitano l'enumerazione in una query. Poiché l' [API di scripting WinRM](winrm-scripting-api.md) e l' [API C++ WinRM](winrm-c---api.md) sono strettamente modellate sul protocollo di WS-Management sottostante, i parametri utilizzano la stessa terminologia per l'esecuzione di query come protocollo:*filtro* e *dialetto del filtro*.

È possibile usare i parametri Filter e dialetto di [**Session. enumerate**](session-enumerate.md) oppure è possibile creare e fornire un oggetto [**resourceLocator**](resourcelocator.md) e il metodo [**AddSelector**](resourcelocator-addselector.md) , ma non è possibile eseguire entrambe le operazioni.

Questa procedura consente di eseguire una query per le schede di rete con binding TCP/IP e abilitati. La query richiede tutte le istanze di [**Win32 \_ NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration) con la proprietà **IpEnabled** impostata su **true**. Fatta eccezione per l'aggiunta del *filtro* e del *dialetto*, la query viene gestita come una semplice enumerazione.

In questo esempio, il nome della risorsa per la costante di risorsa è rappresentato da un asterisco " \* " perché il nome della classe, [**Win32 \_ NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration), è già indicato nella stringa *strFilter* .

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

    

3.  Costruire la stringa di filtro. Gestione remota Windows supporta [WQL](/windows/desktop/WmiSdk/wql-sql-for-wmi) come dialetto del filtro.

    ```VB
    strFilter = "SELECT * FROM Win32_NetworkAdapterConfiguration WHERE IpEnabled=TRUE"
    ```

    

4.  Impostare le [**costanti di enumerazione**](enumeration-constants.md) necessarie nel parametro *Flags* .

    Tenere presente che se i flag includono le [**costanti di enumerazione**](enumeration-constants.md) **WSManFlagHierarchyDeepBasePropsOnly** o **WSManFlagHierarchyShallow** , il servizio WinRM restituisce il codice di errore **errore \_ WSMan \_ modalità di polimorfismo non \_ \_ supportata**.

5.  Chiamare il metodo [**Session. enumerate**](session-enumerate.md) . Questa chiamata avvia un'enumerazione. Il metodo **Session. enumerate** stabilisce un contesto di enumerazione del protocollo WS-Management, gestito nell'oggetto [**enumeratore**](enumerator.md) .

    ```VB
    Set objResultSet = objSession.Enumerate(Resource, strFilter, Dialect)
    ```

    

6.  Chiamare il metodo [**Enumerator. ReadItem**](enumerator-readitem.md) per ottenere l'elemento successivo dei risultati. Nel protocollo WS-Management corrisponde all'operazione pull. Usare il metodo [**Enumerator. AtEndOfStream**](enumerator-atendofstream.md) come controllo per capire quando interrompere la lettura.

    ```VB
    While Not objResultSet.AtEndOfStream
        DisplayOutput(objResultSet.ReadItem)
    Wend
    ```

    

Nell'esempio di codice VBScript riportato di seguito viene illustrato lo script completo.


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

[Utilizzo di Gestione remota Windows](using-windows-remote-management.md)
</dt> <dt>

[Enumerazione o elenco di tutte le istanze di una risorsa](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> <dt>

[**ResourceLocator**](resourcelocator.md)
</dt> </dl>

 

 