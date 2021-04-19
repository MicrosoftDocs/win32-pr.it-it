---
description: Elenca le costanti usate per le API di autenticazione Microsoft.
ms.assetid: 3e5b7fd8-01bf-4090-b68f-006b7e2228a9
title: Costanti di autenticazione (autenticazione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d671f356f11ccaf1f5aece1dc1168d3106d578c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316233"
---
# <a name="authentication-constants-authentication"></a><span data-ttu-id="f4cee-103">Costanti di autenticazione (autenticazione)</span><span class="sxs-lookup"><span data-stu-id="f4cee-103">Authentication Constants (Authentication)</span></span>

## <a name="credentials-management-constants"></a><span data-ttu-id="f4cee-104">Costanti di gestione delle credenziali</span><span class="sxs-lookup"><span data-stu-id="f4cee-104">Credentials Management Constants</span></span>

<span data-ttu-id="f4cee-105">Gestione credenziali usa le costanti seguenti per specificare le dimensioni massime delle stringhe.</span><span class="sxs-lookup"><span data-stu-id="f4cee-105">Credentials Management uses the following constants to specify maximum string sizes.</span></span>



| <span data-ttu-id="f4cee-106">Costante</span><span class="sxs-lookup"><span data-stu-id="f4cee-106">Constant</span></span>                                        | <span data-ttu-id="f4cee-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f4cee-107">Description</span></span>                                                                                                                   |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4cee-108">\_lunghezza massima \_ messaggi \_ CREDUI</span><span class="sxs-lookup"><span data-stu-id="f4cee-108">CREDUI\_MAX\_MESSAGE\_LENGTH</span></span><br/>         | <span data-ttu-id="f4cee-109">Numero massimo di caratteri per il membro **pszMessageText** di una struttura di [**\_ informazioni CREDUI**](/windows/desktop/api/WinCred/ns-wincred-credui_infoa) .</span><span class="sxs-lookup"><span data-stu-id="f4cee-109">Maximum number of characters for the **pszMessageText** member of a [**CREDUI\_INFO**](/windows/desktop/api/WinCred/ns-wincred-credui_infoa) structure.</span></span><br/> |
| <span data-ttu-id="f4cee-110">\_ \_ lunghezza didascalia massima CREDUI \_</span><span class="sxs-lookup"><span data-stu-id="f4cee-110">CREDUI\_MAX\_CAPTION\_LENGTH</span></span><br/>         | <span data-ttu-id="f4cee-111">Numero massimo di caratteri per il membro **pszCaptionText** di una struttura di [**\_ informazioni CREDUI**](/windows/desktop/api/WinCred/ns-wincred-credui_infoa) .</span><span class="sxs-lookup"><span data-stu-id="f4cee-111">Maximum number of characters for the **pszCaptionText** member of a [**CREDUI\_INFO**](/windows/desktop/api/WinCred/ns-wincred-credui_infoa) structure.</span></span><br/> |
| <span data-ttu-id="f4cee-112">\_lunghezza di \_ destinazione generica CREDUI Max \_ \_</span><span class="sxs-lookup"><span data-stu-id="f4cee-112">CREDUI\_MAX\_GENERIC\_TARGET\_LENGTH</span></span><br/> | <span data-ttu-id="f4cee-113">Numero massimo di caratteri in una stringa che specifica un nome di destinazione.</span><span class="sxs-lookup"><span data-stu-id="f4cee-113">Maximum number of characters in a string that specifies a target name.</span></span><br/>                                             |
| <span data-ttu-id="f4cee-114">\_lunghezza massima \_ \_ destinazione dominio \_ CREDUI</span><span class="sxs-lookup"><span data-stu-id="f4cee-114">CREDUI\_MAX\_DOMAIN\_TARGET\_LENGTH</span></span><br/>  | <span data-ttu-id="f4cee-115">Numero massimo di caratteri in una stringa che specifica un nome di dominio.</span><span class="sxs-lookup"><span data-stu-id="f4cee-115">Maximum number of characters in a string that specifies a domain name.</span></span><br/>                                             |
| <span data-ttu-id="f4cee-116">\_lunghezza max \_ nome utente \_ CREDUI</span><span class="sxs-lookup"><span data-stu-id="f4cee-116">CREDUI\_MAX\_USERNAME\_LENGTH</span></span><br/>        | <span data-ttu-id="f4cee-117">Numero massimo di caratteri in una stringa che specifica il nome di un account utente.</span><span class="sxs-lookup"><span data-stu-id="f4cee-117">Maximum number of characters in a string that specifies a user account name.</span></span><br/>                                       |
| <span data-ttu-id="f4cee-118">\_lunghezza massima \_ password \_ CREDUI</span><span class="sxs-lookup"><span data-stu-id="f4cee-118">CREDUI\_MAX\_PASSWORD\_LENGTH</span></span><br/>        | <span data-ttu-id="f4cee-119">Numero massimo di caratteri in una stringa che specifica una password.</span><span class="sxs-lookup"><span data-stu-id="f4cee-119">Maximum number of characters in a string that specifies a password.</span></span><br/>                                                |



 

## <a name="gina-defined-values"></a><span data-ttu-id="f4cee-120">Valori definiti da Gina</span><span class="sxs-lookup"><span data-stu-id="f4cee-120">Gina Defined Values</span></span>

<span data-ttu-id="f4cee-121">Le funzioni di interfaccia [*Gina*](/windows/desktop/SecGloss/g-gly) e le funzioni di supporto [*Winlogon*](/windows/desktop/SecGloss/w-gly) utilizzano i valori definiti seguenti.</span><span class="sxs-lookup"><span data-stu-id="f4cee-121">[*GINA*](/windows/desktop/SecGloss/g-gly) interface functions and [*Winlogon*](/windows/desktop/SecGloss/w-gly) support functions use the following defined values.</span></span>

> [!Note]  
> <span data-ttu-id="f4cee-122">Le DLL GINA vengono ignorate in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f4cee-122">GINA DLLs are ignored in Windows Vista.</span></span>

 



| <span data-ttu-id="f4cee-123">Valore</span><span class="sxs-lookup"><span data-stu-id="f4cee-123">Value</span></span>                                                              | <span data-ttu-id="f4cee-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f4cee-124">Description</span></span>                                                                                                                          |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f4cee-125">**\_opzione di accesso wlx \_ \_ xxx**</span><span class="sxs-lookup"><span data-stu-id="f4cee-125">**WLX\_LOGON\_OPTION\_XXX**</span></span>](wlx-logon-option-xxx.md)<br/> | <span data-ttu-id="f4cee-126">Contiene opzioni di accesso predefinite.</span><span class="sxs-lookup"><span data-stu-id="f4cee-126">Contains predefined logon options.</span></span> <span data-ttu-id="f4cee-127">Viene usato dal parametro *dwOptions* di [**WlxLoggedOutSAS**](/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas).</span><span class="sxs-lookup"><span data-stu-id="f4cee-127">It is used by the *dwOptions* parameter of [**WlxLoggedOutSAS**](/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas).</span></span><br/> |
| [<span data-ttu-id="f4cee-128">**WLX \_ SAS \_ tipo \_ xxx**</span><span class="sxs-lookup"><span data-stu-id="f4cee-128">**WLX\_SAS\_TYPE\_XXX**</span></span>](wlx-sas-type-xxx.md)<br/>         | <span data-ttu-id="f4cee-129">Definisce un tipo di firma di accesso condiviso specifico.</span><span class="sxs-lookup"><span data-stu-id="f4cee-129">Defines a specific SAS type.</span></span><br/>                                                                                              |



 

 

