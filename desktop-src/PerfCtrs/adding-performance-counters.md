---
description: I contatori delle prestazioni specifici dell'applicazione consentono di ottimizzare le prestazioni durante lo sviluppo e il debug dell'applicazione.
ms.assetid: 016386f6-4675-409e-8446-599e4ff96109
title: Aggiunta di contatori delle prestazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8660af9406de4dedec3ecbd76169a23b342aa7d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312190"
---
# <a name="adding-performance-counters"></a>Aggiunta di contatori delle prestazioni

> [!IMPORTANT]
> A causa di limitazioni significative in merito a prestazioni e affidabilità, il metodo per fornire i dati dei contatori delle prestazioni descritti in questo argomento può essere modificato o non disponibile in futuro. Microsoft consiglia invece di usare il metodo descritto in [fornire i dati del contatore usando la versione 2,0](providing-counter-data-using-version-2-0.md) per la creazione di nuovi contatori delle prestazioni e di migrare i contatori delle prestazioni esistenti per usare anche tale metodo.

I contatori delle prestazioni specifici dell'applicazione consentono di ottimizzare le prestazioni durante lo sviluppo e il debug dell'applicazione. Dopo che l'applicazione è stata completata e installata nei sistemi di destinazione, i contatori possono aiutare gli amministratori di sistema a modificare le impostazioni configurabili per l'applicazione.

## <a name="adding-a-performance-object-and-its-counters"></a>Aggiunta di un oggetto prestazione e dei relativi contatori

1. Progettare i tipi di oggetto e i contatori per l'applicazione. Per informazioni dettagliate, vedere [progettazione di oggetti e contatori](object-and-counter-design.md).
2. Creare un file di inizializzazione (INI) contenente i nomi e le descrizioni degli oggetti e dei contatori delle prestazioni forniti. Per informazioni dettagliate, vedere [aggiunta di nomi di contatori e descrizioni al registro di sistema](adding-counter-names-and-descriptions-to-the-registry.md).
3. Creare un file di intestazione (. h) contenente gli offset relativi in corrispondenza dei quali verranno installati gli oggetti contatore e i contatori nel registro di sistema. Per informazioni dettagliate, vedere [aggiunta di nomi di contatori e descrizioni al registro di sistema](adding-counter-names-and-descriptions-to-the-registry.md).
4. Configurare le voci di monitoraggio delle prestazioni necessarie nel registro di sistema. Sono inclusi i passaggi seguenti.
    1. Creare una chiave del registro di sistema nella chiave **dei servizi** per l'applicazione. Se non si dispone di un nodo di questo tipo, crearlo con la seguente chiave del registro di sistema: `HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services` . Per informazioni dettagliate, vedere [creazione della chiave delle prestazioni dell'applicazione](creating-the-applications-performance-key.md).
    2. Usare l'utilità **lodctr** con i file. ini e. h per installare le informazioni nel registro di sistema. Questa utilità ha esito positivo solo se nella chiave dei **Servizi** per l'applicazione è presente una chiave delle prestazioni. Per informazioni dettagliate, vedere [aggiunta di nomi di contatori e descrizioni al registro di sistema](adding-counter-names-and-descriptions-to-the-registry.md).
5. Creare una DLL di prestazioni contenente un set di funzioni esportate che forniscono al consumer i dati del contatore sottoposti a query. Per informazioni dettagliate, vedere [creazione di una DLL dell'estensione](creating-a-performance-extension-dll.md)per le prestazioni.
6. Modificare il file di installazione dell'applicazione per automatizzare l'aggiunta di informazioni al registro di sistema, come descritto nel passaggio 4, e copiare la DLL di prestazioni nella directory dell'applicazione in fase di installazione.

Per informazioni sulle voci aggiuntive del registro di sistema, vedere [creazione di altre voci del registro di sistema](creating-other-registry-entries.md).
