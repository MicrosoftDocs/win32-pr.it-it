---
title: Ricercabile
description: L'attributo seekable è un attributo a livello di file che specifica se un'applicazione può cercare punti all'interno del contenuto.
ms.assetid: 9653e368-4782-4506-9c44-54c9406b61b5
keywords:
- Formato Windows Media ricercabile
topic_type:
- apiref
api_name:
- Seekable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4db701be363c194c75bd698062d79a0c0c407cc
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "104336626"
---
# <a name="seekable"></a><span data-ttu-id="05385-104">Ricercabile</span><span class="sxs-lookup"><span data-stu-id="05385-104">Seekable</span></span>

<span data-ttu-id="05385-105">L'attributo **seekable** è un attributo a livello di file che specifica se un'applicazione può cercare punti all'interno del contenuto.</span><span class="sxs-lookup"><span data-stu-id="05385-105">The **Seekable** attribute is a file-level attribute specifying whether an application can seek to points within the content.</span></span>

## <a name="global-constant"></a><span data-ttu-id="05385-106">Costante globale</span><span class="sxs-lookup"><span data-stu-id="05385-106">Global Constant</span></span>

<span data-ttu-id="05385-107">g \_ wszWMSeekable</span><span class="sxs-lookup"><span data-stu-id="05385-107">g\_wszWMSeekable</span></span>

## <a name="data-type"></a><span data-ttu-id="05385-108">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="05385-108">Data Type</span></span>

<span data-ttu-id="05385-109">**\_tipo WMT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="05385-109">**WMT\_TYPE\_BOOL**</span></span>

## <a name="remarks"></a><span data-ttu-id="05385-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="05385-110">Remarks</span></span>

<span data-ttu-id="05385-111">Si tratta di un attributo codificato.</span><span class="sxs-lookup"><span data-stu-id="05385-111">This is a coded attribute.</span></span>

<span data-ttu-id="05385-112">Questo attributo non può essere duplicato a livello di file.</span><span class="sxs-lookup"><span data-stu-id="05385-112">This attribute cannot be duplicated at the file level.</span></span> <span data-ttu-id="05385-113">Se questo attributo viene utilizzato per un singolo flusso, verrà considerato come metadati personalizzati e non verrà trasmesso il significato normale agli oggetti di Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="05385-113">If this attribute is used for an individual stream, it will be treated as custom metadata and will not convey its normal meaning to the objects of the Windows Media Format SDK.</span></span>

<span data-ttu-id="05385-114">Il valore di questo attributo per un file può variare a seconda dell'oggetto che espone l'interfaccia [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) o [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) utilizzata per recuperarla.</span><span class="sxs-lookup"><span data-stu-id="05385-114">The value of this attribute for a file may vary depending upon the object exposing the [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) or [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) interface used to retrieve it.</span></span> <span data-ttu-id="05385-115">Ciò è dovuto al fatto che gli oggetti Reader (sincroni e asincroni) eseguono un controllo più approfondito rispetto all'oggetto dell'editor di metadati, per verificare se è possibile cercare un punto in un file.</span><span class="sxs-lookup"><span data-stu-id="05385-115">This is because the reader objects (both synchronous and asynchronous) perform a more thorough check than the metadata editor object does, to ascertain whether you can seek to a point in a file.</span></span> <span data-ttu-id="05385-116">Il valore dell'attributo **cercabile** restituito da un oggetto Reader è più accurato.</span><span class="sxs-lookup"><span data-stu-id="05385-116">The **Seekable** attribute value returned by a reader object is more accurate.</span></span>

## <a name="see-also"></a><span data-ttu-id="05385-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="05385-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05385-118">**Elenco degli attributi**</span><span class="sxs-lookup"><span data-stu-id="05385-118">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




