---
description: Uno spazio dei nomi dell'oggetto protegge gli oggetti denominati da accessi non autorizzati.
ms.assetid: 6a84ec16-fa65-4cdd-861a-eccf5d0eee2b
title: Spazi dei nomi degli oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6137d53e45f27a8de2c76075bc2a5565a5942bd38bf6fa3cd3891e4561870b8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117765488"
---
# <a name="object-namespaces"></a>Spazi dei nomi degli oggetti

Uno spazio *dei nomi dell'oggetto* protegge gli oggetti denominati da accessi non autorizzati. La creazione di uno spazio dei nomi privato consente ad applicazioni e servizi di creare un ambiente più sicuro.

Un processo può creare uno spazio dei nomi privato usando [**la funzione CreatePrivateNamespace.**](/windows/desktop/api/WinBase/nf-winbase-createprivatenamespacea) Questa funzione richiede di specificare un *limite che* definisce come devono essere isolati gli oggetti nello spazio dei nomi. Il chiamante deve essere all'interno del limite specificato perché l'operazione di creazione riesca. Per specificare un limite, usare le [**funzioni CreateBoundaryDescriptor**](/windows/desktop/api/WinBase/nf-winbase-createboundarydescriptora) [**e AddSIDToBoundaryDescriptor.**](/windows/win32/api/namespaceapi/nf-namespaceapi-addsidtoboundarydescriptor)

Il *parametro lpAliasPrefix* di [**CreatePrivateNamespace**](/windows/desktop/api/WinBase/nf-winbase-createprivatenamespacea) funge da nome dello spazio dei nomi. Ogni spazio dei nomi viene identificato in modo univoco in base al nome e ai limiti. Il sistema supporta più spazi dei nomi privati con lo stesso nome, purché specificano limiti diversi.

Si supponga che un processo richiede la creazione di uno spazio dei nomi, NS1, che definisce un limite contenente due elementi: il SID dell'amministratore e il numero di sessione corrente. Lo spazio dei nomi viene creato se il processo viene eseguito con l'account Administrator nella sessione specificata. Un altro processo può accedere a questo spazio dei nomi [**usando la funzione OpenPrivateNamespace.**](/windows/desktop/api/WinBase/nf-winbase-openprivatenamespacea) Il nome e il limite specificati devono corrispondere se questo processo deve aprire lo spazio dei nomi creato dal primo processo. Si noti che un processo può aprire uno spazio dei nomi esistente anche se non si trova all'interno del limite, a meno che l'autore non ha limitato l'accesso allo spazio dei nomi usando il *parametro lpPrivateNamespaceAttributes.*

Gli oggetti creati in questo spazio dei nomi hanno nomi nel formato *prefisso* \\ *objectname*. Il prefisso è il nome dello spazio dei nomi specificato *dal parametro lpAliasPrefix* di [**CreatePrivateNamespace.**](/windows/desktop/api/WinBase/nf-winbase-createprivatenamespacea) Ad esempio, per creare un oggetto evento denominato MyEvent nello spazio dei nomi NS1, chiamare la funzione [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) con il parametro *lpName* impostato su NS1 \\ MyEvent.

Il processo che ha creato lo spazio dei nomi può usare [**la funzione ClosePrivateNamespace**](/windows/win32/api/namespaceapi/nf-namespaceapi-closeprivatenamespace) per chiudere l'handle dello spazio dei nomi. L'handle viene chiuso anche quando termina il processo che ha creato lo spazio dei nomi. Dopo la chiusura dell'handle dello spazio dei nomi, le chiamate successive a [**OpenPrivateNamespace**](/windows/desktop/api/WinBase/nf-winbase-openprivatenamespacea) hanno esito negativo, ma tutte le operazioni sugli oggetti nello spazio dei nomi hanno esito positivo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Spazi dei nomi degli oggetti kernel](../termserv/kernel-object-namespaces.md)
</dt> </dl>

 

 
