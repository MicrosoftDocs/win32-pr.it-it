---
title: Impostazione delle DLL di estensione
description: All'avvio, NPS controlla il registro di sistema per un elenco di dll di terze parti da chiamare.
ms.assetid: fbbd9031-3ebe-47b8-8d8b-e359fa7d4b67
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14e8589f31144f12b120f9a77f281dd57a9f30ce
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047063"
---
# <a name="setting-up-the-extension-dlls"></a><span data-ttu-id="1f676-103">Impostazione delle DLL di estensione</span><span class="sxs-lookup"><span data-stu-id="1f676-103">Setting Up the Extension DLLs</span></span>

> [!Note]  
> <span data-ttu-id="1f676-104">Il servizio di autenticazione Internet (IAS) è stato rinominato server dei criteri di rete (NPS) a partire da Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="1f676-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="1f676-105">Il contenuto di questo argomento si applica sia a IAS che a NPS.</span><span class="sxs-lookup"><span data-stu-id="1f676-105">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="1f676-106">In tutto il testo, NPS viene utilizzato per fare riferimento a tutte le versioni del servizio, incluse le versioni originariamente indicate come IAS.</span><span class="sxs-lookup"><span data-stu-id="1f676-106">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="1f676-107">All'avvio, NPS controlla il registro di sistema per un elenco di dll di terze parti da chiamare.</span><span class="sxs-lookup"><span data-stu-id="1f676-107">At startup, NPS checks the registry for a list of third-party DLLs to call.</span></span>

<span data-ttu-id="1f676-108">Per impostare una DLL di autenticazione o autorizzazione in un server NPS, elencare i percorsi delle dll nei valori sotto la seguente chiave del registro di sistema:</span><span class="sxs-lookup"><span data-stu-id="1f676-108">To set up an Authentication or Authorization DLL on an NPS server, list the paths to the DLLs in values below the following registry key:</span></span>

<span data-ttu-id="1f676-109">**\\ \\ \\ Parametri AuthSrv dei servizi \\ CurrentControlSet \\ di sistema HKLM\\**</span><span class="sxs-lookup"><span data-stu-id="1f676-109">**HKLM\\System\\CurrentControlSet\\Services\\AuthSrv\\Parameters\\**</span></span>

<span data-ttu-id="1f676-110">Se le chiavi **AuthSrv** e **Parameters** non esistono, crearle.</span><span class="sxs-lookup"><span data-stu-id="1f676-110">If the **AuthSrv** and **Parameters** keys do not exist, create them.</span></span>

<span data-ttu-id="1f676-111">Il valore in cui elencare le DLL dell'estensione di autenticazione è:</span><span class="sxs-lookup"><span data-stu-id="1f676-111">The value in which to list the Authentication Extension DLLs is:</span></span>

<span data-ttu-id="1f676-112">**ExtensionDLLs**</span><span class="sxs-lookup"><span data-stu-id="1f676-112">**ExtensionDLLs**</span></span>

<span data-ttu-id="1f676-113">Il valore in cui elencare le DLL dell'estensione di autorizzazione è:</span><span class="sxs-lookup"><span data-stu-id="1f676-113">The value in which to list the Authorization Extension DLLs is:</span></span>

<span data-ttu-id="1f676-114">**AuthorizationDLLs**</span><span class="sxs-lookup"><span data-stu-id="1f676-114">**AuthorizationDLLs**</span></span>

<span data-ttu-id="1f676-115">Entrambi i valori **ExtensionDLLs** e **AuthorizationDLLs** devono essere di tipo **reg \_ \_ multisz**.</span><span class="sxs-lookup"><span data-stu-id="1f676-115">Both the **ExtensionDLLs** and **AuthorizationDLLs** values must be of type **REG\_MULTI\_SZ**.</span></span> <span data-ttu-id="1f676-116">Questo tipo consente di elencare più dll.</span><span class="sxs-lookup"><span data-stu-id="1f676-116">This type allows you to list multiple DLLs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1f676-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1f676-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f676-118">Richiamo delle DLL di estensione</span><span class="sxs-lookup"><span data-stu-id="1f676-118">Invoking the Extension DLLs</span></span>](/windows/desktop/Nps/ias-authentication-and-authorization-process)
</dt> <dt>

[<span data-ttu-id="1f676-119">Attributi di identificazione utente</span><span class="sxs-lookup"><span data-stu-id="1f676-119">User Identification Attributes</span></span>](/windows/desktop/Nps/ias-user-identification-attributes)
</dt> </dl>

 

 