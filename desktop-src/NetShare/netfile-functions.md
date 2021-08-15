---
description: Le funzioni dei file di rete consentono di monitorare e chiudere le risorse di file, dispositivo e pipe aperte in un server. Di seguito sono elencate le funzioni di file.
ms.assetid: cbcdad6e-80dd-49f0-9d69-a82a7010f10b
title: Funzioni NetFile (Gestione condivisione di rete)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8efdd1a9339701ccbb534a91b9dfe0423bea546e8d474455c2a6ffdda02adab1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118362612"
---
# <a name="netfile-functions-network-share-management"></a>Funzioni NetFile (Gestione condivisione di rete)

Le funzioni dei file di rete consentono di monitorare e chiudere le risorse di file, dispositivo e pipe aperte in un server. Di seguito sono elencate le funzioni di file.



| Funzione                                 | Descrizione                                                          |
|------------------------------------------|----------------------------------------------------------------------|
| [**NetFileClose**](/windows/desktop/api/Lmshare/nf-lmshare-netfileclose)     | Forza la chiusura di una risorsa.                                          |
| [**NetFileEnum**](/windows/desktop/api/Lmshare/nf-lmshare-netfileenum)       | Restituisce informazioni sui file aperti in un server.                    |
| [**NetFileGetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netfilegetinfo) | Restituisce informazioni su una particolare apertura di una risorsa server. |



 

Chiamare la [**funzione NetFileClose**](/windows/desktop/api/Lmshare/nf-lmshare-netfileclose) quando il file non può essere chiuso con altri mezzi. Questa funzione deve essere usata con cautela perché **NetFileClose** non scrive i dati memorizzati nella cache del sistema client nel file prima di chiudere il file.

La [**funzione NetFileEnum**](/windows/desktop/api/Lmshare/nf-lmshare-netfileenum) restituisce informazioni sulle risorse aperte in un server. Un file può essere aperto una o più volte da una o più applicazioni. Ogni apertura di file viene identificata in modo univoco. La **funzione NetFileEnum** restituisce una voce per ogni apertura di file. La [**funzione NetFileGetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netfilegetinfo) restituisce informazioni su un'apertura di una risorsa.

Le informazioni sui file sono disponibili ai livelli seguenti.

<dl>

[**FILE \_ INFO \_ 2**](/windows/desktop/api/Lmshare/ns-lmshare-file_info_2)  
[**FILE \_ INFO \_ 3**](/windows/desktop/api/Lmshare/ns-lmshare-file_info_3)  
</dl>

I livelli 0 e 1 non sono supportati. Il livello 2 restituisce solo il numero di identificazione assegnato alla risorsa al momento dell'apertura. Il livello 3 restituisce il numero di identificazione, le autorizzazioni, i blocchi di file e il nome dell'utente che ha aperto la risorsa.

Se si programma per Active Directory, è possibile chiamare determinati metodi ADSI (Active Directory Service Interface) per ottenere le stesse funzionalità che è possibile ottenere chiamando le funzioni [**NetFileEnum**](/windows/desktop/api/Lmshare/nf-lmshare-netfileenum) e [**NetFileGetInfo.**](/windows/desktop/api/Lmshare/nf-lmshare-netfilegetinfo) Per altre informazioni, vedere [**IADsResource**](/windows/desktop/api/iads/nn-iads-iadsresource) e [**IADsFileServiceOperations.**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations)

 

 
