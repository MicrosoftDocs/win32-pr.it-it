---
description: Network Monitor o la DLL del parser può formattare i dati visualizzati nel riquadro dei dettagli dell'interfaccia utente di Network Monitor.
ms.assetid: 60ab9253-ec0f-4c97-a475-ce2a74d469c4
title: Formattazione dei dati visualizzati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 017946dab9db443cf7083109dd75ccee1f6d278a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525146"
---
# <a name="formatting-displayed-data"></a><span data-ttu-id="5d21a-103">Formattazione dei dati visualizzati</span><span class="sxs-lookup"><span data-stu-id="5d21a-103">Formatting Displayed Data</span></span>

<span data-ttu-id="5d21a-104">Network Monitor o la DLL del parser può formattare i dati visualizzati nel riquadro dei dettagli dell'interfaccia utente di Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="5d21a-104">Network Monitor or your parser DLL can format the data that is displayed in the details pane of the Network Monitor UI.</span></span>

<span data-ttu-id="5d21a-105">Network Monitor fornisce un formattatore generico che fornisce i servizi di base necessari per visualizzare la maggior parte dei tipi di dati presenti all'interno di un protocollo.</span><span class="sxs-lookup"><span data-stu-id="5d21a-105">Network Monitor provides a generic formatter that provides the basic services needed to display most data types that exist within a protocol.</span></span> <span data-ttu-id="5d21a-106">Tuttavia, il formattatore generico non supporta tutti i tipi di dati.</span><span class="sxs-lookup"><span data-stu-id="5d21a-106">However, the generic formatter does not support all data types.</span></span> <span data-ttu-id="5d21a-107">Il formattatore generico, ad esempio, non supporta quanto segue:</span><span class="sxs-lookup"><span data-stu-id="5d21a-107">For example, the generic formatter does not support the following:</span></span>

-   <span data-ttu-id="5d21a-108">Diversi tipi di indirizzi.</span><span class="sxs-lookup"><span data-stu-id="5d21a-108">Several address types.</span></span>
-   <span data-ttu-id="5d21a-109">Nomi descrittivi di origine e di destinazione.</span><span class="sxs-lookup"><span data-stu-id="5d21a-109">Source and destination-friendly names.</span></span>
-   <span data-ttu-id="5d21a-110">Identificatori di oggetto.</span><span class="sxs-lookup"><span data-stu-id="5d21a-110">Object identifiers.</span></span>
-   <span data-ttu-id="5d21a-111">Tipi di dati integer di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="5d21a-111">Large integer data types.</span></span>
-   <span data-ttu-id="5d21a-112">Tipi di dati a lunghezza variabile Small Integer.</span><span class="sxs-lookup"><span data-stu-id="5d21a-112">Variable length small integer data types.</span></span>

<span data-ttu-id="5d21a-113">Nell'esempio seguente vengono identificate due stringhe formattate per la proprietà ID dei privilegi.</span><span class="sxs-lookup"><span data-stu-id="5d21a-113">The following example identifies two formatted strings for the Privilege ID property.</span></span>

-   <span data-ttu-id="5d21a-114">La prima riga di codice mostra l'output del formattatore generico.</span><span class="sxs-lookup"><span data-stu-id="5d21a-114">The first line of code shows the output of the generic formatter.</span></span> <span data-ttu-id="5d21a-115">L'output è basato sul tipo di dati.</span><span class="sxs-lookup"><span data-stu-id="5d21a-115">The output is based on the data type.</span></span>
-   <span data-ttu-id="5d21a-116">La seconda riga di codice mostra l'output di un formattatore personalizzato con una stringa per i dati della proprietà.</span><span class="sxs-lookup"><span data-stu-id="5d21a-116">The second line of code shows the output of a custom formatter with a string to the property data.</span></span>

``` syntax
Privilege ID (PID) = 0x0029
Privilege ID   (PID) = 0x0029   The Process has privileges
```

> [!Note]  
> <span data-ttu-id="5d21a-117">Quando possibile, usare il formattatore generico per visualizzare i dati perché consente di controllare le dimensioni della DLL del parser e offre migliori funzionalità multipiattaforma per la DLL del parser.</span><span class="sxs-lookup"><span data-stu-id="5d21a-117">When possible, use the generic formatter to display your data because it allows you to control the size of your parser DLL, and provides better cross-platform capabilities for your parser DLL.</span></span>

 

 

 



