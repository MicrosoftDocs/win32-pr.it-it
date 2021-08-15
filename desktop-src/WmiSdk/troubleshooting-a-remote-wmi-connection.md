---
description: Le sezioni seguenti descrivono i problemi comuni che gli sviluppatori possono avere con la creazione di una connessione WMI remota.
ms.assetid: 328e420b-a859-4ce9-8a31-67150eb0a78f
ms.tgt_platform: multiple
title: Risoluzione dei problemi relativi a una connessione WMI remota
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10603f713fecf861750d70c4166da91e081dc273a0d6d6134ed916a7f84f2bd4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118312417"
---
# <a name="troubleshooting-a-remote-wmi-connection"></a>Risoluzione dei problemi relativi a una connessione WMI remota

Le sezioni seguenti descrivono i problemi comuni che gli sviluppatori possono avere con la creazione di una connessione WMI remota.

In questo argomento vengono illustrate le sezioni seguenti:

-   [Accesso DCOM negato](#dcom-access-denied)
-   [Mancata Connessione](#failure-to-connect)
-   [Timeout della connessione WMI](#wmi-connection-timed-out)
-   [Argomenti correlati](#related-topics)

## <a name="dcom-access-denied"></a>Accesso DCOM negato

<dl> <dt>

<span id="Symptom"></span><span id="symptom"></span><span id="SYMPTOM"></span>Sintomo
</dt> <dd>

La connessione non è riuscita con l'errore "Accesso DCOM negato", insieme al valore decimale -2147024891 o valore esadecimale0x80070005.

</dd> <dt>

<span id="Issue"></span><span id="issue"></span><span id="ISSUE"></span>Problema
</dt> <dd>

DCOM potrebbe non essere configurato per consentire una connessione WMI.

</dd> <dt>

<span id="Resolution"></span><span id="resolution"></span><span id="RESOLUTION"></span>Risoluzione
</dt> <dd>

È possibile configurare le impostazioni DCOM per WMI usando l'utilità di configurazione DCOM (**DCOMCnfg.exe**) disponibile in **Strumenti** di amministrazione in **Pannello di controllo**. Questa utilità espone le impostazioni che consentono a determinati utenti di connettersi al computer in modalità remota tramite DCOM. Ai membri del gruppo Administrators è consentito connettersi in remoto al computer per impostazione predefinita. Con questa utilità è possibile impostare la sicurezza per avviare, accedere e configurare il servizio WMI.

Per altre informazioni, vedere [Protezione di una connessione WMI remota](securing-a-remote-wmi-connection.md).

</dd> </dl>

## <a name="failure-to-connect"></a>Mancata Connessione

<dl> <dt>

<span id="Symptom"></span><span id="symptom"></span><span id="SYMPTOM"></span>Sintomo
</dt> <dd>

Non è possibile connettersi a WMI in un sistema remoto.

</dd> <dt>

<span id="Issue"></span><span id="issue"></span><span id="ISSUE"></span>Problema
</dt> <dd>

È possibile che si stia tentando di connettersi a un sistema che non supporta WMI. Le connessioni seguenti tra le versioni del sistema operativo non sono supportate:

-   Non è possibile connettersi a un computer che esegue un'edizione Starter, Basic o Home.

In alternativa, è possibile che si stia tentando di connettersi a uno spazio dei nomi che richiede una connessione crittografata, una che richiede un livello di autenticazione `pktPrivacy` , **WbemAuthenticationLevelPktPrivacy** o **RPC C \_ \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY**.

</dd> <dt>

<span id="Resolution"></span><span id="resolution"></span><span id="RESOLUTION"></span>Risoluzione
</dt> <dd>

Per altre informazioni, vedere Protezione degli spazi dei nomi [WMI,](securing-wmi-namespaces.md)Protezione di client e provider [C++](securing-c---clients-and-providers.md)o Impostazione del livello di sicurezza del processo predefinito [tramite VBScript.](setting-the-default-process-security-level-using-vbscript.md)

</dd> </dl>

## <a name="wmi-connection-timed-out"></a>Timeout della connessione WMI

<dl> <dt>

<span id="Symptom"></span><span id="symptom"></span><span id="SYMPTOM"></span>Sintomo
</dt> <dd>

Timeout della connessione WMI.

</dd> <dt>

<span id="Issue"></span><span id="issue"></span><span id="ISSUE"></span>Problema
</dt> <dd>

A causa di problemi di ritardo di rete, il computer semplicemente non è in grado di rispondere in tempo.

</dd> <dt>

<span id="Resolution"></span><span id="resolution"></span><span id="RESOLUTION"></span>Risoluzione
</dt> <dd>

Quando ci si connette a WMI tramite una chiamata a [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) o [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver), è possibile impostare il flag **wbemConnectFlagUseMaxWait** (scripting) o **WBEM \_ FLAG CONNECT USE MAX \_ \_ \_ \_ WAIT** in C++ su 128 (0x80) per imporre un timeout di due (2) minuti sulla chiamata.

</dd> </dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Connessione a WMI in un computer remoto](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 



