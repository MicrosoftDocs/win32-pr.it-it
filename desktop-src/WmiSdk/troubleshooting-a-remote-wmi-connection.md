---
description: Nelle sezioni seguenti vengono descritti i problemi comuni che gli sviluppatori possono avere con la creazione di una connessione WMI remota.
ms.assetid: 328e420b-a859-4ce9-8a31-67150eb0a78f
ms.tgt_platform: multiple
title: Risoluzione dei problemi relativi a una connessione WMI remota
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae475f91836b9e99b1c7faaf149c452e00a66722
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309758"
---
# <a name="troubleshooting-a-remote-wmi-connection"></a>Risoluzione dei problemi relativi a una connessione WMI remota

Nelle sezioni seguenti vengono descritti i problemi comuni che gli sviluppatori possono avere con la creazione di una connessione WMI remota.

Le sezioni seguenti sono illustrate in questo argomento:

-   [Accesso DCOM negato](#dcom-access-denied)
-   [Errore di connessione](#failure-to-connect)
-   [Timeout della connessione WMI](#wmi-connection-timed-out)
-   [Argomenti correlati](#related-topics)

## <a name="dcom-access-denied"></a>Accesso DCOM negato

<dl> <dt>

<span id="Symptom"></span><span id="symptom"></span><span id="SYMPTOM"></span>Sintomo
</dt> <dd>

la connessione non è riuscita con l'errore "accesso DCOM negato", insieme al valore decimale-2147024891 o esadecimale value0x80070005.

</dd> <dt>

<span id="Issue"></span><span id="issue"></span><span id="ISSUE"></span>Problema
</dt> <dd>

DCOM potrebbe non essere configurato per consentire una connessione WMI.

</dd> <dt>

<span id="Resolution"></span><span id="resolution"></span><span id="RESOLUTION"></span>Risoluzione
</dt> <dd>

È possibile configurare le impostazioni DCOM per WMI utilizzando l'utilità di configurazione DCOM (**DCOMCnfg.exe**) disponibile in **strumenti di amministrazione** nel **Pannello di controllo**. Questa utilità espone le impostazioni che consentono a determinati utenti di connettersi al computer in modalità remota tramite DCOM. Per impostazione predefinita, i membri del gruppo Administrators possono connettersi in remoto al computer. Con questa utilità è possibile impostare la sicurezza per l'avvio, l'accesso e la configurazione del servizio WMI.

Per ulteriori informazioni, vedere [protezione di una connessione WMI remota](securing-a-remote-wmi-connection.md).

</dd> </dl>

## <a name="failure-to-connect"></a>Errore di connessione

<dl> <dt>

<span id="Symptom"></span><span id="symptom"></span><span id="SYMPTOM"></span>Sintomo
</dt> <dd>

Non è possibile connettersi a WMI in un sistema remoto.

</dd> <dt>

<span id="Issue"></span><span id="issue"></span><span id="ISSUE"></span>Problema
</dt> <dd>

È possibile che si stia tentando di connettersi a un sistema che non supporta WMI. Le seguenti connessioni tra le versioni del sistema operativo non sono supportate:

-   Non è possibile connettersi a un computer che esegue un'edizione iniziale, di base o Home.

In alternativa, è possibile che si stia tentando di connettersi a uno spazio dei nomi che richiede una connessione crittografata, una che richiede un livello di autenticazione `pktPrivacy` , **WbemAuthenticationLevelPktPrivacy** o la **\_ \_ \_ \_ \_ privacy PKT del livello di autenticazione RPC C**.

</dd> <dt>

<span id="Resolution"></span><span id="resolution"></span><span id="RESOLUTION"></span>Risoluzione
</dt> <dd>

Per ulteriori informazioni, vedere [protezione di spazi dei nomi WMI](securing-wmi-namespaces.md), [protezione di client e provider C++](securing-c---clients-and-providers.md)o [impostazione del livello di sicurezza del processo predefinito tramite VBScript](setting-the-default-process-security-level-using-vbscript.md).

</dd> </dl>

## <a name="wmi-connection-timed-out"></a>Timeout della connessione WMI

<dl> <dt>

<span id="Symptom"></span><span id="symptom"></span><span id="SYMPTOM"></span>Sintomo
</dt> <dd>

Si verifica il timeout della connessione WMI.

</dd> <dt>

<span id="Issue"></span><span id="issue"></span><span id="ISSUE"></span>Problema
</dt> <dd>

A causa di problemi di ritardo di rete, il computer non è in grado di rispondere nel tempo.

</dd> <dt>

<span id="Resolution"></span><span id="resolution"></span><span id="RESOLUTION"></span>Risoluzione
</dt> <dd>

Quando si esegue la connessione a WMI tramite una chiamata a [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) o [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver), è possibile impostare il flag **wbemConnectFlagUseMaxWait** (scripting) o il **\_ flag WBEM Connect usare il valore \_ \_ \_ Max \_ wait** in C++ su 128 (0x80) per imporre un intervallo di due (2) minuti per la chiamata.

</dd> </dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Connessione a WMI in un computer remoto](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 



