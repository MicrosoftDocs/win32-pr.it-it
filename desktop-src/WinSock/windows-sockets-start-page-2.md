---
description: Windows Sockets 2 (Winsock) consente ai programmatori di creare applicazioni Internet, Intranet e altre applicazioni idonee per la rete per la trasmissione di dati dell'applicazione in transito, indipendentemente dal protocollo di rete utilizzato.
ms.assetid: 1ec8758a-40fd-4c98-b839-c2409ef712d6
title: Windows Sockets 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df253572d2fca117dbc8b45b451f8c3bacc2f360
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130410"
---
# <a name="windows-sockets-2"></a><span data-ttu-id="dae7b-103">Windows Sockets 2</span><span class="sxs-lookup"><span data-stu-id="dae7b-103">Windows Sockets 2</span></span>

## <a name="purpose"></a><span data-ttu-id="dae7b-104">Scopo</span><span class="sxs-lookup"><span data-stu-id="dae7b-104">Purpose</span></span>

<span data-ttu-id="dae7b-105">Windows Sockets 2 (Winsock) consente ai programmatori di creare applicazioni Internet, Intranet e altre applicazioni idonee per la rete per la trasmissione di dati dell'applicazione in transito, indipendentemente dal protocollo di rete utilizzato.</span><span class="sxs-lookup"><span data-stu-id="dae7b-105">Windows Sockets 2 (Winsock) enables programmers to create advanced Internet, intranet, and other network-capable applications to transmit application data across the wire, independent of the network protocol being used.</span></span> <span data-ttu-id="dae7b-106">Con Winsock, i programmatori possono accedere alle funzionalità di rete avanzate di Microsoft® Windows®, ad esempio il multicast e la qualità del servizio (QoS).</span><span class="sxs-lookup"><span data-stu-id="dae7b-106">With Winsock, programmers are provided access to advanced Microsoft® Windows® networking capabilities such as multicast and Quality of Service (QoS).</span></span>

<span data-ttu-id="dae7b-107">Winsock segue il modello WOSA (Windows Open System Architecture); definisce un'interfaccia del provider di servizi (SPI) standard tra il Application Programming Interface (API), con le funzioni esportate e gli stack di protocolli.</span><span class="sxs-lookup"><span data-stu-id="dae7b-107">Winsock follows the Windows Open System Architecture (WOSA) model; it defines a standard service provider interface (SPI) between the application programming interface (API), with its exported functions and the protocol stacks.</span></span> <span data-ttu-id="dae7b-108">Usa il paradigma Sockets che è stato inizialmente popolare da Berkeley Software Distribution (BSD) UNIX.</span><span class="sxs-lookup"><span data-stu-id="dae7b-108">It uses the sockets paradigm that was first popularized by Berkeley Software Distribution (BSD) UNIX.</span></span> <span data-ttu-id="dae7b-109">In seguito è stato adattato per Windows in Windows Sockets 1,1, con cui le applicazioni Windows Sockets 2 sono compatibili con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="dae7b-109">It was later adapted for Windows in Windows Sockets 1.1, with which Windows Sockets 2 applications are backward compatible.</span></span> <span data-ttu-id="dae7b-110">Programmazione Winsock precedentemente centrata su TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="dae7b-110">Winsock programming previously centered around TCP/IP.</span></span> <span data-ttu-id="dae7b-111">Alcune procedure di programmazione che hanno funzionato con TCP/IP non funzionano con ogni protocollo.</span><span class="sxs-lookup"><span data-stu-id="dae7b-111">Some programming practices that worked with TCP/IP do not work with every protocol.</span></span> <span data-ttu-id="dae7b-112">Di conseguenza, l'API di Windows Sockets 2 aggiunge funzioni laddove necessario per gestire diversi protocolli.</span><span class="sxs-lookup"><span data-stu-id="dae7b-112">As a result, the Windows Sockets 2 API adds functions where necessary to handle several protocols.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="dae7b-113">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="dae7b-113">Developer audience</span></span>

<span data-ttu-id="dae7b-114">Windows Sockets 2 è progettato per l'uso da programmatori C/C++.</span><span class="sxs-lookup"><span data-stu-id="dae7b-114">Windows Sockets 2 is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="dae7b-115">È necessaria una certa familiarità con la rete di Windows.</span><span class="sxs-lookup"><span data-stu-id="dae7b-115">Familiarity with Windows networking is required.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="dae7b-116">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="dae7b-116">Run-time requirements</span></span>

