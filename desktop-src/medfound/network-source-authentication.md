---
description: Autenticazione origine rete
ms.assetid: bffc33ec-0fb0-4bbe-9bac-583b9d4e1153
title: Autenticazione origine rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09c38968fccf501f49ac7666a066b88528b237bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049661"
---
# <a name="network-source-authentication"></a><span data-ttu-id="e0b92-103">Autenticazione origine rete</span><span class="sxs-lookup"><span data-stu-id="e0b92-103">Network Source Authentication</span></span>

<span data-ttu-id="e0b92-104">Alcuni host multimediali potrebbero richiedere credenziali utente dalle applicazioni client prima di consentire l'accesso al supporto.</span><span class="sxs-lookup"><span data-stu-id="e0b92-104">Certain media hosts may require user credentials from client applications before allowing access to the media.</span></span> <span data-ttu-id="e0b92-105">Le credenziali utente includono l'identificazione e la prova dell'identificazione, ad esempio nome utente e password, che vengono usate dal server multimediale per concedere l'accesso all'origine di rete ospitata.</span><span class="sxs-lookup"><span data-stu-id="e0b92-105">User credentials include identification and proof of identification, such as user name and password, which are used by the media server to grant access to the network source it hosts.</span></span> <span data-ttu-id="e0b92-106">L'origine di rete può fornire l'autenticazione NTLM, digest o di base.</span><span class="sxs-lookup"><span data-stu-id="e0b92-106">The network source can provide NTLM, Digest, or Basic authentication.</span></span>

<span data-ttu-id="e0b92-107">Le applicazioni basate su Media Foundation possono archiviare le credenziali utente per un URL specifico in un oggetto *credenziale* che espone l'interfaccia [**IMFNetCredential**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) .</span><span class="sxs-lookup"><span data-stu-id="e0b92-107">Applications based on Media Foundation can store user credentials for a specific URL in a *credential* object that exposes the [**IMFNetCredential**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) interface.</span></span> <span data-ttu-id="e0b92-108">L'oggetto Credential archivia le credenziali crittografate e fornisce i metodi per restituire informazioni come nome utente, password e dominio.</span><span class="sxs-lookup"><span data-stu-id="e0b92-108">The credential object stores encrypted credentials and provides methods to return information such as user name, password, and domain.</span></span>

<span data-ttu-id="e0b92-109">Gli oggetti credenziale vengono creati e gestiti in una cache.</span><span class="sxs-lookup"><span data-stu-id="e0b92-109">The credential objects are created and maintained in a cache.</span></span> <span data-ttu-id="e0b92-110">L'oggetto della *cache delle credenziali* , esposto dall'interfaccia [**IMFNetCredentialCache**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialcache) , fornisce metodi per il recupero degli oggetti Credential dalla cache delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="e0b92-110">The *credential cache* object, exposed by the [**IMFNetCredentialCache**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialcache) interface provides methods for retrieving the credential objects from the credential cache.</span></span>

<span data-ttu-id="e0b92-111">Un'applicazione che supporta l'autenticazione deve implementare l'interfaccia [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) .</span><span class="sxs-lookup"><span data-stu-id="e0b92-111">An application that supports authentication must implement the [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) interface.</span></span> <span data-ttu-id="e0b92-112">Media Foundation non fornisce un'implementazione predefinita di questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="e0b92-112">Media Foundation does not provide a default implementation of this interface.</span></span> <span data-ttu-id="e0b92-113">Gestione credenziali è responsabile della raccolta delle credenziali necessarie per un URL dall'input dell'utente o della lettura da un archivio permanente.</span><span class="sxs-lookup"><span data-stu-id="e0b92-113">The credential manager is responsible for gathering the required credentials for a URL from user input or reading from persisted storage.</span></span>

<span data-ttu-id="e0b92-114">Questa sezione contiene i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="e0b92-114">This section contains the following topics:</span></span>

-   [<span data-ttu-id="e0b92-115">Impostazione di una gestione credenziali</span><span class="sxs-lookup"><span data-stu-id="e0b92-115">Setting a Credential Manager</span></span>](setting-a-credential-manager.md)
-   [<span data-ttu-id="e0b92-116">Uso della cache delle credenziali</span><span class="sxs-lookup"><span data-stu-id="e0b92-116">Using the Credential Cache</span></span>](using-the-credential-cache.md)
-   [<span data-ttu-id="e0b92-117">Implementazione di IMFNetCredentialManager</span><span class="sxs-lookup"><span data-stu-id="e0b92-117">Implementing IMFNetCredentialManager</span></span>](implementing-imfnetcredentialmanager.md)

## <a name="related-topics"></a><span data-ttu-id="e0b92-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e0b92-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0b92-119">Rete in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e0b92-119">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 



