---
title: Architettura Gestione remota Windows
description: L'architettura Gestione remota Windows è costituita da componenti nei computer client e server.
ms.assetid: 82e67851-fe46-4bb0-8278-9718b5e0c7ae
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0f5576913c5e4a1f2a105fb77e2282dc682c6659
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729186"
---
# <a name="windows-remote-management-architecture"></a>Architettura Gestione remota Windows

L'architettura Gestione remota Windows è costituita da componenti nei computer client e server. Nella figura seguente sono illustrati i componenti di entrambi i computer, il modo in cui i componenti interagiscono con altri componenti e il protocollo utilizzato per la comunicazione tra i computer.

![architettura WinRM](images/winrm-architecture.png)

## <a name="requesting-client"></a>Client richiedente

I componenti WinRM seguenti si trovano nel computer in cui è in esecuzione lo script che richiede i dati.

-   Applicazione WinRM

    Questo è lo script o lo strumento da riga di comando **WinRM** che utilizza l'API di scripting WinRM per effettuare chiamate ai dati della richiesta o per eseguire metodi. Per ulteriori informazioni, vedere l' [API di scripting WinRM](winrm-scripting-api.md).

-   WSMAuto.dll

    Livello di automazione che fornisce supporto per gli script.

-   WsmCL.dll

    Livello API C all'interno del sistema operativo.

-   API HTTP

    WinRM richiede il supporto per il trasporto HTTP e HTTPS.

## <a name="responding-server"></a>Server di risposta

I componenti WinRM seguenti risiedono nel computer che risponde.

-   API HTTP

    WinRM richiede il supporto per il trasporto HTTP e HTTPS.

-   WSMAuto.dll

    Livello di automazione che fornisce supporto per gli script.

-   WsmCL.dll

    Livello API C all'interno del sistema operativo.

-   WsmSvc.dll

    Servizio [*listener*](windows-remote-management-glossary.md) WinRM.

-   WsmProv.dll

    Sottosistema del provider.

-   WsmRes.dll

    File di risorse.

-   WsmWmiPl.dll

    [*Plug-in WMI*](windows-remote-management-glossary.md). In questo modo è possibile ottenere dati WMI tramite WinRM.

-   Driver IPMI (Intelligent Platform Management Interface) e provider IPMI WMI

    Questi componenti forniscono tutti i dati hardware richiesti usando le classi IPMI. Per ulteriori informazioni, vedere [provider IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider). L'hardware BMC deve essere stato rilevato da SMBIOS o dal dispositivo creato manualmente mediante il caricamento del driver. Per ulteriori informazioni, vedere [installazione e configurazione per gestione remota Windows](installation-and-configuration-for-windows-remote-management.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su Gestione remota Windows](about-windows-remote-management.md)
</dt> </dl>

 

 