---
description: CryptXML supporta in modo nativo gli URI elencati di seguito.
ms.assetid: 012bad01-228a-4bb0-b883-0c2c7abd9271
title: Algoritmi di crittografia per la firma digitale XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 896348375d1d1a51288980aad3793dfffc69eb18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307217"
---
# <a name="xml-digital-signature-cryptographic-algorithms"></a><span data-ttu-id="f4d41-103">Algoritmi di crittografia per la firma digitale XML</span><span class="sxs-lookup"><span data-stu-id="f4d41-103">XML Digital Signature Cryptographic Algorithms</span></span>

<span data-ttu-id="f4d41-104">CryptXML supporta in modo nativo gli URI elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="f4d41-104">CryptXML natively supports the URIs listed below.</span></span> <span data-ttu-id="f4d41-105">Se è necessario il supporto per gli algoritmi di crittografia e le trasformazioni che non fanno parte del supporto nativo, è possibile usare l' [API di crittografia:](../seccng/cng-portal.md) la nuova generazione e le [Estensioni crittografiche della firma digitale XML](xml-digital-signature-cryptographic-extensions.md) per supportare nuovi algoritmi.</span><span class="sxs-lookup"><span data-stu-id="f4d41-105">If support is required for cryptographic algorithms and transforms that are not part of the native support, you can use [Cryptography API: Next Generation](../seccng/cng-portal.md) and [XML Digital Signature Cryptographic Extensions](xml-digital-signature-cryptographic-extensions.md) to support new algorithms.</span></span>

## <a name="supported-uris"></a><span data-ttu-id="f4d41-106">URI supportati</span><span class="sxs-lookup"><span data-stu-id="f4d41-106">Supported URIs</span></span>

<span data-ttu-id="f4d41-107">Metodi digest</span><span class="sxs-lookup"><span data-stu-id="f4d41-107">Digest Methods</span></span>



| <span data-ttu-id="f4d41-108">Costante</span><span class="sxs-lookup"><span data-stu-id="f4d41-108">Constant</span></span>                                 | <span data-ttu-id="f4d41-109">Valore URI</span><span class="sxs-lookup"><span data-stu-id="f4d41-109">URI value</span></span>                                                   |
|------------------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="f4d41-110">wszURI \_ xmlns \_ DIGSIG \_ SHA1</span><span class="sxs-lookup"><span data-stu-id="f4d41-110">wszURI\_XMLNS\_DIGSIG\_SHA1</span></span><br/>   | <span data-ttu-id="f4d41-111">"https://www.w3.org/2000/09/xmldsig\#sha1"</span><span class="sxs-lookup"><span data-stu-id="f4d41-111">"https://www.w3.org/2000/09/xmldsig\#sha1"</span></span><br/>        |
| <span data-ttu-id="f4d41-112">wszURI \_ xmlns \_ DIGSIG \_ SHA256</span><span class="sxs-lookup"><span data-stu-id="f4d41-112">wszURI\_XMLNS\_DIGSIG\_SHA256</span></span><br/> | <span data-ttu-id="f4d41-113">"https://www.w3.org/2001/04/xmlenc\#sha256"</span><span class="sxs-lookup"><span data-stu-id="f4d41-113">"https://www.w3.org/2001/04/xmlenc\#sha256"</span></span><br/>       |
| <span data-ttu-id="f4d41-114">wszURI \_ xmlns \_ DIGSIG \_ SHA384</span><span class="sxs-lookup"><span data-stu-id="f4d41-114">wszURI\_XMLNS\_DIGSIG\_SHA384</span></span><br/> | <span data-ttu-id="f4d41-115">"https://www.w3.org/2001/04/xmldsig-more\#sha384"</span><span class="sxs-lookup"><span data-stu-id="f4d41-115">"https://www.w3.org/2001/04/xmldsig-more\#sha384"</span></span><br/> |
| <span data-ttu-id="f4d41-116">wszURI \_ xmlns \_ DIGSIG \_ SHA512</span><span class="sxs-lookup"><span data-stu-id="f4d41-116">wszURI\_XMLNS\_DIGSIG\_SHA512</span></span><br/> | <span data-ttu-id="f4d41-117">"https://www.w3.org/2001/04/xmlenc\#sha512"</span><span class="sxs-lookup"><span data-stu-id="f4d41-117">"https://www.w3.org/2001/04/xmlenc\#sha512"</span></span><br/>       |



 

