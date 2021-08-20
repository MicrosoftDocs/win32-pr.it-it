---
description: "VDS fornisce due oggetti helper: l'oggetto enumerazione e l'oggetto asincrono. In questo argomento viene descritto ognuno di questi oggetti e vengono forniti collegamenti a esempi di utilizzo di ognuno di essi da parte dei chiamanti."
ms.assetid: 0f809c71-a3bd-4c62-8086-9651ea1a3400
title: Oggetti helper
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98464c31548309b50e21b2b8e3e20a867efe7ca647d7a9879efd0ef346e6a147
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999481"
---
# <a name="helper-objects"></a>Oggetti helper

\[A partire Windows 8 e Windows Server 2012, l'interfaccia [COM](virtual-disk-service-portal.md) del servizio disco virtuale viene sostituita dal Windows Archiviazione API Gestione [.](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)\]

VDS fornisce due oggetti helper: l'oggetto enumerazione e l'oggetto asincrono. In questo argomento viene descritto ognuno di questi oggetti e vengono forniti collegamenti a esempi di utilizzo di ognuno di essi da parte dei chiamanti.

## <a name="enumeration-object"></a>Oggetto Enumeration

Un oggetto enumerazione enumera tramite un set di oggetti VDS di un tipo specificato. Gli oggetti possono essere provider, sottosistemi, controller, LUN, plex LUN, unità, pacchetti di dischi, dischi, volumi o plex di volumi. I chiamanti possono ottenere un puntatore a un oggetto specifico selezionando l'oggetto desiderato dall'enumerazione restituita dal metodo appropriato. Per un esempio di codice, vedere [Utilizzo di oggetti di enumerazione.](working-with-enumeration-objects.md)

Nella tabella seguente sono elencate le interfacce, le enumerazioni e le strutture correlate. 

| Tipo                                              | Elemento                                  |
|---------------------------------------------------|------------------------------------------|
| Interfacce sempre esposte da questo oggetto | [**IEnumVdsObject**](/windows/desktop/api/Vds/nn-vds-ienumvdsobject) |
| Enumerazioni associate                           | Nessuno.                                    |
| Strutture associate                             | Nessuno.                                    |



 

## <a name="async-object"></a>Oggetto asincrono

Un oggetto asincrono gestisce le operazioni asincrone. I metodi che avviano operazioni asincrone restituiscono un puntatore a un'interfaccia [**IVdsAsync,**](/windows/desktop/api/Vds/nn-vds-ivdsasync) che consente al chiamante di annullare, attendere ed eseguire query sullo stato dell'operazione asincrona.

Le operazioni VDS a esecuzione lunga tendono a essere implementate in modo asincrono. I programmi provider software di base e dinamici implementano metodi asincroni in modo coerente per le operazioni su volume, partizione e disco. I provider hardware implementano facoltativamente metodi correlati a asincroni in modo asincrono. Indipendentemente dal modo in cui il provider implementa il metodo, l'operazione deve restituire al chiamante un puntatore a [**un'interfaccia IVdsAsync.**](/windows/desktop/api/Vds/nn-vds-ivdsasync) Per un esempio di codice, vedere [Gestione delle operazioni asincrone.](managing-asynchronous-operations.md)

Le operazioni asincrone includono:

-   Creazione di un LUN, un volume o una partizione.
-   Formattazione di un volume o di una partizione.
-   Aggiunta o rimozione di un LUN o di un volume plex.
-   Interruzione di un volume plex.
-   Estensione o riduzione di un LUN o di un volume.
-   Ripristino di un LUN o di un volume.
-   Pulizia di un disco.
-   Sostituzione di un disco.

Nella tabella seguente sono elencate le interfacce, le enumerazioni e le strutture correlate. 

| Tipo                                              | Elemento                        |
|---------------------------------------------------|--------------------------------|
| Interfacce sempre esposte da questo oggetto | [**IVdsAsync**](/windows/desktop/api/Vds/nn-vds-ivdsasync) |
| Enumerazioni associate                           | Nessuno.                          |
| Strutture associate                             | Nessuno.                          |



 

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

 

 
