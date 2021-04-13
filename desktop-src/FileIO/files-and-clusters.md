---
description: Un file è un'unità di dati nel file system a cui un utente può accedere e gestire.
ms.assetid: 271bad79-c23b-45ee-938c-d17dae89db1a
title: File e cluster
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75384900d5d487ab02bd19c13cc2c25e9a310b3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226872"
---
# <a name="files-and-clusters"></a>File e cluster

Un *file* è un'unità di dati nel file System a cui un utente può accedere e gestire. Un file deve avere un nome univoco nella directory. È costituito da uno o più flussi di byte che contengono un set di dati correlati, oltre a un set di attributi (detti anche proprietà) che descrivono il file o i dati all'interno del file. L'ora di creazione di un file è un esempio di attributo di file.

Quando viene creato un file, viene creato un flusso predefinito senza nome per archiviare tutti i dati scritti nel file mentre è aperto. È anche possibile creare altri flussi all'interno del file. Questi flussi aggiuntivi sono detti flussi alternativi. Nella figura seguente viene illustrato un file con il flusso predefinito e due flussi alternativi.

![file con un flusso predefinito e due flussi alternativi](images/fig1.png)

Gli attributi di file non vengono archiviati nei flussi di dati con i dati del file, ma vengono archiviati altrove e gestiti dal sistema operativo.

Tutti i dati file system, inclusi il codice e le directory di bootstrap del sistema, vengono archiviati dal file system NTFS nei file. In altri file System le informazioni vengono archiviate in aree disco esterne al file system. Il vantaggio di archiviare queste informazioni nei file è che Windows è in grado di individuare, accedere e gestire facilmente le informazioni. Altri vantaggi sono che ognuno di questi file può essere protetto da un descrittore di sicurezza e, nel caso di danneggiamenti parziali del disco, possono essere spostati rapidamente in una parte più sicura del disco.

L'unità di archiviazione fondamentale di tutti i file system supportati è un *cluster*, ovvero un gruppo di settori. Ciò consente all'file system di ottimizzare l'amministrazione dei dati del disco indipendentemente dalle dimensioni del settore del disco impostate dal controller del disco hardware. Se il disco da amministrare è grande e grandi quantità di dati vengono spostati e organizzati in un'unica operazione, l'amministratore può modificare le dimensioni del cluster per adattarle a questo.

Windows gestisce i file tramite [oggetti file](file-objects.md), [handle di file](file-handles.md)e [puntatori di file](file-pointers.md).

Per ulteriori informazioni sui flussi di file, vedere [flussi di file](file-streams.md). Per ulteriori informazioni sui cluster, vedere [cluster ed extent](clusters-and-extents.md). Per ulteriori informazioni su come accedere e gestire i file, vedere la pagina relativa alla [gestione dei](file-management.md) file e ai file di [riferimento](file-management-reference.md).

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                       | Descrizione                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Flussi di file](file-streams.md)<br/>                 | Nel file system NTFS i flussi contengono i dati scritti in un file e che forniscono altre informazioni su un file rispetto agli attributi e alle proprietà.<br/>                                                                                         |
| [Oggetti file](file-objects.md)<br/>                 | *Gli oggetti file* funzionano come interfaccia logica tra il kernel e i processi in modalità utente e i dati dei file che risiedono sul disco fisico.<br/>                                                                                                      |
| [Handle di file](file-handles.md)<br/>                 | Quando un file viene aperto da un processo che utilizza la funzione [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) , a esso viene associato un *handle di file* fino al termine del processo o alla chiusura dell'handle tramite la funzione [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) .<br/> |
| [Puntatori a file](file-pointers.md)<br/>               | Un puntatore di file è un valore di offset a 64 bit che specifica il byte successivo da leggere o la posizione in cui viene scritto il byte successivo.<br/>                                                                                                                 |
| [Cluster ed extent](clusters-and-extents.md)<br/> | È possibile fare riferimento a cluster da due diverse prospettive: all'interno del file e nel volume.<br/>                                                                                                                                                   |



 

 

