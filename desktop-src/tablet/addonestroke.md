---
description: Aggiunge un nuovo oggetto IInkStrokeDisp all'oggetto InkDivider passato.
ms.assetid: d5b82244-68d5-4137-aaf4-d3232f7c0779
title: AddOneStroke (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddOneStroke
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: 0af3913f2579363afbb0c3985ad0f40f58051eac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483997"
---
# <a name="addonestroke-function"></a><span data-ttu-id="afdc5-103">AddOneStroke (funzione)</span><span class="sxs-lookup"><span data-stu-id="afdc5-103">AddOneStroke function</span></span>

<span data-ttu-id="afdc5-104">Aggiunge un nuovo oggetto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) all'oggetto [**InkDivider**](inkdivider-class.md) passato.</span><span class="sxs-lookup"><span data-stu-id="afdc5-104">Adds a new [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object to the [**InkDivider**](inkdivider-class.md) object that was passed in.</span></span>

<span data-ttu-id="afdc5-105">Questa funzione non deve essere usata dal codice dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="afdc5-105">This function is not intended to be used by application code.</span></span>

## <a name="syntax"></a><span data-ttu-id="afdc5-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="afdc5-106">Syntax</span></span>


```C++
HRESULT WINAPI AddOneStroke(
  _In_ INT_PTR hDivider,
  _In_ int     strokeId,
  _In_ int     cPoints,
  _In_ POINT   *aPoints
);
```



## <a name="parameters"></a><span data-ttu-id="afdc5-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="afdc5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="afdc5-108">*hDivider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="afdc5-108">*hDivider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="afdc5-109">Handle per l'oggetto [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="afdc5-109">A handle to the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="afdc5-110">*strokeId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="afdc5-110">*strokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="afdc5-111">[**ID**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) dell'oggetto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) da aggiungere all'oggetto [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="afdc5-111">The [**Id**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) of the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object to be added to the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="afdc5-112">*cPoints* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="afdc5-112">*cPoints* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="afdc5-113">Il numero di pacchetti che costituiscono il nuovo oggetto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) .</span><span class="sxs-lookup"><span data-stu-id="afdc5-113">The number of packets that make up the new [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="afdc5-114">*aPoints* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="afdc5-114">*aPoints* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="afdc5-115">Matrice di pacchetti che costituiscono l'oggetto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) in *strokeId*.</span><span class="sxs-lookup"><span data-stu-id="afdc5-115">The array of packets that make up the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object in *strokeId*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="afdc5-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="afdc5-116">Return value</span></span>

<span data-ttu-id="afdc5-117">Questa funzione può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="afdc5-117">This function can return one of these values.</span></span>



| <span data-ttu-id="afdc5-118">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="afdc5-118">Return code</span></span>                                                                                  | <span data-ttu-id="afdc5-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="afdc5-119">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="afdc5-120"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="afdc5-120"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="afdc5-121">Funzione completata.</span><span class="sxs-lookup"><span data-stu-id="afdc5-121">The function succeeded.</span></span><br/>              |
| <dl> <span data-ttu-id="afdc5-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="afdc5-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="afdc5-123">Il parametro *hDivider* non è valido.</span><span class="sxs-lookup"><span data-stu-id="afdc5-123">The *hDivider* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="afdc5-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="afdc5-124">Requirements</span></span>



| <span data-ttu-id="afdc5-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="afdc5-125">Requirement</span></span> | <span data-ttu-id="afdc5-126">Valore</span><span class="sxs-lookup"><span data-stu-id="afdc5-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="afdc5-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="afdc5-127">Minimum supported client</span></span><br/> | <span data-ttu-id="afdc5-128">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="afdc5-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="afdc5-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="afdc5-129">Minimum supported server</span></span><br/> | <span data-ttu-id="afdc5-130">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="afdc5-130">None supported</span></span><br/>                                                             |
| <span data-ttu-id="afdc5-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="afdc5-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="afdc5-132"><dt>InkDiv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="afdc5-132"><dt>InkDiv.dll</dt></span></span> </dl> |



 

 




