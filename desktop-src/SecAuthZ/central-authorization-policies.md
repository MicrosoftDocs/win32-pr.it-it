---
description: Un criterio di autorizzazione centrale (CAP) raccoglie le specifiche regole di autorizzazione (CAPRs) in un singolo criterio.
ms.assetid: E3E43D9F-6826-468A-86E9-AC8F9A381FD4
title: Criteri di autorizzazione centrale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b890236b0dae0f8f8d51254def4e1607cc35894
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308878"
---
# <a name="central-authorization-policies"></a><span data-ttu-id="12d96-103">Criteri di autorizzazione centrale</span><span class="sxs-lookup"><span data-stu-id="12d96-103">Central Authorization Policies</span></span>

<span data-ttu-id="12d96-104">Un criterio di autorizzazione centrale (CAP) raccoglie le specifiche regole di autorizzazione (CAPRs) in un singolo criterio.</span><span class="sxs-lookup"><span data-stu-id="12d96-104">A Central Authorization Policy (CAP) collects the specific authorization rules (CAPRs) into a single policy.</span></span> <span data-ttu-id="12d96-105">Per consentire la combinazione di regole di autorizzazione specifiche (CAPRs) nel criterio di autorizzazione olistica dell'organizzazione, è possibile fare riferimento a CAPRs insieme a un set di risorse.</span><span class="sxs-lookup"><span data-stu-id="12d96-105">To allow the specific authorization rules (CAPRs) to be combined into the holistic authorization policy of the organization, CAPRs can be referenced together and applied to a set of resources.</span></span> <span data-ttu-id="12d96-106">Questa operazione viene eseguita raccogliendo più (per riferimento) in un limite.</span><span class="sxs-lookup"><span data-stu-id="12d96-106">This is done by collecting multiple (by reference) into a CAP.</span></span> <span data-ttu-id="12d96-107">Una volta definito un limite, è possibile distribuirlo utilizzato dai responsabili delle risorse per applicare i criteri di autorizzazione delle organizzazioni alle risorse.</span><span class="sxs-lookup"><span data-stu-id="12d96-107">Once a CAP is defined it can be distributed consumed by resource managers to apply the organizations authorization policy to resources.</span></span>

<span data-ttu-id="12d96-108">Un limite ha gli attributi seguenti:</span><span class="sxs-lookup"><span data-stu-id="12d96-108">A CAP has the following attributes:</span></span>

-   <span data-ttu-id="12d96-109">Raccolta di CAPRs: un elenco di riferimenti agli oggetti CAPR esistenti</span><span class="sxs-lookup"><span data-stu-id="12d96-109">Collection of CAPRs – a list of references to existing CAPR objects</span></span>
-   <span data-ttu-id="12d96-110">Identificatore (SID)</span><span class="sxs-lookup"><span data-stu-id="12d96-110">An identifier (Sid)</span></span>
-   <span data-ttu-id="12d96-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="12d96-111">Description</span></span>
-   <span data-ttu-id="12d96-112">Nome</span><span class="sxs-lookup"><span data-stu-id="12d96-112">Name</span></span>

<span data-ttu-id="12d96-113">Un limite viene valutato durante la valutazione dell'accesso per i file e le cartelle in cui è abilitato da un amministratore.</span><span class="sxs-lookup"><span data-stu-id="12d96-113">A CAP is evaluated during access evaluation for files and folders on which an administrator enables it.</span></span> <span data-ttu-id="12d96-114">Durante una chiamata [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) , il controllo della copertura viene combinato logicamente con il controllo ACL discrezionale; Ciò significa che per ottenere l'accesso a un file a cui si applica il limite, un utente deve avere accesso sia in base all'estremità (il CAPRs associato) che all'ACL discrezionale del file.</span><span class="sxs-lookup"><span data-stu-id="12d96-114">During an [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) call, the CAP check is logically combined with the discretionary ACL check; this means that in order to obtain access to a file to which the CAP applies, a user needs to have access both according to the CAP (its associated CAPRs) and the discretionary ACL on the file.</span></span>

<span data-ttu-id="12d96-115">LIMITE di esempio:</span><span class="sxs-lookup"><span data-stu-id="12d96-115">Example CAP:</span></span>

``` syntax
CORPORATE-FINANCE-CAP]
CAPID=S-1-5-3-4-56-45-67-123
Policies=HBI-CAPE;RETENTION-CAPR
```

## <a name="cap-definition"></a><span data-ttu-id="12d96-116">Definizione CAP</span><span class="sxs-lookup"><span data-stu-id="12d96-116">CAP Definition</span></span>

<span data-ttu-id="12d96-117">Un limite viene creato e modificato in Active Directory usando una nuova esperienza utente in centro di amministrazione di sistema (o PowerShell) che consente all'amministratore di creare un limite e specificare un set di CAPRs che costituiscono il limite.</span><span class="sxs-lookup"><span data-stu-id="12d96-117">A CAP is created and edited in Active Directory using a new UX in ADAC (or PowerShell) that allows the administrator to create a CAP and specify a set of CAPRs that make up the CAP.</span></span>

 

 
