---
description: Windows Il programma di installazione 5.0 in esecuzione in Windows Server 2008 R2 o Windows 7 può enumerare tutti i componenti installati nel computer e ottenere il percorso della chiave per il componente.
ms.assetid: a6676340-1695-48c7-a1e4-7a02a7bc3fef
title: Enumerazione dei componenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 598e80e270d0442b06fdb6db50cc5b58df529a1305936f2610211f192c8572be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947042"
---
# <a name="enumerating-components"></a>Enumerazione dei componenti

Windows Il programma di installazione 5.0 in esecuzione in Windows Server 2008 R2 o Windows 7 può enumerare tutti i componenti installati nel computer e ottenere il percorso della chiave per il componente. Un pacchetto creato per Windows Installer 5.0 può usare le funzioni [**MsiEnumComponentsEx**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsexa), [**MsiEnumClientsEx**](/windows/desktop/api/Msi/nf-msi-msienumclientsexa)e [**MsiGetComponentPathEx**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa) per cercare componenti e prodotti tra account utente e contesti di installazione. Le [**funzioni MsiEnumComponents**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsa), [**MsiEnumClients**](/windows/desktop/api/Msi/nf-msi-msienumclientsa)e [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) restituiscono informazioni solo per i componenti e i prodotti installati per l'account utente che ha chiamato la funzione. Sono necessarie più chiamate a queste funzioni, almeno una volta per ogni account utente, per raccogliere informazioni per l'intero computer.

La [**funzione MsiEnumComponentsEx**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsexa) enumera i componenti installati. La funzione recupera un codice componente ogni volta che viene chiamata. [**L'oggetto Component**](components.md) riceve informazioni su un componente installato da questa funzione.

La [**funzione MsiEnumClientsEx**](/windows/desktop/api/Msi/nf-msi-msienumclientsexa) enumera i prodotti che sono client di un componente installato specificato. [**L'oggetto client**](client.md) riceve informazioni su un client da questa funzione.

La [**funzione MsiGetComponentPathEx**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa) restituisce il percorso completo di un componente installato. La funzione restituisce la chiave del Registro di sistema se il percorso della chiave per il componente è una chiave del Registro di sistema. [**L'oggetto ComponentInfo**](componentinfo.md) riceve informazioni su un componente installato da questa funzione.

**[Windows Installer 4.5 o versioni precedenti:](not-supported-in-windows-installer-4-5.md)** Non supportato. Questa funzionalità è disponibile a partire da Windows Installer 5.0 in esecuzione in Windows 7 o Windows Server 2008 R2.

 

 



