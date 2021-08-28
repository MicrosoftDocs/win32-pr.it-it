---
title: Attributi di identificazione utente
description: L'identità dell'utente che richiede l'autenticazione viene fornita alle DLL dell'estensione del Server dei criteri di rete in diversi attributi.
ms.assetid: 2f741a81-e432-47fe-a14a-8b77ecd41e28
ms.tgt_platform: multiple
keywords:
- Attributi, Identificazione utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff099b46844f2259ad127346bb1ee2bfafccf4b116f3dba86dff3e175d11c28c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128761"
---
# <a name="user-identification-attributes"></a>Attributi di identificazione utente

> [!Note]  
> Il servizio di autenticazione Internet (IAS) è stato rinominato Server dei criteri di rete (NPS) a partire Windows Server 2008. Il contenuto di questo argomento si applica sia a IAS che a Server dei criteri di rete. In tutto il testo, Server dei criteri di rete viene usato per fare riferimento a tutte le versioni del servizio, incluse le versioni originariamente indicate come IAS.

 

L'identità dell'utente che richiede l'autenticazione viene fornita alle DLL dell'estensione del Server dei criteri di rete in diversi attributi.

-   **cognomeNomeutente**
-   **StrippedUserName**
-   **fqdnFQUserName**

Ogni attributo fornisce l'identità utente in un formato diverso. In generale, gli sviluppatori devono **usarestrippedUserName**. Gli usi degli **attributiuserName** **e fqdnFQUserName** sono più specializzati.

> [!Note]  
> Il User-Password **attributo,passwordUserPassword**, è già stato decrittografato quando viene inviato alla DLL di estensione ed è utilizzabile in tale formato.

 

## <a name="ratusername"></a>cognomeNomeutente

**L'attributouserName** contiene il nome effettivamente inviato "in rete". Server dei criteri di rete non ha in alcun modo elaborato o convalidato il contenuto di questo attributo. Questo attributo potrebbe non essere disponibile perché l'utente potrebbe essere stato identificato tramite un mezzo, ad esempio l'ID chiamante.

Quando si [**usa RadiusExtensionProcess/Ex,**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex)se questo attributo è disponibile, è disponibile solo nel punto di plug-in DELLA DLL dell'estensione di autenticazione. **L'attributo authorizationUserName** non è disponibile nel punto di plug-in DLL dell'estensione di autorizzazione perché nelle DLL dell'estensione di autorizzazione le funzioni **RadiusExtensionProcess/Ex** visualizzano solo gli attributi "in uscita".

Quando si [**usa RadiusExtensionProcess2,**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2)se questo attributo è disponibile, è disponibile sia nel punto di plug-in DELLA DLL dell'estensione di autenticazione che nel punto di plug-in DLL dell'estensione di autorizzazione.

## <a name="ratstrippedusername"></a>StrippedUserName

**il valore distrippedUserName è** l'identità dell'utente dopo lo "stripping dell'area di autenticazione". Per altre informazioni sulla stripping dell'area di autenticazione, vedere l'argomento [Realm names](/previous-versions/windows/it-pro/windows-server-2003/cc779938(v=ws.10)) (Nomi delle aree di autenticazione) in http: \\ \\ technet2.microsoft.com.

Questo attributo può essere presente nel punto di plug-in DLL dell'estensione di autenticazione, nel punto di plug-in DLL dell'estensione di autorizzazione o in entrambi. È garantito che questo attributo abbia il formato:

*Domain* **\\** _UserName_

Dove *Dominio* è il nome di dominio NetBIOS.

## <a name="ratfqusername"></a>fqdnFQUserName

**L'attributo fqdnFQUserName** è il nome utente "completo".

Questo attributo può essere presente nel punto di plug-in DLL dell'estensione di autenticazione, nel punto di plug-in DLL dell'estensione di autorizzazione o in entrambi. Tuttavia, il formato dell'attributo può differire tra i due punti plug-in. Nel punto di plug-in DLL dell'estensione di autenticazione questo attributo sarà sempre nel formato seguente:

*Domain* **\\** _UserName_

Il formato **dell'attributo fqdnFQUserName** nel punto di plug-in DLL dell'estensione di autorizzazione dipende dal fatto che l'utente sia un utente di Active Directory.

-   Se l'utente è un utente **locale ,FQUserName** ha lo stesso formato del punto di plug-in DLL dell'estensione per l'autenticazione:

    *Domain* **\\** _UserName_

    .

-   Se l'utente è un utente di Active Directory, **fqdnFQUserName** può contenere il nome dell'utente in formato "canonico". Il formato canonico è il formato usato da Active Directory per identificare l'utente. Si tratta del percorso dalla radice dell'albero di Active Directory e include l'unità organizzativa (OU) dell'utente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Configurazione delle DLL di estensione](/windows/desktop/Nps/ias-setting-up-the-extension-and-authorization-dlls)
</dt> <dt>

[Richiamo delle DLL di estensione](/windows/desktop/Nps/ias-authentication-and-authorization-process)
</dt> </dl>

 

 