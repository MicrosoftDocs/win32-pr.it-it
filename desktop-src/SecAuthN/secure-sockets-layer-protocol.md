---
description: Le informazioni contenute in questo argomento si applicano a Windows Server 2003 e Windows XP.
ms.assetid: 45536902-af80-4dca-b3ce-207086844763
title: Protocollo Secure Sockets Layer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3ed2555c854a6cc25948abe0dc83043ee632170
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967386"
---
# <a name="secure-sockets-layer-protocol"></a><span data-ttu-id="0415a-103">Protocollo Secure Sockets Layer</span><span class="sxs-lookup"><span data-stu-id="0415a-103">Secure Sockets Layer Protocol</span></span>

<span data-ttu-id="0415a-104">Le informazioni contenute in questo argomento si applicano a Windows Server 2003 e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0415a-104">The information in this topic applies to Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="0415a-105">Per i pacchetti di crittografia per Windows Server 2008 e Windows Vista, vedere pacchetti [di crittografia in Schannel](cipher-suites-in-schannel.md).</span><span class="sxs-lookup"><span data-stu-id="0415a-105">For cipher suites for Windows Server 2008 and Windows Vista, see [Cipher Suites in Schannel](cipher-suites-in-schannel.md).</span></span>

<span data-ttu-id="0415a-106">Schannel supporta le versioni 2,0 e 3,0 del [*protocollo Secure Sockets Layer (SSL)*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="0415a-106">Schannel supports versions 2.0 and 3.0 of the [*Secure Sockets Layer (SSL) protocol*](../secgloss/s-gly.md).</span></span>

> [!Note]  
> <span data-ttu-id="0415a-107">A partire da Windows 10, versione 1607 e Windows Server 2016, SSL 2,0 è stato rimosso e non è più supportato.</span><span class="sxs-lookup"><span data-stu-id="0415a-107">Beginning with Windows 10, version 1607 and Windows Server 2016, SSL 2.0 has been removed and is no longer supported.</span></span>

 

## <a name="ssl-30"></a><span data-ttu-id="0415a-108">SSL 3.0</span><span class="sxs-lookup"><span data-stu-id="0415a-108">SSL 3.0</span></span>

<span data-ttu-id="0415a-109">SSL 3,0 è il predecessore del [protocollo Transport Layer Security](transport-layer-security-protocol.md).</span><span class="sxs-lookup"><span data-stu-id="0415a-109">SSL 3.0 is the predecessor of the [Transport Layer Security Protocol](transport-layer-security-protocol.md).</span></span>

<span data-ttu-id="0415a-110">Schannel supporta i pacchetti di crittografia elencati in pacchetti di [crittografia TLS](tls-cipher-suites.md) per SSL 3,0.</span><span class="sxs-lookup"><span data-stu-id="0415a-110">Schannel supports the cipher suites listed under [TLS Cipher Suites](tls-cipher-suites.md) for SSL 3.0.</span></span> <span data-ttu-id="0415a-111">SSL 3,0 supporta tutti i pacchetti di crittografia elencati in pacchetti di crittografia TLS e SSL \_ fortezza \_ Kea \_ con la \_ fortezza \_ CBC \_ Sha.</span><span class="sxs-lookup"><span data-stu-id="0415a-111">SSL 3.0 supports all of the cipher suites listed under TLS Cipher Suites as well as SSL\_FORTEZZA\_KEA\_WITH\_FORTEZZA\_CBC\_SHA.</span></span>

## <a name="ssl-20"></a><span data-ttu-id="0415a-112">SSL 2.0</span><span class="sxs-lookup"><span data-stu-id="0415a-112">SSL 2.0</span></span>

<span data-ttu-id="0415a-113">SSL 2,0 è stato sostituito da TLS e non deve essere usato per il nuovo sviluppo.</span><span class="sxs-lookup"><span data-stu-id="0415a-113">SSL 2.0 has been superseded by TLS and should not be used for new development.</span></span>

<span data-ttu-id="0415a-114">Schannel supporta i pacchetti di crittografia seguenti per SSL 2,0.</span><span class="sxs-lookup"><span data-stu-id="0415a-114">Schannel supports the following cipher suites for SSL 2.0.</span></span> <span data-ttu-id="0415a-115">I gruppi vengono elencati in ordine dal più sicuro al meno sicuro.</span><span class="sxs-lookup"><span data-stu-id="0415a-115">The suites are listed in order from most secure to least secure.</span></span>

-   <span data-ttu-id="0415a-116">SSL \_ RC4 \_ 128 \_ con \_ MD5</span><span class="sxs-lookup"><span data-stu-id="0415a-116">SSL\_RC4\_128\_WITH\_MD5</span></span>
-   <span data-ttu-id="0415a-117">SSL \_ DES \_ 192 \_ EDE3 \_ CBC \_ con \_ MD5</span><span class="sxs-lookup"><span data-stu-id="0415a-117">SSL\_DES\_192\_EDE3\_CBC\_WITH\_MD5</span></span>
-   <span data-ttu-id="0415a-118">SSL \_ RC2 \_ CBC \_ 128 \_ CBC \_ con \_ MD5</span><span class="sxs-lookup"><span data-stu-id="0415a-118">SSL\_RC2\_CBC\_128\_CBC\_WITH\_MD5</span></span>
-   <span data-ttu-id="0415a-119">SSL \_ DES \_ 64 \_ CBC \_ con \_ MD5</span><span class="sxs-lookup"><span data-stu-id="0415a-119">SSL\_DES\_64\_CBC\_WITH\_MD5</span></span>
-   <span data-ttu-id="0415a-120">SSL \_ RC4 \_ 128 \_ EXPORT40 \_ con \_ MD5</span><span class="sxs-lookup"><span data-stu-id="0415a-120">SSL\_RC4\_128\_EXPORT40\_WITH\_MD5</span></span>

 

 
