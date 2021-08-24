---
description: Elenca le interfacce nelle API di autenticazione.
ms.assetid: bde3bcae-2152-4589-92a0-b44d98f233ef
title: Interfacce di autenticazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6843385004095499a59593bf548ff21998c4079e48667ea0e472e4a55d1f57ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141404"
---
# <a name="authentication-interfaces"></a>Interfacce di autenticazione

Le interfacce di autenticazione vengono categorizzate in base all'utilizzo, come indicato di seguito:

-   [Interfacce smart card](#smart-card-interfaces)
-   [Interfacce di condivisione delle identità](#identity-sharing-interfaces)

## <a name="smart-card-interfaces"></a>Interfacce smart card

Smart Card SDK fornisce le interfacce COM seguenti. I metodi per un'interfaccia specifica sono elencati nel sommario e nella pagina di riferimento per tale interfaccia.



| Interfaccia                                    | Descrizione                                                                                                                                                                              |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IByteBuffer**](ibytebuffer.md)           | Gestisce un oggetto flusso.                                                                                                                                                                 |
| [**ISCard**](iscard.md)                     | Apre e gestisce una connessione a un smart card [*.*](/windows/desktop/SecGloss/s-gly)                                                                    |
| [**ISCardAuth**](iscardauth.md)             | Autentica un'applicazione, smart card o un utente.                                                                                                                                       |
| [**ISCardCmd**](iscardcmd.md)               | Costruisce e gestisce un'smart card [*application protocol data unit*](/windows/desktop/SecGloss/a-gly) (APDU). |
| [**ISCardDatabase**](iscarddatabase.md)     | Esegue smart card di database [*di Resource Manager.*](/windows/desktop/SecGloss/r-gly)                                              |
| [**ISCardFileAccess**](iscardfileaccess.md) | Esegue servizi di file comuni, ad esempio l'individuazione, la selezione, la lettura, la scrittura, la creazione e l'eliminazione di file.                                                                               |
| [**ISCardISO7816**](iscardiso7816.md)       | Costruisce un comando APDU.                                                                                                                                                              |
| [**ISCardLocate**](iscardlocate.md)         | Individua un smart card.                                                                                                                                                                    |
| [**ISCardManage**](iscardmanage.md)         | Gestisce il smart card sistema.                                                                                                                                                           |
| [**ISCardTypeConv**](iscardtypeconv.md)     | Fornisce metodi usati per supportare altre smart card COM. Questa interfaccia viene fornita solo per la compatibilità con le versioni precedenti e non deve più essere usata.                               |
| [**ISCardVerify**](iscardverify.md)         | Verifica o modifica i criteri di verifica del titolare della carta (CHV).                                                                                                                               |



 

## <a name="identity-sharing-interfaces"></a>Interfacce di condivisione delle identità

Identity Sharing SDK fornisce le interfacce COM seguenti. I metodi per un'interfaccia specifica sono elencati nel sommario e nella pagina di riferimento per tale interfaccia.



| Interfaccia                                                          | Descrizione                                                                              |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [**IAssociatedIdentityProvider**](/windows/desktop/api/IdentityProvider/nn-identityprovider-iassociatedidentityprovider) | Consente a un provider di identità di associare le identità agli account utente locali.            |
| [**IIdentityAdvise**](/windows/desktop/api/IdentityProvider/nn-identityprovider-iidentityadvise)                         | Consente a un provider di identità di inviare una notifica a un'applicazione chiamante quando viene aggiornata un'identità. |
| [**IIdentityProvider**](/windows/desktop/api/Identityprovider/nn-identityprovider-iidentityprovider)                     | Rappresenta un provider di identità.                                                         |
| [**IIdentityStore**](/windows/desktop/api/Identitystore/nn-identitystore-iidentitystore)                           | Fornisce metodi per enumerare e gestire identità e provider di identità.              |



 

 

 
