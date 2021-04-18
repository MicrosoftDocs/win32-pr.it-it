---
description: Viene illustrato come verificare un controfirma usando CryptMsgVerifyCountersignatureEncoded.
ms.assetid: b7be0d4c-338f-4319-bd82-5cf3d158d6fe
title: Verifica di un controfirma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 711e15388144fbf674cbb0c42ff41883edbb5af0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308625"
---
# <a name="verifying-a-countersignature"></a><span data-ttu-id="b9024-103">Verifica di un controfirma</span><span class="sxs-lookup"><span data-stu-id="b9024-103">Verifying a Countersignature</span></span>

<span data-ttu-id="b9024-104">**Per verificare un controfirma**</span><span class="sxs-lookup"><span data-stu-id="b9024-104">**To verify a countersignature**</span></span>

1.  <span data-ttu-id="b9024-105">Chiamare [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode) per ottenere un handle per il messaggio firmato.</span><span class="sxs-lookup"><span data-stu-id="b9024-105">Call [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode) to get a handle to the signed message.</span></span>
2.  <span data-ttu-id="b9024-106">Ottenere un puntatore al certificato di countersigner ( [**\_ informazioni**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info)sul certificato).</span><span class="sxs-lookup"><span data-stu-id="b9024-106">Get a pointer to the countersigner's certificate ( [**CERT\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info)).</span></span>
3.  <span data-ttu-id="b9024-107">Chiamare [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) per recuperare le informazioni sul firmatario dal messaggio.</span><span class="sxs-lookup"><span data-stu-id="b9024-107">Call [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) to retrieve the signer information from the message.</span></span>
4.  <span data-ttu-id="b9024-108">Chiamare [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) per recuperare [*controfirma*](../secgloss/c-gly.md) dal messaggio.</span><span class="sxs-lookup"><span data-stu-id="b9024-108">Call [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) to retrieve the [*countersignature*](../secgloss/c-gly.md) from the message.</span></span>
5.  <span data-ttu-id="b9024-109">Chiamare [**CryptMsgVerifyCountersignatureEncoded**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgverifycountersignatureencoded) per verificare il controfirma.</span><span class="sxs-lookup"><span data-stu-id="b9024-109">Call [**CryptMsgVerifyCountersignatureEncoded**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgverifycountersignatureencoded) to verify the countersignature.</span></span>

<span data-ttu-id="b9024-110">Se la chiamata alla funzione [**CryptMsgVerifyCountersignatureEncoded**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgverifycountersignatureencoded) ha esito positivo, viene verificata la [*controfirma*](../secgloss/c-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="b9024-110">If the [**CryptMsgVerifyCountersignatureEncoded**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgverifycountersignatureencoded) function call succeeds, the [*countersignature*](../secgloss/c-gly.md) is verified.</span></span>

 

 
