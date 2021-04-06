---
title: Apertura e chiusura di una sessione WinSNMP
description: Per aprire una sessione, un'applicazione chiama la funzione SnmpCreateSession.
ms.assetid: 76650231-509b-45be-b156-09752b817854
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e006ffb81f6c2508b3505678b28c3ace8e60c85
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045038"
---
# <a name="opening-and-closing-a-winsnmp-session"></a><span data-ttu-id="70ff6-103">Apertura e chiusura di una sessione WinSNMP</span><span class="sxs-lookup"><span data-stu-id="70ff6-103">Opening and Closing a WinSNMP Session</span></span>

<span data-ttu-id="70ff6-104">Per aprire una sessione, un'applicazione chiama la funzione [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession) .</span><span class="sxs-lookup"><span data-stu-id="70ff6-104">To open a session, an application calls the [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession) function.</span></span> <span data-ttu-id="70ff6-105">Se la funzione viene completata correttamente, l'implementazione di Microsoft WinSNMP apre una sessione e la funzione restituisce un identificatore di sessione sotto forma di handle **di \_ sessione HSNMP** .</span><span class="sxs-lookup"><span data-stu-id="70ff6-105">If the function completes successfully, the Microsoft WinSNMP implementation opens a session, and the function returns a session identifier in the form of an **HSNMP\_SESSION** handle.</span></span> <span data-ttu-id="70ff6-106">Tutte le funzioni WinSNMP che restituiscono variabili di handle includono l'identificatore di sessione come parametro di input.</span><span class="sxs-lookup"><span data-stu-id="70ff6-106">All WinSNMP functions that return handle variables include the session identifier as an input parameter.</span></span> <span data-ttu-id="70ff6-107">Questo consente all'implementazione di usare l'handle per gestire in modo efficiente le risorse a livello di sessione.</span><span class="sxs-lookup"><span data-stu-id="70ff6-107">This enables the implementation to use the handle to efficiently manage resources at the session level.</span></span>

<span data-ttu-id="70ff6-108">Un'applicazione può avere più sessioni aperte alla volta.</span><span class="sxs-lookup"><span data-stu-id="70ff6-108">An application can have multiple sessions open at one time.</span></span> <span data-ttu-id="70ff6-109">Più sessioni all'interno di un'applicazione possono condividere le variabili di handle.</span><span class="sxs-lookup"><span data-stu-id="70ff6-109">Multiple sessions within an application can share handle variables.</span></span>

<span data-ttu-id="70ff6-110">Se l'implementazione non è in grado di aprire una sessione a causa di limitazioni delle risorse, restituisce un \_ errore snmpapi quando l'applicazione chiama [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession).</span><span class="sxs-lookup"><span data-stu-id="70ff6-110">If the implementation cannot open a session because of resource limitations, it returns SNMPAPI\_FAILURE when the application calls [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession).</span></span> <span data-ttu-id="70ff6-111">Se l'applicazione chiama la funzione [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) , viene restituito un \_ errore di allocazione snmpapi \_ .</span><span class="sxs-lookup"><span data-stu-id="70ff6-111">If the application then calls the [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) function, it returns SNMPAPI\_ALLOC\_ERROR.</span></span>

<span data-ttu-id="70ff6-112">Una chiamata alla funzione [**SnmpClose**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose) consente all'implementazione di liberare tutte le risorse rimanenti e di chiudere la sessione.</span><span class="sxs-lookup"><span data-stu-id="70ff6-112">A call to the [**SnmpClose**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose) function enables the implementation to free any remaining resources and to close the session.</span></span>

<span data-ttu-id="70ff6-113">Per altre informazioni, vedere [oggetti handle di risorsa](resource-handle-objects.md) e [sessioni WinSNMP](winsnmp-sessions.md).</span><span class="sxs-lookup"><span data-stu-id="70ff6-113">For more information, see [Resource Handle Objects](resource-handle-objects.md) and [WinSNMP Sessions](winsnmp-sessions.md).</span></span>

 

 




