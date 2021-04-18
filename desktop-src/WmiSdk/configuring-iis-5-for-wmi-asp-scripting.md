---
description: Tutte le impostazioni di autenticazione vengono eseguite tramite il Gestione servizi Internet.
ms.assetid: 9b118120-f0cb-4973-b537-dd3d12a7a6d5
ms.tgt_platform: multiple
title: Configurazione di IIS 5,0 e versioni successive per lo scripting ASP WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff4b5ddde139b3eef32fd7c80f4cca4e10fd816a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310414"
---
# <a name="configuring-iis-50-and-later-for-wmi-asp-scripting"></a>Configurazione di IIS 5,0 e versioni successive per lo scripting ASP WMI

Tutte le impostazioni di autenticazione vengono eseguite tramite il Gestione servizi Internet.

Quando si configurano Internet Information Server (IIS) 5,0 e IIS 6,0 Security per gli script ASP WMI, tenere presenti i seguenti problemi:

-   [Livello di autenticazione](#authentication-level)

    È possibile configurare a livello di server, di directory o di file.

-   [Impostazione di autenticazione](#authentication-setting)

    È possibile impostare l'autenticazione su finestre anonime, integrate o entrambe.

-   [Protezione](#protection)

    È possibile impostare l'ASP per l'esecuzione in-process (protezione ridotta) o out-of-process usando Dllhost.exe (media o High Protection).

## <a name="authentication-level"></a>Livello di autenticazione

Per una maggiore sicurezza, è possibile configurare l'autenticazione a livello di directory o di file.

Se l'autenticazione viene impostata a livello di server, tutte le directory e i file successivi rispettano l'autenticazione del server, a meno che non vengano modificati in modo esplicito a livello di directory o di file. È possibile creare una struttura di directory che contenga tutti gli script ASP WMI in cui le pagine HTML e gli ASP specifici di WMI possono essere configurati in modo indipendente dal resto del server. Eseguire la procedura seguente per modificare il livello di autenticazione di un server, di una directory o di un file.

**Per impostare l'autenticazione a qualsiasi livello**

1.  Nel pannello di controllo fare doppio clic su **strumenti di amministrazione**, quindi fare doppio clic sullo snap-in IIS.

2.  Individuare l'icona pagina ASP, quindi aprire le proprietà del livello da impostare, che può essere server, directory o file.

    > [!Note]  
    > Le impostazioni di autenticazione si trovano nella scheda **sicurezza directory** o **sicurezza file** della finestra delle **proprietà**.

     

## <a name="authentication-setting"></a>Impostazione di autenticazione

Per gli script ASP WMI, la combinazione di autenticazione anonima disattivata (deselezionata) e l'autenticazione integrata di Windows attivata (selezionata) offre maggiore opportunità di impostare la sicurezza. Per utilizzare le impostazioni di autenticazione IIS NT (NTLM), Passport o digest, è necessario attivare i privilegi di abilitazione remota, perché l'utente viene considerato come un'identità di rete e registrato in modalità remota. L'impostazione Abilita remoto non è necessaria per l'autenticazione anonima e di base. Tuttavia, il sistema è molto meno sicuro quando si usa l'autenticazione anonima e di base.

Se l'autenticazione anonima viene utilizzata con o senza l'autenticazione integrata di Windows, l'approccio più sicuro consiste nell'utilizzare un accesso che richiede all'utente di immettere un nome utente e una password. L'account di accesso predefinito è l'identità IIS, ma è possibile creare un accesso utilizzando autorizzazioni specifiche appropriate per gli script ASP WMI che possono essere utilizzati come account per le connessioni anonime o Guest.

Se si sceglie un identificatore di accesso che non è un'identità IIS, deselezionare la casella **di controllo Consenti a IIS di controllare la password** e immettere la password corretta. Questa operazione impone a tutte le connessioni anonime o Guest di utilizzare l'identificatore di accesso. Creando un accesso separato dall'identità IIS, è possibile controllare i privilegi di un account che accede a WMI senza influire sulle altre directory o sui file nel server IIS, a meno che l'autenticazione non sia impostata a livello di server.

Eseguire la procedura seguente per impostare i requisiti di autenticazione per la pagina ASP tramite lo snap-in IIS nel pannello di controllo.

**Per ottenere l'impostazione dell'account**

1.  Nel pannello di controllo fare doppio clic sull'icona **strumenti di amministrazione** , aprire lo snap-in IIS, individuare la pagina ASP e aprire le proprietà del livello da impostare, che può essere server, directory o file.

    È possibile trovare le impostazioni di autenticazione nella scheda **sicurezza directory** o **sicurezza file** della finestra delle **proprietà** .

2.  Nell'area autenticazione anonima fare clic su **modifica**.

3.  Se è selezionato un identificatore di accesso diverso dall'identità IIS, deselezionare la casella **di controllo Consenti a IIS di controllare la password** e immettere la password corretta. Questa operazione impone a tutte le connessioni anonime o Guest di utilizzare l'identificatore di accesso.

Utilizzando un accesso diverso dall'identità IIS, i privilegi dell'account che accede a WMI possono essere controllati senza influire sulle altre directory o sui file nel server IIS, a meno che l'autenticazione non sia impostata a livello di server.

La configurazione precedente consente al server IIS di usare l'autenticazione anonima in alcune aree, oltre a Windows integrata o all'autenticazione mista in altri.

## <a name="protection"></a>Protezione

L'ultima considerazione per la configurazione del server IIS è la protezione da utilizzare durante l'esecuzione di un'applicazione ASP.

È possibile impostare un ASP per eseguire le operazioni seguenti:

-   In-process per IIS (bassa protezione).

-   Da esterno a IIS con Dllhost.exe in pool o out-of-process (protezione da pool).

-   Self-of-process-host (protezione elevata).

> [!Note]  
> Per il migliore equilibrio tra sicurezza e prestazioni, utilizzare l'host in pool.

 

 

 



