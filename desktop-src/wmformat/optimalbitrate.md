---
title: OptimalBitrate
description: L'attributo OptimalBitrate contiene la velocità in bit in cui è possibile riprodurre il file.
ms.assetid: cd13b9b5-34d2-4ebb-9f10-3bf42dd9de81
keywords:
- OptimalBitrate Windows Media Format
topic_type:
- apiref
api_name:
- OptimalBitrate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff71c6b64cbc4bf4ccc4f346e62a5eae066e78ce
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299197"
---
# <a name="optimalbitrate"></a><span data-ttu-id="63ada-104">OptimalBitrate</span><span class="sxs-lookup"><span data-stu-id="63ada-104">OptimalBitrate</span></span>

<span data-ttu-id="63ada-105">L'attributo **OptimalBitrate** contiene la velocità in bit in cui è possibile riprodurre il file.</span><span class="sxs-lookup"><span data-stu-id="63ada-105">The **OptimalBitrate** attribute contains the bit rate at which the file is best played.</span></span>

## <a name="global-constant"></a><span data-ttu-id="63ada-106">Costante globale</span><span class="sxs-lookup"><span data-stu-id="63ada-106">Global Constant</span></span>

<span data-ttu-id="63ada-107">g \_ wszWMOptimalBitrate</span><span class="sxs-lookup"><span data-stu-id="63ada-107">g\_wszWMOptimalBitrate</span></span>

## <a name="data-type"></a><span data-ttu-id="63ada-108">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="63ada-108">Data Type</span></span>

<span data-ttu-id="63ada-109">**WMT \_ tipo \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="63ada-109">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="63ada-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="63ada-110">Remarks</span></span>

<span data-ttu-id="63ada-111">Si tratta di un attributo codificato.</span><span class="sxs-lookup"><span data-stu-id="63ada-111">This is a coded attribute.</span></span>

<span data-ttu-id="63ada-112">Per i file che contengono flussi di velocità in bit variabili (VBR), questo valore è la velocità in bit massima per i flussi nel file.</span><span class="sxs-lookup"><span data-stu-id="63ada-112">For files that contain variable bit rate (VBR) streams, this value is the peak bit rate for the streams in the file.</span></span> <span data-ttu-id="63ada-113">Per i file senza VBR, questo valore è uguale a quello della [**velocità in bit**](bit-rate.md).</span><span class="sxs-lookup"><span data-stu-id="63ada-113">For files without VBR, this value is the same as [**Bitrate**](bit-rate.md).</span></span>

<span data-ttu-id="63ada-114">Questo attributo non può essere duplicato a livello di file.</span><span class="sxs-lookup"><span data-stu-id="63ada-114">This attribute cannot be duplicated at the file level.</span></span> <span data-ttu-id="63ada-115">Se questo attributo viene utilizzato per un singolo flusso, verrà considerato come metadati personalizzati e non verrà trasmesso il significato normale agli oggetti di Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="63ada-115">If this attribute is used for an individual stream, it will be treated as custom metadata and will not convey its normal meaning to the objects of the Windows Media Format SDK.</span></span>

## <a name="see-also"></a><span data-ttu-id="63ada-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="63ada-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63ada-117">**Elenco degli attributi**</span><span class="sxs-lookup"><span data-stu-id="63ada-117">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




