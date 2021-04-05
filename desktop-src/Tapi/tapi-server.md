---
description: Il server TAPI (TAPISRV) è il repository centrale dei dati di telefonia in un computer utente.
ms.assetid: 794d230c-abe8-429d-bbf5-91ba364b16ab
title: Server TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 838a6886a5d8e56519f10fc370ed15adc3b1af7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883557"
---
# <a name="tapi-server"></a>Server TAPI

Il server TAPI (TAPISRV) è il repository centrale dei dati di telefonia in un computer utente. Questo processo del servizio tiene traccia delle risorse di telefonia locale e remota, delle applicazioni registrate per gestire le richieste di telefonia assistita e delle funzioni asincrone in sospeso e consente inoltre un'interfaccia coerente con i provider di servizi di telefonia (TSPs). Per ulteriori informazioni e un diagramma che illustra la relazione tra il server TAPI e altri componenti e una panoramica dei relativi ruoli, vedere [Microsoft Telephony Programming Model](microsoft-telephony-programming-model.md).

Per i computer che eseguono sistemi operativi Windows Server 2003, Windows XP e Windows 2000, TAPISRV viene eseguito nel contesto di Svchost.exe. Per i computer che eseguono Windows NT, viene eseguito come processo di servizio separato. Quando un'applicazione carica una DLL TAPI nello spazio di processo ed esegue un'operazione di inizializzazione, la DLL stabilisce un collegamento RPC al server TAPI. Il server TAPI carica i provider del servizio telefonico (TSPs) nello spazio di elaborazione. Indipendentemente dal numero di applicazioni che accedono ai dispositivi di un determinato provider, sarà presente una sola istanza di un determinato TSP.

 

 



