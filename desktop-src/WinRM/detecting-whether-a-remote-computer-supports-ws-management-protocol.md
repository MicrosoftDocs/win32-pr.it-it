---
title: Rilevamento dell'eventuale supporto di un computer WS-Management remoto
description: È possibile usare i metodi Session.Identify o IWSManSession.Identify per determinare se il computer remoto dispone di un servizio che supporta il protocollo WS-Management remoto.
ms.assetid: 4d11ac02-fa8b-45d7-bceb-a18f561bc928
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49a7ebeb25f7f3af69a03c55499dd53a890e540c1a1ed677e7d48e5b11b82b1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119643231"
---
# <a name="detecting-whether-a-remote-computer-supports-ws-management-protocol"></a>Rilevamento dell'eventuale supporto di un computer WS-Management remoto

È possibile usare i [**metodi Session.Identify**](session-identify.md) o [**IWSManSession.Identify**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-identify) per determinare se il computer remoto dispone di un servizio che supporta il protocollo WS-Management remoto.

Se nel computer WS-Management è configurato un servizio del protocollo di configurazione e è in ascolto delle richieste, il servizio può rilevare una richiesta Di identificazione dal codice XML seguente nell'intestazione.


```XML
xmlns:wsmid="https://schemas.dmtf.org/wbem/wsman/identity/1/wsmanidentity"
```



Il WS-Management protocollo che riceve la richiesta restituisce le informazioni contenute nell'elenco seguente nel corpo del messaggio:

-   Versione WS-Management protocollo. Ad esempio, "https://schemas.dmtf.org/wbem/wsman/1/wsman".
-   Il fornitore del prodotto, ad esempio "Microsoft Corporation".
-   Versione del prodotto. Se la richiesta viene inviata con **WSManFlagUseNoAuthentication** nel parametro *flags,* non viene restituita alcuna informazione sulla versione del prodotto. Se la richiesta viene inviata con l'autenticazione predefinita attiva o con un'altra modalità di autenticazione specificata, è possibile restituire le informazioni sulla versione del prodotto.

La richiesta di rilevare se il computer remoto dispone di un servizio protocollo WS-Management configurato e in ascolto può essere eseguito all'inizio di uno script con altre operazioni. In questo modo si verificherà che il computer o i computer di destinazione possano rispondere ad altre richieste WS-Management protocollo. La verifica può essere eseguita anche in uno script separato.

**Per rilevare un WS-Management di protocollo**

1.  Creare un [**oggetto WSMan.**](wsman.md)

    ```VB
    Set objWsman = CreateObject("Wsman.Automation")
    ```

    

2.  Determinare se la richiesta deve essere inviata autenticata o non autenticata e impostare il parametro *flags* di conseguenza nella chiamata a [**WSMan.CreateSession**](wsman-createsession.md).

    ```VB
    set objSession = objWsman.CreateSession("Remote1", _
       objWsman.SessionFlagUseNoAuthentication)
    ```

    

3.  Chiamare [**Session.Identify**](session-identify.md).

    ```VB
    objSession.Identify
    ```

    

## <a name="examples"></a>Esempio

L'esempio di codice VBScript seguente invia una richiesta di identificazione non autenticata al computer remoto denominato "Remote1" nello stesso dominio.


```VB
set objWsman = CreateObject("Wsman.Automation")
set objSession = objWsman.CreateSession("Remote1", _
  objWsman.SessionFlagUseNoAuthentication)
WScript.Echo objSession.Identify
```



La risposta seguente mostra il codice XML restituito dal computer remoto. La WS-Management del protocollo (" ") e il fornitore del sistema operativo https://schemas.dmtf.org/wbem/wsman/1/wsman.xsd ("Microsoft Corporation") vengono specificati nel codice XML restituito. Poiché il messaggio viene inviato non autenticato, la versione del prodotto non viene restituita dal Windows di gestione remota.


```XML
<wsmid:IdentifyResponse xmlns:wsmid=
    "https://schemas.dmtf.org/wbem/wsman/identity/1/wsmanidentity.xsd">
<wsmid:ProtocolVersion>https://schemas.dmtf.org/wbem/wsman/1/wsman.xsd
    </wsmid:ProtocolVersion>
<wsmid:ProductVendor>Microsoft Corporation</wsmid:ProductVendor>
<wsmid:ProductVersion>OS: 0.0.0 SP: 0.0 Stack:1.0</wsmid:ProductVersion>
</wsmid:IdentifyResponse>
```



L'esempio di codice VBScript seguente invia una richiesta Di identificazione autenticata al computer remoto.


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

[Informazioni Windows gestione remota](about-windows-remote-management.md)
</dt> <dt>

[Uso Windows gestione remota](using-windows-remote-management.md)
</dt> <dt>

[Windows Informazioni di riferimento sulla gestione remota](windows-remote-management-reference.md)
</dt> </dl>

 

 




