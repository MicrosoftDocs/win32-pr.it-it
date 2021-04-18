---
description: Le funzioni dei file di rete consentono di monitorare e chiudere le risorse di file, dispositivi e pipe aperte in un server. Le funzioni file sono elencate di seguito.
ms.assetid: cbcdad6e-80dd-49f0-9d69-a82a7010f10b
title: Funzioni NetFile (gestione delle condivisioni di rete)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3df51d556647f16cc30ec51182fde5dd5551831d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317099"
---
# <a name="netfile-functions-network-share-management"></a>Funzioni NetFile (gestione delle condivisioni di rete)

Le funzioni dei file di rete consentono di monitorare e chiudere le risorse di file, dispositivi e pipe aperte in un server. Le funzioni file sono elencate di seguito.



| Funzione                                 | Descrizione                                                          |
|------------------------------------------|----------------------------------------------------------------------|
| [**NetFileClose**](/windows/desktop/api/Lmshare/nf-lmshare-netfileclose)     | Impone la chiusura di una risorsa.                                          |
| [**NetFileEnum**](/windows/desktop/api/Lmshare/nf-lmshare-netfileenum)       | Restituisce informazioni sui file aperti in un server.                    |
| [**NetFileGetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netfilegetinfo) | Restituisce informazioni su una particolare apertura di una risorsa server. |



 

Chiamare la funzione [**NetFileClose**](/windows/desktop/api/Lmshare/nf-lmshare-netfileclose) quando il file non può essere chiuso con altri mezzi. Questa funzione deve essere usata con cautela perché **NetFileClose** non scrive i dati memorizzati nella cache del sistema client nel file prima di chiudere il file.

La funzione [**NetFileEnum**](/windows/desktop/api/Lmshare/nf-lmshare-netfileenum) restituisce informazioni sulle risorse aperte in un server. Un file può essere aperto una o più volte da una o più applicazioni. Ogni apertura di file viene identificata in modo univoco. La funzione **NetFileEnum** restituisce una voce per ogni apertura del file. La funzione [**NetFileGetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netfilegetinfo) restituisce informazioni su un'apertura di una risorsa.

Le informazioni sui file sono disponibili ai livelli seguenti.

<dl>

[**Informazioni sul FILE \_ \_ 2**](/windows/desktop/api/Lmshare/ns-lmshare-file_info_2)  
[**Informazioni sul FILE \_ \_ 3**](/windows/desktop/api/Lmshare/ns-lmshare-file_info_3)  
</dl>

I livelli 0 e 1 non sono supportati. Il livello 2 restituisce solo il numero di identificazione assegnato alla risorsa quando è stato aperto. Il livello 3 restituisce il numero di identificazione, le autorizzazioni, i blocchi di file e il nome dell'utente che ha aperto la risorsa.

Se si sta programmando per Active Directory, è possibile chiamare determinati metodi di Active Directory Service Interface (ADSI) per ottenere la stessa funzionalità che è possibile ottenere chiamando le funzioni [**NetFileEnum**](/windows/desktop/api/Lmshare/nf-lmshare-netfileenum) e [**NetFileGetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netfilegetinfo) . Per ulteriori informazioni, vedere [**IADsResource**](/windows/desktop/api/iads/nn-iads-iadsresource) e [**IADsFileServiceOperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations).

 

 
