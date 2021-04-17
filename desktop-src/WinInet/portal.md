---
title: Windows Internet
description: Microsoft Windows Internet (WinINet) Application Programming Interface (API) consente alle applicazioni di accedere ai protocolli Internet standard, ad esempio FTP e HTTP. Per semplicità d'uso, WinINet astrae questi protocolli in un'interfaccia di alto livello.
ms.assetid: 9d1856ac-f281-4582-bb70-83a8ec674914
keywords:
- Windows Internet WinINet
- WinINet WinINet, portale
- Windows Internet WinINet, pagina iniziale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6b5b76fefea900d3f187deb89929d3a09fe3c78
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473851"
---
# <a name="windows-internet"></a><span data-ttu-id="a34dc-107">Windows Internet</span><span class="sxs-lookup"><span data-stu-id="a34dc-107">Windows Internet</span></span>

## <a name="purpose"></a><span data-ttu-id="a34dc-108">Scopo</span><span class="sxs-lookup"><span data-stu-id="a34dc-108">Purpose</span></span>

<span data-ttu-id="a34dc-109">Microsoft Windows Internet (WinINet) Application Programming Interface (API) consente alle applicazioni di accedere ai protocolli Internet standard, ad esempio FTP e HTTP.</span><span class="sxs-lookup"><span data-stu-id="a34dc-109">The Microsoft Windows Internet (WinINet) application programming interface (API) enables applications to access standard Internet protocols, such as FTP and HTTP.</span></span> <span data-ttu-id="a34dc-110">Per semplicità d'uso, WinINet astrae questi protocolli in un'interfaccia di alto livello.</span><span class="sxs-lookup"><span data-stu-id="a34dc-110">For ease of use, WinINet abstracts these protocols into a high-level interface.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="a34dc-111">Se applicabile</span><span class="sxs-lookup"><span data-stu-id="a34dc-111">Where applicable</span></span>

<span data-ttu-id="a34dc-112">WinINet non supporta le implementazioni del server.</span><span class="sxs-lookup"><span data-stu-id="a34dc-112">WinINet does not support server implementations.</span></span> <span data-ttu-id="a34dc-113">Inoltre, non deve essere utilizzato da un servizio.</span><span class="sxs-lookup"><span data-stu-id="a34dc-113">In addition, it should not be used from a service.</span></span> <span data-ttu-id="a34dc-114">Per le implementazioni o i servizi del server, usare i [Servizi http di Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="a34dc-114">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

## <a name="developer-audience"></a><span data-ttu-id="a34dc-115">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="a34dc-115">Developer audience</span></span>

<span data-ttu-id="a34dc-116">WinINet è progettato per l'uso da programmatori C/C++.</span><span class="sxs-lookup"><span data-stu-id="a34dc-116">WinINet is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="a34dc-117">Richiede una conoscenza di base dei protocolli FTP e HTTP.</span><span class="sxs-lookup"><span data-stu-id="a34dc-117">It requires a basic understanding of the FTP and HTTP protocols.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="a34dc-118">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="a34dc-118">Run-time requirements</span></span>

<span data-ttu-id="a34dc-119">Le applicazioni che usano l'API WinINet richiedono Windows NT 4,0 o versione successiva o Windows Me/98/95.</span><span class="sxs-lookup"><span data-stu-id="a34dc-119">Applications that use the WinINet API require Windows NT 4.0 or later, or Windows Me/98/95.</span></span> <span data-ttu-id="a34dc-120">Per ulteriori informazioni sui sistemi operativi o sui componenti necessari per utilizzare un particolare elemento di programmazione, vedere la sezione requisiti della documentazione.</span><span class="sxs-lookup"><span data-stu-id="a34dc-120">For more information about which operating systems or components are required to use a particular programming element, see the Requirements section of the documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="a34dc-121">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="a34dc-121">In this section</span></span>



| <span data-ttu-id="a34dc-122">Argomento</span><span class="sxs-lookup"><span data-stu-id="a34dc-122">Topic</span></span>                                                          | <span data-ttu-id="a34dc-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a34dc-123">Description</span></span>                                                      |
|----------------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="a34dc-124">Informazioni su Windows Internet</span><span class="sxs-lookup"><span data-stu-id="a34dc-124">About Windows Internet</span></span>](about-wininet.md)<br/>         | <span data-ttu-id="a34dc-125">Informazioni generali sull'API Windows Internet.</span><span class="sxs-lookup"><span data-stu-id="a34dc-125">General information about the Windows Internet API.</span></span><br/>   |
| [<span data-ttu-id="a34dc-126">Utilizzo di Windows Internet</span><span class="sxs-lookup"><span data-stu-id="a34dc-126">Using Windows Internet</span></span>](using-wininet.md)<br/>         | <span data-ttu-id="a34dc-127">Guida alla programmazione per l'API di Windows Internet.</span><span class="sxs-lookup"><span data-stu-id="a34dc-127">Programming guide for the Windows Internet API.</span></span><br/>       |
| [<span data-ttu-id="a34dc-128">Informazioni di riferimento su Windows Internet</span><span class="sxs-lookup"><span data-stu-id="a34dc-128">Windows Internet Reference</span></span>](wininet-reference.md)<br/> | <span data-ttu-id="a34dc-129">Documentazione di riferimento per l'API di Windows Internet.</span><span class="sxs-lookup"><span data-stu-id="a34dc-129">Reference documentation for the Windows Internet API.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="a34dc-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a34dc-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a34dc-131">Servizi HTTP di Microsoft Windows (WinHTTP)</span><span class="sxs-lookup"><span data-stu-id="a34dc-131">Microsoft Windows HTTP Services (WinHTTP)</span></span>](/windows/desktop/WinHttp/winhttp-start-page)
</dt> </dl>

 

