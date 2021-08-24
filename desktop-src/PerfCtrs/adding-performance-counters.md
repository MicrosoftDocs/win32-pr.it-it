---
description: I contatori delle prestazioni specifici dell'applicazione consentono di ottimizzare le prestazioni durante lo sviluppo e il debug dell'applicazione.
ms.assetid: 016386f6-4675-409e-8446-599e4ff96109
title: Aggiunta di contatori delle prestazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4aaf66d6a0e2f0c98ad0e9fe3cc66069509d4c2391ab74e4ecaa17d6780f4561
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034001"
---
# <a name="adding-performance-counters"></a>Aggiunta di contatori delle prestazioni

> [!IMPORTANT]
> A causa di limitazioni significative di prestazioni e affidabilità, il metodo per fornire i dati dei contatori delle prestazioni descritti in questo argomento potrebbe essere modificato o non disponibile in futuro. Al contrario, Microsoft consiglia di usare il metodo descritto in Fornire dati dei contatori usando la versione [2.0](providing-counter-data-using-version-2-0.md) per la creazione di nuovi contatori delle prestazioni e di eseguire la migrazione dei contatori delle prestazioni esistenti per usare anche tale metodo.

I contatori delle prestazioni specifici dell'applicazione consentono di ottimizzare le prestazioni durante lo sviluppo e il debug dell'applicazione. Dopo aver completato e installato l'applicazione nei sistemi di destinazione, i contatori consentono agli amministratori di sistema di modificare le impostazioni configurabili per l'applicazione.

## <a name="adding-a-performance-object-and-its-counters"></a>Aggiunta di un oggetto prestazioni e dei relativi contatori

1. Progettare i tipi di oggetto e i contatori per l'applicazione. Per informazioni dettagliate, vedere [Progettazione di oggetti e contatori.](object-and-counter-design.md)
2. Creare un file di inizializzazione (.ini) contenente i nomi e le descrizioni degli oggetti prestazioni e dei contatori specificati. Per informazioni dettagliate, vedere [Aggiunta di nomi e descrizioni dei contatori al Registro di sistema.](adding-counter-names-and-descriptions-to-the-registry.md)
3. Creare un file di intestazione (con estensione h) contenente gli offset relativi in corrispondenza dei quali gli oggetti contatore e i contatori verranno installati nel Registro di sistema. Per informazioni dettagliate, vedere [Aggiunta di nomi e descrizioni dei contatori al Registro di sistema.](adding-counter-names-and-descriptions-to-the-registry.md)
4. Configurare le voci di monitoraggio delle prestazioni necessarie nel Registro di sistema. Sono inclusi i passaggi seguenti.
    1. Creare una chiave del Registro di sistema nella **chiave Services** per l'applicazione. Se tale nodo non è disponibile, crearlo nella chiave del Registro di sistema seguente: `HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services` . Per informazioni dettagliate, [vedere Creazione della chiave delle prestazioni dell'applicazione.](creating-the-applications-performance-key.md)
    2. Usare **l'utilità lodctr** con i file .ini e h per installare le informazioni nel Registro di sistema. Questa utilità ha esito positivo solo se esiste una chiave per le prestazioni nella **chiave Servizi** per l'applicazione. Per informazioni dettagliate, vedere [Aggiunta di nomi e descrizioni dei contatori al Registro di sistema.](adding-counter-names-and-descriptions-to-the-registry.md)
5. Creare una DLL delle prestazioni contenente un set di funzioni esportate che forniscono i dati dei contatori sottoposti a query al consumer. Per informazioni dettagliate, vedere [Creazione di una DLL dell'estensione per le prestazioni.](creating-a-performance-extension-dll.md)
6. Modificare il file di installazione dell'applicazione per automatizzare l'aggiunta di informazioni al Registro di sistema (come descritto nel passaggio 4) e copiare la DLL delle prestazioni nella directory dell'applicazione al momento dell'installazione.

Per informazioni sulle voci aggiuntive del Registro di sistema, vedere [Creazione di altre voci del Registro di sistema.](creating-other-registry-entries.md)
