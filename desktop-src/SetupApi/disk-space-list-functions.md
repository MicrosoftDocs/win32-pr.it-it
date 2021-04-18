---
description: Le funzioni seguenti vengono utilizzate con l'elenco spazio su disco.
ms.assetid: 18693b2d-6b0f-4f9c-b3cf-e50c36e2f2e1
title: Funzioni elenco Disk-Space
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f520cc7a3ddcd0b12b27bd11768a95231a8ed4b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346516"
---
# <a name="disk-space-list-functions"></a>Funzioni elenco Disk-Space

Le funzioni seguenti vengono utilizzate con l'elenco spazio su disco.



| Funzione                                                                                         | Descrizione                                                                                                                          |
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [**SetupAdjustDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupadjustdiskspacelista)                                     | Regola la quantità di spazio necessario per un'unità specificata.                                                                          |
| [**SetupCreateDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupcreatediskspacelista)                                     | Consente di creare un elenco di spazio su disco e di allocarvi risorse.                                                                             |
| [**SetupDestroyDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupdestroydiskspacelist)                                   | Elimina un elenco di spazio su disco, liberando le risorse allocate.                                                                   |
| [**SetupDuplicateDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupduplicatediskspacelista)                               | Duplica un elenco di spazio su disco come nuovo elenco di spazio su disco indipendente.                                                                   |
| [**SetupQueryDrivesInDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerydrivesindiskspacelista)                       | Riempie un buffer con le specifiche di unità per tutte le unità elencate nell'elenco spazio su disco.                                       |
| [**SetupQuerySpaceRequiredOnDrive**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryspacerequiredondrivea)                         | Restituisce la quantità totale di spazio su disco necessario per completare le operazioni sui file in una determinata unità elencata nell'elenco spazio su disco. |
| [**SetupAddToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddtodiskspacelista)                                       | Aggiunge un'operazione di copia o eliminazione di file all'elenco di spazio su disco.                                                                         |
| [**SetupAddSectionToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddsectiontodiskspacelista)                         | Aggiunge tutte le operazioni sui file in una sezione **copia file** o **Elimina file** di un file inf in un elenco di spazio su disco.                    |
| [**SetupAddInstallSectionToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddinstallsectiontodiskspacelista)           | Aggiunge tutte le operazioni sui file in una sezione di **installazione** di un file inf all'elenco spazio su disco.                                        |
| [**SetupRemoveFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefromdiskspacelista)                             | Rimuove un'operazione di copia o eliminazione di file da un elenco di spazio su disco.                                                                      |
| [**SetupRemoveSectionFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovesectionfromdiskspacelista)               | Rimuove tutte le operazioni sui file in una sezione **copia file** o **Elimina file** di un file inf da un elenco spazio su disco.               |
| [**SetupRemoveInstallSectionFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremoveinstallsectionfromdiskspacelista) | Rimuove tutte le operazioni sui file nella sezione di **installazione** di un file inf dall'elenco spazio su disco.                                  |



 

 

 



