---
title: VBRPeak
description: L'attributo VBRPeak contiene la velocità in bit più elevata del momento in un flusso codificato a velocità in bit variabile (VBR).
ms.assetid: 7b735145-8235-4efb-986f-952989b739bc
keywords:
- VBRPeak Windows Media Format
topic_type:
- apiref
api_name:
- VBRPeak
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e8aacb076c3e92cfa676e73e945506cc4942bf4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045832"
---
# <a name="vbrpeak"></a><span data-ttu-id="0fd8a-104">VBRPeak</span><span class="sxs-lookup"><span data-stu-id="0fd8a-104">VBRPeak</span></span>

<span data-ttu-id="0fd8a-105">L'attributo **VBRPeak** contiene la velocità in bit più elevata del momento in un flusso codificato a velocità in bit variabile (VBR).</span><span class="sxs-lookup"><span data-stu-id="0fd8a-105">The **VBRPeak** attribute contains the highest momentary bit rate in a variable bit rate (VBR) encoded stream.</span></span>

## <a name="global-constant"></a><span data-ttu-id="0fd8a-106">Costante globale</span><span class="sxs-lookup"><span data-stu-id="0fd8a-106">Global Constant</span></span>

<span data-ttu-id="0fd8a-107">g \_ wszVBRPeak</span><span class="sxs-lookup"><span data-stu-id="0fd8a-107">g\_wszVBRPeak</span></span>

## <a name="data-type"></a><span data-ttu-id="0fd8a-108">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="0fd8a-108">Data Type</span></span>

<span data-ttu-id="0fd8a-109">**WMT \_ tipo \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="0fd8a-109">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="0fd8a-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="0fd8a-110">Remarks</span></span>

<span data-ttu-id="0fd8a-111">Quando si accede all'interfaccia **IWMHeaderInfo3** dell'oggetto writer, è possibile aggiungere o modificare questo valore.</span><span class="sxs-lookup"><span data-stu-id="0fd8a-111">When accessing the **IWMHeaderInfo3** interface of the writer object, you can add or change this value.</span></span> <span data-ttu-id="0fd8a-112">In altri oggetti (editor di metadati, lettore e lettore sincrono), questo valore è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="0fd8a-112">In other objects (metadata editor, reader, and synchronous reader), this value is read-only.</span></span>

<span data-ttu-id="0fd8a-113">Il writer scrive automaticamente un valore **VBRPeak** per ogni flusso VBR.</span><span class="sxs-lookup"><span data-stu-id="0fd8a-113">The writer automatically writes a **VBRPeak** value for each VBR stream.</span></span>

## <a name="see-also"></a><span data-ttu-id="0fd8a-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0fd8a-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fd8a-115">**Elenco degli attributi**</span><span class="sxs-lookup"><span data-stu-id="0fd8a-115">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




