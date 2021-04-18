---
description: Per creare estensioni personalizzate o per codificare un'estensione complessa, è possibile scrivere gestori di estensioni personalizzati che esportano interfacce personalizzate.
ms.assetid: a33ac417-b5f9-4ad7-a26e-13cdb1e4ac1b
title: Scrittura di gestori estensioni personalizzati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61c8c4380b11fd0b0b1a5484ba0a7ab80f69c967
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316646"
---
# <a name="writing-custom-extension-handlers"></a><span data-ttu-id="9bf0f-103">Scrittura di gestori estensioni personalizzati</span><span class="sxs-lookup"><span data-stu-id="9bf0f-103">Writing Custom Extension Handlers</span></span>

<span data-ttu-id="9bf0f-104">Per creare estensioni personalizzate o per codificare un'estensione complessa, è possibile scrivere gestori di estensioni personalizzati che esportano interfacce personalizzate.</span><span class="sxs-lookup"><span data-stu-id="9bf0f-104">To create custom extensions or to encode a complex extension, you can write your own extension handlers that export custom interfaces.</span></span> <span data-ttu-id="9bf0f-105">Servizi certificati Microsoft viene fornito con le interfacce seguenti che possono essere usate per codificare diversi tipi di dati di estensione: [**ICertEncodeAltName**](/windows/desktop/api/Certenc/nn-certenc-icertencodealtname), [**ICertEncodeBitString**](/windows/desktop/api/Certenc/nn-certenc-icertencodebitstring), [**ICertEncodeCRLDistInfo**](/windows/desktop/api/Certenc/nn-certenc-icertencodecrldistinfo), [**ICertEncodeDateArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodedatearray), [**ICertEncodeLongArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodelongarray)e [**ICertEncodeStringArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodestringarray).</span><span class="sxs-lookup"><span data-stu-id="9bf0f-105">Microsoft Certificate Services ships with the following interfaces which can be used to encode various types of extension data: [**ICertEncodeAltName**](/windows/desktop/api/Certenc/nn-certenc-icertencodealtname), [**ICertEncodeBitString**](/windows/desktop/api/Certenc/nn-certenc-icertencodebitstring), [**ICertEncodeCRLDistInfo**](/windows/desktop/api/Certenc/nn-certenc-icertencodecrldistinfo), [**ICertEncodeDateArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodedatearray), [**ICertEncodeLongArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodelongarray), and [**ICertEncodeStringArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodestringarray).</span></span> <span data-ttu-id="9bf0f-106">Queste interfacce sono contenute in Certenc.dll.</span><span class="sxs-lookup"><span data-stu-id="9bf0f-106">These interfaces are contained in Certenc.dll.</span></span> <span data-ttu-id="9bf0f-107">Inoltre, le informazioni sul tipo per queste interfacce sono contenute in Certencl.dll, contenuto nella piattaforma Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="9bf0f-107">Additionally, the type information for these interfaces is contained in Certencl.dll, which is contained in the Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="9bf0f-108">Per altre informazioni sui gestori di estensioni, vedere [gestori di estensioni](extension-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="9bf0f-108">For more information about extension handlers, see [Extension Handlers](extension-handlers.md).</span></span>

 

 



