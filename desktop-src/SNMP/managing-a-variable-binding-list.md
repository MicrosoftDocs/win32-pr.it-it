---
title: Gestione di un elenco di associazioni variabili
description: La funzione SnmpGetVb recupera le informazioni di associazione variabili da un elenco di associazioni variabili. La funzione recupera il nome della variabile e il valore associato della variabile dalla voce di associazione della variabile specificata dall'applicazione WinSNMP.
ms.assetid: 357aebd6-171a-4221-b12a-712702f9d9c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cc8c1cbfa4eb0ec3acdc13e9c9cc480b88ddae8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044467"
---
# <a name="managing-a-variable-binding-list"></a><span data-ttu-id="7af36-104">Gestione di un elenco di associazioni variabili</span><span class="sxs-lookup"><span data-stu-id="7af36-104">Managing a Variable Binding List</span></span>

<span data-ttu-id="7af36-105">La funzione [**SnmpGetVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetvb) recupera le informazioni di associazione variabili da un elenco di associazioni variabili.</span><span class="sxs-lookup"><span data-stu-id="7af36-105">The [**SnmpGetVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetvb) function retrieves variable binding information from a variable binding list.</span></span> <span data-ttu-id="7af36-106">La funzione recupera il nome della variabile e il valore associato della variabile dalla voce di associazione della variabile specificata dall'applicazione WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="7af36-106">The function retrieves the variable name and the variable's associated value from the variable binding entry specified by the WinSNMP application.</span></span>

<span data-ttu-id="7af36-107">Per aggiornare le voci di associazione variabili in un elenco di associazioni variabili, chiamare la funzione [**SnmpSetVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetvb) .</span><span class="sxs-lookup"><span data-stu-id="7af36-107">To update variable binding entries in a variable binding list, call the [**SnmpSetVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetvb) function.</span></span> <span data-ttu-id="7af36-108">La funzione **SnmpSetVb** aggiunge anche nuove voci di associazione di variabili a un elenco di associazioni variabili esistente.</span><span class="sxs-lookup"><span data-stu-id="7af36-108">The **SnmpSetVb** function also appends new variable binding entries to an existing variable binding list.</span></span>

<span data-ttu-id="7af36-109">È necessario che l'applicazione WinSNMP chiami la funzione [**SnmpDeleteVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpdeletevb) per rimuovere le voci da un elenco di associazioni variabili.</span><span class="sxs-lookup"><span data-stu-id="7af36-109">The WinSNMP application must call the [**SnmpDeleteVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpdeletevb) function to remove entries from a variable binding list.</span></span>

<span data-ttu-id="7af36-110">Per recuperare, modificare o eliminare una voce di binding variabile, l'applicazione WinSNMP deve specificare la posizione della voce nell'elenco di associazioni variabili.</span><span class="sxs-lookup"><span data-stu-id="7af36-110">To retrieve, modify or delete a variable binding entry, the WinSNMP application must specify the position of the entry in the variable binding list.</span></span>

<span data-ttu-id="7af36-111">Una chiamata alla funzione [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) associa un elenco di associazioni variabili a una PDU.</span><span class="sxs-lookup"><span data-stu-id="7af36-111">A call to the [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) function associates a variable binding list with a PDU.</span></span> <span data-ttu-id="7af36-112">Una chiamata alla funzione [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) recupera un elenco di associazioni variabili da un PDU.</span><span class="sxs-lookup"><span data-stu-id="7af36-112">A call to the [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) function retrieves a variable binding list from a PDU.</span></span> <span data-ttu-id="7af36-113">Un binding di una singola variabile non è associato direttamente a una PDU, ma è indirettamente associato tramite la relativa inclusione in un elenco di associazioni variabili.</span><span class="sxs-lookup"><span data-stu-id="7af36-113">An individual variable binding is not directly associated with a PDU, but it is indirectly associated through its inclusion in a variable binding list.</span></span>

 

 




