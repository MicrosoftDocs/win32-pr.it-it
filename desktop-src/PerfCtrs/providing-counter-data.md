---
description: In Windows Vista, i contatori delle prestazioni implementavano una nuova architettura (versione 2,0) per fornire i dati dei contatori.
ms.assetid: c17eda2f-3cf8-40d6-8be6-c1ce190d1a26
title: Fornire dati del contatore
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: ed5aa4cc505baab9e15d3f69c3fb466712eddbfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312092"
---
# <a name="providing-counter-data"></a>Fornire dati del contatore

I componenti software che pubblicano i dati tramite i contatori delle prestazioni di Windows sono detti provider di dati sulle prestazioni.

Windows supporta due tipi di provider di dati sulle prestazioni. I provider di dati delle prestazioni legacy (**V1 provider**) vengono implementati mediante un. File INI e DLL delle prestazioni. I provider di dati delle prestazioni moderni (**provider v2**) usano un. MAN (manifesto XML) e API del provider del contatore delle prestazioni.

## <a name="manifests"></a>Manifesti

I provider di dati delle prestazioni moderni usano un. MAN (manifesto XML) per definire i dati del contatore e utilizzare le API del provider del contatore delle prestazioni per gestire i dati all'interno del contesto del provider.

I provider implementati utilizzando un manifesto e le API del provider del contatore delle prestazioni vengono spesso chiamati **provider v2**.

Windows supporta i provider v2 in modalità utente in Windows Vista o versioni successive. Per informazioni dettagliate sulla modalità utente, vedere la pagina relativa alla [fornitura di dati del contatore con la versione 2,0](providing-counter-data-using-version-2-0.md).

Windows supporta i provider v2 in modalità kernel in Windows 7 o versioni successive. Per informazioni dettagliate sulla modalità kernel, vedere [monitoraggio delle prestazioni in modalità kernel](/windows-hardware/drivers/devtest/kernel-mode-performance-monitoring).

## <a name="performance-dll-deprecated"></a>DLL prestazioni (deprecata)

Nell'architettura del contatore delle prestazioni legacy, i provider implementavano una DLL di prestazioni in che veniva eseguita nel processo del consumer per raccogliere e fornire i dati del contatore quando un consumer lo ha richiesto. Il provider ha utilizzato un'inizializzazione (. INI) e le voci del registro di sistema per definire i contatori e configurare la DLL delle prestazioni.

Provider implementati utilizzando un oggetto. Il file INI e una DLL di prestazioni sono spesso denominati **provider v1**.

> [!CAUTION]
> Sebbene sia comunque possibile utilizzare una DLL di prestazioni per fornire i dati dei contatori, questa architettura è deprecata a causa di limitazioni significative in merito a prestazioni e affidabilità. Inoltre, i provider v1 sono spesso più difficili da implementare perché richiedono la distribuzione di una DLL separata che deve essere eseguita nel processo del consumer.

Per informazioni dettagliate, vedere [fornire dati del contatore tramite una DLL di prestazioni](providing-counter-data-using-a-performance-dll.md).
