---
title: Servizi di distribuzione Windows
description: Distribuire i sistemi operativi Windows. Configurare nuovi client con un'installazione basata sulla rete senza richiedere agli amministratori di visitare ogni computer o di installarli direttamente da supporti CD o DVD.
ms.assetid: 790abc27-03cc-4f93-bf04-a4eb37e614bb
keywords:
- Servizi di distribuzione Windows servizi di distribuzione Windows
- Servizi di distribuzione Windows servizi di distribuzione Windows, home page
- Servizi di distribuzione Windows servizi di distribuzione
- Servizi di distribuzione Windows WDS vedere Servizi di distribuzione Windows
- Servizi di installazione remota servizi di distribuzione Windows vedere Servizi di distribuzione Windows
- Servizi di distribuzione Windows RIS vedere Servizi di distribuzione Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b35bebb000b383552f12d259ca17552165e9247f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300358"
---
# <a name="windows-deployment-services"></a>Servizi di distribuzione Windows

## <a name="purpose"></a>Scopo

Servizi di distribuzione Windows (WDS) è la versione aggiornata di servizi di installazione remota (RIS). WDS consente la distribuzione dei sistemi operativi Windows. È possibile utilizzare WDS per configurare nuovi client con un'installazione basata su rete senza richiedere agli amministratori di visitare ogni computer o di installare direttamente da supporti CD o DVD.

## <a name="developer-audience"></a>Sviluppatori

Il principale pubblico per gli sviluppatori dell'API WDS è costituito dai gruppi che sviluppano strumenti e processi personalizzati per l'IT e altri gruppi di amministrazione del computer. Negli ambienti in cui non è possibile usare la soluzione standard di servizi di distribuzione Windows (WDS), l'API WDS consente l'accesso programmatico ad alcuni componenti di WDS.

Original Equipment Manufacturer (OEM), System Builder e professionisti IT aziendali che cercano informazioni su come distribuire Windows in nuovi computer, dovrebbero visualizzare le informazioni sulla soluzione Servizi di distribuzione Windows (WDS) standard nella [Guida dettagliata all'aggiornamento di servizi di distribuzione Windows](/previous-versions/windows/it-pro/windows-vista/cc766320(v=ws.10)) e [Windows Automated Installation Kit (WAIK)](https://www.microsoft.com/download/details.aspx?id=10333).

## <a name="run-time-requirements"></a>Requisiti di runtime

WDS è disponibile come componente aggiuntivo per Windows Server 2003 con Service Pack 1 (SP1) ed è incluso nel sistema operativo a partire da Windows Server 2003 con Service Pack 2 (SP2) e Windows Server 2008. L'API del server PXE WDS richiede il ruolo server WDS nel server per implementare i provider PXE personalizzati. Per l'API client WDS è necessaria la fase di elaborazione del programma di installazione di Microsoft Ambiente preinstallazione di Windows (Windows PE 2,0). Immagine di avvio RAMDISK di Windows PE 2,0 in. Per implementare client WDS personalizzati, è necessario scaricare il formato WIM come parte del processo di avvio di rete.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                 | Descrizione                                                                    |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Informazioni sull'API di servizi di distribuzione Windows](about-the-windows-deployment-services-api.md)<br/> | Informazioni generali sull'API del server WDS e sull'API client WDS.<br/>    |
| [Guida di riferimento a servizi di distribuzione Windows](windows-deployment-services-reference.md)<br/>         | Vengono descritte le funzioni e le strutture di servizi di distribuzione Windows.<br/> |



 

 

