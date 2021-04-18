---
description: A partire da Windows Server 2008, il provider di funzionalità server fornisce informazioni sulle funzionalità server installate nel server. Questa classe consente agli amministratori di inventariare e gestire i ruoli e le funzionalità del server.
ms.assetid: f7932eaa-6730-4301-9809-32de9c1a20de
ms.tgt_platform: multiple
title: Provider di funzionalità server
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 73666dc810a40f33e3d35acb1b9d7ade5d2b021a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313176"
---
# <a name="server-feature-provider"></a>Provider di funzionalità server

A partire da Windows Server 2008, il provider di funzionalità server fornisce informazioni sulle funzionalità server installate nel server. Questa classe consente agli amministratori di inventariare e gestire i ruoli e le funzionalità del server.

Un ruolo del server è definito come un gruppo di componenti che forniscono funzioni per un'area specifica di funzionalità, ad esempio la stampa, i file, il controllo del dominio e così via. I ruoli del server tipici sono file server, server di posta elettronica, server DNS, controller di dominio, server applicazioni e così via.

Se un'organizzazione non esegue un software di gestione che segnala i ruoli del server, ad esempio Microsoft Operations Manager con i Management Pack installati, è possibile ottenere tali informazioni eseguendo una query sulla classe [**Win32 \_ ServerFeature**](win32-serverfeature.md) . Il ruolo del server e le informazioni sulle funzionalità dei computer remoti sono disponibili tramite le normali connessioni remote WMI o tramite il servizio Gestione remota Windows (WinRM). Per ulteriori informazioni sulle connessioni DCOM remote WMI, vedere [la pagina relativa alla connessione a WMI in un computer remoto](connecting-to-wmi-on-a-remote-computer.md). Per ulteriori informazioni sulle connessioni che utilizzano il protocollo [*WS-Management*](/windows/desktop/WinRM/windows-remote-management-glossary) , vedere [gestione remota Windows](/windows/desktop/WinRM/portal).

Il provider di funzionalità Server supporta le classi WMI seguenti:

-   [**\_ServerFeature Win32**](win32-serverfeature.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Provider WMI](wmi-providers.md)
</dt> </dl>

 

 
