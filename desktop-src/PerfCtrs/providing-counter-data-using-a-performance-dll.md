---
description: Un servizio, un driver o un'applicazione che desidera fornire i dati dei contatori può scrivere una DLL delle prestazioni per fornire i dati.
ms.assetid: 030316e5-f9f3-4333-9bb4-7ad301bbe7bf
title: Specifica dei dati dei contatori tramite una DLL delle prestazioni
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 165e6a8797c50a22acff1d3cd3ded7f8b06a0ee2a7153300e98e46bea1127f27
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910311"
---
# <a name="providing-counter-data-using-a-performance-dll"></a>Specifica dei dati dei contatori tramite una DLL delle prestazioni

> [!IMPORTANT]
> A causa di limitazioni significative di prestazioni e affidabilità, il metodo per fornire i dati dei contatori delle prestazioni descritti in questo argomento potrebbe essere modificato o non disponibile in futuro. Al contrario, Microsoft consiglia di usare il metodo descritto in Fornire dati dei contatori usando la versione [2.0](providing-counter-data-using-version-2-0.md) per la creazione di nuovi contatori delle prestazioni e di eseguire la migrazione dei contatori delle prestazioni esistenti per usare anche tale metodo.

Un servizio, un driver o un'applicazione che desidera fornire i dati dei contatori può scrivere una DLL delle prestazioni per fornire i dati. Quando un consumer esegue query sui dati sulle prestazioni, il sistema carica la DLL del provider nel processo del consumer e chiama il provider per raccogliere i dati. Per informazioni dettagliate sulla scrittura della DLL delle prestazioni, vedere [Creating a Performance Extension DLL](creating-a-performance-extension-dll.md).

Il sistema utilizza il Registro di sistema per determinare il provider da chiamare. Per informazioni sulla registrazione del provider e dei contatori supportati, vedere [Aggiunta di contatori delle prestazioni.](adding-performance-counters.md)

> [!Note]
> Le DLL delle prestazioni non sono supportate in Windows OneCore. Se si scrive un componente che deve essere eseguito Windows OneCore, usare il metodo descritto in Fornire i dati dei contatori [usando la versione 2.0.](providing-counter-data-using-version-2-0.md)
