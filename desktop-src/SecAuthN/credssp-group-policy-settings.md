---
description: Per il protocollo CredSSP (Credential Security Support Provider Protocol) per delegare le credenziali, è necessario specificare quali server possono essere delegati a.
ms.assetid: 15ed9a62-2eee-4f29-92c5-ccf2754cdf13
title: Impostazioni Criteri di gruppo CredSSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a159b7a162df3eda692462a3d3972159e61797e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313746"
---
# <a name="credssp-group-policy-settings"></a><span data-ttu-id="2fcd2-103">Impostazioni Criteri di gruppo CredSSP</span><span class="sxs-lookup"><span data-stu-id="2fcd2-103">CredSSP Group Policy Settings</span></span>

<span data-ttu-id="2fcd2-104">Per il [protocollo CredSSP (Credential Security Support Provider Protocol)](credential-security-support-provider.md) per delegare le credenziali, è necessario specificare quali server possono essere delegati a.</span><span class="sxs-lookup"><span data-stu-id="2fcd2-104">For [Credential Security Support Provider protocol (CredSSP)](credential-security-support-provider.md) to delegate credentials, you must specify which servers can be delegated to.</span></span> <span data-ttu-id="2fcd2-105">Per specificare tali server, modificare le impostazioni nello snap-in di Editor Criteri di gruppo (GPE) di Microsoft Management Console (MMC).</span><span class="sxs-lookup"><span data-stu-id="2fcd2-105">To specify those servers, modify settings in the Group Policy Editor (GPE) Microsoft Management Console (MMC) snap-in.</span></span> <span data-ttu-id="2fcd2-106">Le impostazioni GPE che controllano la delega sono in **Configurazione Computer \| modelli amministrativi \| \| delega credenziali di sistema**.</span><span class="sxs-lookup"><span data-stu-id="2fcd2-106">The GPE settings that control delegation are under **Computer Configuration \| Administrative Templates \| System \| Credentials Delegation**.</span></span>

> [!Caution]  
> <span data-ttu-id="2fcd2-107">La delega non è vincolata.</span><span class="sxs-lookup"><span data-stu-id="2fcd2-107">This is not constrained delegation.</span></span> <span data-ttu-id="2fcd2-108">CredSSP passa le credenziali complete dell'utente al server senza vincoli.</span><span class="sxs-lookup"><span data-stu-id="2fcd2-108">CredSSP passes the user's full credentials to the server without any constraint.</span></span>

 

<span data-ttu-id="2fcd2-109">Le impostazioni di criteri di gruppo controllano la delega dei tipi di credenziali seguenti.</span><span class="sxs-lookup"><span data-stu-id="2fcd2-109">Group policy settings control delegation of the following types of credentials.</span></span>



| <span data-ttu-id="2fcd2-110">Tipo di credenziali</span><span class="sxs-lookup"><span data-stu-id="2fcd2-110">Credentials Type</span></span>                                                                                                                                 | <span data-ttu-id="2fcd2-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2fcd2-111">Description</span></span>                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2fcd2-112"><span id="Default_credentials"></span><span id="default_credentials"></span><span id="DEFAULT_CREDENTIALS"></span>Credenziali predefinite</span><span class="sxs-lookup"><span data-stu-id="2fcd2-112"><span id="Default_credentials"></span><span id="default_credentials"></span><span id="DEFAULT_CREDENTIALS"></span>Default credentials</span></span><br/> | <span data-ttu-id="2fcd2-113">Credenziali ottenute quando l'utente accede per la prima volta a Windows.</span><span class="sxs-lookup"><span data-stu-id="2fcd2-113">The credentials obtained when the user first logs on to Windows.</span></span><br/>                   |
| <span data-ttu-id="2fcd2-114"><span id="Fresh_credentials"></span><span id="fresh_credentials"></span><span id="FRESH_CREDENTIALS"></span>Credenziali aggiornate</span><span class="sxs-lookup"><span data-stu-id="2fcd2-114"><span id="Fresh_credentials"></span><span id="fresh_credentials"></span><span id="FRESH_CREDENTIALS"></span>Fresh credentials</span></span><br/>         | <span data-ttu-id="2fcd2-115">Credenziali richieste all'utente durante l'esecuzione di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2fcd2-115">The credentials that the user is prompted for when executing an application.</span></span><br/>       |
| <span data-ttu-id="2fcd2-116"><span id="Saved_credentials"></span><span id="saved_credentials"></span><span id="SAVED_CREDENTIALS"></span>Credenziali salvate</span><span class="sxs-lookup"><span data-stu-id="2fcd2-116"><span id="Saved_credentials"></span><span id="saved_credentials"></span><span id="SAVED_CREDENTIALS"></span>Saved credentials</span></span><br/>         | <span data-ttu-id="2fcd2-117">Credenziali salvate mediante [Gestione credenziali](credential-manager.md).</span><span class="sxs-lookup"><span data-stu-id="2fcd2-117">The credentials that are saved using [Credential Manager](credential-manager.md).</span></span><br/> |



 

<span data-ttu-id="2fcd2-118">Per includere un server nella categoria associata a una particolare impostazione di criteri di gruppo, aggiungere il [*nome dell'entità servizio*](/windows/desktop/SecGloss/s-gly) (SPN) del server all'elenco dei server per l'impostazione di criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="2fcd2-118">To include a server in the category associated with a particular group policy setting, add the [*Service Principal Name*](/windows/desktop/SecGloss/s-gly) (SPN) of that server to the list of servers for that group policy setting.</span></span> <span data-ttu-id="2fcd2-119">Il nome SPN può contenere un singolo carattere jolly.</span><span class="sxs-lookup"><span data-stu-id="2fcd2-119">The SPN can contain a single wildcard character.</span></span>

 

