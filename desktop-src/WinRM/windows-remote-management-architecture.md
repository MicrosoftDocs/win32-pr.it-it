---
title: Windows Architettura di gestione remota
description: L Windows di gestione remota è costituita da componenti nei computer client e server.
ms.assetid: 82e67851-fe46-4bb0-8278-9718b5e0c7ae
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 889a823c4c67bed29f9ce695d84c893654b541aed76e0c79860e31f24c543662
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121596"
---
# <a name="windows-remote-management-architecture"></a>Windows Architettura di gestione remota

L Windows di gestione remota è costituita da componenti nei computer client e server. Nella figura seguente vengono illustrati i componenti in entrambi i computer, il modo in cui i componenti interagiscono con altri componenti e il protocollo utilizzato per comunicare tra i computer.

![Architettura di winrm](images/winrm-architecture.png)

## <a name="requesting-client"></a>Richiesta del client

I componenti WinRM seguenti si trovano nel computer che esegue lo script che richiede i dati.

-   Applicazione WinRM

    Si tratta dello script o dello strumento da riga di comando **Winrm** che usa l'API di scripting WinRM per effettuare chiamate per richiedere dati o eseguire metodi. Per altre informazioni, vedere [l'API di scripting WinRM.](winrm-scripting-api.md)

-   WSMAuto.dll

    Livello di automazione che fornisce supporto per gli script.

-   WsmCL.dll

    Livello API C all'interno del sistema operativo.

-   API HTTP

    WinRM richiede il supporto per il trasporto HTTP e HTTPS.

## <a name="responding-server"></a>Server di risposta

I componenti winrm seguenti si trovano nel computer che risponde.

-   API HTTP

    WinRM richiede il supporto per il trasporto HTTP e HTTPS.

-   WSMAuto.dll

    Livello di automazione che fornisce supporto per gli script.

-   WsmCL.dll

    Livello API C all'interno del sistema operativo.

-   WsmSvc.dll

    Servizio [*listener WinRM.*](windows-remote-management-glossary.md)

-   WsmProv.dll

    Sottosistema provider.

-   WsmRes.dll

    File di risorse.

-   WsmWmiPl.dll

    [*Plug-in WMI*](windows-remote-management-glossary.md). In questo modo è possibile ottenere dati WMI tramite WinRM.

-   Driver IPMI (Intelligent Platform Management Interface) e provider IPMI WMI

    Questi componenti forniscono tutti i dati hardware richiesti usando le classi IPMI. Per altre informazioni, vedere [Provider IPMI.](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) L'hardware BMC deve essere stato rilevato da SMBIOS o dal dispositivo creato manualmente caricando il driver. Per altre informazioni, vedere [Installation and Configuration for Windows Remote Management](installation-and-configuration-for-windows-remote-management.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni Windows gestione remota](about-windows-remote-management.md)
</dt> </dl>

 

 