---
title: Supporto per le stringhe di indirizzi IPX in WinSNMP
description: WinSNMP 2,0 formalizza l'uso di stringhe di indirizzi IPX.
ms.assetid: b90b8e95-dab0-483b-9336-07e20c122cba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc33c3ff3b589f9614b139260cef993e232f4343
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707312"
---
# <a name="support-for-ipx-address-strings-in-winsnmp"></a><span data-ttu-id="71ad2-103">Supporto per le stringhe di indirizzi IPX in WinSNMP</span><span class="sxs-lookup"><span data-stu-id="71ad2-103">Support for IPX Address Strings in WinSNMP</span></span>

<span data-ttu-id="71ad2-104">WinSNMP 2,0 formalizza l'uso di stringhe di indirizzi IPX.</span><span class="sxs-lookup"><span data-stu-id="71ad2-104">WinSNMP 2.0 formalizes the use of IPX address strings.</span></span> <span data-ttu-id="71ad2-105">Se si specifica una stringa di indirizzo IPX come parametro di input per la funzione [**SnmpStrToEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity) , è necessario formattare la stringa usando gli standard seguenti:</span><span class="sxs-lookup"><span data-stu-id="71ad2-105">If you specify an IPX address string as an input parameter to the [**SnmpStrToEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity) function, you must format the string using the following standards:</span></span>

-   <span data-ttu-id="71ad2-106">Numero di rete costituito da otto cifre esadecimali, se necessario con riempimento zero</span><span class="sxs-lookup"><span data-stu-id="71ad2-106">A network number that consists of eight hexadecimal digits (zero-filled if necessary)</span></span>
-   <span data-ttu-id="71ad2-107">Separatore (":", "." o "-")</span><span class="sxs-lookup"><span data-stu-id="71ad2-107">A separator (either ":", "." or " – ")</span></span>
-   <span data-ttu-id="71ad2-108">Numero di nodo costituito da 12 cifre esadecimali, se necessario con riempimento zero</span><span class="sxs-lookup"><span data-stu-id="71ad2-108">A node number that consists of 12 hexadecimal digits (zero-filled if necessary)</span></span>

<span data-ttu-id="71ad2-109">Ad esempio, 00000001:00081A0D01C2 o 00000001.00081 a0d01c2.</span><span class="sxs-lookup"><span data-stu-id="71ad2-109">For example, 00000001:00081A0D01C2 or 00000001.00081a0d01c2.</span></span> <span data-ttu-id="71ad2-110">Le cifre esadecimali possono essere maiuscole o minuscole.</span><span class="sxs-lookup"><span data-stu-id="71ad2-110">Hexadecimal digits can be uppercase or lowercase.</span></span>

<span data-ttu-id="71ad2-111">Si tratta del formato utilizzato dalla funzione [**SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr) per restituire una stringa di indirizzo IPX.</span><span class="sxs-lookup"><span data-stu-id="71ad2-111">This is the format the [**SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr) function uses to return an IPX address string.</span></span> <span data-ttu-id="71ad2-112">La stringa viene restituita quando un'applicazione che opera in una delle modalità SNMPAPI non \_ tradotta chiama la funzione **SnmpEntityToStr** .</span><span class="sxs-lookup"><span data-stu-id="71ad2-112">The string is returned when an application that is operating in one of the SNMPAPI\_UNTRANSLATED modes calls the **SnmpEntityToStr** function.</span></span> <span data-ttu-id="71ad2-113">La stringa può essere restituita anche quando l'applicazione funziona in \_ modalità snmpapi tradotta e non è disponibile alcun nome descrittivo per l'entità.</span><span class="sxs-lookup"><span data-stu-id="71ad2-113">The string can also be returned when the application is operating in SNMPAPI\_TRANSLATED mode and no user-friendly name is available for the entity.</span></span>

 

 




