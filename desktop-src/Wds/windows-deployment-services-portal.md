---
title: Servizi di distribuzione Windows
description: Distribuire Windows sistemi operativi. Configurare nuovi client con un'installazione basata sulla rete senza che gli amministratori visitino ogni computer o installino direttamente da supporti CD o DVD.
ms.assetid: 790abc27-03cc-4f93-bf04-a4eb37e614bb
keywords:
- Windows Servizi di Windows distribuzione
- Windows Servizi di Windows distribuzione , home page
- servizi di distribuzione Windows Deployment Services
- WDS Windows Deployment Services Vedere Windows Deployment Services
- Servizi di installazione remota Windows di distribuzione Vedere Windows Deployment Services
- RIS Windows Deployment Services Vedere Windows Deployment Services
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 100483541420015ed84a95543f2f94bafb2d509d44e6b321b53729caa94588cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999511"
---
# <a name="windows-deployment-services"></a>Servizi di distribuzione Windows

## <a name="purpose"></a>Scopo

Windows Servizi di distribuzione è la versione aggiornata di Servizi di installazione remota (RIS). WDS consente la distribuzione di Windows operativi. È possibile usare WdS per configurare nuovi client con un'installazione basata sulla rete senza che gli amministratori visitino ogni computer o installino direttamente da supporti CD o DVD.

## <a name="developer-audience"></a>Sviluppatori

Il principale gruppo di sviluppatori dell'API WDS è per i gruppi che sviluppano strumenti e processi personalizzati per l'IT e altri gruppi di amministrazione di computer. Negli ambienti in cui non è possibile usare la soluzione WdS (Windows Deployment Services) standard, l'API WDS consente l'accesso a livello di codice ad alcuni componenti wds.

Original Equipment Manufacturers (OEM), system builder e professionisti IT aziendali che cercano informazioni su come distribuire Windows in nuovi computer, dovrebbero vedere le informazioni sulla soluzione standard di Servizi di distribuzione Windows (WDS) nella guida dettagliata all'aggiornamento di [Windows Deployment Services](/previous-versions/windows/it-pro/windows-vista/cc766320(v=ws.10)) e Windows [Automated Installation Kit (WAIK).](https://www.microsoft.com/download/details.aspx?id=10333)

## <a name="run-time-requirements"></a>Requisiti di runtime

WDS è disponibile come componente aggiuntivo per Windows Server 2003 con Service Pack 1 (SP1) ed è incluso nel sistema operativo a partire da Windows Server 2003 con Service Pack 2 (SP2) e Windows Server 2008. L'API server WDS PXE richiede il ruolo del server WDS nel server per implementare provider PXE personalizzati. L'API client WDS richiede la fase di Windows di preinstallazione di Microsoft Windows PE 2.0. Immagine di avvio RAMDISK Windows PE 2.0 in . Il formato WIM deve essere scaricato come parte del processo di avvio di rete per implementare client WDS personalizzati.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                 | Descrizione                                                                    |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Informazioni sull'API Windows Deployment Services](about-the-windows-deployment-services-api.md)<br/> | Informazioni generali sull'API del server WDS e sull'API client wds.<br/>    |
| [Windows Informazioni di riferimento su Servizi di distribuzione](windows-deployment-services-reference.md)<br/>         | Vengono descritte le Windows e le strutture di Servizi di distribuzione.<br/> |



 

 

