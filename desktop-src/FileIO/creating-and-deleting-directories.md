---
description: Un'applicazione può creare ed eliminare le directory a livello di codice.
ms.assetid: 52d1d8a8-e5a7-44f5-9bf2-2a496ef79d32
title: Creazione ed eliminazione di directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 140547594271e13bc78bfa78336f167f228879a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130454"
---
# <a name="creating-and-deleting-directories"></a>Creazione ed eliminazione di directory

Un'applicazione può creare ed eliminare le directory a livello di codice.

Per creare una nuova directory, usare la funzione [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya), [**CreateDirectoryEx**](/windows/desktop/api/WinBase/nf-winbase-createdirectoryexa)o [**CreateDirectoryTransacted**](/windows/desktop/api/WinBase/nf-winbase-createdirectorytransacteda) . A una directory viene assegnato il nome specificato al momento della creazione. Le convenzioni per la denominazione di una directory seguono le convenzioni per la denominazione di un file. Per una descrizione di queste convenzioni, vedere [denominazione di un file](naming-a-file.md).

Per eliminare una directory esistente, usare la funzione [**RemoveDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-removedirectorya) o [**RemoveDirectoryTransacted**](/windows/desktop/api/WinBase/nf-winbase-removedirectorytransacteda) . Prima di rimuovere una directory, è necessario assicurarsi che la directory sia vuota e che si disponga del privilegio di accesso DELETE per la directory. Per eseguire quest'ultima operazione, chiamare la funzione [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) .

 

 
