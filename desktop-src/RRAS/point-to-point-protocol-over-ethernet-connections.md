---
title: Point-to-Point Protocol su connessioni Ethernet
description: Windows Server 2003, Windows XP e i sistemi operativi successivi offrono il supporto per Point-to-Point Protocol su Ethernet (PPPoE). Per una connessione PPPoE, impostare i valori seguenti nella struttura RASENTRY.
ms.assetid: abdbf22c-abeb-4363-bfa6-e0002d1637f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eed66d3a694896bdec9e0f53215a782d5896cd38
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963383"
---
# <a name="point-to-point-protocol-over-ethernet-connections"></a><span data-ttu-id="bcc21-104">Point-to-Point Protocol su connessioni Ethernet</span><span class="sxs-lookup"><span data-stu-id="bcc21-104">Point-to-Point Protocol over Ethernet Connections</span></span>

<span data-ttu-id="bcc21-105">Windows Server 2003, Windows XP e i sistemi operativi successivi offrono il supporto per Point-to-Point Protocol su Ethernet (PPPoE).</span><span class="sxs-lookup"><span data-stu-id="bcc21-105">Windows Server 2003, Windows XP, and later operating systems provide support for Point-to-Point Protocol over Ethernet (PPPoE).</span></span> <span data-ttu-id="bcc21-106">Per una connessione PPPoE, impostare i valori seguenti nella struttura [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="bcc21-106">For a PPPoE connection, set the following values in the [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) structure.</span></span>



| <span data-ttu-id="bcc21-107">Membro</span><span class="sxs-lookup"><span data-stu-id="bcc21-107">Member</span></span>                      | <span data-ttu-id="bcc21-108">Valore</span><span class="sxs-lookup"><span data-stu-id="bcc21-108">Value</span></span>             |
|-----------------------------|-------------------|
| <span data-ttu-id="bcc21-109">RASENTRY. dwType</span><span class="sxs-lookup"><span data-stu-id="bcc21-109">RASENTRY.dwType</span></span>             | <span data-ttu-id="bcc21-110">RASET \_ Broadband</span><span class="sxs-lookup"><span data-stu-id="bcc21-110">RASET\_Broadband</span></span>  |
| <span data-ttu-id="bcc21-111">RAENTRY.szDeviceType</span><span class="sxs-lookup"><span data-stu-id="bcc21-111">RAENTRY.szDeviceType</span></span>        | <span data-ttu-id="bcc21-112">RASDT \_ PPPoE</span><span class="sxs-lookup"><span data-stu-id="bcc21-112">RASDT\_PPPoE</span></span>      |
| <span data-ttu-id="bcc21-113">RASENTRY.szLocalPhoneNumber</span><span class="sxs-lookup"><span data-stu-id="bcc21-113">RASENTRY.szLocalPhoneNumber</span></span> | <span data-ttu-id="bcc21-114">Nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="bcc21-114">The service name.</span></span> |



 

<span data-ttu-id="bcc21-115">Per impostare questi valori, usare la funzione [**RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) .</span><span class="sxs-lookup"><span data-stu-id="bcc21-115">Use the [**RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) function to set these values.</span></span>

<span data-ttu-id="bcc21-116">È anche possibile usare [**RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) e il \_ flag RASEDFLAG NewBroadbandEntry per [**RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) per visualizzare una procedura guidata per la creazione di una voce della rubrica PPPoE.</span><span class="sxs-lookup"><span data-stu-id="bcc21-116">You can also use [**RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) and the RASEDFLAG\_NewBroadbandEntry flag for [**RASENTRYDLG**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) to display a wizard for creating a PPPoE phonebook entry.</span></span>

 

 