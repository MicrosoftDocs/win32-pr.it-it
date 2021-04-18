---
description: XML è uno standard di settore per la descrizione dei dati strutturati. Una firma digitale XML è una rappresentazione XML di una firma digitale che offre la possibilità di verificare l'origine e l'integrità del documento XML e i dati a cui si fa riferimento esternamente.
ms.assetid: 02ca8d9b-be08-4b15-895f-9c8c4b0ed536
title: Cenni preliminari sulla firma digitale XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b41a1b748305ab26b686e126cd201ad9e7f34d51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312777"
---
# <a name="xml-digital-signature-overview"></a><span data-ttu-id="d4215-104">Cenni preliminari sulla firma digitale XML</span><span class="sxs-lookup"><span data-stu-id="d4215-104">XML Digital Signature Overview</span></span>

<span data-ttu-id="d4215-105">XML è uno standard di settore per la descrizione dei dati strutturati.</span><span class="sxs-lookup"><span data-stu-id="d4215-105">XML is an industry standard for describing structured data.</span></span> <span data-ttu-id="d4215-106">Una firma digitale XML è una rappresentazione XML di una [*firma digitale*](../secgloss/d-gly.md) che offre la possibilità di verificare l'origine e l'integrità del documento XML e i dati a cui si fa riferimento esternamente.</span><span class="sxs-lookup"><span data-stu-id="d4215-106">An XML Digital Signature is an XML representation of a [*digital signature*](../secgloss/d-gly.md) that provides the ability to verify the origin and integrity of XML document and externally referenced data.</span></span> <span data-ttu-id="d4215-107">Le firme digitali XML possono essere utilizzate per firmare dati arbitrari, inclusi un documento o un frammento XML, una pagina HTML, testo normale o dati con codifica binaria, ad esempio un file JPEG.</span><span class="sxs-lookup"><span data-stu-id="d4215-107">XML digital signatures can be used to sign arbitrary data, including an XML document or fragment, an HTML page, plain text, or binary-encoded data such as a JPEG file.</span></span>

<span data-ttu-id="d4215-108">Il formato di firma digitale XML supportato dall'API CryptXML Digital Signature viene specificato dalla raccomandazione W3C XML Signature Syntax and Processing (Second Edition).</span><span class="sxs-lookup"><span data-stu-id="d4215-108">The XML digital signature format supported by the CryptXML digital signature API is specified by the XML Signature Syntax and Processing (Second Edition) W3C recommendation.</span></span>

<span data-ttu-id="d4215-109">La firma digitale CryptXML implementa il supporto per i tipi di firma richiesti, gli algoritmi di crittografia, gli algoritmi di canonizzazione e la trasformazione busta specificata.</span><span class="sxs-lookup"><span data-stu-id="d4215-109">The CryptXML digital signature implements support for the required signature types, cryptographic algorithms, canonicalization algorithms, and the specified enveloped transform.</span></span>

<span data-ttu-id="d4215-110">Gli sviluppatori possono estendere il set predefinito di algoritmi di crittografia supportati da CryptXML creando dll di estensioni crittografiche.</span><span class="sxs-lookup"><span data-stu-id="d4215-110">Developers can extend the default set of cryptographic algorithms supported by CryptXML by creating cryptographic extension DLLs.</span></span> <span data-ttu-id="d4215-111">Gli sviluppatori possono anche creare le proprie trasformazioni e gli algoritmi di canonizzazione personalizzati sull'API CryptXML.</span><span class="sxs-lookup"><span data-stu-id="d4215-111">Developers can also create their own custom transforms and canonicalization algorithms on top of CryptXML API.</span></span> <span data-ttu-id="d4215-112">Gli sviluppatori possono usare le API CryptXML con le API di Windows Certificate.</span><span class="sxs-lookup"><span data-stu-id="d4215-112">Developers can use the CryptXML APIs with the Windows certificate APIs.</span></span>

 

 
