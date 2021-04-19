---
title: CurrentBitrate
description: L'attributo CurrentBitrate contiene la velocità in bit totale corrente dei flussi attivi nel file.
ms.assetid: 961f36d5-a408-40d9-9ca1-0ed7c484858f
keywords:
- CurrentBitrate Windows Media Format
topic_type:
- apiref
api_name:
- CurrentBitrate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdcd8db7d60c65bcb7ceedcac4498ac650f90d9a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299241"
---
# <a name="currentbitrate"></a><span data-ttu-id="63839-104">CurrentBitrate</span><span class="sxs-lookup"><span data-stu-id="63839-104">CurrentBitrate</span></span>

<span data-ttu-id="63839-105">L'attributo CurrentBitrate contiene la velocità in bit totale corrente dei flussi attivi nel file.</span><span class="sxs-lookup"><span data-stu-id="63839-105">The CurrentBitrate attribute contains the current total bit rate of the active streams in the file.</span></span>

## <a name="global-constant"></a><span data-ttu-id="63839-106">Costante globale</span><span class="sxs-lookup"><span data-stu-id="63839-106">Global Constant</span></span>

<span data-ttu-id="63839-107">g \_ wszWMCurrentBitrate</span><span class="sxs-lookup"><span data-stu-id="63839-107">g\_wszWMCurrentBitrate</span></span>

## <a name="data-type"></a><span data-ttu-id="63839-108">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="63839-108">Data Type</span></span>

<span data-ttu-id="63839-109">**WMT \_ tipo \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="63839-109">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="63839-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="63839-110">Remarks</span></span>

<span data-ttu-id="63839-111">Si tratta di un attributo codificato.</span><span class="sxs-lookup"><span data-stu-id="63839-111">This is a coded attribute.</span></span>

<span data-ttu-id="63839-112">Il valore recuperato per **CurrentBitrate** è diverso a seconda dell'oggetto utilizzato.</span><span class="sxs-lookup"><span data-stu-id="63839-112">The value retrieved for **CurrentBitrate** is different depending upon the object used.</span></span> <span data-ttu-id="63839-113">Nell'oggetto Reader o Reader sincrono, il valore è la velocità in bit effettiva al momento della chiamata.</span><span class="sxs-lookup"><span data-stu-id="63839-113">In the reader or synchronous reader object, the value is the actual bit rate at the time of the call.</span></span> <span data-ttu-id="63839-114">Nell'oggetto dell'editor di metadati, il valore corrisponde alla velocità in bit media del file.</span><span class="sxs-lookup"><span data-stu-id="63839-114">In the metadata editor object, the value is the average bit rate of the file.</span></span>

<span data-ttu-id="63839-115">La velocità in bit effettiva di un file è uguale alla velocità in bit di tutti i flussi attivi, oltre a un sovraccarico.</span><span class="sxs-lookup"><span data-stu-id="63839-115">The actual bit rate of a file is equal to the bit rates of all active streams plus some overhead.</span></span> <span data-ttu-id="63839-116">Questo è il valore, ad esempio, visualizzato quando si riproduce un file con Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="63839-116">This is the value that is, for example, displayed when playing a file with the Windows Media Player.</span></span>

<span data-ttu-id="63839-117">Questo attributo non può essere duplicato a livello di file.</span><span class="sxs-lookup"><span data-stu-id="63839-117">This attribute cannot be duplicated at the file level.</span></span> <span data-ttu-id="63839-118">Se questo attributo viene utilizzato per un singolo flusso, verrà considerato come metadati personalizzati e non verrà trasmesso il significato normale agli oggetti di Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="63839-118">If this attribute is used for an individual stream, it will be treated as custom metadata and will not convey its normal meaning to the objects of the Windows Media Format SDK.</span></span>

## <a name="see-also"></a><span data-ttu-id="63839-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="63839-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63839-120">**Elenco degli attributi**</span><span class="sxs-lookup"><span data-stu-id="63839-120">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




