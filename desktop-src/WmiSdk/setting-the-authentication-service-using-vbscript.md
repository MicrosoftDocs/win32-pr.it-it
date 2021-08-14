---
description: Quando si accede a un server Windows Management Instrumentation (WMI) con uno script, è possibile scegliere tra i protocolli di autenticazione NT LAN Manager (NTLM) o Kerberos.
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
ms.openlocfilehash: 837a69df251b5bbb6cc8bef5ac0b882349fde74646ac6ed33149978b8f69ad7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118315388"
---
# <a name="setting-the-authentication-service-using-vbscript"></a>Impostazione del servizio di autenticazione tramite VBScript

Quando si accede a un server Windows Management Instrumentation (WMI) con uno script, è possibile scegliere tra i protocolli di autenticazione NT LAN Manager (NTLM) o Kerberos. La specifica di Kerberos non è necessaria se non quando si usa la delega. Per altre informazioni, vedere [Connessione a una terza delega computer.](connecting-to-a-3rd-computer-delegation.md)

Poiché le versioni del sistema operativo differiscono per il servizio di autenticazione che usano, è consigliabile non specificare un valore per il campo autorità durante la connessione a un sistema remoto. Consentire invece al sistema operativo e alla versione distribuita di Component Object Model (DCOM) di selezionare NTLM o Kerberos. Se viene specificato un servizio di autenticazione, la sintassi richiede il nome dell'entità server, ovvero il nome del computer di destinazione anziché il controller di dominio.

È possibile usare il parametro authority solo con connessioni a server WMI remoti. Il tentativo di connessione ha esito negativo se si tenta di impostare i livelli di autorizzazione come parte di un moniker o con una chiamata a [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) per una connessione locale.

Eseguire la procedura seguente per specificare il servizio di autenticazione che si vuole usare nel *parametro strAuthority* del metodo [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) o della connessione della stringa [del moniker.](constructing-a-moniker-string.md)

**Per specificare l'autenticazione NTLM o Kerberos con l'API di scripting per WMI**

1.  Se il *parametro strAuthority* inizia con la stringa "kerberos:", WMI presuppone che la stringa faccia riferimento a un nome dell'entità Kerberos e che sia usata l'autenticazione Kerberos. Se il *parametro strAuthority* inizia con la stringa "ntlmdomain:", WMI usa invece l'autenticazione NTLM.
2.  In alternativa, è possibile usare la parte autorità di un moniker per specificare il tipo di autenticazione usato per connettersi a WMI. Per usare l'autenticazione Kerberos quando si usa un moniker, includere la stringa "authority=kerberos:" seguita dal nome dell'entità. Per usare l'autenticazione NTLM, includere la stringa "authority=ntlmdomain:" seguita dal nome di dominio NTLM.

    L'esempio seguente illustra un moniker che richiede l'autenticazione Kerberos usando l'entità "server \\ mydomain".

    ```VB
    winmgmts:{impersonationLevel=delegate, _
            authority=kerberos:mydomain\server} _
            !//myserver/root/default:__cimomidentification=@
    ```

    

    L'esempio seguente mostra invece un moniker che richiede l'autenticazione NTLM usando il dominio "mydomain".

    ```VB
    winmgmts:{impersonationLevel=impersonate, _
            authority=ntlmdomain:mydomain} _
            !//myserver/root/default:__cimomidentification=@
    ```

    

 

 



