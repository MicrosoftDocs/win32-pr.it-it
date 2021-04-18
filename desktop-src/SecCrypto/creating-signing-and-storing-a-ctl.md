---
description: Creare un elenco certificati attendibili (CTL) firmato e salvarlo in un archivio certificati.
ms.assetid: 82d75d60-2343-413c-ba53-ccee02d1ad41
title: Creazione, firma e archiviazione di un elenco di scopi consentiti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2da66ce5acb882d36451118700178519455a4ded
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306469"
---
# <a name="creating-signing-and-storing-a-ctl"></a><span data-ttu-id="2c75b-103">Creazione, firma e archiviazione di un elenco di scopi consentiti</span><span class="sxs-lookup"><span data-stu-id="2c75b-103">Creating, Signing, and Storing a CTL</span></span>

<span data-ttu-id="2c75b-104">Le procedure seguenti creano un [*elenco certificati attendibili*](../secgloss/c-gly.md) (CTL) firmato e lo salvano in un [*archivio certificati*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="2c75b-104">The following procedures create a signed [*certificate trust list*](../secgloss/c-gly.md) (CTL) and save it to a [*certificate store*](../secgloss/c-gly.md).</span></span>

<span data-ttu-id="2c75b-105">**Per creare e firmare un elenco di scopi consentiti**</span><span class="sxs-lookup"><span data-stu-id="2c75b-105">**To create and sign a CTL**</span></span>

1.  <span data-ttu-id="2c75b-106">Creare una matrice di elementi da archiviare nell' [*elenco*](../secgloss/c-gly.md)di scopi consentiti.</span><span class="sxs-lookup"><span data-stu-id="2c75b-106">Create an array of items to be stored in the [*CTL*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="2c75b-107">Nel caso di certificati attendibili, devono essere gli hash SHA1 o MD5 dei certificati attendibili.</span><span class="sxs-lookup"><span data-stu-id="2c75b-107">In the case of trusted certificates, this must be the SHA1 or MD5 hashes of the trusted certificates.</span></span>
2.  <span data-ttu-id="2c75b-108">Inizializzare una struttura di [**\_ informazioni CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_info) che includa la matrice di elementi appena creati.</span><span class="sxs-lookup"><span data-stu-id="2c75b-108">Initialize a [**CTL\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_info) structure that includes the array of items just created.</span></span>
3.  <span data-ttu-id="2c75b-109">Inizializza una struttura di [**\_ informazioni di \_ codifica \_ CMSG firmata**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signed_encode_info) .</span><span class="sxs-lookup"><span data-stu-id="2c75b-109">Initialize a [**CMSG\_SIGNED\_ENCODE\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signed_encode_info) structure.</span></span>
4.  <span data-ttu-id="2c75b-110">Chiamare [**CryptMsgEncodeAndSignCTL**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgencodeandsignctl).</span><span class="sxs-lookup"><span data-stu-id="2c75b-110">Call [**CryptMsgEncodeAndSignCTL**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgencodeandsignctl).</span></span> <span data-ttu-id="2c75b-111">Questa chiamata di funzione restituisce un puntatore a un elenco di scopi consentiti codificato (in \# formato PKCS 7) che contiene l'elenco di elementi creati nel passaggio 1.</span><span class="sxs-lookup"><span data-stu-id="2c75b-111">This function call returns a pointer to a signed, encoded CTL (in PKCS \#7 format) that contains the list of items created in step 1.</span></span>

<span data-ttu-id="2c75b-112">**Per aggiungere un elenco di scopi consentiti a un archivio certificati**</span><span class="sxs-lookup"><span data-stu-id="2c75b-112">**To add a CTL to a certificate store**</span></span>

1.  <span data-ttu-id="2c75b-113">Ottenere un puntatore a un elenco di scopi consentiti firmato e codificato.</span><span class="sxs-lookup"><span data-stu-id="2c75b-113">Get a pointer to a signed and encoded CTL.</span></span>
2.  <span data-ttu-id="2c75b-114">Aprire l'archivio certificati di destinazione con una chiamata a [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore).</span><span class="sxs-lookup"><span data-stu-id="2c75b-114">Open the target certificate store with a call to [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore).</span></span>
3.  <span data-ttu-id="2c75b-115">Chiamare [**CertAddEncodedCTLToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedctltostore).</span><span class="sxs-lookup"><span data-stu-id="2c75b-115">Call [**CertAddEncodedCTLToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedctltostore).</span></span>

 

 
