---
description: In Windows Vista i contatori delle prestazioni implementano una nuova architettura (versione 2.0) per fornire i dati dei contatori.
ms.assetid: c17eda2f-3cf8-40d6-8be6-c1ce190d1a26
title: Specifica dei dati dei contatori
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 0a17a6c75a86a7ee86f26350b9ea7680f0ba08338dbe7dc18cd56a8c425ba3ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117793624"
---
# <a name="providing-counter-data"></a>Specifica dei dati dei contatori

I componenti software che pubblicano i dati Windows contatori delle prestazioni sono denominati provider di dati delle prestazioni.

Windows supporta due tipi di provider di dati per le prestazioni. I provider di dati sulle prestazioni legacy (**provider V1**) vengono implementati usando un file .INI e una DLL delle prestazioni. I provider di dati delle prestazioni moderni **(provider V2)** usano un oggetto . MAN (manifesto XML) e le API del provider del contatore delle prestazioni.

## <a name="manifests"></a>Manifesti

I provider di dati sulle prestazioni moderni usano un oggetto . MAN (manifesto XML) per definire i dati del contatore e usare le API del provider del contatore delle prestazioni per gestire i dati all'interno del contesto del provider.

I provider implementati usando un manifesto e le API del provider dei contatori delle prestazioni sono spesso denominati **provider V2.**

Windows supporta i provider V2 in modalità utente Windows Vista o versioni successive. Per informazioni dettagliate sulla modalità utente, vedere [Specifica dei dati dei contatori con la versione 2.0.](providing-counter-data-using-version-2-0.md)

Windows supporta i provider V2 in modalità kernel Windows 7 o versione successiva. Per informazioni dettagliate sulla modalità kernel, vedere [Kernel Mode Performance Monitoring](/windows-hardware/drivers/devtest/kernel-mode-performance-monitoring).

## <a name="performance-dll-deprecated"></a>DLL delle prestazioni (deprecata)

Nell'architettura dei contatori delle prestazioni legacy, i provider implementavano una DLL delle prestazioni eseguita nel processo del consumer per raccogliere e fornire i dati del contatore quando richiesto da un consumer. Il provider ha utilizzato un file di inizializzazione (.INI) e le voci del Registro di sistema per definire i contatori e configurare la DLL delle prestazioni.

I provider implementati usando un file .INI e una DLL delle prestazioni sono spesso denominati **provider V1.**

> [!CAUTION]
> Anche se è comunque possibile usare una DLL delle prestazioni per fornire i dati dei contatori, questa architettura è deprecata a causa di limitazioni significative di prestazioni e affidabilità. Inoltre, i provider V1 sono spesso più difficili da implementare perché richiedono la distribuzione di una DLL separata che deve essere eseguita nel processo del consumer.

Per informazioni dettagliate, vedere [Specifica dei dati dei contatori tramite una DLL delle prestazioni.](providing-counter-data-using-a-performance-dll.md)
