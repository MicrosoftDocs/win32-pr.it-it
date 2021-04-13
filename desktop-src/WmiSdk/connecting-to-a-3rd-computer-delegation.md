---
description: Quando si esegue uno script in un sistema locale che ottiene dati da un sistema remoto, WMI fornisce le credenziali al provider dei dati nel sistema remoto.
ms.assetid: e27ff207-b067-47df-9706-e8af51646d28
ms.tgt_platform: multiple
title: Delega con WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e8a624f3d437d977ff73b3854a59cfd634350e7
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104401832"
---
# <a name="delegating-with-wmi"></a>Delega con WMI

Quando si esegue uno script in un sistema locale che ottiene dati da un sistema remoto, WMI fornisce le credenziali al provider dei dati nel sistema remoto. È necessario solo un livello di **rappresentazione, perché** è necessario solo un hop di rete. Tuttavia, se lo script si connette a WMI nel sistema remoto e tenta di aprire un file di log in un sistema remoto aggiuntivo, lo script avrà esito negativo a meno che il livello di rappresentazione non sia **delegato**. Il livello di rappresentazione del **delegato** è necessario per qualsiasi operazione che implica più di un hop di rete. Per ulteriori informazioni sulla sicurezza DCOM in WMI, vedere [impostazione della sicurezza del processo dell'applicazione client](setting-client-application-process-security.md). Per ulteriori informazioni su una connessione hop a una rete tra due computer, vedere la pagina [relativa alla connessione a WMI in un computer remoto](connecting-to-wmi-on-a-remote-computer.md).

**Per utilizzare la delega per connettersi a un computer tramite un altro computer**

1.  Abilitare la delega in Active Directory (**Active Directory utenti e computer** nel **Pannello di controllo** **attività amministrative**) sul controller di dominio. L'account nel sistema remoto deve essere contrassegnato come **trusted per la delega** e l'account nel sistema locale non deve essere contrassegnato come l' **account è sensibile e non può essere delegato**. il sistema locale, il sistema remoto e il controller di dominio devono essere membri dello stesso dominio o in domini trusted.

    **Nota**  L'uso della delega costituisce un rischio per la sicurezza perché fornisce ai processi esterni al controllo diretto la possibilità di usare le credenziali.

2.  Modificare il codice nel modo seguente per indicare che si desidera utilizzare la delega.

    <dl> <dt>

    <span id="PowerShell"></span><span id="powershell"></span><span id="POWERSHELL"></span>PowerShell
    </dt> <dd>

    Impostare il parametro *-Impersonation* sul cmdlet WMI per **delegare**.

    </dd> <dt>

    <span id="VBScript"></span><span id="vbscript"></span><span id="VBSCRIPT"></span>VBScript
    </dt> <dd>

    Impostare il parametro *ImpersonationLevel* su **delegate** nella chiamata a [SWbemLocator. ConnectServer](swbemlocator-connectserver.md) o a **delegate** nella stringa del [moniker](constructing-a-moniker-string.md) . È anche possibile impostare la rappresentazione in un oggetto [**SWbemSecurity**](swbemsecurity.md).

    </dd> <dt>

    <span id="C__"></span><span id="c__"></span>C++
    </dt> <dd>

    Impostare il parametro del livello di rappresentazione sul **\_ delegato RPC C \_ Imp \_ level \_** nella chiamata a [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) o [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket). Per ulteriori informazioni su quando effettuare queste chiamate, vedere [inizializzazione di com per un'applicazione WMI](initializing-com-for-a-wmi-application.md).

    Per passare l'identità del client ai server COM remoti in C++, impostare il mascheramento nella chiamata a [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket). Per altre informazioni, vedere [mascheramento](../com/cloaking.md).

    </dd> </dl>

## <a name="examples"></a>Esempio

Nell'esempio di codice seguente viene illustrata una stringa del moniker che imposta la rappresentazione da **delegare**. Tenere presente che l'autorità deve essere impostata su Kerberos.


```vb
set objWMIServices = Getobject("winmgmts:{impersonationLevel=Delegate,authority=kerberos:MyDomain\Computer_B}!\\ComputerB\Root\CIMv2")
```



Nell'esempio di codice seguente viene illustrato come impostare la rappresentazione su **delegate** (valore 4) utilizzando [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md).


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

 

 
