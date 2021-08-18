---
description: Il server TAPI (TAPISRV) è il repository centrale dei dati di telefonia in un computer utente.
ms.assetid: 794d230c-abe8-429d-bbf5-91ba364b16ab
title: TAPI Server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19eb335ddef68f5f4cc588e34edab4931ad8be1e5e1d768e07a142989afe2291
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002679"
---
# <a name="tapi-server"></a>TAPI Server

Il server TAPI (TAPISRV) è il repository centrale dei dati di telefonia in un computer utente. Questo processo di servizio tiene traccia delle risorse di telefonia locali e remote, delle applicazioni registrate per gestire le richieste di telefonia assistita e delle funzioni asincrone in sospeso e consente anche un'interfaccia coerente con i provider di servizi di telefonia (TSP). Per altre informazioni e un diagramma che illustra la relazione del server TAPI con altri componenti e una panoramica dei relativi ruoli, vedere [Microsoft Telephony Programming Model](microsoft-telephony-programming-model.md).

Per i computer in esecuzione nei sistemi operativi Windows Server 2003, Windows XP e Windows 2000, TAPISRV viene eseguito nel contesto di Svchost.exe. Per i computer in Windows NT, viene eseguito come processo di servizio separato. Quando un'applicazione carica una DLL TAPI nello spazio di elaborazione ed esegue un'operazione di inizializzazione, la DLL stabilisce un collegamento RPC al server TAPI. Il server TAPI carica i provider di servizi telefonici (TSP) nello spazio di elaborazione. Indipendentemente dal numero di applicazioni che accedono ai dispositivi di un determinato provider, esisterà una sola istanza di un TSP specifico.

 

 



