---
description: Gli archivi, le applicazioni e gli ambiti dei criteri di autorizzazione rappresentano diversi livelli di organizzazione dei criteri di gestione autorizzazioni.
ms.assetid: 235f236d-59c9-4a8c-aec6-60d1ddba4d5d
title: Archivi, applicazioni e ambiti dei criteri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4155d7bf60d34474d52c27efd50d2f53741fa73a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879670"
---
# <a name="policy-stores-applications-and-scopes"></a>Archivi, applicazioni e ambiti dei criteri

Gli archivi, le applicazioni e gli ambiti dei criteri di autorizzazione rappresentano diversi livelli di organizzazione dei criteri di gestione autorizzazioni. Un archivio criteri può contenere una o più applicazioni e un'applicazione può contenere uno o più ambiti.

-   [Archivi dei criteri di autorizzazione](#authorization-policy-stores)
-   [Applicazioni](#policy-stores-applications-and-scopes)
-   [Ambiti](#policy-stores-applications-and-scopes)
-   [Delegation](#delegation)
-   [Argomenti correlati](#related-topics)

## <a name="authorization-policy-stores"></a>Archivi dei criteri di autorizzazione

Nell'API di gestione autorizzazioni, un archivio dei criteri di autorizzazione è rappresentato da un oggetto [**IAzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) . L'archivio dei criteri di autorizzazione contiene le definizioni e le assegnazioni di applicazioni, ambiti, operazioni, attività, ruoli e gruppi di utenti.

Un archivio dei criteri di autorizzazione può essere archiviato come file XML o in Active Directory.

Un'applicazione deve inizializzare un archivio dei criteri di autorizzazione prima di modificare le informazioni nell'archivio o usare i criteri di archiviazione per controllare l'accesso client alle risorse.

Un archivio dei criteri di autorizzazione può contenere uno o più oggetti [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) che rappresentano i criteri di autorizzazione per un'applicazione specifica.

## <a name="applications"></a>Applicazioni

Nell'API di gestione autorizzazioni, un'applicazione viene rappresentata da un oggetto [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) . Un archivio dei criteri di autorizzazione può contenere informazioni sui criteri di autorizzazione per molte applicazioni. L'uso di oggetti **IAzApplication** consente di archiviare criteri di autorizzazione diversi per applicazioni diverse in un singolo archivio criteri.

Un archivio dei criteri di autorizzazione deve contenere almeno un'applicazione.

## <a name="scopes"></a>Ambiti

Nell'API di gestione autorizzazioni, un ambito è rappresentato da un oggetto [**IAzScope**](/windows/desktop/api/Azroles/nn-azroles-iazscope) . Gli ambiti forniscono un livello di organizzazione aggiuntivo facoltativo per i criteri di autorizzazione. Un'applicazione può contenere uno o più ambiti, ma non deve contenere alcun (gestione autorizzazioni fornisce un ambito predefinito a livello di applicazione).

Un ambito è una suddivisione in un'applicazione che separa le risorse da altre risorse utilizzate da tale applicazione. Se si dispone di gruppi di gestione autorizzazioni, assegnazioni di ruolo, definizioni di ruoli o definizioni di attività che non si desidera applicare a un'intera applicazione, è possibile crearle a livello di ambito.

## <a name="delegation"></a>Delegation

Gli archivi dei criteri di autorizzazione archiviati in Active Directory supportano la delega dell'amministrazione. L'amministrazione può essere delegata a utenti e gruppi a livello di punto vendita, applicazione o ambito. Ogni livello definisce i ruoli amministrativi per i criteri a tale livello. Per delegare il controllo a un utente o a un gruppo, assegnarlo al ruolo di amministratore. per consentire a un utente o a un gruppo di leggere il criterio, assegnarlo al ruolo Reader.

Gli amministratori di un archivio, di un'applicazione o di un ambito possono leggere e modificare l'archivio criteri a livello delegato. I lettori possono leggere l'archivio criteri a livello delegato, ma non modificare l'archivio.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di un oggetto archivio criteri di autorizzazione in C++](creating-an-authorization-policy-store-object-in-c--.md)
</dt> <dt>

[Creazione di un oggetto applicazione in C++](creating-an-application-object-in-c--.md)
</dt> <dt>

[Delega della definizione di autorizzazioni in C++](delegating-the-defining-of-permissions-in-c--.md)
</dt> </dl>

 

 



