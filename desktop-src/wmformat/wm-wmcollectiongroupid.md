---
title: WM/WMCollectionGroupID
description: L'attributo WM/WMCollectionGroupID contiene un GUID che identifica il gruppo di raccolta.
ms.assetid: 5cfa1747-ce3b-4e8d-bcce-84fb719123e8
keywords:
- Formato di Windows Media WM/WMCollectionGroupID
topic_type:
- apiref
api_name:
- WM/WMCollectionGroupID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 652007933669db4ed7977474858c7089ca0d577f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104397790"
---
# <a name="wmwmcollectiongroupid"></a><span data-ttu-id="24de6-104">WM/WMCollectionGroupID</span><span class="sxs-lookup"><span data-stu-id="24de6-104">WM/WMCollectionGroupID</span></span>

<span data-ttu-id="24de6-105">L'attributo **WM/WMCollectionGroupID** contiene un GUID che identifica il gruppo di raccolta.</span><span class="sxs-lookup"><span data-stu-id="24de6-105">The **WM/WMCollectionGroupID** attribute contains a GUID identifying the collection group.</span></span>

## <a name="global-constant"></a><span data-ttu-id="24de6-106">Costante globale</span><span class="sxs-lookup"><span data-stu-id="24de6-106">Global Constant</span></span>

<span data-ttu-id="24de6-107">g \_ wszWMWMCollectionGroupID</span><span class="sxs-lookup"><span data-stu-id="24de6-107">g\_wszWMWMCollectionGroupID</span></span>

## <a name="data-type"></a><span data-ttu-id="24de6-108">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="24de6-108">Data Type</span></span>

<span data-ttu-id="24de6-109">**\_GUID di tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="24de6-109">**WMT\_TYPE\_GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="24de6-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="24de6-110">Remarks</span></span>

<span data-ttu-id="24de6-111">Il contenuto viene identificato dalle tecnologie Windows Media usando tre valori: **WM/WMCollectionGroupID**, **WM/WMCollectionID** e **WM/WMContentID**.</span><span class="sxs-lookup"><span data-stu-id="24de6-111">Content is identified by Windows Media technologies by using three values: **WM/WMCollectionGroupID**, **WM/WMCollectionID**, and **WM/WMContentID**.</span></span> <span data-ttu-id="24de6-112">Questi valori identificano il contenuto, la raccolta a cui appartiene e il gruppo a cui appartiene la raccolta.</span><span class="sxs-lookup"><span data-stu-id="24de6-112">These values identify the content, the collection to which it belongs, and the group to which the collection belongs.</span></span> <span data-ttu-id="24de6-113">Tutti e tre questi valori vengono popolati da Windows Media Player quando vengono recuperati i metadati per il contenuto.</span><span class="sxs-lookup"><span data-stu-id="24de6-113">All three of these values are populated by Windows Media Player when metadata for the content is retrieved.</span></span> <span data-ttu-id="24de6-114">È possibile fare in modo che l'applicazione registri questi valori e li usi per identificare il contenuto, ma non è necessario modificarli se presenti.</span><span class="sxs-lookup"><span data-stu-id="24de6-114">You can have your application record these values and use them to identify content, but you should not change them if they are present.</span></span>

## <a name="see-also"></a><span data-ttu-id="24de6-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="24de6-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24de6-116">**Elenco degli attributi**</span><span class="sxs-lookup"><span data-stu-id="24de6-116">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




