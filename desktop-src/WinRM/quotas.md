---
title: Gestione delle quote per le shell remote
description: La gestione delle quote consente agli utenti di gestire le risorse di sistema in modo più efficiente.
ms.assetid: 6651a500-a95a-45a1-b46a-27b2e9b36a1c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f8cfa177d6f09552238471ff29d81d0ac0b7351
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883220"
---
# <a name="quota-management-for-remote-shells"></a>Gestione delle quote per le shell remote

La gestione delle quote consente agli utenti di gestire le risorse di sistema in modo più efficiente. Windows Gestione remota Windows (WinRM) ha aggiunto un set specifico di quote che offrono una migliore qualità del servizio, consentono di evitare problemi denial of service e allocano le risorse del server agli utenti simultanei. Il set di quote winrm si basa sull'infrastruttura di quota implementata per il servizio Internet Information Services (IIS).

L'implementazione delle quote consente di evitare problemi di riduzione delle prestazioni e Denial of Service eseguendo le operazioni seguenti:

-   Limitazione del numero di shell e processi della shell che un utente può creare
-   Limitazione del numero massimo di utenti simultanei
-   Gestione della quantità di memoria allocata a una shell
-   Impostazione di un timeout per le shell inattive

## <a name="quota-settings"></a>Quota Impostazioni

Per la gestione remota della shell è necessario applicare le quote seguenti. Queste quote possono essere configurate tramite l'utilità winrm o tramite Criteri di gruppo impostazioni. Impostazioni configurate da un Criteri di gruppo le quote impostate dall'utilità winrm. Per altre informazioni sull'impostazione di Criteri di gruppo per Gestione remota Windows, vedere Installazione e configurazione [Windows gestione remota](installation-and-configuration-for-windows-remote-management.md).

<dl> <dt>

<span id="IdleTimeout"></span><span id="idletimeout"></span><span id="IDLETIMEOUT"></span>IdleTimeout
</dt> <dd>

Tempo massimo in millisecondi prima dell'eliminazione di una shell remota inattiva. Il valore predefinito è 180000 millisecondi. Il tempo minimo è 1000 millisecondi.

</dd> <dt>

<span id="MaxProcessesPerShell"></span><span id="maxprocessespershell"></span><span id="MAXPROCESSESPERSHELL"></span>MaxProcessesPerShell
</dt> <dd>

Numero massimo di processi consentiti per shell, inclusi i processi figlio della shell. Il valore predefinito è 25.

</dd> <dt>

<span id="MaxMemoryPerShellMB"></span><span id="maxmemorypershellmb"></span><span id="MAXMEMORYPERSHELLMB"></span>MaxMemoryPerShellMB
</dt> <dd>

Quantità massima di memoria allocata per shell, inclusi i processi figlio della shell. Il valore predefinito è 1024 MB.

> [!Note]  
> Il comportamento non è supportato se MaxMemoryPerShellMB è impostato su un valore minore del valore predefinito.

 

</dd> <dt>

<span id="MaxShellsPerUser"></span><span id="maxshellsperuser"></span><span id="MAXSHELLSPERUSER"></span>MaxShellsPerUser
</dt> <dd>

Numero massimo di shell per utente. Il valore predefinito è 30.

</dd> <dt>

<span id="MaxConcurrentUsers"></span><span id="maxconcurrentusers"></span><span id="MAXCONCURRENTUSERS"></span>MaxConcurrentUsers
</dt> <dd>

Numero massimo di utenti simultanei che possono aprire le shell. Il valore predefinito è 10.

</dd> </dl>

## <a name="deprecated-quotas"></a>Quote deprecate

WinRM 2.0 imposta la quota MaxShellRunTime su sola lettura. La modifica del valore per questa quota non avrà alcun effetto sulle shell remote.

## <a name="retrieving-quota-configuration-information"></a>Recupero delle informazioni di configurazione della quota

Per controllare le impostazioni di configurazione della quota, digitare **winrm get winrm/config**.

Il frammento di codice seguente è un esempio basato su testo di una configurazione winrm con le impostazioni di quota predefinite.

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

Le quote possono essere impostate tramite un'Criteri di gruppo o manualmente. Per altre informazioni sulle impostazioni di configurazione specifiche, vedere [Installation and Configuration for Windows Remote Management](installation-and-configuration-for-windows-remote-management.md).

**Per impostare una quota con Criteri di gruppo**

1.  Aprire una finestra del Prompt dei comandi come amministratore.
2.  Al prompt dei comandi digitare **gpedit.msc**. Verrà **Editor oggetti Criteri di gruppo** finestra di dialogo.
3.  Trovare il **Windows gestione** remota e Windows oggetti **Criteri di gruppo Shell** remota in Configurazione computer Modelli amministrativi **Windows \\ \\ componenti**.
4.  Nella scheda **Esteso** selezionare un'impostazione per visualizzare una descrizione. Fare doppio clic su un'impostazione per modificarla.

**Per impostare manualmente una quota**

1.  Aprire una finestra del Prompt dei comandi come amministratore.
2.  Al prompt dei comandi digitare **winrm set winrm/config/winrs '@{**_&lt; Quota &gt;_*_="_*_&lt; Value &gt;_*_"}'_*

Ad esempio, per aumentare il numero massimo di shell per utente da 5 a 7, digitare **winrm set winrm/config/winrs '@{MaxShellsPerUser="7"}'**.

 

 




