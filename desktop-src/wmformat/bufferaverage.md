---
title: BufferAverage
description: L'attributo BufferAverage contiene la dimensione media del buffer necessaria per un flusso di velocità in bit variabile (VBR).
ms.assetid: 5fd69534-6655-4c98-bf07-a694585fc9ae
keywords:
- BufferAverage Windows Media Format
topic_type:
- apiref
api_name:
- BufferAverage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce5767ed329fde43cc1022af54d937fc99e0e323
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104117104"
---
# <a name="bufferaverage"></a><span data-ttu-id="f5257-104">BufferAverage</span><span class="sxs-lookup"><span data-stu-id="f5257-104">BufferAverage</span></span>

<span data-ttu-id="f5257-105">L'attributo **BufferAverage** contiene la dimensione media del buffer necessaria per un flusso di velocità in bit variabile (VBR).</span><span class="sxs-lookup"><span data-stu-id="f5257-105">The **BufferAverage** attribute contains the average buffer size needed for a variable bit rate (VBR) stream.</span></span>

## <a name="global-constant"></a><span data-ttu-id="f5257-106">Costante globale</span><span class="sxs-lookup"><span data-stu-id="f5257-106">Global Constant</span></span>

<span data-ttu-id="f5257-107">g \_ wszBufferAverage</span><span class="sxs-lookup"><span data-stu-id="f5257-107">g\_wszBufferAverage</span></span>

## <a name="data-type"></a><span data-ttu-id="f5257-108">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="f5257-108">Data Type</span></span>

<span data-ttu-id="f5257-109">**WMT \_ tipo \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="f5257-109">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="f5257-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="f5257-110">Remarks</span></span>

<span data-ttu-id="f5257-111">Quando si accede all'interfaccia **IWMHeaderInfo3** dell'oggetto writer, è possibile aggiungere o modificare questo valore.</span><span class="sxs-lookup"><span data-stu-id="f5257-111">When accessing the **IWMHeaderInfo3** interface of the writer object, you can add or change this value.</span></span> <span data-ttu-id="f5257-112">In altri oggetti (editor di metadati, lettore e lettore sincrono), questo valore è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="f5257-112">In other objects (metadata editor, reader, and synchronous reader), this value is read-only.</span></span>

<span data-ttu-id="f5257-113">Il writer scrive automaticamente un valore **BufferAverage** per ogni flusso VBR.</span><span class="sxs-lookup"><span data-stu-id="f5257-113">The writer automatically writes a **BufferAverage** value for each VBR stream.</span></span>

## <a name="see-also"></a><span data-ttu-id="f5257-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f5257-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5257-115">**Elenco degli attributi**</span><span class="sxs-lookup"><span data-stu-id="f5257-115">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




