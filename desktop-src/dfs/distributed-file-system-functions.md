---
title: Funzioni file system distribuito
description: Di seguito sono riportate le funzioni file system distribuito (DFS).
ms.assetid: 8f86b717-fe26-4550-8b71-8f7df5ca6022
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 463c085115f6d3e88f9a3be80a890caa0aacb340
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483765"
---
# <a name="distributed-file-system-functions"></a>Funzioni file system distribuito

Di seguito sono riportate le funzioni file system distribuito (DFS).

## <a name="in-this-section"></a>Contenuto della sezione

<dl> <dt>

[NetDfsAdd](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsadd)
</dt> <dd>
Crea un nuovo collegamento file system distribuito (DFS) o aggiunge destinazioni a un collegamento esistente in uno spazio dei nomi DFS.

</dd> <dt>

[NetDfsAddFtRoot](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsaddftroot)
</dt> <dd>
Crea un nuovo spazio dei nomi di file system distribuito basato su dominio (DFS). Se lo spazio dei nomi esiste già, la funzione aggiunge la destinazione radice specificata.

</dd> <dt>

[NetDfsAddRootTarget](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsaddroottarget)
</dt> <dd>
Consente di creare uno spazio dei nomi DFS basato su dominio o autonomo o di aggiungere una nuova destinazione radice a uno spazio dei nomi basato su dominio esistente.

</dd> <dt>

[NetDfsAddStdRoot](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsaddstdroot)
</dt> <dd>
Crea un nuovo spazio dei nomi di file system distribuito autonomo (DFS).

</dd> <dt>

[NetDfsEnum](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsenum)
</dt> <dd>
Enumera gli spazi dei nomi file system distribuito (DFS) ospitati in un server o in un collegamento DFS di uno spazio dei nomi ospitato da un server.

</dd> <dt>

[NetDfsGetClientInfo](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo)
</dt> <dd>
Recupera le informazioni su una radice file system distribuito (DFS) o un collegamento dalla cache gestita dal client DFS.

</dd> <dt>

[NetDfsGetFtContainerSecurity](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetftcontainersecurity)
</dt> <dd>
Recupera il descrittore di sicurezza dell'oggetto contenitore per gli spazi dei nomi DFS basati su dominio nel dominio di Active Directory specificato.

</dd> <dt>

[NetDfsGetInfo](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetinfo)
</dt> <dd>
Recupera le informazioni relative a una radice file system distribuito (DFS) specificata o a un collegamento in uno spazio dei nomi DFS.

</dd> <dt>

[NetDfsGetSecurity](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetsecurity)
</dt> <dd>
Recupera il descrittore di sicurezza per l'oggetto radice dello spazio dei nomi DFS specificato.

</dd> <dt>

[NetDfsGetStdContainerSecurity](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetstdcontainersecurity)
</dt> <dd>
Recupera il descrittore di sicurezza per l'oggetto contenitore dello spazio dei nomi DFS autonomo specificato.

</dd> <dt>

[NetDfsGetSupportedNamespaceVersion](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetsupportednamespaceversion)
</dt> <dd>
Determina il numero di versione dei metadati supportata.

</dd> <dt>

[NetDfsMove](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsmove)
</dt> <dd>
Rinomina o sposta un collegamento DFS.

</dd> <dt>

[NetDfsRemove](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremove)
</dt> <dd>
Rimuove un collegamento di file system distribuito (DFS) o una destinazione di collegamento specifica di un collegamento DFS in uno spazio dei nomi DFS. Quando si rimuove una destinazione di collegamento specifica, il collegamento viene rimosso se viene rimossa l'ultima destinazione del collegamento del collegamento.

</dd> <dt>

[NetDfsRemoveFtRoot](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveftroot)
</dt> <dd>
Rimuove la destinazione radice specificata da uno spazio dei nomi di file system distribuito basato su dominio (DFS). Se è in corso la rimozione dell'ultima destinazione radice dello spazio dei nomi DFS, la funzione eliminerà anche lo spazio dei nomi DFS. È possibile eliminare uno spazio dei nomi DFS senza prima eliminare tutti i relativi collegamenti.

</dd> <dt>

[NetDfsRemoveFtRootForced](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveftrootforced)
</dt> <dd>
Rimuove la destinazione radice specificata da uno spazio dei nomi file system distribuito (DFS) basato su dominio, anche se il server di destinazione radice è offline. Se è in corso la rimozione dell'ultima destinazione radice dello spazio dei nomi DFS, la funzione eliminerà anche lo spazio dei nomi DFS. È possibile eliminare uno spazio dei nomi DFS senza prima eliminare tutti i relativi collegamenti.

> [!Note]
> La funzione [**NetDfsRemoveFtRootForced**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveftrootforced) non aggiorna il registro di sistema nel server di destinazione radice DFS. Per altre informazioni, vedere la sezione Osservazioni.

</dd> <dt>

[NetDfsRemoveRootTarget](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveroottarget)
</dt> <dd>
Rimuove una destinazione radice DFS da uno spazio dei nomi DFS basato su dominio. Se la destinazione radice è l'ultima destinazione radice nello spazio dei nomi DFS, questa funzione rimuove lo spazio dei nomi DFS. Questa funzione può essere utilizzata anche per rimuovere uno spazio dei nomi DFS autonomo.

</dd> <dt>

[NetDfsRemoveStdRoot](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremovestdroot)
</dt> <dd>
Elimina uno spazio dei nomi di file system distribuito autonomo (DFS).

</dd> <dt>

[NetDfsSetClientInfo](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetclientinfo)
</dt> <dd>
Modifica le informazioni relative a una radice file system distribuito (DFS) o a un collegamento nella cache gestita dal client DFS.

</dd> <dt>

[NetDfsSetFtContainerSecurity](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetftcontainersecurity)
</dt> <dd>
Imposta il descrittore di sicurezza dell'oggetto contenitore per gli spazi dei nomi DFS basati su dominio nel dominio di Active Directory specificato.

</dd> <dt>

[NetDfsSetInfo](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetinfo)
</dt> <dd>
Imposta o modifica le informazioni relative a una radice file system distribuito (DFS), una destinazione radice, un collegamento o una destinazione di collegamento specifici.

</dd> <dt>

[NetDfsSetSecurity](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetsecurity)
</dt> <dd>
Imposta il descrittore di sicurezza per l'oggetto radice dello spazio dei nomi DFS specificato.

</dd> <dt>

[NetDfsSetStdContainerSecurity](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetstdcontainersecurity)
</dt> <dd>
Imposta il descrittore di sicurezza per l'oggetto contenitore dello spazio dei nomi DFS autonomo specificato.

</dd> </dl>

Si noti che un'applicazione che richiama una delle funzioni può causare indirettamente al server dello spazio dei nomi DFS locale di gestire la chiamata di funzione per eseguire una sincronizzazione completa dei metadati dello spazio dei nomi correlati dal master emulatore PDC per quel dominio. Questa sincronizzazione completa potrebbe verificarsi anche quando è configurata la modalità di scalabilità radice per lo spazio dei nomi.
