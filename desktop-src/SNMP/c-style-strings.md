---
title: Stringhe di tipo C
description: Un'applicazione WinSNMP può usare stringhe di tipo C con terminazione NULL per convertire oggetti di entità e identificatori di oggetto (OID) in e dalle relative rappresentazioni di stringa.
ms.assetid: df04071c-df46-410b-ad92-6adecbfcd454
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 878398b6d8691982aa90b9f1376a38214030e52e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855214"
---
# <a name="c-style-strings"></a><span data-ttu-id="1a144-103">Stringhe di tipo C</span><span class="sxs-lookup"><span data-stu-id="1a144-103">C-Style Strings</span></span>

<span data-ttu-id="1a144-104">Un'applicazione WinSNMP può usare stringhe di tipo C con terminazione **null** per convertire oggetti di entità e identificatori di oggetto (OID) in e dalle relative rappresentazioni di stringa.</span><span class="sxs-lookup"><span data-stu-id="1a144-104">A WinSNMP application can use **NULL**-terminated C-style strings to convert entity and object identifier (OID) objects to and from their string representations.</span></span>

<span data-ttu-id="1a144-105">Le funzioni WinSNMP che modificano le stringhe di tipo C includono [**SnmpStrToEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity), [**SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr), [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid)e [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr).</span><span class="sxs-lookup"><span data-stu-id="1a144-105">The WinSNMP functions that manipulate C-style strings include [**SnmpStrToEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity), [**SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr), [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid), and [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr).</span></span> <span data-ttu-id="1a144-106">Poiché [**SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr) e [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr) restituiscono un puntatore a una variabile stringa di tipo C, l'applicazione WinSNMP deve passare un valore appropriato nel parametro *size* quando effettua chiamate a queste funzioni.</span><span class="sxs-lookup"><span data-stu-id="1a144-106">Because [**SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr) and [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr) return a pointer to a C-style string variable, the WinSNMP application must pass an appropriate value in the *size* parameter when it makes calls to these functions.</span></span> <span data-ttu-id="1a144-107">Per ulteriori informazioni, vedere le pagine di riferimento per queste funzioni.</span><span class="sxs-lookup"><span data-stu-id="1a144-107">For more information, see the reference pages for these functions.</span></span>

> [!Note]  
> <span data-ttu-id="1a144-108">Il parametro *context* delle funzioni [**SnmpStrToContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtocontext) e [**SnmpContextToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcontexttostr) deve essere una struttura di stringhe di ottetti, ovvero una struttura [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) .</span><span class="sxs-lookup"><span data-stu-id="1a144-108">The *context* parameter of the [**SnmpStrToContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtocontext) and [**SnmpContextToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcontexttostr) functions must be an octet string structure, that is, an [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) structure.</span></span> <span data-ttu-id="1a144-109">Il parametro *context* non può essere una stringa di tipo C.</span><span class="sxs-lookup"><span data-stu-id="1a144-109">The *context* parameter cannot be a C-style string.</span></span> <span data-ttu-id="1a144-110">La stringa contenuta in una struttura **smiOCTETS** non richiede un byte di terminazione **null**.</span><span class="sxs-lookup"><span data-stu-id="1a144-110">The string contained in an **smiOCTETS** structure does not require a **NULL**-terminating byte.</span></span>

 

 

 




