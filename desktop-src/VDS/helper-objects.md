---
description: VDS fornisce due oggetti helper, ovvero l'oggetto di enumerazione e l'oggetto asincrono. Questo argomento descrive ognuno di questi oggetti e fornisce collegamenti ad esempi di funzionamento dei chiamanti con ognuno di essi.
ms.assetid: 0f809c71-a3bd-4c62-8086-9651ea1a3400
title: Oggetti helper
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac5193003abd10d9fa2c311b250272d9ad5847a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234005"
---
# <a name="helper-objects"></a>Oggetti helper

\[A partire da Windows 8 e Windows Server 2012, l'interfaccia com del [servizio dischi virtuali](virtual-disk-service-portal.md) viene sostituita dall' [API di gestione archiviazione di Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

VDS fornisce due oggetti helper, ovvero l'oggetto di enumerazione e l'oggetto asincrono. Questo argomento descrive ognuno di questi oggetti e fornisce collegamenti ad esempi di funzionamento dei chiamanti con ognuno di essi.

## <a name="enumeration-object"></a>Enumerazione (oggetto)

Un oggetto di enumerazione enumera un set di oggetti VDS di un tipo specificato. Gli oggetti possono essere provider, sottosistemi, controller, lun, Plex di LUN, unità, dischi, dischi, volumi o Plex del volume. I chiamanti possono ottenere un puntatore a un oggetto specifico selezionando l'oggetto desiderato dall'enumerazione restituita dal metodo appropriato. Per un esempio di codice, vedere [utilizzo di oggetti di enumerazione](working-with-enumeration-objects.md).

Nella tabella seguente sono elencate le interfacce, le enumerazioni e le strutture correlate. 

| Tipo                                              | Elemento                                  |
|---------------------------------------------------|------------------------------------------|
| Interfacce sempre esposte da questo oggetto | [**IEnumVdsObject**](/windows/desktop/api/Vds/nn-vds-ienumvdsobject) |
| Enumerazioni associate                           | Nessuna.                                    |
| Strutture associate                             | Nessuna.                                    |



 

## <a name="async-object"></a>Oggetto asincrono

Un oggetto asincrono gestisce le operazioni asincrone. I metodi che avviano operazioni asincrone restituiscono un puntatore a un'interfaccia [**IVdsAsync**](/windows/desktop/api/Vds/nn-vds-ivdsasync) , che consente al chiamante di annullare, attendere ed eseguire query sullo stato dell'operazione asincrona.

Le operazioni VDS con esecuzione prolungata tendono a essere implementate in modo asincrono. I programmi del provider software di base e dinamici implementano i metodi asincroni in modo coerente per le operazioni di volume, partizione e disco. I provider hardware implementano facoltativamente metodi correlati a Async in modo asincrono. Indipendentemente dal modo in cui il provider implementa il metodo, l'operazione deve restituire un puntatore a un'interfaccia [**IVdsAsync**](/windows/desktop/api/Vds/nn-vds-ivdsasync) al chiamante. Per un esempio di codice, vedere [gestione delle operazioni asincrone](managing-asynchronous-operations.md).

Le operazioni asincrone includono:

-   Creazione di un LUN, un volume o una partizione.
-   Formattazione di un volume o di una partizione.
-   Aggiunta o rimozione di un LUN o un plex del volume.
-   Suddivisione di un volume Plex.
-   Estensione o compattazione di un LUN o un volume.
-   Ripristino di un LUN o un volume.
-   Pulizia di un disco.
-   Sostituzione di un disco.

Nella tabella seguente sono elencate le interfacce, le enumerazioni e le strutture correlate. 

| Tipo                                              | Elemento                        |
|---------------------------------------------------|--------------------------------|
| Interfacce sempre esposte da questo oggetto | [**IVdsAsync**](/windows/desktop/api/Vds/nn-vds-ivdsasync) |
| Enumerazioni associate                           | Nessuna.                          |
| Strutture associate                             | Nessuna.                          |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modello a oggetti VDS](vds-object-model.md)
</dt> <dt>

[**IVdsAsync**](/windows/desktop/api/Vds/nn-vds-ivdsasync)
</dt> <dt>

[Utilizzo di oggetti di enumerazione](working-with-enumeration-objects.md)
</dt> <dt>

[Gestione delle operazioni asincrone](managing-asynchronous-operations.md)
</dt> </dl>

 

 
