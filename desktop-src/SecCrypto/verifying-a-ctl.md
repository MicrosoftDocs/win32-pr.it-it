---
description: Per rendere più difficile per un intertruso sostituire un elenco di certificati attendibili (CTL, Certificate Trust List) fasullo per uno esistente, verificare la firma nel CTL ogni volta che viene usato il CTL.
ms.assetid: 24ba6955-f6d1-4123-ab39-50385f6e03a0
title: Verifica di un CTL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac88362c96d5b419a7c16731e31456b569079d7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527613"
---
# <a name="verifying-a-ctl"></a><span data-ttu-id="5d6c2-103">Verifica di un CTL</span><span class="sxs-lookup"><span data-stu-id="5d6c2-103">Verifying a CTL</span></span>

<span data-ttu-id="5d6c2-104">Per rendere più difficile per un intertruso sostituire un [*elenco di certificati attendibili (CTL, Certificate Trust List*](../secgloss/c-gly.md) ) fasullo per uno esistente, verificare la firma nel CTL ogni volta che viene usato il CTL.</span><span class="sxs-lookup"><span data-stu-id="5d6c2-104">To make it more difficult for an interloper to substitute a bogus [*certificate trust list*](../secgloss/c-gly.md) (CTL) for an existing one, verify the signature on the CTL each time the CTL is used.</span></span> <span data-ttu-id="5d6c2-105">Non usare un elenco di scopi consentiti che non contenga una firma attendibile.</span><span class="sxs-lookup"><span data-stu-id="5d6c2-105">Do not use a CTL that does not contain a trusted signature.</span></span>

<span data-ttu-id="5d6c2-106">**Per verificare una firma CTL**</span><span class="sxs-lookup"><span data-stu-id="5d6c2-106">**To verify a CTL signature**</span></span>

1.  <span data-ttu-id="5d6c2-107">Aprire l' [*archivio certificati*](../secgloss/c-gly.md) contenente l'elenco di scopi consentiti desiderato.</span><span class="sxs-lookup"><span data-stu-id="5d6c2-107">Open the [*certificate store*](../secgloss/c-gly.md) containing the desired CTL.</span></span>
2.  <span data-ttu-id="5d6c2-108">Ottenere un handle per un [**\_ contesto CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) per l'elenco di scopi consentiti.</span><span class="sxs-lookup"><span data-stu-id="5d6c2-108">Get a handle to a [**CTL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) for the CTL.</span></span> <span data-ttu-id="5d6c2-109">Questa operazione può essere eseguita chiamando le funzioni che restituiscono un handle al **\_ contesto CTL**, ad esempio [**CertFindCTLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore).</span><span class="sxs-lookup"><span data-stu-id="5d6c2-109">This can be done by calling any of the functions that return a handle to the **CTL\_CONTEXT**, such as [**CertFindCTLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore).</span></span>
3.  <span data-ttu-id="5d6c2-110">Chiamare [**CryptMsgGetAndVerifySigner**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetandverifysigner), passando il [**\_ contesto CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) recuperato nel passaggio 2 nel parametro *hCryptMsg* , un handle all'archivio certificati contenente il certificato dell'origine attendibile per scopi consentiti nel parametro *rghSignerStore* e il \_ flag del firmatario attendibile CMSG \_ \_ nel parametro *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="5d6c2-110">Call [**CryptMsgGetAndVerifySigner**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetandverifysigner), passing the [**CTL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) retrieved in step 2 in the *hCryptMsg* parameter, a handle to the certificate store containing the certificate of the trusted source for CTLs in the *rghSignerStore* parameter, and the CMSG\_TRUSTED\_SIGNER\_FLAG in the *dwFlags* parameter.</span></span> <span data-ttu-id="5d6c2-111">Se la funzione restituisce **true**, la firma è stata verificata e viene restituito un puntatore al [**\_ contesto PCCERT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) del firmatario CTL nel parametro *ppSigner* .</span><span class="sxs-lookup"><span data-stu-id="5d6c2-111">If the function returns **TRUE**, the signature was verified, and a pointer to the CTL signer's [**PCCERT\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) is returned in the *ppSigner* parameter.</span></span>

 

 
