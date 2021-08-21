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
ms.openlocfilehash: b97ee9d0f2f407c0cae2c9c1466a1904cf79eaecb353b94ac11bb3373367ed2f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050249"
---
# <a name="setting-up-a-fixed-port-for-wmi"></a>Configurazione di una porta fissa per WMI

WMI viene eseguito come parte di un host del servizio condiviso con porte assegnate tramite DCOM per impostazione predefinita. Tuttavia, è possibile configurare il servizio WMI per l'esecuzione come unico processo in un host separato e specificare una porta fissa.

La procedura seguente è un'installazione automatica per consentire a WMI di avere una porta fissa. La procedura usa lo strumento da riga di comando [**winmgmt.**](winmgmt.md)

**Per configurare una porta fissa per WMI**

1.  Al prompt dei comandi digitare **winmgmt -standalonehost**
2.  Arrestare il servizio WMI digitando il comando **net stop "Windows Management Instrumentation"** o usare il nome breve **di net stop winmgmt**
3.  Riavviare di nuovo il servizio WMI in un nuovo host del servizio digitando **net start "Windows Management Instrumentation"** o **net start winmgmt**
4.  Stabilire un nuovo numero di porta per il servizio WMI digitando **netsh firewall add portapening TCP 24158 WMIFixedPort**

Per annullare le modifiche apportate a WMI, digitare **winmgmt /sharedhost**, quindi arrestare e riavviare il servizio winmgmt.

## <a name="examples"></a>Esempio

Per uno script che configura una porta fissa per WMI, vedere l'esempio di codice di Scripting Gallery [seguente.](https://Gallery.TechNet.Microsoft.Com/Set-WmiSinglePortps1-20fa8389 )

o un esempio di codice di PowerShell che abilita o disabilita le impostazioni della porta WMI, vedere l'esempio [Set-WmiSinglePort](https://Gallery.TechNet.Microsoft.Com/Set-WmiSinglePortps1-20fa8389) in TechNet Gallery.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Connessione a WMI in un computer remoto](connecting-to-wmi-on-a-remote-computer.md)
</dt> <dt>

[Risoluzione dei problemi relativi a connessioni WMI remote](connecting-to-wmi-remotely-starting-with-vista.md)
</dt> <dt>

[Hosting e sicurezza dei provider](provider-hosting-and-security.md)
</dt> </dl>

 

 



