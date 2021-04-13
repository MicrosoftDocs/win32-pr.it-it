---
title: Gestione delle quote per le shell remote
description: Gestione delle quote consente agli utenti di gestire le risorse di sistema in modo più efficiente.
ms.assetid: 6651a500-a95a-45a1-b46a-27b2e9b36a1c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1310efd37b913ae0bf8394015f6df792711ac6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331759"
---
# <a name="quota-management-for-remote-shells"></a>Gestione delle quote per le shell remote

Gestione delle quote consente agli utenti di gestire le risorse di sistema in modo più efficiente. Gestione remota Windows (WinRM) ha aggiunto un set specifico di quote che forniscono una migliore qualità del servizio, consentono di evitare problemi di tipo Denial of Service e di allocare le risorse del server agli utenti simultanei. Il set di quote WinRM è basato sull'infrastruttura delle quote implementata per il servizio Internet Information Services (IIS).

L'implementazione delle quote consentirà di evitare il calo delle prestazioni e problemi di tipo Denial of Service effettuando le operazioni seguenti:

-   Limitazione del numero di Shell e processi shell che un utente può creare
-   Limitazione del numero massimo di utenti simultanei
-   Gestione della quantità di memoria allocata a una shell
-   Impostazione di un timeout per le shell inattive

## <a name="quota-settings"></a>Impostazioni quota

Per la gestione della shell remota è necessario applicare le quote seguenti. Queste quote possono essere configurate tramite l'utilità WinRM o tramite Criteri di gruppo impostazioni. Le impostazioni configurate da un Criteri di gruppo sostituiscono le quote impostate dall'utilità WinRM. Per ulteriori informazioni sull'impostazione dei criteri di gruppo per WinRM, vedere [installazione e configurazione per gestione remota Windows](installation-and-configuration-for-windows-remote-management.md).

<dl> <dt>

<span id="IdleTimeout"></span><span id="idletimeout"></span><span id="IDLETIMEOUT"></span>IdleTimeout
</dt> <dd>

Tempo massimo, in millisecondi, prima dell'eliminazione di una shell remota inattiva. Il valore predefinito è 180000 millisecondi. Il tempo minimo è pari a 1000 millisecondi.

</dd> <dt>

<span id="MaxProcessesPerShell"></span><span id="maxprocessespershell"></span><span id="MAXPROCESSESPERSHELL"></span>MaxProcessesPerShell
</dt> <dd>

Numero massimo di processi consentiti per Shell, inclusi i processi figlio della shell. Il valore predefinito è 25.

</dd> <dt>

<span id="MaxMemoryPerShellMB"></span><span id="maxmemorypershellmb"></span><span id="MAXMEMORYPERSHELLMB"></span>MaxMemoryPerShellMB
</dt> <dd>

Quantità massima di memoria allocata per Shell, inclusi i processi figlio della shell. Il valore predefinito è 1024 MB.

> [!Note]  
> Il comportamento non è supportato se MaxMemoryPerShellMB è impostato su un valore minore di quello predefinito.

 

</dd> <dt>

<span id="MaxShellsPerUser"></span><span id="maxshellsperuser"></span><span id="MAXSHELLSPERUSER"></span>MaxShellsPerUser
</dt> <dd>

Numero massimo di Shell per utente. Il valore predefinito è 30.

</dd> <dt>

<span id="MaxConcurrentUsers"></span><span id="maxconcurrentusers"></span><span id="MAXCONCURRENTUSERS"></span>MaxConcurrentUsers
</dt> <dd>

Numero massimo di utenti simultanei che possono aprire le shell. Il valore predefinito è 10.

</dd> </dl>

## <a name="deprecated-quotas"></a>Quote deprecate

WinRM 2,0 imposta la quota MaxShellRunTime su sola lettura. La modifica del valore per questa quota non avrà alcun effetto sulle shell remote.

## <a name="retrieving-quota-configuration-information"></a>Recupero delle informazioni di configurazione della quota

Per verificare le impostazioni di configurazione della quota, digitare **WinRM get winrm/config**.

Il frammento di codice seguente è un esempio basato su testo di una configurazione WinRM con le impostazioni di quota predefinite.

``` syntax
Config

          ...         

          Winrs

                   AllowRemoteShellAccess = true

                   IdleTimeout = 7200000

                   MaxConcurrentUsers = 10

                   MaxProcessesPerShell = 25

                   MaxMemoryPerShellMB = 1024

                   MaxShellsPerUser = 30
```

## <a name="configuring-shell-quotas"></a>Configurazione delle quote della shell

Le quote possono essere impostate tramite un'impostazione di Criteri di gruppo o manualmente. Per ulteriori informazioni sulle impostazioni di configurazione specifiche, vedere [installazione e configurazione per gestione remota Windows](installation-and-configuration-for-windows-remote-management.md).

**Per impostare una quota con Criteri di gruppo**

1.  Aprire una finestra del Prompt dei comandi come amministratore.
2.  Al prompt dei comandi digitare **gpedit. msc**. Viene visualizzata la finestra **Editor oggetti Criteri di gruppo** .
3.  Trovare gli oggetti **gestione remota Windows** e **windows Remote Shell** criteri di gruppo (GPO) in **Configurazione computer \\ modelli amministrativi \\ componenti di Windows**.
4.  Nella scheda **esteso** selezionare un'impostazione per visualizzare una descrizione. Fare doppio clic su un'impostazione per modificarla.

**Per impostare una quota manualmente**

1.  Aprire una finestra del Prompt dei comandi come amministratore.
2.  Al prompt dei comandi digitare **winrm set winrm/config/winrs ' @ { ***<Quota>*** = " ***<Value>*** "}'**

Ad esempio, per aumentare il numero massimo di Shell per utente da 5 a 7, digitare **winrm set winrm/config/winrs ' @ {MaxShellsPerUser = "7"}'**.

 

 




