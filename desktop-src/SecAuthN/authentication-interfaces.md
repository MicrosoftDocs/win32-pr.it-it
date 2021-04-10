---
description: Elenca le interfacce nelle API di autenticazione.
ms.assetid: bde3bcae-2152-4589-92a0-b44d98f233ef
title: Interfacce di autenticazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b101fd4fdd3c518d24b5b6f798fcaa4e0327dd22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232048"
---
# <a name="authentication-interfaces"></a>Interfacce di autenticazione

Le interfacce di autenticazione vengono categorizzate in base all'utilizzo come indicato di seguito:

-   [Interfacce smart card](#smart-card-interfaces)
-   [Interfacce di condivisione delle identità](#identity-sharing-interfaces)

## <a name="smart-card-interfaces"></a>Interfacce smart card

Smart Card SDK fornisce le seguenti interfacce COM. I metodi per un'interfaccia specifica sono elencati nel sommario e nella pagina di riferimento per tale interfaccia.



| Interfaccia                                    | Descrizione                                                                                                                                                                              |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IByteBuffer**](ibytebuffer.md)           | Gestisce un oggetto flusso.                                                                                                                                                                 |
| [**Scheda di**](iscard.md)                     | Apre e gestisce una connessione a una [*Smart Card*](/windows/desktop/SecGloss/s-gly).                                                                    |
| [**ISCardAuth**](iscardauth.md)             | Autentica un'applicazione, una smart card o un utente.                                                                                                                                       |
| [**ISCardCmd**](iscardcmd.md)               | Costruisce e gestisce un' [*unità dati del protocollo dell'applicazione*](/windows/desktop/SecGloss/a-gly) Smart Card (APDU). |
| [**ISCardDatabase**](iscarddatabase.md)     | Esegue operazioni del database di [*Resource Manager*](/windows/desktop/SecGloss/r-gly) per smart card.                                              |
| [**ISCardFileAccess**](iscardfileaccess.md) | Esegue Servizi file comuni, ad esempio l'individuazione, la selezione, la lettura, la scrittura, la creazione e l'eliminazione di file.                                                                               |
| [**ISCardISO7816**](iscardiso7816.md)       | Costruisce un comando APDU.                                                                                                                                                              |
| [**ISCardLocate**](iscardlocate.md)         | Individua una smart card.                                                                                                                                                                    |
| [**ISCardManage**](iscardmanage.md)         | Gestisce il sistema di smart card.                                                                                                                                                           |
| [**ISCardTypeConv**](iscardtypeconv.md)     | Fornisce i metodi utilizzati per supportare altre interfacce COM per smart card. Questa interfaccia viene fornita solo per compatibilità con le versioni precedenti e non deve più essere utilizzata.                               |
| [**ISCardVerify**](iscardverify.md)         | Verifica o modifica i criteri di verifica del contenitore di schede (CHV).                                                                                                                               |



 

## <a name="identity-sharing-interfaces"></a>Interfacce di condivisione delle identità

Identity sharing SDK fornisce le seguenti interfacce COM. I metodi per un'interfaccia specifica sono elencati nel sommario e nella pagina di riferimento per tale interfaccia.



| Interfaccia                                                          | Descrizione                                                                              |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [**IAssociatedIdentityProvider**](/windows/desktop/api/IdentityProvider/nn-identityprovider-iassociatedidentityprovider) | Consente a un provider di identità di associare le identità agli account utente locali.            |
| [**IIdentityAdvise**](/windows/desktop/api/IdentityProvider/nn-identityprovider-iidentityadvise)                         | Consente a un provider di identità di notificare un'applicazione chiamante quando viene aggiornata un'identità. |
| [**Metodo IIdentityProvider**](/windows/desktop/api/Identityprovider/nn-identityprovider-iidentityprovider)                     | Rappresenta un provider di identità.                                                         |
| [**IIdentityStore**](/windows/desktop/api/Identitystore/nn-identitystore-iidentitystore)                           | Fornisce metodi per enumerare e gestire identità e provider di identità.              |



 

 

 
