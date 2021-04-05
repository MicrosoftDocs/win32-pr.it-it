---
title: Utilizzo degli elenchi di associazioni variabili
description: Un'associazione variabile è l'associazione di un nome di istanza dell'oggetto SNMP a un valore associato. Un elenco di associazioni variabili è una serie di voci di associazione variabili. In WinSNMP, un'unità dati del protocollo (PDU) include un elenco di associazioni variabili.
ms.assetid: e6353ae7-1d32-4de4-8518-49864fcbfc57
keywords:
- Utilizzo degli elenchi di associazione variabili SNMP
- Binding di variabili che elenca SNMP, SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26719c7dc987e61542f38a0b86db78c573793f98
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "103723663"
---
# <a name="working-with-variable-binding-lists"></a><span data-ttu-id="2a6ad-107">Utilizzo degli elenchi di associazioni variabili</span><span class="sxs-lookup"><span data-stu-id="2a6ad-107">Working with Variable Binding Lists</span></span>

<span data-ttu-id="2a6ad-108">Un' *associazione variabile* è l'associazione di un nome di istanza dell'oggetto SNMP a un valore associato.</span><span class="sxs-lookup"><span data-stu-id="2a6ad-108">A *variable binding* is the pairing of an SNMP object instance name with an associated value.</span></span> <span data-ttu-id="2a6ad-109">Un *elenco di associazioni variabili* è una serie di voci di associazione variabili.</span><span class="sxs-lookup"><span data-stu-id="2a6ad-109">A *variable binding list* is a series of variable binding entries.</span></span> <span data-ttu-id="2a6ad-110">In WinSNMP, un'unità dati del protocollo (PDU) include un elenco di associazioni variabili.</span><span class="sxs-lookup"><span data-stu-id="2a6ad-110">In WinSNMP, a protocol data unit (PDU) includes a variable binding list.</span></span>

<span data-ttu-id="2a6ad-111">I dettagli della struttura dell'elenco di associazioni variabili sono limitati all'implementazione di Microsoft WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="2a6ad-111">The details of the variable binding list structure are restricted to the Microsoft WinSNMP implementation.</span></span> <span data-ttu-id="2a6ad-112">Un'applicazione WinSNMP può accedere a un elenco di associazioni variabili con un handle di tipo **HSNMP \_ VBL**.</span><span class="sxs-lookup"><span data-stu-id="2a6ad-112">A WinSNMP application can access a variable binding list with a handle of type **HSNMP\_VBL**.</span></span> <span data-ttu-id="2a6ad-113">Per altre informazioni, vedere [oggetti handle di risorsa](resource-handle-objects.md).</span><span class="sxs-lookup"><span data-stu-id="2a6ad-113">For more information, see [Resource Handle Objects](resource-handle-objects.md).</span></span>

<span data-ttu-id="2a6ad-114">L'applicazione WinSNMP può creare e modificare elenchi di associazioni variabili e includerli in PDU.</span><span class="sxs-lookup"><span data-stu-id="2a6ad-114">The WinSNMP application can construct and manipulate variable binding lists, and include them in PDUs.</span></span> <span data-ttu-id="2a6ad-115">Per eseguire queste operazioni, l'applicazione usa le [funzioni di associazione della variabile](winsnmp-functions.md)WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="2a6ad-115">To perform these operations, the application uses the WinSNMP [variable binding functions](winsnmp-functions.md).</span></span> <span data-ttu-id="2a6ad-116">Per ulteriori informazioni sull'utilizzo di WinSNMP e degli elenchi di associazioni variabili, vedere gli argomenti elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="2a6ad-116">For more information about working with WinSNMP and variable binding lists, see the topics listed in the following table.</span></span>



| <span data-ttu-id="2a6ad-117">Argomento</span><span class="sxs-lookup"><span data-stu-id="2a6ad-117">Topic</span></span>                                                                    | <span data-ttu-id="2a6ad-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2a6ad-118">Description</span></span>                                      |
|--------------------------------------------------------------------------|--------------------------------------------------|
| [<span data-ttu-id="2a6ad-119">Creazione di un elenco di associazioni variabili</span><span class="sxs-lookup"><span data-stu-id="2a6ad-119">Creating a Variable Binding List</span></span>](creating-a-variable-binding-list.md) | <span data-ttu-id="2a6ad-120">Viene descritto come creare un elenco di associazioni variabili.</span><span class="sxs-lookup"><span data-stu-id="2a6ad-120">Describes how to create a variable binding list.</span></span> |
| [<span data-ttu-id="2a6ad-121">Gestione di un elenco di associazioni variabili</span><span class="sxs-lookup"><span data-stu-id="2a6ad-121">Managing a Variable Binding List</span></span>](managing-a-variable-binding-list.md) | <span data-ttu-id="2a6ad-122">Viene descritto come gestire un elenco di associazioni variabili.</span><span class="sxs-lookup"><span data-stu-id="2a6ad-122">Describes how to manage a variable binding list.</span></span> |



 

<span data-ttu-id="2a6ad-123">Per ulteriori informazioni sulle associazioni variabili e sugli elenchi di associazioni variabili, vedere [RFC1905](https://www.ietf.org/rfc/rfc1905.txt), "operazioni di protocollo per la versione 2 del Simple Network Management Protocol (SNMPv2)," e le [funzioni di associazione delle variabili](winsnmp-functions.md)WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="2a6ad-123">For more information about variable bindings and variable binding lists, see [RFC1905](https://www.ietf.org/rfc/rfc1905.txt), "Protocol Operations for Version 2 of the Simple Network Management Protocol (SNMPv2)," and the WinSNMP [Variable Binding Functions](winsnmp-functions.md).</span></span>

 

 




