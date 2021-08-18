---
description: Le funzioni seguenti vengono usate con l'elenco di spazio su disco.
ms.assetid: 18693b2d-6b0f-4f9c-b3cf-e50c36e2f2e1
title: Disk-Space funzioni list
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e20e6f656110cc3b8c2ebd607f28b5d701ce3007b4ce8812f7e3bcad2f7f5b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118887367"
---
# <a name="disk-space-list-functions"></a>Disk-Space funzioni list

Le funzioni seguenti vengono usate con l'elenco di spazio su disco.



| Funzione                                                                                         | Descrizione                                                                                                                          |
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [**SetupAdjustDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupadjustdiskspacelista)                                     | Regola la quantità di spazio necessario per un'unità specificata.                                                                          |
| [**SetupCreateDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupcreatediskspacelista)                                     | Crea un elenco di spazio su disco e alloca le risorse.                                                                             |
| [**SetupDestroyDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupdestroydiskspacelist)                                   | Elimina un elenco di spazio su disco, liberando le risorse allocate.                                                                   |
| [**SetupDuplicateDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupduplicatediskspacelista)                               | Duplica un elenco di spazio su disco come nuovo elenco di spazio su disco indipendente.                                                                   |
| [**SetupQueryDrivesInDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerydrivesindiskspacelista)                       | Riempie un buffer con le specifiche dell'unità per tutte le unità elencate nell'elenco di spazio su disco.                                       |
| [**SetupQuerySpaceRequiredOnDrive**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryspacerequiredondrivea)                         | Restituisce la quantità totale di spazio su disco necessaria per completare le operazioni sui file in una determinata unità elencata nell'elenco di spazio su disco. |
| [**SetupAddToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddtodiskspacelista)                                       | Aggiunge un'operazione di copia o eliminazione di file all'elenco di spazio su disco.                                                                         |
| [**SetupAddSectionToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddsectiontodiskspacelista)                         | Aggiunge tutte le operazioni sui file in una **sezione Copia file** o Elimina **file** di un file INF a un elenco di spazio su disco.                    |
| [**SetupAddInstallSectionToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddinstallsectiontodiskspacelista)           | Aggiunge tutte le operazioni sui file in **una sezione Install** di un file INF all'elenco di spazio su disco.                                        |
| [**SetupRemoveFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefromdiskspacelista)                             | Rimuove un'operazione di copia o eliminazione di file da un elenco di spazi su disco.                                                                      |
| [**SetupRemoveSectionFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovesectionfromdiskspacelista)               | Rimuove tutte le operazioni sui  file in una **sezione Copia file** o Elimina file di un file INF da un elenco di spazio su disco.               |
| [**SetupRemoveInstallSectionFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremoveinstallsectionfromdiskspacelista) | Rimuove tutte le operazioni sui file nella **sezione Install** di un file INF dall'elenco di spazio su disco.                                  |



 

 

 



