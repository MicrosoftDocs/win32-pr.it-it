---
title: External. DownloadManager
description: Si noti che in questo argomento viene descritta la funzionalità progettata per l'utilizzo da punti vendita online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato. La proprietà DownloadManager recupera l'oggetto DownloadManager.
ms.assetid: 9fec7175-611e-4e7e-8978-132e6f86329a
keywords:
- Media Player di Windows External. DownloadManager
topic_type:
- apiref
api_name:
- External.DownloadManager
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f55e6371f5c8d1e5dfcb17762340a82e8d921c17
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328887"
---
# <a name="externaldownloadmanager"></a><span data-ttu-id="757ff-106">External. DownloadManager</span><span class="sxs-lookup"><span data-stu-id="757ff-106">External.DownloadManager</span></span>

> [!Note]  
> <span data-ttu-id="757ff-107">Questo argomento descrive la funzionalità progettata per l'uso da punti vendita online.</span><span class="sxs-lookup"><span data-stu-id="757ff-107">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="757ff-108">L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.</span><span class="sxs-lookup"><span data-stu-id="757ff-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="757ff-109">La proprietà **downloadmanager** recupera l'oggetto **downloadmanager** .</span><span class="sxs-lookup"><span data-stu-id="757ff-109">The **DownloadManager** property retrieves the **DownloadManager** object.</span></span>

``` syntax
window.external.DownloadManager
      
```

## <a name="possible-values"></a><span data-ttu-id="757ff-110">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="757ff-110">Possible Values</span></span>

<span data-ttu-id="757ff-111">Questa proprietà è un oggetto **downloadmanager** di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="757ff-111">This property is a read-only **DownloadManager** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="757ff-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="757ff-112">Remarks</span></span>

<span data-ttu-id="757ff-113">In Windows Media Player 10 o versioni successive, la proprietà e l'oggetto **downloadmanager** sono accessibili solo dai riquadri attività del servizio di archiviazione online.</span><span class="sxs-lookup"><span data-stu-id="757ff-113">In Windows Media Player 10 or later, the **DownloadManager** property and object are accessible only from online store service task panes.</span></span> <span data-ttu-id="757ff-114">Non è possibile usare **downloadmanager** da altre funzionalità in cui l'oggetto **esterno** è disponibile, ad esempio HtmlView, visualizzazione centro informazioni e informazioni sugli album.</span><span class="sxs-lookup"><span data-stu-id="757ff-114">You cannot use the **DownloadManager** from other features where the **External** object is available, such as HTMLView, Info Center View, and album information.</span></span>

## <a name="requirements"></a><span data-ttu-id="757ff-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="757ff-115">Requirements</span></span>



| <span data-ttu-id="757ff-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="757ff-116">Requirement</span></span> | <span data-ttu-id="757ff-117">Valore</span><span class="sxs-lookup"><span data-stu-id="757ff-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="757ff-118">Versione</span><span class="sxs-lookup"><span data-stu-id="757ff-118">Version</span></span><br/> | <span data-ttu-id="757ff-119">Windows Media Player 9 serie o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="757ff-119">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="757ff-120">DLL</span><span class="sxs-lookup"><span data-stu-id="757ff-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="757ff-121"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="757ff-121"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="757ff-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="757ff-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="757ff-123">**Oggetto esterno per i negozi di tipo 2 online**</span><span class="sxs-lookup"><span data-stu-id="757ff-123">**External Object for Type 2 Online Stores**</span></span>](external-object-for-type-2-online-stores.md)
</dt> </dl>

 

 





