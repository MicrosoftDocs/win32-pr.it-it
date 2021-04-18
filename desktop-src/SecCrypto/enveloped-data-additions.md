---
description: Elenca le modifiche apportate alle funzionalità per l'inviluppo dei dati.
ms.assetid: b025a9c6-d6a3-40b2-9b7f-1e6caa706b59
title: Aggiunte di dati in busta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 360cc7cb6a65853ae6c23bb995df94566d0adc09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310754"
---
# <a name="enveloped-data-additions"></a><span data-ttu-id="e2bcb-103">Aggiunte di dati in busta</span><span class="sxs-lookup"><span data-stu-id="e2bcb-103">Enveloped Data Additions</span></span>

<span data-ttu-id="e2bcb-104">Sono state apportate le modifiche seguenti alle funzionalità dei dati in busta:</span><span class="sxs-lookup"><span data-stu-id="e2bcb-104">The following changes have been made to enveloped data capabilities:</span></span>

-   <span data-ttu-id="e2bcb-105">L'identificazione del destinatario può essere eseguita non solo dall'emittente e dal numero di serie (PKCS \# 7 1,5), ma anche dall'identificatore di chiave.</span><span class="sxs-lookup"><span data-stu-id="e2bcb-105">Recipient identification can be done not only by Issuer and Serial Number (PKCS \#7 1.5), but also by Key Identifier.</span></span>
-   <span data-ttu-id="e2bcb-106">Sono disponibili tre opzioni di scambio delle chiavi del destinatario:</span><span class="sxs-lookup"><span data-stu-id="e2bcb-106">Three recipient key exchange choices are provided:</span></span>
    -   <span data-ttu-id="e2bcb-107">Trasporto chiavi con chiavi RSA.</span><span class="sxs-lookup"><span data-stu-id="e2bcb-107">Key Transport using RSA keys.</span></span>
    -   <span data-ttu-id="e2bcb-108">Accordo chiave che usa Ephemeral-Static Diffie-Hellman le chiavi dell'algoritmo incapsulate con 3DES o RC2 oppure Ephemeral-Static la curva ellittica Diffie-Hellman chiavi di algoritmo incapsulate con AES.</span><span class="sxs-lookup"><span data-stu-id="e2bcb-108">Key Agreement using either Ephemeral-Static Diffie-Hellman algorithm keys wrapped with 3DES or RC2, or Ephemeral-Static Elliptic Curve Diffie-Hellman algorithm keys wrapped with AES.</span></span>
    -   <span data-ttu-id="e2bcb-109">Trasferimento della chiave di crittografia della chiave o dell'elenco di messaggi in cui la chiave usata per crittografare la chiave di crittografia del contenuto è già stata distribuita ai destinatari.</span><span class="sxs-lookup"><span data-stu-id="e2bcb-109">Key Encryption Key or Mail List key transfer where the key used to encrypt the content encryption key has already been distributed to the recipients.</span></span> <span data-ttu-id="e2bcb-110">RC2, 3DES e AES sono consentiti come algoritmi di wrapping delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="e2bcb-110">RC2, 3DES and AES are allowed as key-wrapping algorithms.</span></span>
-   <span data-ttu-id="e2bcb-111">Gli attributi non protetti possono essere inclusi nel messaggio.</span><span class="sxs-lookup"><span data-stu-id="e2bcb-111">Unprotected attributes can be included in the message.</span></span>
-   <span data-ttu-id="e2bcb-112">È stato aggiunto un campo **OriginatorInfo** che contiene informazioni sul creatore che può contenere certificati e CRL.</span><span class="sxs-lookup"><span data-stu-id="e2bcb-112">An **OriginatorInfo** field that contains information about the originator has been added that can contain certificates and CRLs.</span></span>
-   <span data-ttu-id="e2bcb-113">Algoritmi basati sulla crittografia a curva ellittica (ECC) e AES richiedono Windows Vista o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="e2bcb-113">Elliptic Curve Cryptography (ECC) based algorithms and AES require Windows Vista or later.</span></span>

 

 



