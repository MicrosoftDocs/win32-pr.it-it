---
description: Nella tabella seguente sono elencati i
ms.assetid: 3f47a52c-2d36-4a74-9d7f-df37645b8e72
title: Strumenti dei contatori delle prestazioni
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: a4f1640a269b87cce7452e54a2557dcc9c34fe154ae9e9f95fdd3794e275b59e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033401"
---
# <a name="performance-counters-tools"></a>Strumenti dei contatori delle prestazioni

## <a name="data-collection-tools"></a>Strumenti di raccolta dati

Gli strumenti seguenti sono utili per l'utilizzo o la modifica Windows dei contatori delle prestazioni.

|Strumento|Descrizione
|----|-----------
| [PerfMon](/windows-server/administration/windows-commands/perfmon) | Strumento GUI per la raccolta e la visualizzazione dei dati del contatore delle prestazioni. `perfmon.exe` avvia MMC con lo snap-in Monitor prestazioni, che fornisce l'accesso agli strumenti Monitor prestazioni, insiemi agenti di raccolta dati e report.
| [TypePerf](/windows-server/administration/windows-commands/typeperf) |Strumento da riga di comando per la raccolta e la stampa dei dati del contatore delle prestazioni. Può essere usato per elencare i contatori disponibili, elencare i contatori disponibili, stampare i dati dei contatori nella console o raccogliere i dati dei contatori in un file di log (CSV, TDF, BLG).
| [Eseguire di nuovo il log](/windows-server/administration/windows-commands/relog) |Strumento da riga di comando per la trasformazione e l'unione di file di log (CSV, TDF, BLG) acquisiti tramite o `typeperf.exe` `PDH.dll` tramite le API.
| [Logman](/windows-server/administration/windows-commands/logman) |Strumento da riga di comando per il controllo degli insiemi agenti di raccolta dati.

## <a name="data-provider-tools"></a>Strumenti del provider di dati

Gli strumenti seguenti sono utili quando si pubblicano i Windows dei contatori delle prestazioni.

|Strumento|Descrizione
|----|-----------
| [CtrPP](ctrpp.md) | Strumento di compilazione da riga di comando Windows SDK che convalida e compila il manifesto del provider dei contatori delle prestazioni V2. Questo strumento genera le `.h` intestazioni e gli script delle risorse necessari per `.rc` compilare un provider V2.
| [LodCtr](/windows-server/administration/windows-commands/lodctr) | Strumento da riga di comando usato per installare il provider in un sistema.
| [Unlodctr](/windows-server/administration/windows-commands/unlodctr_1) | Strumento da riga di comando usato per disinstallare il provider da un sistema.
