---
title: Creazione di un elenco di associazioni variabili
description: La funzione SnmpCreateVbl crea un nuovo elenco di associazioni di variabili.
ms.assetid: 18e8a04d-612f-4d85-9cff-8c541a4cdf71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34e9ef7aa208e2e2f887d14c0e124f3bb659ff8f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221554"
---
# <a name="creating-a-variable-binding-list"></a><span data-ttu-id="48983-103">Creazione di un elenco di associazioni variabili</span><span class="sxs-lookup"><span data-stu-id="48983-103">Creating a Variable Binding List</span></span>

<span data-ttu-id="48983-104">La funzione [**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) crea un nuovo elenco di associazioni di variabili.</span><span class="sxs-lookup"><span data-stu-id="48983-104">The [**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) function creates a new variable binding list.</span></span> <span data-ttu-id="48983-105">Se l'applicazione WinSNMP specifica un nome di variabile e un valore, la funzione crea l'elenco e aggiunge il nome e il valore come prima voce nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="48983-105">If the WinSNMP application specifies a variable name and a value, the function creates the list and adds the name and value as the first entry in the list.</span></span> <span data-ttu-id="48983-106">Se l'applicazione specifica **null** come nome della variabile, la funzione crea un elenco vuoto.</span><span class="sxs-lookup"><span data-stu-id="48983-106">If the application specifies **NULL** for the variable name, the function creates an empty list.</span></span>

<span data-ttu-id="48983-107">Per copiare un elenco di associazioni di variabili, chiamare la funzione [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) .</span><span class="sxs-lookup"><span data-stu-id="48983-107">To copy a variable binding list, call the [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) function.</span></span> <span data-ttu-id="48983-108">La funzione crea un nuovo elenco di associazioni di variabili e inizializza il nuovo elenco con una copia dei dati nell'elenco di associazioni della variabile di origine.</span><span class="sxs-lookup"><span data-stu-id="48983-108">The function creates a new variable binding list and initializes the new list with a copy of the data in the source variable binding list.</span></span>

<span data-ttu-id="48983-109">La funzione [**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) e la funzione [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) allocano la memoria necessaria per il nuovo elenco di associazioni di variabili.</span><span class="sxs-lookup"><span data-stu-id="48983-109">The [**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) function and the [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) function allocate any necessary memory for the new variable binding list.</span></span> <span data-ttu-id="48983-110">L'applicazione WinSNMP deve rilasciare le risorse associate a questi elenchi.</span><span class="sxs-lookup"><span data-stu-id="48983-110">The WinSNMP application must release the resources associated with these lists.</span></span> <span data-ttu-id="48983-111">È consigliabile eseguire questa operazione eseguendo la corrispondenza di ogni chiamata a [**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) e [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) con una chiamata corrispondente alla funzione [**SnmpFreeVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl) quando è opportuno liberare la memoria allocata.</span><span class="sxs-lookup"><span data-stu-id="48983-111">It is recommended that the application do this by matching each call to [**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) and [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) with a corresponding call to the [**SnmpFreeVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl) function when it is appropriate to free the allocated memory.</span></span>

 

 




