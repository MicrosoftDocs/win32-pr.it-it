---
description: Quando si esegue uno script in un sistema locale che ottiene dati da un sistema remoto, WMI fornisce le credenziali al provider dei dati nel sistema remoto.
ms.assetid: e27ff207-b067-47df-9706-e8af51646d28
ms.tgt_platform: multiple
title: Delega con WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca844363816e7800aa8b293b86b1b5fe14a7d145773d209da53ebaba4e119abf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118109156"
---
# <a name="delegating-with-wmi"></a>Delega con WMI

Quando si esegue uno script in un sistema locale che ottiene dati da un sistema remoto, WMI fornisce le credenziali al provider dei dati nel sistema remoto. Ciò richiede solo un livello di rappresentazione **impersonate**, perché è necessario un solo hop di rete. Tuttavia, se lo script si connette a WMI nel sistema remoto e tenta di aprire un file di log in un sistema remoto aggiuntivo, lo script ha esito negativo a meno che il livello di rappresentazione non sia **Delegato**. **Il livello** di rappresentazione delegato è richiesto da qualsiasi operazione che coinvolge più hop di rete. Per altre informazioni sulla sicurezza DCOM in WMI, vedere Impostazione della sicurezza del [processo dell'applicazione client](setting-client-application-process-security.md). Per altre informazioni su una connessione hop a una rete tra due computer, vedere [Connessione a WMI in un computer remoto](connecting-to-wmi-on-a-remote-computer.md).

**Per usare la delega per connettersi a un computer tramite un altro computer**

1.  Abilitare la delega in Active Directory (**Utenti e computer di Active Directory** in **Pannello di controllo** **attività amministrative**) nel controller di dominio. L'account nel sistema remoto  deve essere contrassegnato come Trusted per la delega e l'account nel sistema locale non deve essere contrassegnato come Account sensibile e non può **essere delegato**. il sistema locale, il sistema remoto e il controller di dominio devono essere membri dello stesso dominio o in domini trusted.

    **Nota**  L'uso della delega è un rischio per la sicurezza perché offre ai processi esterni al controllo diretto la possibilità di usare le credenziali.

2.  Modificare il codice nel modo seguente per indicare che si vuole usare la delega.

    <dl> <dt>

    <span id="PowerShell"></span><span id="powershell"></span><span id="POWERSHELL"></span>Powershell
    </dt> <dd>

    Impostare il *parametro -Impersonation* nel cmdlet WMI su **Delegate**.

    </dd> <dt>

    <span id="VBScript"></span><span id="vbscript"></span><span id="VBSCRIPT"></span>Vbscript
    </dt> <dd>

    Impostare il *parametro impersonationLevel* su **Delegate** nella chiamata a [SWbemLocator.ConnectServer](swbemlocator-connectserver.md) **o Delegate** nella stringa [del moniker.](constructing-a-moniker-string.md) È anche possibile impostare la rappresentazione in un [**oggetto SWbemSecurity.**](swbemsecurity.md)

    </dd> <dt>

    <span id="C__"></span><span id="c__"></span>C++
    </dt> <dd>

    Impostare il parametro del livello di rappresentazione su **RPC C IMP LEVEL \_ \_ \_ \_ DELEGATE** nella chiamata a [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) o [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket). Per altre informazioni su quando effettuare queste chiamate, vedere [Inizializzazione di COM per un'applicazione WMI](initializing-com-for-a-wmi-application.md).

    Per passare l'identità client ai server COM remoti in C++, impostare cloaking nella chiamata a [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket). Per altre informazioni, vedere [Cloaking](../com/cloaking.md).

    </dd> </dl>

## <a name="examples"></a>Esempio

Nell'esempio di codice seguente viene illustrata una stringa del moniker che imposta la rappresentazione su **Delegate**. Tenere presente che l'autorità deve essere impostata su Kerberos.


```vb
set objWMIServices = Getobject("winmgmts:{impersonationLevel=Delegate,authority=kerberos:MyDomain\Computer_B}!\\ComputerB\Root\CIMv2")
```



Nell'esempio di codice seguente viene illustrato come impostare la rappresentazione su **Delegate** (valore 4) usando [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md).


```vb
Set objLocator = CreateObject("WbemScripting.SWbemLocator")
Set objWMIService = objLocator.ConnectServer(Computer_B, _
                                             "Root\CIMv2", _
                                             AdminAccount, _
                                             MyPassword, _
                                             "kerberos:Domain\Computer_B")
objWMIService.Security_.ImpersonationLevel = 4
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Protezione di una connessione WMI remota](securing-a-remote-wmi-connection.md)
</dt> <dt>

[Creazione di processi in modalità remota con WMI](creating-processes-remotely.md)
</dt> </dl>

 

 
