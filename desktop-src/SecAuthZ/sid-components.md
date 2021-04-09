---
description: Componenti SID
ms.assetid: 528412e7-c2b6-4ddd-86de-999252972421
title: Componenti SID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbd44d0534cc56c6ef998c150810f14b3eda289d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049587"
---
# <a name="sid-components"></a><span data-ttu-id="15d1d-103">Componenti SID</span><span class="sxs-lookup"><span data-stu-id="15d1d-103">SID Components</span></span>

<span data-ttu-id="15d1d-104">Un valore SID include componenti che forniscono informazioni sulla struttura e sui componenti di [**SID**](/windows/desktop/api/Winnt/ns-winnt-sid) che identificano in modo univoco un trustee.</span><span class="sxs-lookup"><span data-stu-id="15d1d-104">A SID value includes components that provide information about the [**SID**](/windows/desktop/api/Winnt/ns-winnt-sid) structure and components that uniquely identify a trustee.</span></span> <span data-ttu-id="15d1d-105">Un SID è costituito dai componenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="15d1d-105">A SID consists of the following components:</span></span>

-   <span data-ttu-id="15d1d-106">Livello di revisione della struttura del [**SID**](/windows/desktop/api/Winnt/ns-winnt-sid)</span><span class="sxs-lookup"><span data-stu-id="15d1d-106">The revision level of the [**SID**](/windows/desktop/api/Winnt/ns-winnt-sid) structure</span></span>
-   <span data-ttu-id="15d1d-107">Valore dell'autorità di identificazione a 48 bit che identifica l'autorità che ha emesso il SID</span><span class="sxs-lookup"><span data-stu-id="15d1d-107">A 48-bit identifier authority value that identifies the authority that issued the SID</span></span>
-   <span data-ttu-id="15d1d-108">Numero variabile di valori di sottoautorizzazione o di [*ID relativo*](/windows/desktop/SecGloss/r-gly) (RID) che identificano in modo univoco il trustee relativo all'autorità che ha emesso il SID</span><span class="sxs-lookup"><span data-stu-id="15d1d-108">A variable number of subauthority or [*relative identifier*](/windows/desktop/SecGloss/r-gly) (RID) values that uniquely identify the trustee relative to the authority that issued the SID</span></span>

<span data-ttu-id="15d1d-109">La combinazione del valore dell'autorità di identificazione e dei valori di sottoautore garantisce che due SID non saranno uguali, anche se due diverse autorità emittenti di SID emettono la stessa combinazione di valori RID.</span><span class="sxs-lookup"><span data-stu-id="15d1d-109">The combination of the identifier authority value and the subauthority values ensures that no two SIDs will be the same, even if two different SID-issuing authorities issue the same combination of RID values.</span></span> <span data-ttu-id="15d1d-110">Ogni autorità emittente SID rilascia un determinato RID una sola volta.</span><span class="sxs-lookup"><span data-stu-id="15d1d-110">Each SID-issuing authority issues a given RID only once.</span></span>

<span data-ttu-id="15d1d-111">I SID vengono archiviati in formato binario in una struttura [**SID**](/windows/desktop/api/Winnt/ns-winnt-sid) .</span><span class="sxs-lookup"><span data-stu-id="15d1d-111">SIDs are stored in binary format in a [**SID**](/windows/desktop/api/Winnt/ns-winnt-sid) structure.</span></span> <span data-ttu-id="15d1d-112">Per visualizzare un SID, è possibile chiamare la funzione [**ConvertSidToStringSid**](/windows/desktop/api/Sddl/nf-sddl-convertsidtostringsida) per convertire un SID binario in formato stringa.</span><span class="sxs-lookup"><span data-stu-id="15d1d-112">To display a SID, you can call the [**ConvertSidToStringSid**](/windows/desktop/api/Sddl/nf-sddl-convertsidtostringsida) function to convert a binary SID to string format.</span></span> <span data-ttu-id="15d1d-113">Per eseguire la conversione di una stringa SID in un SID funzionale valido, chiamare la funzione [**ConvertStringSidToSid**](/windows/desktop/api/Sddl/nf-sddl-convertstringsidtosida) .</span><span class="sxs-lookup"><span data-stu-id="15d1d-113">To convert a SID string back to a valid, functional SID, call the [**ConvertStringSidToSid**](/windows/desktop/api/Sddl/nf-sddl-convertstringsidtosida) function.</span></span>

