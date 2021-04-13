---
title: Descrittori WinSNMP
description: Nell'ambiente di programmazione WinSNMP, un descrittore è una delle due strutture seguenti.
ms.assetid: a329963b-cdb9-40d2-9a82-6f0d9f4ac73a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cd7f844ab1365d6020afce0ca7bfeb3afa244a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328804"
---
# <a name="winsnmp-descriptors"></a><span data-ttu-id="37322-103">Descrittori WinSNMP</span><span class="sxs-lookup"><span data-stu-id="37322-103">WinSNMP Descriptors</span></span>

<span data-ttu-id="37322-104">Nell'ambiente di programmazione WinSNMP, un *descrittore* è una delle due strutture seguenti:</span><span class="sxs-lookup"><span data-stu-id="37322-104">In the WinSNMP programming environment a *descriptor* is one of the following two structures:</span></span>

-   <span data-ttu-id="37322-105">Struttura [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) che descrive una variabile di stringa ottetto</span><span class="sxs-lookup"><span data-stu-id="37322-105">An [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) structure which describes an octet string variable</span></span>
-   <span data-ttu-id="37322-106">Struttura [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) che descrive una variabile dell'identificatore di oggetto SNMP</span><span class="sxs-lookup"><span data-stu-id="37322-106">An [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) structure which describes an SNMP object identifier variable</span></span>

<span data-ttu-id="37322-107">Un descrittore WinSNMP è una struttura con due membri: un membro length, **Len** e un membro puntatore, **ptr**.</span><span class="sxs-lookup"><span data-stu-id="37322-107">A WinSNMP descriptor is a structure that has two members: a length member, **len**, and a pointer member, **ptr**.</span></span> <span data-ttu-id="37322-108">Il membro **ptr** punta alla stringa ottetto o all'identificatore di oggetto di interesse.</span><span class="sxs-lookup"><span data-stu-id="37322-108">The **ptr** member points to the octet string or object identifier of interest.</span></span> <span data-ttu-id="37322-109">Il membro **ptr** può essere il tipo di dati **smiLPBYTE** o **smiLPUINT32** .</span><span class="sxs-lookup"><span data-stu-id="37322-109">The **ptr** member can be either the **smiLPBYTE** or **smiLPUINT32** data type.</span></span>

<span data-ttu-id="37322-110">Un descrittore [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) o un descrittore [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) può essere il membro del **valore** di una struttura **smiVALUE** .</span><span class="sxs-lookup"><span data-stu-id="37322-110">An [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) descriptor or an [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) descriptor can be the **value** member of an **smiVALUE** structure.</span></span> <span data-ttu-id="37322-111">La struttura [**smiVALUE**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue) descrive il valore associato a un nome di variabile in una voce di binding variabile.</span><span class="sxs-lookup"><span data-stu-id="37322-111">The [**smiVALUE**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue) structure describes the value associated with a variable name in a variable binding entry.</span></span>

<span data-ttu-id="37322-112">L'implementazione di Microsoft WinSNMP alloca e dealloca la memoria per tutte le strutture di output **smiOCTETS** e **smiOID** .</span><span class="sxs-lookup"><span data-stu-id="37322-112">The Microsoft WinSNMP implementation allocates and deallocates memory for all output **smiOCTETS** and **smiOID** structures.</span></span> <span data-ttu-id="37322-113">Pertanto, l'applicazione deve chiamare la funzione [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) per liberare la memoria per il membro **ptr** di queste strutture.</span><span class="sxs-lookup"><span data-stu-id="37322-113">Therefore, the application must call the [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) function to free the memory for the **ptr** member of these structures.</span></span>

<span data-ttu-id="37322-114">I membri di stringa nei descrittori non richiedono un byte di terminazione **null** .</span><span class="sxs-lookup"><span data-stu-id="37322-114">String members in descriptors do not require a **NULL** terminating byte.</span></span> <span data-ttu-id="37322-115">Per ulteriori informazioni sulla gestione della memoria allocata per i descrittori, vedere [allocazione di oggetti memoria WinSNMP](allocating-winsnmp-memory-objects.md).</span><span class="sxs-lookup"><span data-stu-id="37322-115">For additional information about managing the memory allocated for descriptors, see [Allocating WinSNMP Memory Objects](allocating-winsnmp-memory-objects.md).</span></span>

 

 




