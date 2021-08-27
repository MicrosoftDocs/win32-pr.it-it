---
description: Server-Side per la rappresentazione
ms.assetid: f6128688-dfd8-40ff-83ec-99d740b9152c
title: Server-Side per la rappresentazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18e43016428f2ff083fc5a783d05c3c79e241dcf299f3af9ca226cb4f6a2cf1b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096801"
---
# <a name="server-side-requirements-for-impersonation"></a>Server-Side per la rappresentazione

Il server esegue la rappresentazione a livello di codice. Presuppone in modo esplicito le credenziali di sicurezza del client usando [**CoImpersonateClient.**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient) Quando il client ha concesso al server un'autorità sufficiente, ciò ha l'effetto di sostituire le credenziali di sicurezza del client con il token del thread del server, al posto del token di processo.

Al termine di questa operazione, il server può, ad esempio, usare il token client per accedere alle risorse sorvegliate con un descrittore di sicurezza. Oppure può effettuare chiamate con l'identità client, se la clonazione è abilitata.

Il server può impostare in modo esplicito la clonazione a livello di codice oppure può basarsi su un'impostazione amministrativa. Per impostazione predefinita, le applicazioni COM+ sono configurate per l'uso della clonazione dinamica. Per altri dettagli, vedere [Cloaking](cloaking.md).

Se il server implementa la delega per conto del client, usando l'identità client in rete, l'identità del processo server deve essere contrassegnata come "Trusted per la delega" nel servizio Active Directory; In caso contrario, la delega avrà esito negativo.

Al termine dell'uso dell'identità del client, il server può ripristinare il proprio token di processo [**usando CoRevertToSelf.**](/windows/desktop/api/combaseapi/nf-combaseapi-coreverttoself)

Per informazioni dettagliate sull'implementazione della rappresentazione e della delega, vedere [Delega e rappresentazione.](/windows/desktop/com/delegation-and-impersonation)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Rappresentazione e delega del client](client-impersonation-and-delegation.md)
</dt> <dt>

[Requisiti lato client per la rappresentazione](client-side-requirements-for-impersonation.md)
</dt> <dt>

[Cloaking](cloaking.md)
</dt> </dl>

 

 
