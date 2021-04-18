---
description: CryptXML fornisce un set di API di basso livello che consentono alle applicazioni di creare e verificare le firme, l'inviluppo e lo scollegamento. È possibile usare CryptXML per creare e verificare il contenuto archiviato negli elementi dell'oggetto Signature, inclusi i manifesti.
ms.assetid: 962dffdb-caa6-4aa7-b5c6-3a9de8cfaf6c
title: Funzionalità API firma digitale XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67ae330fdd8ba75ece885e8ed0b7e2c91e60fc39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312778"
---
# <a name="xml-digital-signature-api-functionality"></a><span data-ttu-id="d6c58-104">Funzionalità API firma digitale XML</span><span class="sxs-lookup"><span data-stu-id="d6c58-104">XML Digital Signature API Functionality</span></span>

<span data-ttu-id="d6c58-105">CryptXML fornisce un set di API di basso livello che consentono alle applicazioni di creare e verificare le firme, l'inviluppo e lo scollegamento.</span><span class="sxs-lookup"><span data-stu-id="d6c58-105">CryptXML provides a low level set of APIs that allow applications to create and verify enveloped, enveloping, and detached signatures.</span></span> <span data-ttu-id="d6c58-106">È possibile usare CryptXML per creare e verificare il contenuto archiviato negli elementi dell'oggetto Signature, inclusi i manifesti.</span><span class="sxs-lookup"><span data-stu-id="d6c58-106">You can use CryptXML to create and verify content stored in signature object elements, including manifests.</span></span> <span data-ttu-id="d6c58-107">Per firmare e verificare la [*firma digitale*](../secgloss/d-gly.md)XML, è possibile usare una chiave pubblica/privata, una chiave condivisa o un certificato [*X. 509*](../secgloss/x-gly.md) o una catena di certificati.</span><span class="sxs-lookup"><span data-stu-id="d6c58-107">A public/private, shared key, or an [*X.509*](../secgloss/x-gly.md) certificate or certificate chain can be used to sign and verify the XML [*digital signature*](../secgloss/d-gly.md).</span></span>

<span data-ttu-id="d6c58-108">Le applicazioni che utilizzano CryptXML per verificare i riferimenti esterni (riferimenti destinati a un documento esterno o a un file esterno al contesto del documento) devono risolvere gli URI esterni e recuperare i dati da digerire.</span><span class="sxs-lookup"><span data-stu-id="d6c58-108">Applications that use CryptXML to verify external references (references that target an external document or file outside of the document context) must resolve the external URIs and retrieve the data to be digested.</span></span>

<span data-ttu-id="d6c58-109">Per informazioni sugli algoritmi di crittografia supportati da CryptXML, vedere algoritmi di [crittografia della firma digitale XML](xml-digital-signature-cryptographic-algorithms.md).</span><span class="sxs-lookup"><span data-stu-id="d6c58-109">For information about the cryptographic algorithms supported by CryptXML, see [XML Digital Signature Cryptographic Algorithms](xml-digital-signature-cryptographic-algorithms.md).</span></span>

<span data-ttu-id="d6c58-110">CryptXML fornisce il supporto per gli algoritmi di canonizzazione con i seguenti identificatori.</span><span class="sxs-lookup"><span data-stu-id="d6c58-110">CryptXML provides support for the canonicalization algorithms with the following identifiers.</span></span>



| <span data-ttu-id="d6c58-111">Costante</span><span class="sxs-lookup"><span data-stu-id="d6c58-111">Constant</span></span>                                              | <span data-ttu-id="d6c58-112">Valore URI</span><span class="sxs-lookup"><span data-stu-id="d6c58-112">URI value</span></span>                                                                  |
|-------------------------------------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="d6c58-113">wszURI \_ canonizzazione \_ c14n</span><span class="sxs-lookup"><span data-stu-id="d6c58-113">wszURI\_CANONICALIZATION\_C14N</span></span><br/>             | <span data-ttu-id="d6c58-114">"https://www.w3.org/TR/2001/REC-xml-c14n-20010315"</span><span class="sxs-lookup"><span data-stu-id="d6c58-114">"https://www.w3.org/TR/2001/REC-xml-c14n-20010315"</span></span><br/>               |
| <span data-ttu-id="d6c58-115">wszURI \_ canonizzazione \_ C14NC</span><span class="sxs-lookup"><span data-stu-id="d6c58-115">wszURI\_CANONICALIZATION\_C14NC</span></span><br/>            | <span data-ttu-id="d6c58-116">"https://www.w3.org/TR/2001/REC-xml-c14n-20010315\#WithComments"</span><span class="sxs-lookup"><span data-stu-id="d6c58-116">"https://www.w3.org/TR/2001/REC-xml-c14n-20010315\#WithComments"</span></span><br/> |
| <span data-ttu-id="d6c58-117">wszURI \_ canonizzazione \_ EXSLUSIVE \_ c14n</span><span class="sxs-lookup"><span data-stu-id="d6c58-117">wszURI\_CANONICALIZATION\_EXSLUSIVE\_C14N</span></span><br/>  | <span data-ttu-id="d6c58-118">"https://www.w3.org/2001/10/xml-exc-c14n\#"</span><span class="sxs-lookup"><span data-stu-id="d6c58-118">"https://www.w3.org/2001/10/xml-exc-c14n\#"</span></span><br/>                      |
| <span data-ttu-id="d6c58-119">wszURI \_ canonizzazione \_ EXSLUSIVE \_ C14NC</span><span class="sxs-lookup"><span data-stu-id="d6c58-119">wszURI\_CANONICALIZATION\_EXSLUSIVE\_C14NC</span></span><br/> | <span data-ttu-id="d6c58-120">"https://www.w3.org/2001/10/xml-exc-c14n\#WithComments"</span><span class="sxs-lookup"><span data-stu-id="d6c58-120">"https://www.w3.org/2001/10/xml-exc-c14n\#WithComments"</span></span><br/>          |



 

<span data-ttu-id="d6c58-121">CryptXML fornisce il supporto per la trasformazione firma protetta.</span><span class="sxs-lookup"><span data-stu-id="d6c58-121">CryptXML provides support for the enveloped signature transform.</span></span>



| <span data-ttu-id="d6c58-122">Costante</span><span class="sxs-lookup"><span data-stu-id="d6c58-122">Constant</span></span>                                       | <span data-ttu-id="d6c58-123">Valore URI</span><span class="sxs-lookup"><span data-stu-id="d6c58-123">URI value</span></span>                                                           |
|------------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="d6c58-124">\_trasformazione xmlns wszURI in \_ \_ busta</span><span class="sxs-lookup"><span data-stu-id="d6c58-124">wszURI\_XMLNS\_TRANSFORM\_ENVELOPED</span></span><br/> | <span data-ttu-id="d6c58-125">"https://www.w3.org/2000/09/xmldsig\#enveloped-signature"</span><span class="sxs-lookup"><span data-stu-id="d6c58-125">"https://www.w3.org/2000/09/xmldsig\#enveloped-signature"</span></span><br/> |



 

<span data-ttu-id="d6c58-126">Per impostazione predefinita, CryptXML non supporta le trasformazioni XPath o XSLT.</span><span class="sxs-lookup"><span data-stu-id="d6c58-126">By default, CryptXML does not support XPath or XSLT transforms.</span></span> <span data-ttu-id="d6c58-127">Se necessario, le applicazioni possono implementare queste trasformazioni in CryptXML.</span><span class="sxs-lookup"><span data-stu-id="d6c58-127">If required, applications can implement these transforms on top of CryptXML.</span></span>

 

 
