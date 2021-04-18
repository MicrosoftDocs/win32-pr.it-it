---
title: ErrorItem. Condition
description: La proprietà Condition recupera un valore che indica la condizione per l'errore.
ms.assetid: efb54b48-cfaa-479f-9ee6-ce6724dca24c
keywords:
- Media Player di Windows ErrorItem. Condition
topic_type:
- apiref
api_name:
- ErrorItem.condition
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c498e7479a7a3e067dea2d8a562800351effd672
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331585"
---
# <a name="erroritemcondition"></a><span data-ttu-id="25bc1-104">ErrorItem. Condition</span><span class="sxs-lookup"><span data-stu-id="25bc1-104">ErrorItem.condition</span></span>

<span data-ttu-id="25bc1-105">La proprietà **Condition** recupera un valore che indica la condizione per l'errore.</span><span class="sxs-lookup"><span data-stu-id="25bc1-105">The **condition** property retrieves a value indicating the condition for the error.</span></span>

``` syntax
player.error.item(
        index
        ).condition
      
```

## <a name="possible-values"></a><span data-ttu-id="25bc1-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="25bc1-106">Possible Values</span></span>

<span data-ttu-id="25bc1-107">Questa proprietà è un **numero** di sola lettura (**Long**) che rappresenta il codice della condizione.</span><span class="sxs-lookup"><span data-stu-id="25bc1-107">This property is a read-only **Number** (**long**) that represents the condition code.</span></span>

## <a name="remarks"></a><span data-ttu-id="25bc1-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="25bc1-108">Remarks</span></span>

<span data-ttu-id="25bc1-109">Il codice della condizione è un valore utilizzato da Microsoft per fornire informazioni aggiuntive per il personale del supporto tecnico.</span><span class="sxs-lookup"><span data-stu-id="25bc1-109">The condition code is a value that is used by Microsoft to provide additional information for technical support personnel.</span></span>

<span data-ttu-id="25bc1-110">**Windows Media Player 10 Mobile:** Questa proprietà restituisce sempre 0.</span><span class="sxs-lookup"><span data-stu-id="25bc1-110">**Windows Media Player 10 Mobile:** This property always returns 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="25bc1-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="25bc1-111">Requirements</span></span>



| <span data-ttu-id="25bc1-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="25bc1-112">Requirement</span></span> | <span data-ttu-id="25bc1-113">Valore</span><span class="sxs-lookup"><span data-stu-id="25bc1-113">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="25bc1-114">Versione</span><span class="sxs-lookup"><span data-stu-id="25bc1-114">Version</span></span><br/> | <span data-ttu-id="25bc1-115">Windows Media Player 9 serie o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="25bc1-115">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="25bc1-116">DLL</span><span class="sxs-lookup"><span data-stu-id="25bc1-116">DLL</span></span><br/>     | <dl> <span data-ttu-id="25bc1-117"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25bc1-117"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25bc1-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="25bc1-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25bc1-119">**Oggetto ErrorItem**</span><span class="sxs-lookup"><span data-stu-id="25bc1-119">**ErrorItem Object**</span></span>](erroritem-object.md)
</dt> </dl>

 

 





