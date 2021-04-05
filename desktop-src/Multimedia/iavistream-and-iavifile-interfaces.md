---
title: Interfacce IAVIStream e IAVIFile
description: Interfacce IAVIStream e IAVIFile
ms.assetid: 3ab602da-239f-44ff-b43d-e0c380619d99
keywords:
- Interfaccia IAVIStream
- Interfaccia IAVIFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f65cdd72a034f2c380638979e656c84a173331fc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856358"
---
# <a name="iavistream-and-iavifile-interfaces"></a><span data-ttu-id="95ef7-105">Interfacce IAVIStream e IAVIFile</span><span class="sxs-lookup"><span data-stu-id="95ef7-105">IAVIStream and IAVIFile Interfaces</span></span>

<span data-ttu-id="95ef7-106">Le interfacce [**IAVIStream**](/windows/desktop/api/Vfw/nn-vfw-iavistream) e [**IAVIFile**](/windows/desktop/api/Vfw/nn-vfw-iavifile) contengono i metodi usati dai gestori di file e flussi.</span><span class="sxs-lookup"><span data-stu-id="95ef7-106">The [**IAVIStream**](/windows/desktop/api/Vfw/nn-vfw-iavistream) and [**IAVIFile**](/windows/desktop/api/Vfw/nn-vfw-iavifile) interfaces contain the methods used by file and stream handlers.</span></span> <span data-ttu-id="95ef7-107">Il tipo di dati **PAVISTREAM** è un puntatore a un oggetto flusso AVI (tramite l'interfaccia **IAVIStream** ) e il tipo di dati **PAVIFILE** è un puntatore a un oggetto file AVI (tramite l'interfaccia **IAVIFile** ).</span><span class="sxs-lookup"><span data-stu-id="95ef7-107">The **PAVISTREAM** data type is a pointer to an AVI stream object (through the **IAVIStream** interface) and the **PAVIFILE** data type is a pointer to an AVI file object (through the **IAVIFile** interface).</span></span>

<span data-ttu-id="95ef7-108">Per creare un puntatore a oggetti in C, allocare prima di tutto lo spazio per una struttura sufficientemente grande da contenere il puntatore alla tabella della funzione virtuale e agli altri membri dati.</span><span class="sxs-lookup"><span data-stu-id="95ef7-108">To create an object pointer in C, first allocate space for a structure that is large enough to contain the pointer to the virtual function table and the other data members.</span></span> <span data-ttu-id="95ef7-109">Creare una tabella di funzioni virtuali per i metodi per il tipo di flusso, quindi impostare il puntatore sulla tabella di funzioni virtuali sull'indirizzo della tabella della funzione virtuale.</span><span class="sxs-lookup"><span data-stu-id="95ef7-109">Create a virtual function table for the methods for your type of stream, then set the pointer to the virtual function table to the address of the virtual function table.</span></span>

 

 




