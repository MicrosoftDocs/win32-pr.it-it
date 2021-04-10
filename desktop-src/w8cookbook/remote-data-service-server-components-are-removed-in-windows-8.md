---
title: Servizio dati remoto rimosso
description: I componenti server di Remote Data Service sono stati rimossi in Windows 8
ms.assetid: 53ECB92C-8868-4A1A-82BD-4ADE75F7BB59
keywords:
- Server RDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b6588b029fe37f1312c709be168fd695bdc5738
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2020
ms.locfileid: "103963525"
---
# <a name="remote-data-service-server-components-are-removed-in-windows-8"></a>I componenti server di Remote Data Service sono stati rimossi in Windows 8

## <a name="platforms"></a>Piattaforme

 **Client** -Windows 8  
**Server** -Windows Server 2012  



## <a name="description"></a>Descrizione

Il server servizio dati remoto (RDS) non è disponibile in Windows 8:

-   File msadcf.dll, che ospita l'oggetto business "RDSServer. DataFactory" predefinito, viene rimosso e i file associati (msadcfr.dll, msadcfr.dll. mui, handler. reg e handsafe. reg) vengono rimossi
-   File msdfmap.dll, che è il gestore predefinito, viene rimosso e il file msdfmap.ini viene rimosso
-   File msadcs.dll, ISAPI, rimosso

## <a name="manifestation"></a>Manifestazione

I clienti non possono ospitare un server RDS in Windows 8.

## <a name="mitigation"></a>Strategia di riduzione del rischio

I clienti possono gestire il server RDS in un computer con Windows 7 o altri sistemi operativi di livello inferiore.

## <a name="solution"></a>Soluzione

I clienti possono gestire il server RDS in un computer con Windows 7 o altri sistemi operativi di livello inferiore.

## <a name="resources"></a>Risorse

[Guida di orientamento alle tecnologie di accesso ai dati](/sql/connect/connect-history?view=sqlallproducts-allversions)

 

 