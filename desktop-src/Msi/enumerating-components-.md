---
description: Windows Installer 5,0 in esecuzione in Windows Server 2008 R2 o Windows 7 è possibile enumerare tutti i componenti installati nel computer e ottenere il percorso della chiave per il componente.
ms.assetid: a6676340-1695-48c7-a1e4-7a02a7bc3fef
title: Enumerazione dei componenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea314ee91c35fb021f5a8da64b6430e8cf950ecd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755418"
---
# <a name="enumerating-components"></a>Enumerazione dei componenti

Windows Installer 5,0 in esecuzione in Windows Server 2008 R2 o Windows 7 è possibile enumerare tutti i componenti installati nel computer e ottenere il percorso della chiave per il componente. Un pacchetto creato per Windows Installer 5,0 può utilizzare le funzioni [**MsiEnumComponentsEx**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsexa), [**MsiEnumClientsEx**](/windows/desktop/api/Msi/nf-msi-msienumclientsexa)e [**MsiGetComponentPathEx**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa) per cercare componenti e prodotti tra gli account utente e i contesti di installazione. Le funzioni [**MsiEnumComponents**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsa), [**MsiEnumClients**](/windows/desktop/api/Msi/nf-msi-msienumclientsa)e [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) restituiscono solo le informazioni per i componenti e i prodotti installati per l'account utente che ha chiamato la funzione. Per raccogliere informazioni per l'intero computer, sono necessarie più chiamate a queste funzioni, almeno una volta per ogni account utente.

La funzione [**MsiEnumComponentsEx**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsexa) enumera i componenti installati. La funzione recupera un codice componente ogni volta che viene chiamato. L' [**oggetto Component**](components.md) riceve informazioni su un componente installato da questa funzione.

La funzione [**MsiEnumClientsEx**](/windows/desktop/api/Msi/nf-msi-msienumclientsexa) enumera i prodotti che sono client di un componente installato specificato. L' [**oggetto client**](client.md) riceve le informazioni relative a un client da questa funzione.

La funzione [**MsiGetComponentPathEx**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa) restituisce il percorso completo di un componente installato. La funzione restituisce la chiave del registro di sistema se il percorso della chiave per il componente è una chiave del registro di sistema. L' [**oggetto ComponentInfo**](componentinfo.md) riceve informazioni su un componente installato da questa funzione.

**[Windows Installer 4,5 o versioni precedenti](not-supported-in-windows-installer-4-5.md):** Non supportato. Questa funzionalità è disponibile a partire da Windows Installer 5,0 in esecuzione in Windows 7 o Windows Server 2008 R2.

 

 



