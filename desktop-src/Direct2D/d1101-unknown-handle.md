---
title: Handle sconosciuto d1101
ms.assetid: ae40058a-ea17-4262-87dc-0ce852c16c2a
description: È stata passata un'interfaccia non allocata da questa DLL.
keywords:
- D1101 handle Direct2D sconosciuto
topic_type:
- apiref
api_name:
- D1101 Unknown Handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 2a87491a02d3dea992f8dd767ad34cf83b2cbf40
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/27/2021
ms.locfileid: "106334282"
---
# <a name="d1101-unknown-handle"></a><span data-ttu-id="4b6cf-104">D1101: handle sconosciuto</span><span class="sxs-lookup"><span data-stu-id="4b6cf-104">D1101: Unknown Handle</span></span>

<span data-ttu-id="4b6cf-105">Un' \[ *interfaccia* \] di interfaccia non allocata da questa dll è stata passata.</span><span class="sxs-lookup"><span data-stu-id="4b6cf-105">An interface \[*interface*\] not allocated by this DLL was passed to it.</span></span>

## <a name="placeholders"></a><span data-ttu-id="4b6cf-106">Segnaposto</span><span class="sxs-lookup"><span data-stu-id="4b6cf-106">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="4b6cf-107"><span id="interface"></span><span id="INTERFACE"></span>*interfaccia*</span><span class="sxs-lookup"><span data-stu-id="4b6cf-107"><span id="interface"></span><span id="INTERFACE"></span>*interface*</span></span>
</dt> <dd>

<span data-ttu-id="4b6cf-108">Indirizzo dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="4b6cf-108">The address of the interface.</span></span>

</dd> </dl> 




 

## <a name="possible-causes"></a><span data-ttu-id="4b6cf-109">Possibili cause</span><span class="sxs-lookup"><span data-stu-id="4b6cf-109">Possible Causes</span></span>

<span data-ttu-id="4b6cf-110">Utilizzo di risorse non valido.</span><span class="sxs-lookup"><span data-stu-id="4b6cf-110">Invalid resource usage.</span></span> <span data-ttu-id="4b6cf-111">La risorsa creata all'esterno di Direct2D viene usata con una factory Direct2D oppure le risorse create in una factory sono state usate con una risorsa creata da un'altra Factory.</span><span class="sxs-lookup"><span data-stu-id="4b6cf-111">The resource created outside of Direct2D is used with a Direct2D factory, or the resources created on one factory was used with a resource created by another factory.</span></span>

 

 




