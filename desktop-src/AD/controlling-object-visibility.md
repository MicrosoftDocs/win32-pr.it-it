---
title: Controllo della visibilità degli oggetti
description: Active Directory Domain Services offrono la possibilità di nascondere gli oggetti degli utenti a cui sono stati negati determinati diritti.
ms.assetid: 3a65ec79-7de0-4d14-b980-1ca6a972ac70
ms.tgt_platform: multiple
keywords:
- controllo della visibilità degli oggetti Active Directory
- Active Directory Active Directory, uso, controllo della visibilità degli oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11b1ab364f0711174d5ac1dd1e4fbe98303c50b3
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104046543"
---
# <a name="controlling-object-visibility"></a>Controllo della visibilità degli oggetti

Active Directory Domain Services offrono la possibilità di nascondere gli oggetti degli utenti a cui sono stati negati determinati diritti. Se un oggetto è nascosto, un'applicazione in esecuzione con le credenziali di un utente non sarà in grado di enumerare o associare all'oggetto.

Se a un utente viene concesso il diritto di accesso [**\_ \_ ACTRL \_ \_ elenco**](/windows/win32/api/iads/ne-iads-ads_rights_enum) di controllo di accesso in un contenitore, l'utente può visualizzare gli oggetti figlio del contenitore. Analogamente, se a un utente viene negato l'elenco di controllo di accesso **\_ \_ ACTRL \_ DS \_ List** right in un contenitore, l'utente non può visualizzare alcuno degli oggetti figlio del contenitore. Ciò consente di nascondere il contenuto di tutti i contenitori.

Il server di Active Directory può anche essere inserito in una speciale modalità oggetto elenco impostando il terzo carattere della proprietà [**dsHeuristics**](/windows/desktop/ADSchema/a-dsheuristics) su "1". La modalità oggetto elenco può essere disabilitata impostando il terzo carattere della proprietà **dsHeuristics** su "0". Quando il server Active Directory è in modalità oggetto elenco, un oggetto sarà ancora visibile se all'utente è stato concesso l' [**elenco Rights \_ \_ ACTRL \_ DS \_ ADS**](/windows/win32/api/iads/ne-iads-ads_rights_enum) Right nell'oggetto padre. Se, tuttavia, all'utente è stato negato l' **elenco degli annunci \_ right \_ ACTRL \_ \_ DS** Right nell'elemento padre, gli oggetti figlio specifici possono comunque essere resi visibili se all'utente viene concesso l' **\_ \_ \_ \_ oggetto List Rights DS ADS** direttamente negli oggetti padre e figlio. La modalità oggetto elenco consente all'amministratore di sistema di concedere o negare l'accesso a singoli oggetti per utenti o gruppi. La modalità oggetto elenco deve essere utilizzata con moderazione, perché richiede un numero significativamente più elevato di chiamate di controllo di accesso che devono essere eseguite dal servizio directory per determinare se un oggetto è visibile a un utente. Può quindi avere un effetto negativo sulle prestazioni di esplorazione o lettura di oggetti da Active Directory Domain Services.

 

 