---
description: In questa sezione vengono descritte le estensioni Winsock specifiche di Internet-Packet Exchange/Sequenced Packet Exchange (IPX/SPX). Vengono inoltre descritti gli aspetti delle funzioni Winsock di base che richiedono una particolare attenzione oppure possono presentare un comportamento univoco.
ms.assetid: 8447e063-767a-40b8-b094-724393e85be2
title: Winsock IPX/SPX Annex
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c533781fa07c997d7f2363dd6b00d6b4213f22e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308861"
---
# <a name="winsock-ipxspx-annex"></a><span data-ttu-id="13f02-104">Winsock IPX/SPX Annex</span><span class="sxs-lookup"><span data-stu-id="13f02-104">Winsock IPX/SPX Annex</span></span>

<span data-ttu-id="13f02-105">In questa sezione vengono descritte le estensioni Winsock specifiche di Internet-Packet Exchange/Sequenced Packet Exchange (IPX/SPX).</span><span class="sxs-lookup"><span data-stu-id="13f02-105">This section describes Winsock extensions specific to Internetwork Packet Exchange/Sequenced Packet Exchange (IPX/SPX).</span></span> <span data-ttu-id="13f02-106">Vengono inoltre descritti gli aspetti delle funzioni Winsock di base che richiedono una particolare attenzione oppure possono presentare un comportamento univoco.</span><span class="sxs-lookup"><span data-stu-id="13f02-106">It also describes aspects of base Winsock functions that either require special consideration or may exhibit unique behavior.</span></span>



| <span data-ttu-id="13f02-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="13f02-107">Element</span></span>          | <span data-ttu-id="13f02-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="13f02-108">Description</span></span>                                                                                                                                     |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13f02-109">Nome/i protocollo</span><span class="sxs-lookup"><span data-stu-id="13f02-109">Protocol name(s)</span></span> | <span data-ttu-id="13f02-110">IPX, SPX</span><span class="sxs-lookup"><span data-stu-id="13f02-110">IPX, SPX</span></span>                                                                                                                                        |
| <span data-ttu-id="13f02-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="13f02-111">Description</span></span>      | <span data-ttu-id="13f02-112">Fornisce servizi di trasporto sul livello di rete IPX: IPX per datagrammi non affidabili, SPX per flussi di messaggi affidabili e orientati alla connessione.</span><span class="sxs-lookup"><span data-stu-id="13f02-112">Provides transport services over the IPX networking layer: IPX for unreliable datagrams, SPX for reliable, connection-oriented message streams.</span></span> |
| <span data-ttu-id="13f02-113">Famiglia di indirizzi</span><span class="sxs-lookup"><span data-stu-id="13f02-113">Address family</span></span>   | <span data-ttu-id="13f02-114">\_IPX AF</span><span class="sxs-lookup"><span data-stu-id="13f02-114">AF\_IPX</span></span>                                                                                                                                         |
| <span data-ttu-id="13f02-115">File di intestazione</span><span class="sxs-lookup"><span data-stu-id="13f02-115">Header file</span></span>      | <span data-ttu-id="13f02-116">WSIPX. h</span><span class="sxs-lookup"><span data-stu-id="13f02-116">Wsipx.h</span></span>                                                                                                                                         |



 

<span data-ttu-id="13f02-117">In questa sezione viene illustrato come utilizzare Winsock con la famiglia di protocolli IPX, consentendo il trasferimento di applicazioni IPX tradizionali in Winsock.</span><span class="sxs-lookup"><span data-stu-id="13f02-117">This section discusses how to use Winsock with the IPX family of protocols, enabling traditional IPX applications to be ported to Winsock.</span></span> <span data-ttu-id="13f02-118">Le reti IPX operano in modo sostanzialmente diverso rispetto alle reti IP, pertanto è necessario considerare tali differenze quando si utilizza IPX/SPX.</span><span class="sxs-lookup"><span data-stu-id="13f02-118">IPX networks operate in a fundamentally different manner than IP networks, so such differences must be considered when using IPX/SPX.</span></span>

 

 



