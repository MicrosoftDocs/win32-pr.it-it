---
description: L'API di firma digitale XPS consente a un utente di firmare un documento, verificare l'identità del firmatario e indicare se un documento XPS è stato modificato dopo la firma.
ms.assetid: 8a23617e-92fe-4662-b602-47add5716358
title: API di firma digitale XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c56485a532afbb148e62901c38db49ab81963c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317271"
---
# <a name="xps-digital-signature-api"></a><span data-ttu-id="eff4a-103">API di firma digitale XPS</span><span class="sxs-lookup"><span data-stu-id="eff4a-103">XPS Digital Signature API</span></span>

<span data-ttu-id="eff4a-104">L'API di firma digitale XPS consente a un utente di firmare un documento, verificare l'identità del firmatario e indicare se un documento XPS è stato modificato dopo la firma.</span><span class="sxs-lookup"><span data-stu-id="eff4a-104">The XPS Digital Signature API enables a user to sign a document, verify the identity of the signer, and indicate whether an XPS document has changed since it was signed.</span></span> <span data-ttu-id="eff4a-105">L'API di firma digitale XPS è basata sulla tecnologia di firma digitale usata nelle convenzioni Open Packaging, che sono specificate nella prima edizione, parte 2, "Open Packaging Conventions", dei [formati di file standard ECMA-376, Office Open XML](https://www.ecma-international.org/publications/standards/Ecma-376.htm).</span><span class="sxs-lookup"><span data-stu-id="eff4a-105">The XPS Digital Signature API is built on the digital signature technology that is used in the Open Packaging Conventions, which are specified in the 1st edition, Part 2, "Open Packaging Conventions," of [Standard ECMA-376, Office Open XML File Formats](https://www.ecma-international.org/publications/standards/Ecma-376.htm).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="eff4a-106">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="eff4a-106">In This Section</span></span>

<span data-ttu-id="eff4a-107">In questa sezione vengono trattati gli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="eff4a-107">This section contains the following topics.</span></span>

### <a name="about-xps-digital-signature-api"></a><span data-ttu-id="eff4a-108">Informazioni sull'API di firma digitale XPS</span><span class="sxs-lookup"><span data-stu-id="eff4a-108">About XPS Digital Signature API</span></span>

<span data-ttu-id="eff4a-109">[Informazioni su XPS Digital Signature API](about-xps-digital-signatures.md) descrive l'API di firma digitale XPS a un livello elevato.</span><span class="sxs-lookup"><span data-stu-id="eff4a-109">[About XPS Digital Signature API](about-xps-digital-signatures.md) describes the XPS Digital Signature API at a high level.</span></span>

### <a name="using-xps-digital-signature-api"></a><span data-ttu-id="eff4a-110">Uso dell'API di firma digitale XPS</span><span class="sxs-lookup"><span data-stu-id="eff4a-110">Using XPS Digital Signature API</span></span>

<span data-ttu-id="eff4a-111">[Tramite l'API di firma digitale XPS](using-digital-signatures-in-xps-documents.md) viene descritto come utilizzare l'API di firma digitale XPS.</span><span class="sxs-lookup"><span data-stu-id="eff4a-111">[Using XPS Digital Signature API](using-digital-signatures-in-xps-documents.md) describes how to use the XPS Digital Signature API.</span></span>

### <a name="xps-digital-signatures-reference"></a><span data-ttu-id="eff4a-112">Informazioni di riferimento sulle firme digitali XPS</span><span class="sxs-lookup"><span data-stu-id="eff4a-112">XPS Digital Signatures Reference</span></span>

<span data-ttu-id="eff4a-113">Il [riferimento all'API di firma digitale XPS](xps-digital-signatures-programming-reference.md) contiene un elenco completo delle interfacce, dei metodi e degli enumeratori implementati dall'API XPS Digital Signatures.</span><span class="sxs-lookup"><span data-stu-id="eff4a-113">The [XPS Digital Signature API Reference](xps-digital-signatures-programming-reference.md) contains a complete listing of the interfaces, methods, and enumerators that are implemented by the XPS Digital Signatures API.</span></span>

## <a name="platform-update-for-windows-vista"></a><span data-ttu-id="eff4a-114">Aggiornamento della piattaforma per Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eff4a-114">Platform Update for Windows Vista</span></span>

<span data-ttu-id="eff4a-115">Le interfacce di firma digitale XPS descritte in questa sezione non sono supportate dall'aggiornamento della piattaforma per Windows Vista o dall'aggiornamento della piattaforma per Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="eff4a-115">The XPS Digital Signature interfaces that are described in this section are not supported by the Platform Update for Windows Vista or the Platform Update for Windows Server 2008.</span></span> <span data-ttu-id="eff4a-116">Un'applicazione che richiede queste interfacce deve essere eseguita in Windows 7 o versione successiva o in Windows Server 2008 R2 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="eff4a-116">An application that requires these interfaces should run on Windows 7 or later, or on Windows Server 2008 R2 or later.</span></span> <span data-ttu-id="eff4a-117">In caso contrario, l'applicazione potrebbe non fornire all'utente la funzionalità completa dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="eff4a-117">Otherwise, the application may not provide the user with the application's complete functionality.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eff4a-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="eff4a-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eff4a-119">Packaging</span><span class="sxs-lookup"><span data-stu-id="eff4a-119">Packaging</span></span>](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[<span data-ttu-id="eff4a-120">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="eff4a-120">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> <dt>

[<span data-ttu-id="eff4a-121">Standard ECMA-376, formati di file Office Open XML</span><span class="sxs-lookup"><span data-stu-id="eff4a-121">Standard ECMA-376, Office Open XML File Formats</span></span>](https://www.ecma-international.org/publications/standards/Ecma-376.htm)
</dt> </dl>

 

 