<span data-ttu-id="dae7b-117">Windows Sockets 2 può essere usato in tutte le piattaforme Windows.</span><span class="sxs-lookup"><span data-stu-id="dae7b-117">Windows Sockets 2 can be used on all Windows platforms.</span></span> <span data-ttu-id="dae7b-118">Laddove sono presenti alcune implementazioni o funzionalità delle restrizioni della piattaforma Windows Sockets 2, sono chiaramente indicate nella documentazione.</span><span class="sxs-lookup"><span data-stu-id="dae7b-118">Where certain implementations or capabilities of Windows Sockets 2 platform restrictions do exist, they are clearly noted in the documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="dae7b-119">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="dae7b-119">In this section</span></span>



| <span data-ttu-id="dae7b-120">Argomento</span><span class="sxs-lookup"><span data-stu-id="dae7b-120">Topic</span></span>                                                                                             | <span data-ttu-id="dae7b-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dae7b-121">Description</span></span>                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dae7b-122">Novità di Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="dae7b-122">What's New for Windows Sockets</span></span>](what-s-new-for-windows-sockets-2.md)<br/>                 | <span data-ttu-id="dae7b-123">Informazioni sulle nuove funzionalità per Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="dae7b-123">Information on new features for Windows Sockets.</span></span><br/>                                                                                                                                                                                                                                 |
| [<span data-ttu-id="dae7b-124">Supporto del protocollo di rete Winsock in Windows</span><span class="sxs-lookup"><span data-stu-id="dae7b-124">Winsock Network Protocol Support in Windows</span></span>](network-protocol-support-in-windows.md)<br/> | <span data-ttu-id="dae7b-125">Informazioni sul supporto del protocollo di rete per Windows Sockets in versioni diverse di Windows.</span><span class="sxs-lookup"><span data-stu-id="dae7b-125">Information on network protocol support for Windows Sockets on different versions of Windows.</span></span><br/>                                                                                                                                                                                    |
| [<span data-ttu-id="dae7b-126">Informazioni su Winsock</span><span class="sxs-lookup"><span data-stu-id="dae7b-126">About Winsock</span></span>](about-winsock.md)<br/>                                                     | <span data-ttu-id="dae7b-127">Informazioni generali sulla programmazione di Windows Socket considerazioni, architettura e funzionalità disponibili per gli sviluppatori.</span><span class="sxs-lookup"><span data-stu-id="dae7b-127">General information on Windows Sockets programming considerations, architecture, and capabilities available to developers.</span></span><br/>                                                                                                                                                       |
| [<span data-ttu-id="dae7b-128">Uso di Winsock</span><span class="sxs-lookup"><span data-stu-id="dae7b-128">Using Winsock</span></span>](using-winsock.md)<br/>                                                     | <span data-ttu-id="dae7b-129">Procedure e tecniche di programmazione utilizzate con Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="dae7b-129">Procedures and programming techniques used with Windows Sockets.</span></span> <span data-ttu-id="dae7b-130">Questa sezione include tecniche di programmazione Winsock di base, ad esempio [Introduzione con Winsock](getting-started-with-winsock.md), nonché tecniche avanzate utili per gli sviluppatori Winsock esperti.</span><span class="sxs-lookup"><span data-stu-id="dae7b-130">This section includes basic Winsock programming techniques, such as [Getting Started With Winsock](getting-started-with-winsock.md), as well as advanced techniques useful for experienced Winsock developers.</span></span><br/> |
| [<span data-ttu-id="dae7b-131">Riferimento Winsock</span><span class="sxs-lookup"><span data-stu-id="dae7b-131">Winsock Reference</span></span>](winsock-reference.md)<br/>                                             | <span data-ttu-id="dae7b-132">Documentazione dell'API di Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="dae7b-132">Documentation of the Windows Sockets API.</span></span><br/>                                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="dae7b-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="dae7b-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dae7b-134">Helper IP</span><span class="sxs-lookup"><span data-stu-id="dae7b-134">IP Helper</span></span>](../iphlp/ip-helper-start-page.md)
</dt> <dt>

[<span data-ttu-id="dae7b-135">QoS (Quality of Service)</span><span class="sxs-lookup"><span data-stu-id="dae7b-135">Quality of Service</span></span>](/previous-versions/windows/desktop/qos/qos-start-page)
</dt> </dl>

 

 
