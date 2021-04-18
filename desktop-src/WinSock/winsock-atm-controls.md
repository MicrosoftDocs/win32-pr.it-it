---
description: La configurazione della connessione Point-to-Point e di connessione Point-to-multipoint ATM e teardown sono supportati in modo nativo dalla specifica di Windows Sockets 2.
ms.assetid: 07e4fcb8-f7b5-450d-a2f4-ba81267ef8ca
title: Controlli ATM Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b3eb0fc798878066f6e3a4fa04af688eee28ea8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306880"
---
# <a name="winsock-atm-controls"></a><span data-ttu-id="68bb2-103">Controlli ATM Winsock</span><span class="sxs-lookup"><span data-stu-id="68bb2-103">Winsock ATM Controls</span></span>

<span data-ttu-id="68bb2-104">La configurazione della connessione Point-to-Point e di connessione Point-to-multipoint ATM e teardown sono supportati in modo nativo dalla specifica di Windows Sockets 2.</span><span class="sxs-lookup"><span data-stu-id="68bb2-104">ATM point-to-point and point-to-multipoint connection setup and teardown are natively supported by the Windows Sockets 2 specification.</span></span> <span data-ttu-id="68bb2-105">Infatti, le specifiche QoS di Windows Sockets 2 e i meccanismi multipoint/multicast indipendenti dal protocollo sono stati progettati tenendo conto di ATM, insieme ad altri protocolli.</span><span class="sxs-lookup"><span data-stu-id="68bb2-105">In fact, Windows Sockets 2 QoS specification and protocol-independent multipoint/multicast mechanisms were designed with ATM in mind, along with other protocols.</span></span> <span data-ttu-id="68bb2-106">Vedere la sezione 2,7 e l'Appendice D della specifica dell'API di Windows Sockets 2 per Windows Sockets 2, qualità del servizio e supporto Multipoint, rispettivamente.</span><span class="sxs-lookup"><span data-stu-id="68bb2-106">See Section 2.7 and Appendix D of the Windows Sockets 2 API specification for Windows Sockets 2, Quality of Service, and Multipoint Support, respectively.</span></span> <span data-ttu-id="68bb2-107">Non è pertanto necessario introdurre IOCTL specifici di ATM in questo documento.</span><span class="sxs-lookup"><span data-stu-id="68bb2-107">Therefore, no ATM-specific Ioctls need to be introduced in this document.</span></span>

 

 



