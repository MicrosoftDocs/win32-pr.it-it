---
title: Il tipo della risorsa D1106 non è corretto
ms.assetid: 79a618cb-1d05-4895-b801-7663890b456a
description: La risorsa specificata non è di un tipo previsto.
keywords:
- La risorsa D1106 non è di tipo Direct2D
topic_type:
- apiref
api_name:
- D1106 Resource Is Wrong Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 5c38ef36319b8021de918a798c94a3be0683a7b7
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/27/2021
ms.locfileid: "106334162"
---
# <a name="d1106-resource-is-wrong-type"></a><span data-ttu-id="3e489-104">D1106: la risorsa è di tipo errato</span><span class="sxs-lookup"><span data-stu-id="3e489-104">D1106: Resource Is Wrong Type</span></span>

<span data-ttu-id="3e489-105">La risorsa della risorsa specificata \[  \] non è di un tipo previsto.</span><span class="sxs-lookup"><span data-stu-id="3e489-105">The given resource \[*resource*\] is not of an expected type.</span></span>

## <a name="placeholders"></a><span data-ttu-id="3e489-106">Segnaposto</span><span class="sxs-lookup"><span data-stu-id="3e489-106">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="3e489-107"><span id="resource"></span><span id="RESOURCE"></span>*risorse*</span><span class="sxs-lookup"><span data-stu-id="3e489-107"><span id="resource"></span><span id="RESOURCE"></span>*resource*</span></span>
</dt> <dd>

<span data-ttu-id="3e489-108">Indirizzo della risorsa.</span><span class="sxs-lookup"><span data-stu-id="3e489-108">The address of the resource.</span></span>

</dd> </dl> 




 

## <a name="possible-causes"></a><span data-ttu-id="3e489-109">Possibili cause</span><span class="sxs-lookup"><span data-stu-id="3e489-109">Possible Causes</span></span>

<span data-ttu-id="3e489-110">Un'interfaccia è stata cast e usata in modo errato come parametro per un metodo o una funzione.</span><span class="sxs-lookup"><span data-stu-id="3e489-110">An interface was improperly cast and used as a parameter for a method or function.</span></span>

## <a name="examples"></a><span data-ttu-id="3e489-111">Esempio</span><span class="sxs-lookup"><span data-stu-id="3e489-111">Examples</span></span>

<span data-ttu-id="3e489-112">Nell'esempio seguente viene passato un [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) quando è previsto un [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) .</span><span class="sxs-lookup"><span data-stu-id="3e489-112">The following example passes an [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) when an [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) is expected.</span></span>


```C++
        m_pRenderTarget->FillGeometry(
            (ID2D1Geometry*)m_pYellowGreenBrush,
            m_pYellowGreenBrush
            );
```



<span data-ttu-id="3e489-113">Questo esempio produce il seguente messaggio di debug:</span><span class="sxs-lookup"><span data-stu-id="3e489-113">This example produces the following debug message:</span></span>

``` syntax
DEBUG ERROR - The given resource[003A2C98] is not of an expected type
```

## <a name="fixes"></a><span data-ttu-id="3e489-114">Correzioni</span><span class="sxs-lookup"><span data-stu-id="3e489-114">Fixes</span></span>

<span data-ttu-id="3e489-115">Usare il tipo richiesto dal metodo.</span><span class="sxs-lookup"><span data-stu-id="3e489-115">Use the type required by the method.</span></span>

 

 
