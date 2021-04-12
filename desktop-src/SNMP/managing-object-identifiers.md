---
title: Gestione degli identificatori di oggetto
description: L'API WinSNMP fornisce diverse funzioni di utilità WinSNMP che semplificano la manipolazione degli identificatori di oggetto per le applicazioni WinSNMP.
ms.assetid: 6ca5f5bc-aa49-4826-97a7-2ea4a882dc2d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9745cb8018b6833a1ef0569e69f201c621aa38e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471643"
---
# <a name="managing-object-identifiers"></a><span data-ttu-id="7a0b2-103">Gestione degli identificatori di oggetto</span><span class="sxs-lookup"><span data-stu-id="7a0b2-103">Managing Object Identifiers</span></span>

<span data-ttu-id="7a0b2-104">L'API WinSNMP fornisce diverse [funzioni di utilità WinSNMP](winsnmp-functions.md) che semplificano la manipolazione degli identificatori di oggetto per le applicazioni WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="7a0b2-104">The WinSNMP API provides several [WinSNMP utility functions](winsnmp-functions.md) that simplify the manipulation of object identifiers for WinSNMP applications.</span></span>

<span data-ttu-id="7a0b2-105">La funzione [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr) converte la rappresentazione binaria interna di un identificatore di oggetto nel formato della stringa numerica punteggiata.</span><span class="sxs-lookup"><span data-stu-id="7a0b2-105">The [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr) function converts the internal binary representation of an object identifier to its dotted numeric string format.</span></span> <span data-ttu-id="7a0b2-106">Quando si chiama [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr), specificare un buffer di stringa di lunghezza MAXOBJIDSTRSIZE (1408 byte) per assicurarsi che il buffer di output sia sufficientemente grande da mantenere la stringa convertita.</span><span class="sxs-lookup"><span data-stu-id="7a0b2-106">When you call [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr), specify a string buffer of MAXOBJIDSTRSIZE length (1408 bytes) to ensure that the output buffer is large enough to hold the converted string.</span></span> <span data-ttu-id="7a0b2-107">Per convertire un identificatore di oggetto dal formato della stringa numerica punteggiata alla relativa rappresentazione binaria interna, chiamare la funzione [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid) .</span><span class="sxs-lookup"><span data-stu-id="7a0b2-107">To convert an object identifier from the dotted numeric string format to its internal binary representation, call the [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid) function.</span></span>

<span data-ttu-id="7a0b2-108">Per copiare un identificatore di oggetto SNMP, chiamare la funzione [**SnmpOidCopy**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy) .</span><span class="sxs-lookup"><span data-stu-id="7a0b2-108">To copy an SNMP object identifier call the [**SnmpOidCopy**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy) function.</span></span> <span data-ttu-id="7a0b2-109">Questa funzione alloca qualsiasi memoria necessaria per il nuovo identificatore di oggetto.</span><span class="sxs-lookup"><span data-stu-id="7a0b2-109">This function allocates any necessary memory for the new object identifier.</span></span>

<span data-ttu-id="7a0b2-110">Un'applicazione WinSNMP deve chiamare la funzione [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) per liberare le risorse allocate per il membro **ptr** della struttura [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) specificata dalle funzioni [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid) e [**SnmpOidCopy**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy) .</span><span class="sxs-lookup"><span data-stu-id="7a0b2-110">A WinSNMP application must call the [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) function to free resources allocated for the **ptr** member of the [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) structure specified by both the [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid) and the [**SnmpOidCopy**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy) functions.</span></span>

<span data-ttu-id="7a0b2-111">La funzione [**SnmpOidCompare**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcompare) Confronta due identificatori di oggetto SNMP.</span><span class="sxs-lookup"><span data-stu-id="7a0b2-111">The [**SnmpOidCompare**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcompare) function compares two SNMP object identifiers.</span></span> <span data-ttu-id="7a0b2-112">L'applicazione WinSNMP può specificare il numero di sottoidentificatori da confrontare.</span><span class="sxs-lookup"><span data-stu-id="7a0b2-112">The WinSNMP application can specify the number of subidentifiers to compare.</span></span> <span data-ttu-id="7a0b2-113">Chiamare **SnmpOidCompare** per determinare se due identificatori di oggetto hanno prefissi comuni.</span><span class="sxs-lookup"><span data-stu-id="7a0b2-113">Call **SnmpOidCompare** to determine whether two object identifiers have common prefixes.</span></span>

<span data-ttu-id="7a0b2-114">Per ulteriori informazioni sulla gestione della memoria allocata per gli identificatori di oggetto, vedere [allocazione di oggetti memoria WinSNMP](allocating-winsnmp-memory-objects.md).</span><span class="sxs-lookup"><span data-stu-id="7a0b2-114">For additional information about managing the memory allocated for object identifiers, see [Allocating WinSNMP Memory Objects](allocating-winsnmp-memory-objects.md).</span></span>

 

 




