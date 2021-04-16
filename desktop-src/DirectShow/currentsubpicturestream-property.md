---
description: La proprietà CurrentSubpictureStream imposta o Recupera il flusso di sottoimmagine corrente.
ms.assetid: 66473c87-ddfe-4555-89ad-90e210a75694
title: Proprietà CurrentSubpictureStream
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c954ad7cfb7aba6dd9bc800ac983d86b6325843
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522569"
---
# <a name="currentsubpicturestream-property"></a><span data-ttu-id="b8cf5-103">Proprietà CurrentSubpictureStream</span><span class="sxs-lookup"><span data-stu-id="b8cf5-103">CurrentSubpictureStream Property</span></span>

> [!Note]  
> <span data-ttu-id="b8cf5-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b8cf5-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="b8cf5-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="b8cf5-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="b8cf5-106">La `CurrentSubpictureStream` proprietà imposta o Recupera il flusso di sottoimmagine corrente.</span><span class="sxs-lookup"><span data-stu-id="b8cf5-106">The `CurrentSubpictureStream` property sets or retrieves the current subpicture stream.</span></span>

``` syntax
[ iSPStream = ] MSWebDVD.CurrentSubpictureStream
```

## <a name="return-value"></a><span data-ttu-id="b8cf5-107">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b8cf5-107">Return Value</span></span>

<span data-ttu-id="b8cf5-108">Restituisce un valore intero che rappresenta il flusso.</span><span class="sxs-lookup"><span data-stu-id="b8cf5-108">Returns an integer value representing the stream.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8cf5-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="b8cf5-109">Remarks</span></span>

<span data-ttu-id="b8cf5-110">I valori possibili di questa proprietà sono:</span><span class="sxs-lookup"><span data-stu-id="b8cf5-110">The possible values of this property are:</span></span>



| <span data-ttu-id="b8cf5-111">Valore</span><span class="sxs-lookup"><span data-stu-id="b8cf5-111">Value</span></span>   | <span data-ttu-id="b8cf5-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b8cf5-112">Description</span></span>              |
|---------|--------------------------|
| <span data-ttu-id="b8cf5-113">da 0 a 31</span><span class="sxs-lookup"><span data-stu-id="b8cf5-113">0 to 31</span></span> | <span data-ttu-id="b8cf5-114">Flusso di sottoimmagine</span><span class="sxs-lookup"><span data-stu-id="b8cf5-114">The subpicture stream</span></span>    |
| <span data-ttu-id="b8cf5-115">63</span><span class="sxs-lookup"><span data-stu-id="b8cf5-115">63</span></span>      | <span data-ttu-id="b8cf5-116">Flusso a bitrate ridotto disattivato</span><span class="sxs-lookup"><span data-stu-id="b8cf5-116">Muted low-bitrate stream</span></span> |



 

<span data-ttu-id="b8cf5-117">Questa proprietà è di lettura/scrittura e non prevede alcun valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="b8cf5-117">This property is read/write with no default value.</span></span> <span data-ttu-id="b8cf5-118">Prima di impostare un nuovo flusso di sottoimmagine, chiamare [**IsSubpictureStreamEnabled**](issubpicturestreamenabled-method.md) per verificare che il flusso sia disponibile.</span><span class="sxs-lookup"><span data-stu-id="b8cf5-118">Before setting a new subpicture stream, call [**IsSubpictureStreamEnabled**](issubpicturestreamenabled-method.md) to verify that the stream is available.</span></span>

<span data-ttu-id="b8cf5-119">L'impostazione di questa proprietà fa sì che la proprietà [**SubpictureOn**](subpictureon-property.md) sia impostata su **true**.</span><span class="sxs-lookup"><span data-stu-id="b8cf5-119">Setting this property causes the [**SubpictureOn**](subpictureon-property.md) property to toggle to **True**.</span></span>

## <a name="see-also"></a><span data-ttu-id="b8cf5-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b8cf5-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8cf5-121">**SubpictureOn**</span><span class="sxs-lookup"><span data-stu-id="b8cf5-121">**SubpictureOn**</span></span>](subpictureon-property.md)
</dt> <dt>

[<span data-ttu-id="b8cf5-122">**SubpictureStreamsAvailable**</span><span class="sxs-lookup"><span data-stu-id="b8cf5-122">**SubpictureStreamsAvailable**</span></span>](subpicturestreamsavailable-property.md)
</dt> </dl>

 

 



