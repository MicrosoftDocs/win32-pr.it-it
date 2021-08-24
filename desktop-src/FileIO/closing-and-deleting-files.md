---
description: Per usare in modo efficiente le risorse del sistema operativo, un'applicazione deve chiudere i file quando non sono più necessari usando la funzione CloseHandle. Se un file è aperto al termine di un'applicazione, il sistema lo chiude automaticamente.
ms.assetid: 6cf9694a-00c4-4750-8822-c25a1a102fd4
title: Chiusura ed eliminazione di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03c74ad36f2f099b8d2430f52cc2c40b789862c691f56df1ccebcd20e82586ad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696301"
---
# <a name="closing-and-deleting-files"></a>Chiusura ed eliminazione di file

Per usare in modo efficiente le risorse del sistema operativo, un'applicazione deve chiudere i file quando non sono più necessari usando la [**funzione CloseHandle.**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) Se un file è aperto al termine di un'applicazione, il sistema lo chiude automaticamente.

La [**funzione DeleteFile**](/windows/desktop/api/FileAPI/nf-fileapi-deletefilea) può essere usata per eliminare un file alla chiusura. Un file non può essere eliminato fino a quando non vengono chiusi tutti gli handle. Se non è possibile eliminare un file, non è possibile riutilizzarne il nome. Per riutilizzare immediatamente un nome file, rinominare il file esistente.

Se si elimina un file o una directory aperta in un computer remoto ed è già stato aperto nel computer remoto senza il set di autorizzazioni di condivisione di lettura, non chiamare [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) o [**OpenFile**](/windows/desktop/api/WinBase/nf-winbase-openfile) per aprire prima il file o la directory per l'eliminazione. Questa operazione comporta una violazione della condivisione.

 

 
