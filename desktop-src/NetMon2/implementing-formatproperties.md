---
description: Network Monitor chiama la funzione FormatProperties per formattare i dati visualizzati nel riquadro dei dettagli dell'interfaccia utente di Network Monitor.
ms.assetid: d0a58e1d-c867-4277-916e-f408627b5269
title: Implementazione di FormatProperties
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 660b581bf29fd8e5d40af65f5ff90e1e9223ad2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128914"
---
# <a name="implementing-formatproperties"></a><span data-ttu-id="0a279-103">Implementazione di FormatProperties</span><span class="sxs-lookup"><span data-stu-id="0a279-103">Implementing FormatProperties</span></span>

<span data-ttu-id="0a279-104">Network Monitor chiama la funzione [**FormatProperties**](formatproperties.md) per formattare i dati visualizzati nel riquadro dei dettagli dell'interfaccia utente di Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="0a279-104">Network Monitor calls the [**FormatProperties**](formatproperties.md) function to format the data that is displayed in the details pane of the Network Monitor UI.</span></span> <span data-ttu-id="0a279-105">In genere, **FormatProperties** viene chiamato per formattare la riga di riepilogo per un protocollo e quindi per formattare tutte le istanze di proprietà del protocollo all'interno di un frame.</span><span class="sxs-lookup"><span data-stu-id="0a279-105">Typically, **FormatProperties** is called to format the summary line for a protocol, and then to format all the property instances of the protocol within a frame.</span></span> <span data-ttu-id="0a279-106">Tuttavia, Network Monitor non identifica il numero di volte in cui viene chiamato **FormatProperties** per un parser specifico.</span><span class="sxs-lookup"><span data-stu-id="0a279-106">However, Network Monitor does not identify the number of times that **FormatProperties** is called for a specific parser.</span></span>

<span data-ttu-id="0a279-107">Quando si chiama [**FormatProperties**](formatproperties.md), Network Monitor fornisce una struttura [**PROPERTYINST**](propertyinst.md) per ogni proprietà visualizzata.</span><span class="sxs-lookup"><span data-stu-id="0a279-107">When calling [**FormatProperties**](formatproperties.md), Network Monitor provides a [**PROPERTYINST**](propertyinst.md) structure for each property that it displays.</span></span> <span data-ttu-id="0a279-108">La struttura **PROPERTYINST** fornisce informazioni sui dati da visualizzare, incluso un puntatore alla struttura [**PROPERTYINFO**](propertyinfo.md) che specifica la funzione da utilizzare per formattare la proprietà dei dati visualizzati.</span><span class="sxs-lookup"><span data-stu-id="0a279-108">The **PROPERTYINST** structure provides information about the data to be displayed, including a pointer to the [**PROPERTYINFO**](propertyinfo.md) structure that specifies the function to use to format the displayed data property.</span></span>

> [!Note]  
> <span data-ttu-id="0a279-109">Quando si aggiunge una proprietà al [*database della proprietà*](p.md) del parser, viene specificata una struttura [**PROPERTYINFO**](propertyinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="0a279-109">A [**PROPERTYINFO**](propertyinfo.md) structure is specified when adding a property to the [*property database*](p.md) of the parser.</span></span>

 

<span data-ttu-id="0a279-110">Network Monitor identifica la funzione Format da chiamare per ogni istanza della proprietà.</span><span class="sxs-lookup"><span data-stu-id="0a279-110">Network Monitor identifies the format function to call for each property instance.</span></span> <span data-ttu-id="0a279-111">Il membro **InstanceData** della struttura [**PROPERTYINFO**](propertyinfo.md) può specificare gli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="0a279-111">The **InstanceData** member of the [**PROPERTYINFO**](propertyinfo.md) structure can specify the following:</span></span>

-   <span data-ttu-id="0a279-112">Funzione [**FormatPropertyInstance**](formatpropertyinstance.md) per utilizzare il [*formattatore generico*](g.md) fornito da Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="0a279-112">The [**FormatPropertyInstance**](formatpropertyinstance.md) function to use the [*generic formatter*](g.md) that Network Monitor provides.</span></span>

    <span data-ttu-id="0a279-113">- oppure -</span><span class="sxs-lookup"><span data-stu-id="0a279-113">– or –</span></span>

-   <span data-ttu-id="0a279-114">Nome di una funzione di formato personalizzata fornita dal parser.</span><span class="sxs-lookup"><span data-stu-id="0a279-114">The name of a custom format function that the parser provides.</span></span>

<span data-ttu-id="0a279-115">Le funzioni [**FormatPropertyInstance**](formatpropertyinstance.md) e Format personalizzato restituiscono i dati formattati che vengono visualizzati nel riquadro dei dettagli dell'interfaccia utente di Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="0a279-115">The [**FormatPropertyInstance**](formatpropertyinstance.md) and the custom format functions return the formatted data that is displayed in the details pane of the Network Monitor UI.</span></span>

<span data-ttu-id="0a279-116">Nella figura seguente viene illustrato il modo in cui Network Monitor identifica la funzione da chiamare per ogni istanza della proprietà.</span><span class="sxs-lookup"><span data-stu-id="0a279-116">The following illustration shows how Network Monitor identifies the function to call for each property instance.</span></span>

![modalità di identificazione della funzione da chiamare in Network Monitor](images/formatprop1.png)

<span data-ttu-id="0a279-118">Nella procedura seguente vengono identificati i passaggi necessari per implementare [**FormatProperties**](formatproperties.md).</span><span class="sxs-lookup"><span data-stu-id="0a279-118">The following procedure identifies the steps necessary to implement [**FormatProperties**](formatproperties.md).</span></span>

<span data-ttu-id="0a279-119">**Per implementare FormatProperties**</span><span class="sxs-lookup"><span data-stu-id="0a279-119">**To implement FormatProperties**</span></span>

-   <span data-ttu-id="0a279-120">Utilizzando una struttura di ciclo, chiamare la funzione Format per ogni struttura [**PROPERTYINST**](propertyinst.md) passata al parser nel parametro *LpPropInst* della funzione [**FormatProperties**](formatproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="0a279-120">Using a loop structure, call the format function for each [**PROPERTYINST**](propertyinst.md) structure that is passed to the parser in the *lpPropInst* parameter of the [**FormatProperties**](formatproperties.md) function.</span></span>

<span data-ttu-id="0a279-121">Di seguito è riportata un'implementazione di base di [**FormatProperties**](formatproperties.md).</span><span class="sxs-lookup"><span data-stu-id="0a279-121">The following is a basic implementation of [**FormatProperties**](formatproperties.md).</span></span>

``` syntax
#include <windows.h>

DWORD BHAPI MyProtocolFormatProperties( HFRAME hFrame,
                                        LPBYTE         pMacFrame,
                                        LPBYTE         pBLRPLATEFrame,
                                        DWORD          nPropertyInsts
                                        LPPROPERTYINST  p)
  {
    while( nPropertyInsts-- > 0)
      {
         ( (FORMAT) p->lpPropertyInfo->InstanceData) ) (p);
         p++;
      }
  return BHERR_SUCCESS;
  }
```

 

 



