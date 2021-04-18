---
description: Un servizio, un driver o un'applicazione che desidera fornire dati del contatore può scrivere una DLL di prestazioni per fornire i dati.
ms.assetid: 030316e5-f9f3-4333-9bb4-7ad301bbe7bf
title: Fornire dati del contatore mediante una DLL di prestazioni
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: e14b8a0e59b1fc9af3d8cad6e895d4a0067b9ae6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312098"
---
# <a name="providing-counter-data-using-a-performance-dll"></a>Fornire dati del contatore mediante una DLL di prestazioni

> [!IMPORTANT]
> A causa di limitazioni significative in merito a prestazioni e affidabilità, il metodo per fornire i dati dei contatori delle prestazioni descritti in questo argomento può essere modificato o non disponibile in futuro. Microsoft consiglia invece di usare il metodo descritto in [fornire i dati del contatore usando la versione 2,0](providing-counter-data-using-version-2-0.md) per la creazione di nuovi contatori delle prestazioni e di migrare i contatori delle prestazioni esistenti per usare anche tale metodo.

Un servizio, un driver o un'applicazione che desidera fornire dati del contatore può scrivere una DLL di prestazioni per fornire i dati. Quando un consumer esegue una query sui dati sulle prestazioni, il sistema carica la DLL del provider nel processo del consumer e chiama il provider per raccogliere i dati. Per informazioni dettagliate sulla scrittura della DLL di prestazioni, vedere [creazione di una DLL di estensione](creating-a-performance-extension-dll.md)per le prestazioni.

Il sistema utilizza il registro di sistema per determinare il provider da chiamare. Per informazioni sulla registrazione del provider e dei contatori supportati, vedere [aggiunta di contatori delle prestazioni](adding-performance-counters.md).

> [!Note]
> Le DLL delle prestazioni non sono supportate in Windows OneCore. Se si scrive un componente che deve essere eseguito in Windows OneCore, usare il metodo descritto in [fornire dati del contatore usando la versione 2,0](providing-counter-data-using-version-2-0.md).
