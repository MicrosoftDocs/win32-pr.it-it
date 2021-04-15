---
title: Funzioni NetFile (gestione della rete)
description: Le funzioni del file di gestione di rete consentono di monitorare e chiudere le risorse di file, dispositivi e pipe aperte in un server. Le funzioni file sono elencate di seguito.
ms.assetid: 3cfb5222-7e02-4bc3-959e-0fc7bc4f0f19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46b56d1c6d50463989e64386f5829a8e663cddd4
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104517307"
---
# <a name="netfile-functions-network-management"></a>Funzioni NetFile (gestione della rete)

Le funzioni del file di gestione di rete consentono di monitorare e chiudere le risorse di file, dispositivi e pipe aperte in un server. Le funzioni file sono elencate di seguito.



| Funzione                                | Descrizione                                                          |
|-----------------------------------------|----------------------------------------------------------------------|
| [**NetFileClose**](/windows/desktop/api/lmshare/nf-lmshare-netfileclose)     | Impone la chiusura di una risorsa.                                          |
| [**NetFileEnum**](/windows/desktop/api/lmshare/nf-lmshare-netfileenum)       | Restituisce informazioni sui file aperti in un server.                    |
| [**NetFileGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netfilegetinfo) | Restituisce informazioni su una particolare apertura di una risorsa server. |



 

Chiamare la funzione [**NetFileClose**](/windows/desktop/api/lmshare/nf-lmshare-netfileclose) quando il file non può essere chiuso con altri mezzi. Questa funzione deve essere usata con cautela perché **NetFileClose** non scrive i dati memorizzati nella cache del sistema client nel file prima di chiudere il file.

La funzione [**NetFileEnum**](/windows/desktop/api/lmshare/nf-lmshare-netfileenum) restituisce informazioni sulle risorse aperte in un server. Un file può essere aperto una o più volte da una o più applicazioni. Ogni apertura di file viene identificata in modo univoco. La funzione **NetFileEnum** restituisce una voce per ogni apertura del file. La funzione [**NetFileGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netfilegetinfo) restituisce informazioni su un'apertura di una risorsa.

Le informazioni sui file sono disponibili ai livelli seguenti:

-   [**Informazioni sul FILE \_ \_ 2**](/windows/desktop/api/lmshare/ns-lmshare-file_info_2)
-   [**Informazioni sul FILE \_ \_ 3**](/windows/desktop/api/lmshare/ns-lmshare-file_info_3)

I livelli 0 e 1 non sono supportati. Il livello 2 restituisce solo il numero di identificazione assegnato alla risorsa quando è stato aperto. Il livello 3 restituisce il numero di identificazione, le autorizzazioni, i blocchi di file e il nome dell'utente che ha aperto la risorsa.

Se si sta programmando per Active Directory, è possibile chiamare determinati metodi di Active Directory Service Interface (ADSI) per ottenere la stessa funzionalità che è possibile ottenere chiamando le funzioni [**NetFileEnum**](/windows/desktop/api/lmshare/nf-lmshare-netfileenum) e [**NetFileGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netfilegetinfo) . Per ulteriori informazioni, vedere [**IADsResource**](/windows/desktop/api/iads/nn-iads-iadsresource) e [**IADsFileServiceOperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations).

 

 
