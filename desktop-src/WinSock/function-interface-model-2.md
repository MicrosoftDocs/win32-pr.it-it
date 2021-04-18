---
description: Il trasporto e lo spazio dei nomi Windows Sockets&\# 8211; i provider di servizi sono dll con un singolo punto di ingresso della routine esportato per la funzione di inizializzazione del provider di servizi WSPStartup o NSPStartup.
ms.assetid: a3422513-92e2-4011-a756-04ed853e9d56
title: Modello di interfaccia di funzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a500de391dd5f65da610ba79d33938443794262
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306976"
---
# <a name="function-interface-model"></a><span data-ttu-id="72bd2-103">Modello di interfaccia di funzione</span><span class="sxs-lookup"><span data-stu-id="72bd2-103">Function Interface Model</span></span>

<span data-ttu-id="72bd2-104">Trasporto e spazio dei nomi Windows Sockets: i provider di servizi sono dll con un singolo punto di ingresso della procedura esportato per la funzione di inizializzazione del provider di servizi [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup) o [**NSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup).</span><span class="sxs-lookup"><span data-stu-id="72bd2-104">Windows Sockets transport and namespace–service providers are DLLs with a single exported procedure entry point for the service provider initialization function [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup) or [**NSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup), respectively.</span></span> <span data-ttu-id="72bd2-105">Tutte le altre funzioni del provider di servizi vengono rese accessibili a WS2 \_32.dll tramite la tabella dispatch del provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="72bd2-105">All other service provider functions are made accessible to the Ws2\_32.dll through the service provider's dispatch table.</span></span> <span data-ttu-id="72bd2-106">Le DLL del provider di servizi vengono caricate in memoria da WS2 \_32.dll solo quando sono necessarie e vengono scaricate quando i servizi non sono più necessari.</span><span class="sxs-lookup"><span data-stu-id="72bd2-106">Service provider DLL's are loaded into memory by the Ws2\_32.dll only when needed, and are unloaded when their services are no longer required.</span></span>

<span data-ttu-id="72bd2-107">SPI definisce inoltre diverse circostanze in cui un provider di servizi di trasporto chiama il32.dll WS2 \_ (chiamate) per ottenere i servizi di supporto dll.</span><span class="sxs-lookup"><span data-stu-id="72bd2-107">The SPI also defines several circumstances in which a transport service provider calls up into the Ws2\_32.dll (upcalls) to obtain DLL support services.</span></span> <span data-ttu-id="72bd2-108">Alla DLL del provider del servizio di trasporto viene assegnata la tabella WS2 del \_32.dll di invio tramite il parametro *UpcallTable* a [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup).</span><span class="sxs-lookup"><span data-stu-id="72bd2-108">The transport service provider DLL is given the Ws2\_32.dll's upcall dispatch table through the *UpcallTable* parameter to [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup).</span></span>

<span data-ttu-id="72bd2-109">I provider di servizi devono avere l'estensione del nome file modificata da "DLL" a ". WSP "or". NSP ".</span><span class="sxs-lookup"><span data-stu-id="72bd2-109">Service providers should have their file name extension changed from "DLL" to ".WSP" or ".NSP".</span></span> <span data-ttu-id="72bd2-110">Questo requisito non è rigoroso.</span><span class="sxs-lookup"><span data-stu-id="72bd2-110">This requirement is not strict.</span></span> <span data-ttu-id="72bd2-111">Un provider di servizi continuerà a funzionare con il \_32.dll WS2 con qualsiasi estensione di file.</span><span class="sxs-lookup"><span data-stu-id="72bd2-111">A service provider will still operate with the Ws2\_32.dll with any file name extension.</span></span>

<span data-ttu-id="72bd2-112">Winsock SPI usa la convenzione di denominazione dei prefissi di funzione seguente:</span><span class="sxs-lookup"><span data-stu-id="72bd2-112">The Winsock SPI uses the following function prefix naming convention:</span></span>

| <span data-ttu-id="72bd2-113">Prefisso</span><span class="sxs-lookup"><span data-stu-id="72bd2-113">Prefix</span></span> | <span data-ttu-id="72bd2-114">Significato</span><span class="sxs-lookup"><span data-stu-id="72bd2-114">Meaning</span></span>                          | <span data-ttu-id="72bd2-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="72bd2-115">Description</span></span>                                       |
|--------|----------------------------------|---------------------------------------------------|
| <span data-ttu-id="72bd2-116">WSP</span><span class="sxs-lookup"><span data-stu-id="72bd2-116">WSP</span></span>    | <span data-ttu-id="72bd2-117">Provider di servizi Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="72bd2-117">Windows Sockets Service Provider</span></span> | <span data-ttu-id="72bd2-118">Punti di ingresso del provider di servizi di trasporto</span><span class="sxs-lookup"><span data-stu-id="72bd2-118">Transport service provider entry points</span></span>           |
| <span data-ttu-id="72bd2-119">WPU</span><span class="sxs-lookup"><span data-stu-id="72bd2-119">WPU</span></span>    | <span data-ttu-id="72bd2-120">Chiamata del provider Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="72bd2-120">Windows Sockets Provider Upcall</span></span>  | <span data-ttu-id="72bd2-121">WS2 \_32.dll punti di ingresso per i provider di servizi</span><span class="sxs-lookup"><span data-stu-id="72bd2-121">Ws2\_32.dll entry points for service providers</span></span>    |
| <span data-ttu-id="72bd2-122">WSC</span><span class="sxs-lookup"><span data-stu-id="72bd2-122">WSC</span></span>    | <span data-ttu-id="72bd2-123">Configurazione di Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="72bd2-123">Windows Sockets Configuration</span></span>    | <span data-ttu-id="72bd2-124">\_Punti di ingresso di WS232.dll per le applet di installazione</span><span class="sxs-lookup"><span data-stu-id="72bd2-124">WS2\_32.dll entry points for installation applets</span></span> |
| <span data-ttu-id="72bd2-125">NSP</span><span class="sxs-lookup"><span data-stu-id="72bd2-125">NSP</span></span>    | <span data-ttu-id="72bd2-126">Provider dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="72bd2-126">Namespace Provider</span></span>               | <span data-ttu-id="72bd2-127">Punti di ingresso del provider dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="72bd2-127">Namespace provider entry points</span></span>                   |



 

<span data-ttu-id="72bd2-128">Come descritto in precedenza, questi punti di ingresso non vengono esportati (ad eccezione di [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup) e [**NSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup)), ma è possibile accedervi tramite uno scambio di tabelle di invio.</span><span class="sxs-lookup"><span data-stu-id="72bd2-128">As described above, these entry points are not exported (with the exception of [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup) and [**NSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup)), but are accessed through an exchange of dispatch tables.</span></span>

 

 



