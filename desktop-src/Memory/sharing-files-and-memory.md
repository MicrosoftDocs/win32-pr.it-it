---
description: Il mapping dei file può essere usato per condividere un file o una memoria tra due o più processi. Per condividere un file o una memoria, tutti i processi devono usare il nome o l'handle dello stesso oggetto mapping di file.
ms.assetid: 942cb50d-df07-444f-bba5-58194556ae66
title: Condivisione di file e memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98d402eba3f87f1f799593ae0d6b23fba06124a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751727"
---
# <a name="sharing-files-and-memory"></a>Condivisione di file e memoria

Il mapping dei file può essere usato per condividere un file o una memoria tra due o più processi. Per condividere un file o una memoria, tutti i processi devono usare il nome o l'handle dello stesso oggetto mapping di file.

Per condividere un file, il primo processo crea o apre un file utilizzando la funzione [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) . Successivamente, viene creato un oggetto mapping di file utilizzando la funzione [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) , specificando l'handle di file e un nome per l'oggetto mapping di file. I nomi degli oggetti evento, semaforo, mutex, timer waitable, processo e mapping file condividono lo stesso spazio dei nomi. Pertanto, le funzioni **CreateFileMapping** e [**OpenFileMapping**](/windows/desktop/api/WinBase/nf-winbase-openfilemappinga) hanno esito negativo se specificano un nome usato da un oggetto di un altro tipo.

Per condividere memoria non associata a un file, un processo deve usare la funzione [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) e specificare un \_ valore di handle non valido \_ come parametro *hFile* anziché come handle di file esistente. L'oggetto di mapping dei file corrispondente accede alla memoria supportata dal file di paging del sistema. Quando si specifica un valore *di* handle non valido \_ \_ in una chiamata a **CreateFileMapping**, è necessario specificare una dimensione maggiore di zero.

Il modo più semplice per ottenere un handle dell'oggetto mapping dei file creato dal primo processo da parte di altri processi consiste nell'utilizzare la funzione [**OpenFileMapping**](/windows/desktop/api/WinBase/nf-winbase-openfilemappinga) e specificare il nome dell'oggetto. Questa operazione viene definita *memoria condivisa denominata*. Se l'oggetto di mapping dei file non dispone di un nome, il processo deve ottenere un handle tramite l'ereditarietà o la duplicazione. Per ulteriori informazioni sull'ereditarietà e la duplicazione, vedere [ereditarietà](../procthread/inheritance.md).

I processi che condividono file o memoria devono creare visualizzazioni di file tramite la funzione [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) o [**MapViewOfFileEx**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffileex) . Devono coordinare l'accesso tramite semafori, mutex, eventi o altre tecniche di esclusione reciproca. Per ulteriori informazioni, vedere [sincronizzazione](../sync/synchronization.md).

Un oggetto mapping dei file condivisi non verrà eliminato definitivamente fino a quando tutti i processi che lo usano non ne chiuderanno gli handle usando la funzione [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) .

Per informazioni sulla sicurezza degli oggetti di mapping dei file, vedere [sicurezza e accesso ai file](file-mapping-security-and-access-rights.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di una memoria condivisa denominata](creating-named-shared-memory.md)
</dt> </dl>

 

 
