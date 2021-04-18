---
description: Viene illustrato come controfirmare un messaggio utilizzando CryptMsgCountersign.
ms.assetid: e1969b43-f50e-4c7d-a7e5-b22db4e05be2
title: Controfirma un messaggio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02091d25e7ee22f986a26b8f07abff68ebb8c11c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314138"
---
# <a name="countersigning-a-message"></a><span data-ttu-id="27d55-103">Controfirma un messaggio</span><span class="sxs-lookup"><span data-stu-id="27d55-103">Countersigning a Message</span></span>

<span data-ttu-id="27d55-104">**Per controfirmare un messaggio firmato tramite CryptMsgCountersign**</span><span class="sxs-lookup"><span data-stu-id="27d55-104">**To countersign a signed message by using CryptMsgCountersign**</span></span>

1.  <span data-ttu-id="27d55-105">Chiamare [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode) per ottenere un handle per il messaggio firmato.</span><span class="sxs-lookup"><span data-stu-id="27d55-105">Call [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode) to get a handle to the signed message.</span></span>
2.  <span data-ttu-id="27d55-106">Inizializzare una struttura di [**\_ informazioni di \_ codifica \_ del firmatario CMSG**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) per countersigner.</span><span class="sxs-lookup"><span data-stu-id="27d55-106">Initialize a [**CMSG\_SIGNER\_ENCODE\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) structure for the countersigner.</span></span>
3.  <span data-ttu-id="27d55-107">Aggiungere la struttura delle [**\_ informazioni di \_ codifica \_ del firmatario CMSG**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) a una matrice di countersigners (attualmente è supportato un solo countersigner).</span><span class="sxs-lookup"><span data-stu-id="27d55-107">Add the [**CMSG\_SIGNER\_ENCODE\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) structure to an array of countersigners (only one countersigner is currently supported).</span></span>
4.  <span data-ttu-id="27d55-108">Chiamare [**CryptMsgCountersign**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcountersign) per aggiungere controfirma o controfirme.</span><span class="sxs-lookup"><span data-stu-id="27d55-108">Call [**CryptMsgCountersign**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcountersign) to add the countersignature or countersignatures.</span></span>

<span data-ttu-id="27d55-109">Se tutte le chiamate di funzione hanno esito positivo, il messaggio originale dispone ora di un [*controfirma*](../secgloss/c-gly.md) incluso come attributo non autenticato.</span><span class="sxs-lookup"><span data-stu-id="27d55-109">If all of the function calls succeed, the original message now has a [*countersignature*](../secgloss/c-gly.md) included as an unauthenticated attribute.</span></span>

<span data-ttu-id="27d55-110">**Per controfirmare un messaggio firmato tramite CryptMsgCountersignEncoded**</span><span class="sxs-lookup"><span data-stu-id="27d55-110">**To countersign a signed message by using CryptMsgCountersignEncoded**</span></span>

1.  <span data-ttu-id="27d55-111">Chiamare [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode) per ottenere un handle per il messaggio firmato.</span><span class="sxs-lookup"><span data-stu-id="27d55-111">Call [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode) to get a handle to the signed message.</span></span>
2.  <span data-ttu-id="27d55-112">Chiamare [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) per recuperare le informazioni sul firmatario codificato del messaggio firmato.</span><span class="sxs-lookup"><span data-stu-id="27d55-112">Call [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) to retrieve the encoded signer information of the signed message.</span></span>
3.  <span data-ttu-id="27d55-113">Inizializzare una struttura di [**\_ informazioni di \_ codifica \_ del firmatario CMSG**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) per countersigner.</span><span class="sxs-lookup"><span data-stu-id="27d55-113">Initialize a [**CMSG\_SIGNER\_ENCODE\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) structure for the countersigner.</span></span>
4.  <span data-ttu-id="27d55-114">Aggiungere la struttura delle [**\_ informazioni di \_ codifica \_ del firmatario CMSG**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) a una matrice di countersigners (attualmente è supportato un solo countersigner).</span><span class="sxs-lookup"><span data-stu-id="27d55-114">Add the [**CMSG\_SIGNER\_ENCODE\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) structure to an array of countersigners (only one countersigner is currently supported).</span></span>
5.  <span data-ttu-id="27d55-115">Chiamare [**CryptMsgCountersignEncoded**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcountersignencoded) per creare l'attributo controfirma codificato.</span><span class="sxs-lookup"><span data-stu-id="27d55-115">Call [**CryptMsgCountersignEncoded**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcountersignencoded) to create the encoded countersignature attribute.</span></span>
6.  <span data-ttu-id="27d55-116">Chiamare [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol) per aggiungere l'attributo controfirma al messaggio originale come attributo non autenticato.</span><span class="sxs-lookup"><span data-stu-id="27d55-116">Call [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol) to add the countersignature attribute to the original message as an unauthenticated attribute.</span></span>

<span data-ttu-id="27d55-117">Se tutte le chiamate di funzione hanno esito positivo, al messaggio originale viene aggiunto un attributo [*controfirma*](../secgloss/c-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="27d55-117">If all of the function calls succeed, a [*countersignature*](../secgloss/c-gly.md) attribute is added to the original message.</span></span>

 

 
