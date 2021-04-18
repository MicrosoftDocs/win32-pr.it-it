---
description: Windows Sockets (Winsock) Service Provider Interface (SPI).
ms.assetid: 59ac7ce6-10e7-40ac-bdce-dc01251b0bc5
title: SPI di Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ecf63a45f5175a86b8f5eb2a77ef0293182e38f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313223"
---
# <a name="winsock-spi"></a><span data-ttu-id="6e556-103">SPI di Winsock</span><span class="sxs-lookup"><span data-stu-id="6e556-103">Winsock SPI</span></span>

<span data-ttu-id="6e556-104">L'interfaccia del provider di servizi Winsock, o Winsock SPI, è una disciplina specializzata di Winsock utilizzata per creare i provider. i provider di trasporto, ad esempio gli stack di protocolli TCP/IP o IPX/SPX, usano il protocollo SPI SPI, così come i provider di spazio dei nomi, ad esempio il DNS (Domain Naming System) di Internet.</span><span class="sxs-lookup"><span data-stu-id="6e556-104">The Winsock Service Provider Interface, or Winsock SPI, is a specialized discipline of Winsock used to create providers; transport providers such as TCP/IP or IPX/SPX protocol stacks use the Winsock SPI, as do namespace providers such as the Internet's Domain Naming System (DNS).</span></span>

<span data-ttu-id="6e556-105">La programmazione di rete tradizionale, ad esempio l'abilitazione delle applicazioni per la comunicazione in rete, non richiede l'uso di interfacce Winsock SPI; usare invece le interfacce standard [Winsock](winsock-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="6e556-105">Traditional network programming, such as enabling applications to communicate over the network, does not require use of Winsock SPI interfaces; use standard [Winsock](winsock-reference.md) interfaces instead.</span></span>

 

<span data-ttu-id="6e556-106">Winsock SPI usa la convenzione di denominazione dei prefissi di funzione seguente.</span><span class="sxs-lookup"><span data-stu-id="6e556-106">The Winsock SPI uses the following function prefix naming convention.</span></span>



| <span data-ttu-id="6e556-107">Prefisso</span><span class="sxs-lookup"><span data-stu-id="6e556-107">Prefix</span></span> | <span data-ttu-id="6e556-108">Significato</span><span class="sxs-lookup"><span data-stu-id="6e556-108">Meaning</span></span>                          | <span data-ttu-id="6e556-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e556-109">Description</span></span>                                       |
|--------|----------------------------------|---------------------------------------------------|
| <span data-ttu-id="6e556-110">WSP</span><span class="sxs-lookup"><span data-stu-id="6e556-110">WSP</span></span>    | <span data-ttu-id="6e556-111">Provider di servizi Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="6e556-111">Windows Sockets Service Provider</span></span> | <span data-ttu-id="6e556-112">Punti di ingresso del provider di servizi di trasporto</span><span class="sxs-lookup"><span data-stu-id="6e556-112">Transport service provider entry points</span></span>           |
| <span data-ttu-id="6e556-113">WPU</span><span class="sxs-lookup"><span data-stu-id="6e556-113">WPU</span></span>    | <span data-ttu-id="6e556-114">Chiamata del provider Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="6e556-114">Windows Sockets Provider Upcall</span></span>  | <span data-ttu-id="6e556-115">WS2 \_32.dll punti di ingresso per i provider di servizi</span><span class="sxs-lookup"><span data-stu-id="6e556-115">Ws2\_32.dll entry points for service providers</span></span>    |
| <span data-ttu-id="6e556-116">WSC</span><span class="sxs-lookup"><span data-stu-id="6e556-116">WSC</span></span>    | <span data-ttu-id="6e556-117">Configurazione di Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="6e556-117">Windows Sockets Configuration</span></span>    | <span data-ttu-id="6e556-118">\_Punti di ingresso di WS232.dll per le applet di installazione</span><span class="sxs-lookup"><span data-stu-id="6e556-118">WS2\_32.dll entry points for installation applets</span></span> |
| <span data-ttu-id="6e556-119">NSP</span><span class="sxs-lookup"><span data-stu-id="6e556-119">NSP</span></span>    | <span data-ttu-id="6e556-120">Provider dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6e556-120">Namespace Provider</span></span>               | <span data-ttu-id="6e556-121">Punti di ingresso del provider dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6e556-121">Namespace provider entry points</span></span>                   |



 

 

 



