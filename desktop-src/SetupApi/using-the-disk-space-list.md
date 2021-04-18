---
description: Prima di poter aggiungere o rimuovere operazioni di file dall'elenco spazio su disco, è necessario crearlo utilizzando la funzione SetupCreateDiskSpaceList.
ms.assetid: 287fd84a-dc8c-4a5c-b998-db5f2fbee5f1
title: Uso dell'elenco Disk-Space
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a19f100fd5190472f5f6bfebaf74affe1a789cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310742"
---
# <a name="using-the-disk-space-list"></a>Uso dell'elenco Disk-Space

Prima di poter aggiungere o rimuovere operazioni di file dall'elenco spazio su disco, è necessario crearlo utilizzando la funzione [**SetupCreateDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupcreatediskspacelista) .

Dopo aver creato un elenco di spazio su disco, è possibile aggiungere singole operazioni di copia o eliminazione di file all'elenco usando [**SetupAddToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddtodiskspacelista). Per aggiungere tutte le operazioni di copia o eliminazione di file in un'intera sezione INF, usare la funzione [**SetupAddSectionToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddsectiontodiskspacelista) o [**SetupAddInstallSectionToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddinstallsectiontodiskspacelista) .

Dopo aver aggiunto tutte le operazioni di installazione nell'elenco spazio su disco, è possibile eseguire una query per verificare la quantità di spazio su disco necessaria per l'installazione specificata tramite la funzione [**SetupQuerySpaceRequiredOnDrive**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryspacerequiredondrivea) .

La funzione [**SetupQueryDrivesInDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerydrivesindiskspacelista) restituisce le specifiche di unità per ogni unità di destinazione a cui si fa riferimento nelle operazioni sui file nell'elenco spazio su disco. È possibile usare queste informazioni per confrontare a livello di codice lo spazio disponibile in queste unità con lo spazio necessario per l'installazione.

Per rimuovere un'operazione su file dall'elenco spazio su disco, usare la funzione [**SetupRemoveFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefromdiskspacelista) . Per rimuovere tutte le operazioni di copia o eliminazione di file da un'intera sezione INF, usare la funzione [**SetupRemoveSectionFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovesectionfromdiskspacelista) o [**SetupRemoveInstallSectionFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremoveinstallsectionfromdiskspacelista) .

Una volta che l'elenco spazio su disco non è più necessario, è possibile rilasciare le risorse allocate chiamando la funzione [**SetupDestroyDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupdestroydiskspacelist) .

 

 



