---
description: Quando si accede a un server di Strumentazione gestione Windows (WMI) con uno script, è possibile scegliere tra i protocolli di autenticazione NT LAN Manager (NTLM) o Kerberos.
ms.assetid: db2dc750-bfdd-4f6c-859b-e104814f0800
ms.tgt_platform: multiple
title: Impostazione del servizio di autenticazione tramite VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bd2cf444560aac7ebce96b52d9abaa528bdcaa76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318523"
---
# <a name="setting-the-authentication-service-using-vbscript"></a>Impostazione del servizio di autenticazione tramite VBScript

Quando si accede a un server di Strumentazione gestione Windows (WMI) con uno script, è possibile scegliere tra i protocolli di autenticazione NT LAN Manager (NTLM) o Kerberos. Non è necessario specificare Kerberos tranne quando si usa la delega. Per ulteriori informazioni, vedere [la pagina relativa alla connessione a una terza delega del computer](connecting-to-a-3rd-computer-delegation.md).

Poiché le versioni del sistema operativo sono diverse da quelle usate dal servizio di autenticazione, è consigliabile non specificare un valore per il campo Authority quando ci si connette a un sistema remoto. Al contrario, consentire al sistema operativo e alla versione distribuita di Component Object Model (DCOM) di selezionare NTLM o Kerberos. Se viene specificato un servizio di autenticazione, la sintassi richiede il nome dell'entità server, ovvero il nome del computer di destinazione invece del controller di dominio.

È possibile utilizzare il parametro Authority solo con connessioni a server WMI remoti. Il tentativo di connessione non riesce se si tenta di impostare i livelli di autorizzazione come parte di un moniker o con una chiamata a [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) per una connessione locale.

Eseguire la procedura seguente per specificare il servizio di autenticazione che si desidera utilizzare nel parametro *strAuthority* del metodo [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) o la connessione alla stringa del [moniker](constructing-a-moniker-string.md) .

**Per specificare l'autenticazione NTLM o Kerberos con l'API di scripting per WMI**

1.  Se il parametro *strAuthority* inizia con la stringa "Kerberos:", WMI presuppone che la stringa faccia riferimento a un nome di entità Kerberos e venga utilizzata l'autenticazione Kerberos. Se il parametro *strAuthority* inizia con la stringa "ntlmdomain:", WMI utilizza invece l'autenticazione NTLM.
2.  In alternativa, è possibile utilizzare la parte autorità di un moniker per specificare il tipo di autenticazione utilizzato per la connessione a WMI. Per utilizzare l'autenticazione Kerberos quando si utilizza un moniker, includere la stringa "Authority = Kerberos:" seguita dal nome dell'entità. Per utilizzare l'autenticazione NTLM, includere la stringa "Authority = ntlmdomain:" seguita dal nome di dominio NTLM.

    Nell'esempio seguente viene illustrato un moniker che richiede l'autenticazione Kerberos utilizzando l'entità "dominio \\ Server".

    ```VB
    winmgmts:{impersonationLevel=delegate, _
            authority=kerberos:mydomain\server} _
            !//myserver/root/default:__cimomidentification=@
    ```

    

    Al contrario, nell'esempio seguente viene illustrato un moniker che richiede l'autenticazione NTLM utilizzando il dominio "dominio".

    ```VB
    winmgmts:{impersonationLevel=impersonate, _
            authority=ntlmdomain:mydomain} _
            !//myserver/root/default:__cimomidentification=@
    ```

    

 

 



