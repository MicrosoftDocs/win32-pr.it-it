---
description: Uno spazio dei nomi di oggetto protegge gli oggetti denominati da accessi non autorizzati.
ms.assetid: 6a84ec16-fa65-4cdd-861a-eccf5d0eee2b
title: Spazi dei nomi degli oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c3eed750bc91c128251cc66fd7f9ed167771150
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882054"
---
# <a name="object-namespaces"></a>Spazi dei nomi degli oggetti

Uno *spazio dei nomi di oggetto* protegge gli oggetti denominati da accessi non autorizzati. La creazione di uno spazio dei nomi privato consente ad applicazioni e servizi di creare un ambiente più sicuro.

Un processo può creare uno spazio dei nomi privato utilizzando la funzione [**CreatePrivateNamespace**](/windows/desktop/api/WinBase/nf-winbase-createprivatenamespacea) . Questa funzione richiede l'impostazione di un *limite* che definisce la modalità di isolamento degli oggetti nello spazio dei nomi. Il chiamante deve essere all'interno del limite specificato affinché l'operazione di creazione abbia esito positivo. Per specificare un limite, usare le funzioni [**CreateBoundaryDescriptor**](/windows/desktop/api/WinBase/nf-winbase-createboundarydescriptora) e [**AddSIDToBoundaryDescriptor**](/windows/win32/api/namespaceapi/nf-namespaceapi-addsidtoboundarydescriptor) .

Il parametro *lpAliasPrefix* di [**CreatePrivateNamespace**](/windows/desktop/api/WinBase/nf-winbase-createprivatenamespacea) funge da nome dello spazio dei nomi. Ogni spazio dei nomi viene identificato in modo univoco in base al nome e ai limiti. Il sistema supporta più spazi dei nomi privati con lo stesso nome, purché specifichino limiti diversi.

Si supponga che un processo richieda la creazione di uno spazio dei nomi, NS1, che definisce un limite contenente due elementi: il SID amministratore e il numero della sessione corrente. Lo spazio dei nomi viene creato se il processo è in esecuzione con l'account amministratore nella sessione specificata. Un altro processo può accedere a questo spazio dei nomi utilizzando la funzione [**OpenPrivateNamespace**](/windows/desktop/api/WinBase/nf-winbase-openprivatenamespacea) . Il nome e il limite specificati devono corrispondere se questo processo è in grado di aprire lo spazio dei nomi creato dal primo processo. Si noti che un processo può aprire uno spazio dei nomi esistente anche se non si trova all'interno del limite, a meno che l'autore non abbia limitato l'accesso allo spazio dei nomi tramite il parametro *lpPrivateNamespaceAttributes* .

Gli oggetti creati in questo spazio dei nomi hanno nomi nel formato *prefisso* \\ *nomeoggetto*. Il prefisso è il nome dello spazio dei nomi specificato dal parametro *lpAliasPrefix* di [**CreatePrivateNamespace**](/windows/desktop/api/WinBase/nf-winbase-createprivatenamespacea). Per creare, ad esempio, un oggetto evento denominato MyNamespace nello spazio dei nomi NS1, chiamare la funzione [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) con il parametro *LPNAME* impostato su NS1 \\ .

Il processo che ha creato lo spazio dei nomi può utilizzare la funzione [**ClosePrivateNamespace**](/windows/win32/api/namespaceapi/nf-namespaceapi-closeprivatenamespace) per chiudere l'handle allo spazio dei nomi. L'handle viene chiuso anche quando termina il processo che ha creato lo spazio dei nomi. Dopo la chiusura dell'handle dello spazio dei nomi, le chiamate successive a [**OpenPrivateNamespace**](/windows/desktop/api/WinBase/nf-winbase-openprivatenamespacea) hanno esito negativo, ma tutte le operazioni sugli oggetti nello spazio dei nomi vengono eseguite correttamente

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Spazi dei nomi dell'oggetto kernel](../termserv/kernel-object-namespaces.md)
</dt> </dl>

 

 
