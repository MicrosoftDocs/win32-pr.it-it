---
title: Rilevamento dell'eventuale supporto di WS-Management protocollo da un computer remoto
description: È possibile utilizzare i metodi Session. identifi o IWSManSession. identifi per determinare se il computer remoto dispone di un servizio che supporta il protocollo WS-Management.
ms.assetid: 4d11ac02-fa8b-45d7-bceb-a18f561bc928
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af82284b38b2a101c767766d44eb975ff7e1dadc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298309"
---
# <a name="detecting-whether-a-remote-computer-supports-ws-management-protocol"></a>Rilevamento dell'eventuale supporto di WS-Management protocollo da un computer remoto

È possibile utilizzare i metodi [**Session. identifi**](session-identify.md) o [**IWSManSession. identifi**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-identify) per determinare se il computer remoto dispone di un servizio che supporta il protocollo WS-Management.

Se nel computer remoto è configurato un servizio di WS-Management protocollo ed è in attesa di richieste, il servizio può rilevare una richiesta di identificazione in base al codice XML seguente nell'intestazione.


```XML
xmlns:wsmid="https://schemas.dmtf.org/wbem/wsman/identity/1/wsmanidentity"
```



Il servizio del protocollo WS-Management che riceve la richiesta restituisce le informazioni contenute nell'elenco seguente nel corpo del messaggio:

-   Versione del protocollo WS-Management. Ad esempio, "https://schemas.dmtf.org/wbem/wsman/1/wsman".
-   Il fornitore del prodotto, ad esempio, "Microsoft Corporation".
-   Versione del prodotto. Se la richiesta viene inviata con **WSManFlagUseNoAuthentication** nel parametro *Flags* , non vengono restituite informazioni sulla versione del prodotto. Se la richiesta viene inviata con l'autenticazione predefinita attiva o con un'altra modalità di autenticazione specificata, è possibile che vengano restituite le informazioni sulla versione del prodotto.

La richiesta di rilevare se il computer remoto dispone di un servizio di protocollo configurato e in ascolto WS-Management può essere eseguito all'inizio di uno script con altre operazioni. In questo modo si verificherà che il computer o i computer di destinazione possano rispondere a ulteriori WS-Management richieste di protocollo. La verifica può essere eseguita anche in uno script separato.

**Per rilevare un servizio del protocollo di WS-Management**

1.  Creare un oggetto [**WSMan**](wsman.md) .

    ```VB
    Set objWsman = CreateObject("Wsman.Automation")
    ```

    

2.  Determinare se la richiesta deve essere inviata autenticata o non autenticata e impostare di conseguenza il parametro dei *flag* nella chiamata a [**WSMan. CreateSession**](wsman-createsession.md).

    ```VB
    set objSession = objWsman.CreateSession("Remote1", _
       objWsman.SessionFlagUseNoAuthentication)
    ```

    

3.  Chiamare [**Session. identifi**](session-identify.md).

    ```VB
    objSession.Identify
    ```

    

## <a name="examples"></a>Esempio

L'esempio di codice VBScript seguente invia una richiesta di identificazione non autenticata al computer remoto denominato "REMOTE1" nello stesso dominio.


```VB
set objWsman = CreateObject("Wsman.Automation")
set objSession = objWsman.CreateSession("Remote1", _
  objWsman.SessionFlagUseNoAuthentication)
WScript.Echo objSession.Identify
```



Nella risposta seguente viene illustrato il codice XML restituito dal computer remoto. La versione del protocollo WS-Management (" https://schemas.dmtf.org/wbem/wsman/1/wsman.xsd ") e il fornitore del sistema operativo ("Microsoft Corporation") vengono specificati nel codice XML restituito. Poiché il messaggio viene inviato senza autenticazione, la versione del prodotto non viene restituita dal servizio Gestione remota Windows.


```XML
<wsmid:IdentifyResponse xmlns:wsmid=
    "https://schemas.dmtf.org/wbem/wsman/identity/1/wsmanidentity.xsd">
<wsmid:ProtocolVersion>https://schemas.dmtf.org/wbem/wsman/1/wsman.xsd
    </wsmid:ProtocolVersion>
<wsmid:ProductVendor>Microsoft Corporation</wsmid:ProductVendor>
<wsmid:ProductVersion>OS: 0.0.0 SP: 0.0 Stack:1.0</wsmid:ProductVersion>
</wsmid:IdentifyResponse>
```



Nell'esempio di codice VBScript seguente viene inviata una richiesta di identificazione autenticata al computer remoto.


```VB
set ObjWSMan = CreateObject("Wsman.Automation")
set objSession = WSMan.CreateSession("Remote1", _
  objWSMan.SessionFlagUseKerberos)
WScript.Echo objSession.Identify
```



Poiché la richiesta è stata inviata con l'autenticazione, vengono restituite le informazioni sulla versione.


```XML
<wsmid:IdentifyResponse xmlns:wsmid=
    "https://schemas.dmtf.org/wbem/wsman/identity/1/wsmanidentity.xsd">
<wsmid:ProtocolVersion>https://schemas.dmtf.org/wbem/wsman/1/wsman.xsd
    </wsmid:ProtocolVersion>
<wsmid:ProductVendor>Microsoft Corporation</wsmid:ProductVendor>
<wsmid:ProductVersion>OS: 6.0.5384 SP: 0.0 Stack:1.0</wsmid:ProductVersion>
</wsmid:IdentifyResponse>
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su Gestione remota Windows](about-windows-remote-management.md)
</dt> <dt>

[Utilizzo di Gestione remota Windows](using-windows-remote-management.md)
</dt> <dt>

[Riferimento Gestione remota Windows](windows-remote-management-reference.md)
</dt> </dl>

 

 




