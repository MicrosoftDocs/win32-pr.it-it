---
title: file system distribuito funzioni
description: Di seguito sono riportate le file system distribuito (DFS).
ms.assetid: 8f86b717-fe26-4550-8b71-8f7df5ca6022
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da3fd41879293f376dfdb3d769d5152b2e747fc6e387f8f9538854d4d3e06e7a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096721"
---
# <a name="distributed-file-system-functions"></a>file system distribuito funzioni

Di seguito sono riportate le file system distribuito (DFS).

## <a name="in-this-section"></a>Contenuto della sezione

<dl> <dt>

[NetDfsAdd](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsadd)
</dt> <dd>
Crea un nuovo collegamento file system distribuito (DFS) o aggiunge destinazioni a un collegamento esistente in uno spazio dei nomi DFS.

</dd> <dt>

[NetDfsAddFtRoot](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsaddftroot)
</dt> <dd>
Crea un nuovo spazio dei nomi DFS (Domain-Based File system distribuito). Se lo spazio dei nomi esiste già, la funzione aggiunge la destinazione radice specificata.

</dd> <dt>

[NetDfsAddRootTarget](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsaddroottarget)
</dt> <dd>
Crea uno spazio dei nomi DFS autonomo o basato su dominio o aggiunge una nuova destinazione radice a uno spazio dei nomi esistente basato su dominio.

</dd> <dt>

[NetDfsAddStdRoot](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsaddstdroot)
</dt> <dd>
Crea un nuovo spazio dei nomi file system distribuito (DFS).

</dd> <dt>

[NetDfsEnum](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsenum)
</dt> <dd>
Enumera gli file system distribuito (DFS) ospitati in un server o nei collegamenti DFS di uno spazio dei nomi ospitato da un server.

</dd> <dt>

[NetDfsGetClientInfo](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo)
</dt> <dd>
Recupera informazioni su una radice file system distribuito (DFS) o un collegamento dalla cache gestita dal client DFS.

</dd> <dt>

[NetDfsGetFtContainerSecurity](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetftcontainersecurity)
</dt> <dd>
Recupera il descrittore di sicurezza dell'oggetto contenitore per gli spazi dei nomi DFS basati su dominio nel dominio di Active Directory specificato.

</dd> <dt>

[NetDfsGetInfo](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetinfo)
</dt> <dd>
Recupera informazioni su una radice o un collegamento file system distribuito (DFS) specificato in uno spazio dei nomi DFS.

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
Determina il numero di versione dei metadati supportati.

</dd> <dt>

[NetDfsMove](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsmove)
</dt> <dd>
Rinomina o sposta un collegamento DFS.

</dd> <dt>

[NetDfsRemove](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremove)
</dt> <dd>
Rimuove un collegamento file system distribuito (DFS) o una destinazione di collegamento specifica di un collegamento DFS in uno spazio dei nomi DFS. Quando si rimuove una destinazione di collegamento specifica, il collegamento stesso viene rimosso se viene rimossa l'ultima destinazione del collegamento.

</dd> <dt>

[NetDfsRemoveFtRoot](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveftroot)
</dt> <dd>
Rimuove la destinazione radice specificata da uno spazio dei nomi file system distribuito (DFS) basato su dominio. Se viene rimossa l'ultima destinazione radice dello spazio dei nomi DFS, la funzione elimina anche lo spazio dei nomi DFS. Uno spazio dei nomi DFS può essere eliminato senza prima eliminare tutti i collegamenti al suo interno.

</dd> <dt>

[NetDfsRemoveFtRootForced](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveftrootforced)
</dt> <dd>
Rimuove la destinazione radice specificata da uno spazio dei nomi DFS (Domain-Based File system distribuito), anche se il server di destinazione radice è offline. Se viene rimossa l'ultima destinazione radice dello spazio dei nomi DFS, la funzione elimina anche lo spazio dei nomi DFS. Uno spazio dei nomi DFS può essere eliminato senza prima eliminare tutti i collegamenti al suo interno.

> [!Note]
> La [**funzione NetDfsRemoveFtRootForced**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveftrootforced) non aggiorna il Registro di sistema nel server di destinazione radice DFS. Per altre informazioni, vedere la sezione Osservazioni.

</dd> <dt>

[NetDfsRemoveRootTarget](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveroottarget)
</dt> <dd>
Rimuove una destinazione radice DFS da uno spazio dei nomi DFS basato su dominio. Se la destinazione radice è l'ultima destinazione radice nello spazio dei nomi DFS, questa funzione rimuove lo spazio dei nomi DFS. Questa funzione può essere usata anche per rimuovere uno spazio dei nomi DFS autonomo.

</dd> <dt>

[NetDfsRemoveStdRoot](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremovestdroot)
</dt> <dd>
Elimina uno spazio dei nomi file system distribuito (DFS).

</dd> <dt>

[NetDfsSetClientInfo](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetclientinfo)
</dt> <dd>
Modifica le informazioni su una file system distribuito (DFS) o un collegamento nella cache gestita dal client DFS.

</dd> <dt>

[NetDfsSetFtContainerSecurity](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetftcontainersecurity)
</dt> <dd>
Imposta il descrittore di sicurezza dell'oggetto contenitore per gli spazi dei nomi DFS basati su dominio nel dominio di Active Directory specificato.

</dd> <dt>

[NetDfsSetInfo](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetinfo)
</dt> <dd>
Imposta o modifica le informazioni relative a una file system distribuito,una destinazione radice, un collegamento o una destinazione di collegamento (DFS) specifica.

</dd> <dt>

[NetDfsSetSecurity](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetsecurity)
</dt> <dd>
Imposta il descrittore di sicurezza per l'oggetto radice dello spazio dei nomi DFS specificato.

</dd> <dt>

[NetDfsSetStdContainerSecurity](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetstdcontainersecurity)
</dt> <dd>
Imposta il descrittore di sicurezza per l'oggetto contenitore dello spazio dei nomi DFS autonomo specificato.

</dd> </dl>

Si noti che un'applicazione che richiama una qualsiasi delle funzioni può indirettamente fare in modo che il server dello spazio dei nomi DFS locale che esegue la chiamata di funzione ese venga eseguita una sincronizzazione completa dei metadati dello spazio dei nomi correlati dal master emulatore PDC per tale dominio. Questa sincronizzazione completa può verificarsi anche quando è configurata la modalità di scalabilità radice per tale spazio dei nomi.
