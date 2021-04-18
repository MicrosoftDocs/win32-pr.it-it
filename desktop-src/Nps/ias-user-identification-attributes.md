---
title: Attributi di identificazione utente
description: L'identità dell'utente che richiede l'autenticazione viene fornita alle DLL di estensione NPS in una serie di attributi diversi.
ms.assetid: 2f741a81-e432-47fe-a14a-8b77ecd41e28
ms.tgt_platform: multiple
keywords:
- Attributi, identificazione utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 527bdffad376ce92fa2fd7c5d5330fb752fea6aa
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300151"
---
# <a name="user-identification-attributes"></a>Attributi di identificazione utente

> [!Note]  
> Il servizio di autenticazione Internet (IAS) è stato rinominato server dei criteri di rete (NPS) a partire da Windows Server 2008. Il contenuto di questo argomento si applica sia a IAS che a NPS. In tutto il testo, NPS viene utilizzato per fare riferimento a tutte le versioni del servizio, incluse le versioni originariamente indicate come IAS.

 

L'identità dell'utente che richiede l'autenticazione viene fornita alle DLL di estensione NPS in una serie di attributi diversi.

-   **ratUserName**
-   **ratStrippedUserName**
-   **ratFQUserName**

Ogni attributo fornisce l'identità dell'utente in un formato diverso. In generale, gli sviluppatori devono usare **ratStrippedUserName**. Gli utilizzi degli attributi **ratUserName** e **ratFQUserName** sono più specializzati.

> [!Note]  
> L'attributo User-Password, **ratUserPassword**, è già stato decrittografato quando viene inviato alla DLL di estensione ed è utilizzabile in tale formato.

 

## <a name="ratusername"></a>ratUserName

L'attributo **ratUserName** contiene il nome effettivamente inviato "in transito". NPS non è in alcun modo in grado di elaborare o convalidare il contenuto di questo attributo. Questo attributo potrebbe non essere disponibile perché l'utente potrebbe essere stato identificato tramite un mezzo, ad esempio ID chiamante.

Quando si usa [**RadiusExtensionProcess/ex**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex), se questo attributo è disponibile, è disponibile solo nel plug-in DLL dell'estensione di autenticazione. L'attributo **ratUserName** non è disponibile nel punto di plug-in DLL dell'estensione di autorizzazione perché nelle DLL dell'estensione di autorizzazione le funzioni **RadiusExtensionProcess/ex** visualizzano solo gli attributi "in uscita".

Quando si usa [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2), se questo attributo è disponibile, è disponibile sia per il punto di plug-in DLL dell'estensione di autenticazione che per il plug-in DLL dell'estensione di autorizzazione.

## <a name="ratstrippedusername"></a>ratStrippedUserName

**RatStrippedUserName** è l'identità dell'utente dopo l'"estrazione dell'area di autenticazione". Per ulteriori informazioni sulla rimozione dell'area di autenticazione, vedere l'argomento relativo ai nomi dell'area di [autenticazione](/previous-versions/windows/it-pro/windows-server-2003/cc779938(v=ws.10)) in http: \\ \\ technet2.Microsoft.com.

Questo attributo può essere presente nel punto di plug-in DLL dell'estensione di autenticazione, nel punto di plug-in DLL dell'estensione di autorizzazione o in entrambi. Il formato di questo attributo è garantito:

****\\*** Nome utente dominio*

Dove *Domain* è il nome di dominio NetBIOS.

## <a name="ratfqusername"></a>ratFQUserName

L'attributo **ratFQUserName** è il nome utente "completo".

Questo attributo può essere presente nel punto di plug-in DLL dell'estensione di autenticazione, nel punto di plug-in DLL dell'estensione di autorizzazione o in entrambi. Tuttavia, il formato dell'attributo può essere diverso tra i due punti di plug-in. Al punto di plug-in DLL dell'estensione di autenticazione, questo attributo sarà sempre nel formato:

****\\*** Nome utente dominio*

Il formato dell'attributo **ratFQUserName** in corrispondenza del punto di plug-in DLL dell'estensione di autorizzazione varia a seconda che l'utente sia un utente Active Directory.

-   Se l'utente è un utente locale **ratFQUserName** ha lo stesso formato del punto di plug-in DLL dell'estensione di autenticazione:

    ****\\*** Nome utente dominio*

    .

-   Se l'utente è un Active Directory utente, **ratFQUserName** può contenere il nome dell'utente nel formato "canonical". Il formato canonico è il formato utilizzato dal Active Directory per identificare l'utente. Si tratta del percorso dalla radice dell'albero Active Directory e include l'unità organizzativa (OU) dell'utente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Impostazione delle DLL di estensione](/windows/desktop/Nps/ias-setting-up-the-extension-and-authorization-dlls)
</dt> <dt>

[Richiamo delle DLL di estensione](/windows/desktop/Nps/ias-authentication-and-authorization-process)
</dt> </dl>

 

 