<span data-ttu-id="f4d41-118">Metodi di firma</span><span class="sxs-lookup"><span data-stu-id="f4d41-118">Signature Methods</span></span>



| <span data-ttu-id="f4d41-119">Costante</span><span class="sxs-lookup"><span data-stu-id="f4d41-119">Constant</span></span>                                        | <span data-ttu-id="f4d41-120">Valore URI</span><span class="sxs-lookup"><span data-stu-id="f4d41-120">URI value</span></span>                                                         |
|-------------------------------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="f4d41-121">wszURI \_ xmlns \_ DIGSIG \_ RSA \_ SHA1</span><span class="sxs-lookup"><span data-stu-id="f4d41-121">wszURI\_XMLNS\_DIGSIG\_RSA\_SHA1</span></span><br/>     | <span data-ttu-id="f4d41-122">"https://www.w3.org/2000/09/xmldsig\#rsa-sha1"</span><span class="sxs-lookup"><span data-stu-id="f4d41-122">"https://www.w3.org/2000/09/xmldsig\#rsa-sha1"</span></span><br/>          |
| <span data-ttu-id="f4d41-123">wszURI \_ xmlns \_ DIGSIG \_ DSA \_ SHA1</span><span class="sxs-lookup"><span data-stu-id="f4d41-123">wszURI\_XMLNS\_DIGSIG\_DSA\_SHA1</span></span><br/>     | <span data-ttu-id="f4d41-124">"https://www.w3.org/2000/09/xmldsig\#dsa-sha1"</span><span class="sxs-lookup"><span data-stu-id="f4d41-124">"https://www.w3.org/2000/09/xmldsig\#dsa-sha1"</span></span><br/>          |
| <span data-ttu-id="f4d41-125">wszURI \_ xmlns \_ DIGSIG \_ RSA \_ SHA256</span><span class="sxs-lookup"><span data-stu-id="f4d41-125">wszURI\_XMLNS\_DIGSIG\_RSA\_SHA256</span></span><br/>   | <span data-ttu-id="f4d41-126">"https://www.w3.org/2001/04/xmldsig-more\#rsa-sha256"</span><span class="sxs-lookup"><span data-stu-id="f4d41-126">"https://www.w3.org/2001/04/xmldsig-more\#rsa-sha256"</span></span><br/>   |
| <span data-ttu-id="f4d41-127">wszURI \_ xmlns \_ DIGSIG \_ RSA \_ SHA384</span><span class="sxs-lookup"><span data-stu-id="f4d41-127">wszURI\_XMLNS\_DIGSIG\_RSA\_SHA384</span></span><br/>   | <span data-ttu-id="f4d41-128">"https://www.w3.org/2001/04/xmldsig-more\#rsa-sha384"</span><span class="sxs-lookup"><span data-stu-id="f4d41-128">"https://www.w3.org/2001/04/xmldsig-more\#rsa-sha384"</span></span><br/>   |
| <span data-ttu-id="f4d41-129">wszURI \_ xmlns \_ DIGSIG \_ RSA \_ SHA512</span><span class="sxs-lookup"><span data-stu-id="f4d41-129">wszURI\_XMLNS\_DIGSIG\_RSA\_SHA512</span></span><br/>   | <span data-ttu-id="f4d41-130">"https://www.w3.org/2001/04/xmldsig-more\#rsa-sha512"</span><span class="sxs-lookup"><span data-stu-id="f4d41-130">"https://www.w3.org/2001/04/xmldsig-more\#rsa-sha512"</span></span><br/>   |
| <span data-ttu-id="f4d41-131">wszURI \_ xmlns \_ DIGSIG \_ ECDSA \_ SHA1</span><span class="sxs-lookup"><span data-stu-id="f4d41-131">wszURI\_XMLNS\_DIGSIG\_ECDSA\_SHA1</span></span><br/>   | <span data-ttu-id="f4d41-132">"https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha1"</span><span class="sxs-lookup"><span data-stu-id="f4d41-132">"https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha1"</span></span><br/>   |
| <span data-ttu-id="f4d41-133">wszURI \_ xmlns \_ DIGSIG \_ ECDSA \_ SHA256</span><span class="sxs-lookup"><span data-stu-id="f4d41-133">wszURI\_XMLNS\_DIGSIG\_ECDSA\_SHA256</span></span><br/> | <span data-ttu-id="f4d41-134">"https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha256"</span><span class="sxs-lookup"><span data-stu-id="f4d41-134">"https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha256"</span></span><br/> |
| <span data-ttu-id="f4d41-135">wszURI \_ xmlns \_ DIGSIG \_ ECDSA \_ SHA384</span><span class="sxs-lookup"><span data-stu-id="f4d41-135">wszURI\_XMLNS\_DIGSIG\_ECDSA\_SHA384</span></span><br/> | <span data-ttu-id="f4d41-136">"https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha384"</span><span class="sxs-lookup"><span data-stu-id="f4d41-136">"https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha384"</span></span><br/> |
| <span data-ttu-id="f4d41-137">wszURI \_ xmlns \_ DIGSIG \_ ECDSA \_ SHA512</span><span class="sxs-lookup"><span data-stu-id="f4d41-137">wszURI\_XMLNS\_DIGSIG\_ECDSA\_SHA512</span></span><br/> | <span data-ttu-id="f4d41-138">"https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha512"</span><span class="sxs-lookup"><span data-stu-id="f4d41-138">"https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha512"</span></span><br/> |
| <span data-ttu-id="f4d41-139">wszURI \_ xmlns \_ DIGSIG \_ HMAC \_ SHA1</span><span class="sxs-lookup"><span data-stu-id="f4d41-139">wszURI\_XMLNS\_DIGSIG\_HMAC\_SHA1</span></span><br/>    | <span data-ttu-id="f4d41-140">"https://www.w3.org/2000/09/xmldsig\#hmac-sha1"</span><span class="sxs-lookup"><span data-stu-id="f4d41-140">"https://www.w3.org/2000/09/xmldsig\#hmac-sha1"</span></span><br/>         |
| <span data-ttu-id="f4d41-141">wszURI \_ xmlns \_ DIGSIG \_ HMAC \_ SHA256</span><span class="sxs-lookup"><span data-stu-id="f4d41-141">wszURI\_XMLNS\_DIGSIG\_HMAC\_SHA256</span></span><br/>  | <span data-ttu-id="f4d41-142">"https://www.w3.org/2001/04/xmldsig-more\#hmac-sha256"</span><span class="sxs-lookup"><span data-stu-id="f4d41-142">"https://www.w3.org/2001/04/xmldsig-more\#hmac-sha256"</span></span><br/>  |
| <span data-ttu-id="f4d41-143">wszURI \_ xmlns \_ DIGSIG \_ HMAC \_ SHA384</span><span class="sxs-lookup"><span data-stu-id="f4d41-143">wszURI\_XMLNS\_DIGSIG\_HMAC\_SHA384</span></span><br/>  | <span data-ttu-id="f4d41-144">"https://www.w3.org/2001/04/xmldsig-more\#hmac-sha384"</span><span class="sxs-lookup"><span data-stu-id="f4d41-144">"https://www.w3.org/2001/04/xmldsig-more\#hmac-sha384"</span></span><br/>  |
| <span data-ttu-id="f4d41-145">wszURI \_ xmlns \_ DIGSIG \_ HMAC \_ SHA512</span><span class="sxs-lookup"><span data-stu-id="f4d41-145">wszURI\_XMLNS\_DIGSIG\_HMAC\_SHA512</span></span><br/>  | <span data-ttu-id="f4d41-146">"https://www.w3.org/2001/04/xmldsig-more\#hmac-sha512"</span><span class="sxs-lookup"><span data-stu-id="f4d41-146">"https://www.w3.org/2001/04/xmldsig-more\#hmac-sha512"</span></span><br/>  |



 

 

 
