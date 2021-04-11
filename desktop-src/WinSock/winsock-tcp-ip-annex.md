---
description: In questa sezione vengono descritte le funzioni, le strutture di dati e i controlli Transmission Control Protocol/Internet Protocol (TCP/IP).
ms.assetid: ff92750b-453e-4328-821c-1098de8e6125
title: Allegato TCP/IP Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4fd86a016ed80d9c71ac1647323508cb4dc7b08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226479"
---
# <a name="winsock-tcpip-annex"></a><span data-ttu-id="75516-103">Allegato TCP/IP Winsock</span><span class="sxs-lookup"><span data-stu-id="75516-103">Winsock TCP/IP Annex</span></span>

<span data-ttu-id="75516-104">In questa sezione vengono descritte le funzioni, le strutture di dati e i controlli Transmission Control Protocol/Internet Protocol (TCP/IP).</span><span class="sxs-lookup"><span data-stu-id="75516-104">This section describes Transmission Control Protocol/Internet Protocol (TCP/IP) functions, data structures, and controls.</span></span>



| <span data-ttu-id="75516-105">Elemento</span><span class="sxs-lookup"><span data-stu-id="75516-105">Element</span></span>          | <span data-ttu-id="75516-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="75516-106">Description</span></span>                                                                                                                                 |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75516-107">Nome/i protocollo</span><span class="sxs-lookup"><span data-stu-id="75516-107">Protocol name(s)</span></span> | <span data-ttu-id="75516-108">TCP, UDP</span><span class="sxs-lookup"><span data-stu-id="75516-108">TCP, UDP</span></span>                                                                                                                                    |
| <span data-ttu-id="75516-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="75516-109">Description</span></span>      | <span data-ttu-id="75516-110">Fornisce servizi di trasporto sul livello di rete IP: UDP per datagrammi non affidabili, TCP per flussi di byte affidabili e orientati alla connessione.</span><span class="sxs-lookup"><span data-stu-id="75516-110">Provides transport services over the IP networking layer: UDP for unreliable datagrams, TCP for reliable, connection-oriented byte streams.</span></span> |
| <span data-ttu-id="75516-111">Famiglia di indirizzi</span><span class="sxs-lookup"><span data-stu-id="75516-111">Address family</span></span>   | <span data-ttu-id="75516-112">**AF \_ INET**, **AF \_ INET6**</span><span class="sxs-lookup"><span data-stu-id="75516-112">**AF\_INET**, **AF\_INET6**</span></span>                                                                                                                 |
| <span data-ttu-id="75516-113">File di intestazione</span><span class="sxs-lookup"><span data-stu-id="75516-113">Header file</span></span>      | <span data-ttu-id="75516-114">*Ws2tcpip. h*</span><span class="sxs-lookup"><span data-stu-id="75516-114">*Ws2tcpip.h*</span></span>                                                                                                                                |



 

<span data-ttu-id="75516-115">Sono disponibili due tipi di servizi di trasporto di base: datagrammi non affidabili (UDP) e orientato alla connessione affidabile-flussi di byte (TCP).</span><span class="sxs-lookup"><span data-stu-id="75516-115">Two basic types of transport services are offered: unreliable datagrams (UDP), and reliable connection oriented–byte streams (TCP).</span></span> <span data-ttu-id="75516-116">Inoltre, è facoltativamente supportato un socket non elaborato.</span><span class="sxs-lookup"><span data-stu-id="75516-116">In addition, a raw socket is optionally supported.</span></span> <span data-ttu-id="75516-117">I socket RAW consentono a un'applicazione di comunicare tramite protocolli diversi da TCP e UDP, ad esempio ICMP.</span><span class="sxs-lookup"><span data-stu-id="75516-117">Raw sockets allow an application to communicate through protocols other than TCP and UDP such as ICMP.</span></span> <span data-ttu-id="75516-118">I socket raw sono supportati nelle famiglie di indirizzi **AF \_ inet** e **AF \_ INET6** con alcune limitazioni.</span><span class="sxs-lookup"><span data-stu-id="75516-118">Raw sockets are supported on the **AF\_INET** and **AF\_INET6** address families with some limitations.</span></span>

<span data-ttu-id="75516-119">In questa sezione vengono illustrate le estensioni di Winsock specifiche per i protocolli TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="75516-119">This section covers extensions to Winsock that are specific to TCP/IP protocols.</span></span> <span data-ttu-id="75516-120">Vengono inoltre descritti gli aspetti delle funzioni Winsock di base che richiedono una particolare attenzione o che possono presentare un comportamento univoco quando si utilizza TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="75516-120">It also describes aspects of base Winsock functions that require special consideration or that may exhibit unique behavior when using TCP/IP.</span></span>

 

 



