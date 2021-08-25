---
description: Gli archivi, le applicazioni e gli ambiti dei criteri di autorizzazione rappresentano diversi livelli di organizzazione dei criteri di Gestione autorizzazioni.
ms.assetid: 235f236d-59c9-4a8c-aec6-60d1ddba4d5d
title: Archivi criteri, applicazioni e ambiti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5db06b291ef81f391fed1a0094b73c9b31d0342f59bce22d93779c7bfa48a80b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907571"
---
# <a name="policy-stores-applications-and-scopes"></a>Archivi criteri, applicazioni e ambiti

Gli archivi, le applicazioni e gli ambiti dei criteri di autorizzazione rappresentano diversi livelli di organizzazione dei criteri di Gestione autorizzazioni. Un archivio criteri può contenere una o più applicazioni e un'applicazione può contenere uno o più ambiti.

-   [Archivi dei criteri di autorizzazione](#authorization-policy-stores)
-   [Applicazioni](#policy-stores-applications-and-scopes)
-   [Ambiti](#policy-stores-applications-and-scopes)
-   [Delegation](#delegation)
-   [Argomenti correlati](#related-topics)

## <a name="authorization-policy-stores"></a>Archivi dei criteri di autorizzazione

Nell'API di Gestione autorizzazioni un archivio dei criteri di autorizzazione è rappresentato da un [**oggetto IAzAuthorizationStore.**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) L'archivio dei criteri di autorizzazione contiene definizioni e assegnazioni di applicazioni, ambiti, operazioni, attività, ruoli e gruppi di utenti.

Un archivio dei criteri di autorizzazione può essere archiviato come file XML o in Active Directory.

Un'applicazione deve inizializzare un archivio criteri di autorizzazione prima di modificare le informazioni nell'archivio o di usare i criteri di archiviazione per controllare l'accesso client alle risorse.

Un archivio dei criteri di autorizzazione può contenere uno o più [**oggetti IAzApplication,**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) ognuno dei quali rappresenta i criteri di autorizzazione per un'applicazione specifica.

## <a name="applications"></a>Applicazioni

Nell'API di Gestione autorizzazioni un'applicazione è rappresentata da un [**oggetto IAzApplication.**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) Un archivio dei criteri di autorizzazione può contenere informazioni sui criteri di autorizzazione per molte applicazioni. **L'uso di oggetti IAzApplication** consente di archiviare criteri di autorizzazione diversi per applicazioni diverse in un singolo archivio criteri.

Un archivio dei criteri di autorizzazione deve contenere almeno un'applicazione.

## <a name="scopes"></a>Ambiti

Nell'API di Gestione autorizzazioni un ambito è rappresentato da un [**oggetto IAzScope.**](/windows/desktop/api/Azroles/nn-azroles-iazscope) Gli ambiti forniscono un livello di organizzazione aggiuntivo facoltativo per i criteri di autorizzazione. Un'applicazione può contenere uno o più ambiti, ma non deve contenere alcun ambito (Gestione autorizzazioni fornisce un ambito predefinito a livello di applicazione).

Un ambito è una suddivisione all'interno di un'applicazione che separa le risorse dalle altre risorse usate dall'applicazione. Se si dispone di gruppi di Gestione autorizzazioni, assegnazioni di ruolo, definizioni di ruolo o definizioni di attività che non si desidera applicare a un'intera applicazione, è possibile crearli a livello di ambito.

## <a name="delegation"></a>Delegation

Gli archivi di criteri di autorizzazione archiviati in Active Directory supportano la delega dell'amministrazione. L'amministrazione può essere delegata a utenti e gruppi a livello di archivio, applicazione o ambito. Ogni livello definisce i ruoli amministrativi per i criteri a tale livello. Per delegare il controllo a un utente o a un gruppo, assegnarlo al ruolo di amministratore. per consentire a un utente o a un gruppo di leggere i criteri, assegnarli al ruolo lettore.

Gli amministratori di un archivio, di un'applicazione o di un ambito possono leggere e modificare l'archivio criteri a livello delegato. I lettori possono leggere l'archivio criteri a livello delegato, ma non possono modificare l'archivio.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di un oggetto archivio criteri di autorizzazione in C++](creating-an-authorization-policy-store-object-in-c--.md)
</dt> <dt>

[Creazione di un oggetto applicazione in C++](creating-an-application-object-in-c--.md)
</dt> <dt>

[Delega della definizione delle autorizzazioni in C++](delegating-the-defining-of-permissions-in-c--.md)
</dt> </dl>

 

 



