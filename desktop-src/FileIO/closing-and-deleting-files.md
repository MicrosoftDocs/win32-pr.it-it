---
description: Per utilizzare in modo efficiente le risorse del sistema operativo, un'applicazione deve chiudere i file quando non sono più necessari tramite la funzione CloseHandle. Se un file è aperto al termine di un'applicazione, il sistema lo chiude automaticamente.
ms.assetid: 6cf9694a-00c4-4750-8822-c25a1a102fd4
title: Chiusura ed eliminazione di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3da31fe7ff38a1bbd1555e2685ceab9ae432574
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317800"
---
# <a name="closing-and-deleting-files"></a>Chiusura ed eliminazione di file

Per utilizzare in modo efficiente le risorse del sistema operativo, un'applicazione deve chiudere i file quando non sono più necessari tramite la funzione [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) . Se un file è aperto al termine di un'applicazione, il sistema lo chiude automaticamente.

La funzione [**DeleteFile**](/windows/desktop/api/FileAPI/nf-fileapi-deletefilea) può essere usata per eliminare un file alla chiusura. Non è possibile eliminare un file finché non vengono chiusi tutti gli handle. Se non è possibile eliminare un file, non è possibile riutilizzarne il nome. Per riutilizzare immediatamente il nome di un file, rinominare il file esistente.

Se si elimina un file o una directory aperta in un computer remoto ed è già stata aperta nel computer remoto senza il set di autorizzazioni lettura condivisione, non chiamare [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) o [**OpenFile**](/windows/desktop/api/WinBase/nf-winbase-openfile) per aprire prima il file o la directory per l'eliminazione. Questa operazione comporterà una violazione di condivisione.

 

 
