---
description: Un descrittore di sicurezza contiene le informazioni di sicurezza associate a un oggetto a protezione diretta.
ms.assetid: 4ab0e7b1-1b44-4368-b2bd-106c9d2c652c
title: Descrittori di sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f864505f135b46d3e16a4e369c019444918fb97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879650"
---
# <a name="security-descriptors"></a><span data-ttu-id="cb979-103">Descrittori di sicurezza</span><span class="sxs-lookup"><span data-stu-id="cb979-103">Security Descriptors</span></span>

<span data-ttu-id="cb979-104">Un [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly) contiene le informazioni di sicurezza associate a un [oggetto a protezione diretta](securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="cb979-104">A [*security descriptor*](/windows/desktop/SecGloss/s-gly) contains the security information associated with a [securable object](securable-objects.md).</span></span> <span data-ttu-id="cb979-105">Un descrittore di sicurezza è costituito da una struttura di [**\_ descrittori di sicurezza**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) e dalle informazioni di sicurezza</span><span class="sxs-lookup"><span data-stu-id="cb979-105">A security descriptor consists of a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) structure and its associated security information.</span></span> <span data-ttu-id="cb979-106">Un descrittore di sicurezza può includere le informazioni di sicurezza seguenti:</span><span class="sxs-lookup"><span data-stu-id="cb979-106">A security descriptor can include the following security information:</span></span>

-   <span data-ttu-id="cb979-107">[ID di sicurezza](security-identifiers.md) (SID) per il proprietario e il gruppo primario di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="cb979-107">[Security identifiers](security-identifiers.md) (SIDs) for the owner and primary group of an object.</span></span>
-   <span data-ttu-id="cb979-108">[Elenco DACL](access-control-lists.md) che specifica i diritti di accesso consentiti o negati a utenti o gruppi specifici.</span><span class="sxs-lookup"><span data-stu-id="cb979-108">A [DACL](access-control-lists.md) that specifies the access rights allowed or denied to particular users or groups.</span></span>
-   <span data-ttu-id="cb979-109">[SACL](access-control-lists.md) che specifica i tipi di tentativi di accesso che generano record di controllo per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="cb979-109">A [SACL](access-control-lists.md) that specifies the types of access attempts that generate audit records for the object.</span></span>
-   <span data-ttu-id="cb979-110">Set di bit di controllo che qualificano il significato di un descrittore di sicurezza o dei singoli membri.</span><span class="sxs-lookup"><span data-stu-id="cb979-110">A set of control bits that qualify the meaning of a security descriptor or its individual members.</span></span>

<span data-ttu-id="cb979-111">Le applicazioni non devono modificare direttamente il contenuto di un descrittore di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="cb979-111">Applications must not directly manipulate the contents of a security descriptor.</span></span> <span data-ttu-id="cb979-112">L'API di Windows fornisce funzioni per l'impostazione e il recupero delle informazioni di sicurezza nel descrittore di sicurezza di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="cb979-112">The Windows API provides functions for setting and retrieving the security information in an object's security descriptor.</span></span> <span data-ttu-id="cb979-113">Sono inoltre disponibili funzioni per la creazione e l'inizializzazione di un descrittore di sicurezza per un nuovo oggetto.</span><span class="sxs-lookup"><span data-stu-id="cb979-113">In addition, there are functions for creating and initializing a security descriptor for a new object.</span></span>

<span data-ttu-id="cb979-114">Le applicazioni che utilizzano descrittori di sicurezza su oggetti Active Directory possono utilizzare le funzioni di sicurezza di Windows o le interfacce di sicurezza fornite da Active Directory Service Interfaces (ADSI).</span><span class="sxs-lookup"><span data-stu-id="cb979-114">Applications working with security descriptors on Active Directory objects can use the Windows security functions or the security interfaces provided by the Active Directory Service Interfaces (ADSI).</span></span> <span data-ttu-id="cb979-115">Per ulteriori informazioni sulle interfacce di sicurezza ADSI, vedere funzionamento [del controllo di accesso in Active Directory](/windows/desktop/AD/how-access-control-works-in-active-directory-domain-services).</span><span class="sxs-lookup"><span data-stu-id="cb979-115">For more information about ADSI security interfaces, see [How Access Control Works in Active Directory](/windows/desktop/AD/how-access-control-works-in-active-directory-domain-services).</span></span>

 

 
