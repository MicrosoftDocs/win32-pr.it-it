---
title: Controllo del diritto di accesso a un controllo nell'elenco ACL di un oggetto
description: Per controllare l'accesso a un controllo direttamente nell'ACL di un oggetto, usare la funzione AccessCheckByTypeResultList.
ms.assetid: 5a609622-6a1a-46ae-a336-afec504225c7
ms.tgt_platform: multiple
keywords:
- Controllo di un diritto di accesso a un controllo in un annuncio ACL di oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10170bd496da14657356a2334015975da1cc02ff
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104046551"
---
# <a name="checking-a-control-access-right-in-an-objects-acl"></a>Controllo del diritto di accesso a un controllo nell'elenco ACL di un oggetto

Per controllare l'accesso a un controllo direttamente nell'ACL di un oggetto, usare la funzione [**AccessCheckByTypeResultList**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) . Per utilizzare questa funzione, un'applicazione richiede un puntatore al [**\_ descrittore di sicurezza**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) per l'oggetto anziché un'interfaccia [**IADSSECURITYDESCRIPTOR**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) a un oggetto com del descrittore di sicurezza ADSI.

Usare la procedura seguente per controllare l'accesso per un diritto di accesso controllato su un oggetto:

1.  Ottiene un puntatore di interfaccia [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) all'oggetto.
2.  Usare il metodo [**IDirectoryObject:: GetObjectAttributes**](/windows/desktop/api/iads/nf-iads-idirectoryobject-getobjectattributes) per ottenere il descrittore di sicurezza dell'oggetto. Il nome della proprietà che contiene il descrittore di sicurezza è [**ntSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor). La proprietà viene restituita come puntatore a una struttura di [**\_ descrittori di sicurezza**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) .
3.  Utilizzare la struttura del [**\_ descrittore di sicurezza**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) con la funzione [**AccessCheckByTypeResultList**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) per controllare le autorizzazioni per il diritto di accesso al controllo specificato per il client specificato.

Il codice di esempio nel [codice di esempio per verificare un diritto di accesso al controllo nell'elenco ACL di un oggetto](example-code-for-checking-a-control-access-right-in-an-objectampaposs-acl.md) Mostra in dettaglio come eseguire questa operazione.

 

 