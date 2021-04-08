---
description: Nella tabella seguente sono elencate le
ms.assetid: 3f47a52c-2d36-4a74-9d7f-df37645b8e72
title: Strumenti dei contatori delle prestazioni
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: dc40dd5dfe640e09ac6f7258856389f04d60215f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967500"
---
# <a name="performance-counters-tools"></a>Strumenti dei contatori delle prestazioni

## <a name="data-collection-tools"></a>Strumenti di raccolta dati

Gli strumenti seguenti sono utili quando si utilizzano o si modificano i dati dei contatori delle prestazioni di Windows.

|Strumento|Descrizione
|----|-----------
| [PerfMon](/windows-server/administration/windows-commands/perfmon) | Strumento GUI per la raccolta e la visualizzazione dei dati dei contatori delle prestazioni. `perfmon.exe` Avvia MMC con lo snap-in Performance Monitor, che consente di accedere a performance monitor, insiemi agenti di raccolta dati e strumenti report.
| [TypePerf](/windows-server/administration/windows-commands/typeperf) |Strumento da riga di comando per la raccolta e la stampa dei dati dei contatori delle prestazioni. Può essere usato per elencare i CounterSet disponibili, elencare i contatori disponibili, stampare i dati del contatore nella console o raccogliere i dati del contatore in un file di log (CSV, TDF, grosso).
| [Relog](/windows-server/administration/windows-commands/relog) |Strumento da riga di comando per la trasformazione e l'Unione di file di log (CSV, TDF, un grosso) acquisiti tramite `typeperf.exe` o tramite le `PDH.dll` API.
| [LogMan](/windows-server/administration/windows-commands/logman) |Strumento da riga di comando per il controllo degli insiemi agenti di raccolta dati.

## <a name="data-provider-tools"></a>Strumenti del provider di dati

Gli strumenti seguenti sono utili quando si pubblicano i dati dei contatori delle prestazioni di Windows.

|Strumento|Descrizione
|----|-----------
| [CtrPP](ctrpp.md) | Strumento di compilazione da riga di comando dalla Windows SDK che convalida e compila il manifesto del provider v2 dei contatori delle prestazioni. Questo strumento genera le `.h` intestazioni e gli `.rc` script di risorsa necessari per compilare un provider v2.
| [LodCtr](/windows-server/administration/windows-commands/lodctr) | Strumento da riga di comando utilizzato per installare il provider in un sistema.
| [UnlodCtr](/windows-server/administration/windows-commands/unlodctr_1) | Strumento da riga di comando utilizzato per disinstallare il provider da un sistema.