<span data-ttu-id="15d1d-114">Queste funzioni usano la notazione di stringa standardizzata seguente per SID, che semplifica la visualizzazione dei componenti:</span><span class="sxs-lookup"><span data-stu-id="15d1d-114">These functions use the following standardized string notation for SIDs, which makes it simpler to visualize their components:</span></span>

<span data-ttu-id="15d1d-115">s-*R* - *i* - ...</span><span class="sxs-lookup"><span data-stu-id="15d1d-115">S-*R*-*I*-*S*…</span></span>

<span data-ttu-id="15d1d-116">In questa notazione, il carattere letterale "S" identifica la serie di cifre come SID, *R* è il livello di revisione *, è* il valore dell'autorità di identificazione e *S*...</span><span class="sxs-lookup"><span data-stu-id="15d1d-116">In this notation, the literal character "S" identifies the series of digits as a SID, *R* is the revision level, *I* is the identifier-authority value, and *S*…</span></span> <span data-ttu-id="15d1d-117">è uno o più valori di sottoautorizzazione.</span><span class="sxs-lookup"><span data-stu-id="15d1d-117">is one or more subauthority values.</span></span>

<span data-ttu-id="15d1d-118">Nell'esempio seguente viene utilizzata questa notazione per visualizzare il noto SID relativo al dominio del gruppo Administrators locale:</span><span class="sxs-lookup"><span data-stu-id="15d1d-118">The following example uses this notation to display the well-known domain-relative SID of the local Administrators group:</span></span>

<span data-ttu-id="15d1d-119">S-1-5-32-544</span><span class="sxs-lookup"><span data-stu-id="15d1d-119">S-1-5-32-544</span></span>

<span data-ttu-id="15d1d-120">In questo esempio, il SID include i componenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="15d1d-120">In this example, the SID has the following components.</span></span> <span data-ttu-id="15d1d-121">Le costanti racchiuse tra parentesi sono l'autorità di identificazione nota e i valori [*RID*](/windows/desktop/SecGloss/r-gly) definiti in Winnt. h:</span><span class="sxs-lookup"><span data-stu-id="15d1d-121">The constants in parentheses are well-known identifier authority and [*RID*](/windows/desktop/SecGloss/r-gly) values defined in Winnt.h:</span></span>

-   <span data-ttu-id="15d1d-122">Livello di revisione 1</span><span class="sxs-lookup"><span data-stu-id="15d1d-122">A revision level of 1</span></span>
-   <span data-ttu-id="15d1d-123">Valore dell'autorità di identificazione 5 ( \_ autorità NT di sicurezza \_ )</span><span class="sxs-lookup"><span data-stu-id="15d1d-123">An identifier-authority value of 5 (SECURITY\_NT\_AUTHORITY)</span></span>
-   <span data-ttu-id="15d1d-124">Primo valore di subauthority di 32 (SECURITY \_ Builtin \_ Domain \_ RID)</span><span class="sxs-lookup"><span data-stu-id="15d1d-124">A first subauthority value of 32 (SECURITY\_BUILTIN\_DOMAIN\_RID)</span></span>
-   <span data-ttu-id="15d1d-125">Un secondo valore di subauthority di 544 (DOMAIN \_ alias \_ RID \_ Admins)</span><span class="sxs-lookup"><span data-stu-id="15d1d-125">A second subauthority value of 544 (DOMAIN\_ALIAS\_RID\_ADMINS)</span></span>

 

 
