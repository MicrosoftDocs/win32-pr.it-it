---
description: WMI viene eseguito come parte di un host del servizio condiviso con porte assegnate tramite DCOM per impostazione predefinita. Tuttavia, è possibile configurare il servizio WMI per l'esecuzione come unico processo in un host separato e specificare una porta fissa.
ms.assetid: 62908445-2a43-4a20-a998-e497c6ecf48e
ms.tgt_platform: multiple
title: Configurazione di una porta fissa per WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 49c6d6b0bf42951766cfd813ccb4b5eed041600a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318517"
---
# <a name="setting-up-a-fixed-port-for-wmi"></a>Configurazione di una porta fissa per WMI

WMI viene eseguito come parte di un host del servizio condiviso con porte assegnate tramite DCOM per impostazione predefinita. Tuttavia, è possibile configurare il servizio WMI per l'esecuzione come unico processo in un host separato e specificare una porta fissa.

La procedura seguente è un'installazione automatica per consentire a WMI di avere una porta fissa. Nella procedura viene utilizzato lo strumento da riga di comando [**WinMgmt**](winmgmt.md) .

**Per configurare una porta fissa per WMI**

1.  Al prompt dei comandi digitare **winmgmt-standalonehost**
2.  Arrestare il servizio WMI digitando il comando **net stop "Strumentazione gestione Windows"** oppure utilizzare il nome breve di **net stop winmgmt**
3.  Riavviare nuovamente il servizio WMI in un nuovo host del servizio digitando **net start "Strumentazione gestione Windows"** o **net start WinMgmt**
4.  Stabilire un nuovo numero di porta per il servizio WMI digitando **netsh firewall add apertura TCP 24158 WMIFixedPort**

Per annullare le modifiche apportate a WMI, digitare **WinMgmt/sharedhost**, quindi arrestare e avviare di nuovo il servizio Winmgmt.

## <a name="examples"></a>Esempio

Per uno script che configura una porta fissa per WMI, vedere il seguente [esempio di codice](https://Gallery.TechNet.Microsoft.Com/Set-WmiSinglePortps1-20fa8389 )della raccolta di script.

in alternativa, un esempio di codice PowerShell che Abilita o Disabilita le impostazioni della porta WMI, vedere l'esempio [set-WmiSinglePort](https://Gallery.TechNet.Microsoft.Com/Set-WmiSinglePortps1-20fa8389) nella raccolta TechNet.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Connessione a WMI in un computer remoto](connecting-to-wmi-on-a-remote-computer.md)
</dt> <dt>

[Risoluzione dei problemi relativi a connessioni WMI remote](connecting-to-wmi-remotely-starting-with-vista.md)
</dt> <dt>

[Hosting e sicurezza del provider](provider-hosting-and-security.md)
</dt> </dl>

 

 



