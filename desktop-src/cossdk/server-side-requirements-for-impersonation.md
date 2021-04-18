---
description: Server-Side requisiti per la rappresentazione
ms.assetid: f6128688-dfd8-40ff-83ec-99d740b9152c
title: Server-Side requisiti per la rappresentazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e30edbebd37035ab7a7f4ca09e1cff73c2afbabe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304808"
---
# <a name="server-side-requirements-for-impersonation"></a>Server-Side requisiti per la rappresentazione

Il server esegue la rappresentazione a livello di codice. Presuppone in modo esplicito le credenziali di sicurezza del client usando [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient). Quando il client ha concesso al server un'autorità sufficiente, questo ha l'effetto di sostituire le credenziali di sicurezza del client con il token del thread del server, al posto del token di processo.

Al termine di questa operazione, il server può, ad esempio, usare il token client per accedere alle risorse sorvegliate con un descrittore di sicurezza. In alternativa, può effettuare chiamate sotto l'identità del client, se il mascheramento è abilitato.

Il server può impostare in modo esplicito il mascheramento a livello di codice oppure può basarsi su un'impostazione amministrativa. Per impostazione predefinita, le applicazioni COM+ sono configurate per l'utilizzo del mascheramento dinamico. Per informazioni dettagliate, vedere [mascheramento](cloaking.md).

Se il server sta implementando la delega per conto del client, utilizzando l'identità client sulla rete, l'identità del processo server deve essere contrassegnata come "trusted per la delega" nel servizio Active Directory; in caso contrario, la delega avrà esito negativo.

Al termine dell'utilizzo dell'identità del client, il server può ripristinare il proprio token di processo utilizzando [**CoRevertToSelf**](/windows/desktop/api/combaseapi/nf-combaseapi-coreverttoself).

Per informazioni dettagliate sull'implementazione della rappresentazione e della delega, vedere [delega e rappresentazione](/windows/desktop/com/delegation-and-impersonation).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Rappresentazione e delega client](client-impersonation-and-delegation.md)
</dt> <dt>

[Requisiti lato client per la rappresentazione](client-side-requirements-for-impersonation.md)
</dt> <dt>

[Cloaking](cloaking.md)
</dt> </dl>

 

 
