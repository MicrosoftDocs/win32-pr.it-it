---
title: WM/StreamTypeInfo
description: L'attributo WM/StreamTypeInfo contiene le informazioni di configurazione per il flusso specificato nel file ASF.
ms.assetid: 4d7f18d4-d76d-4e2e-b8a9-eb96844a2fa1
keywords:
- Formato di Windows Media WM/StreamTypeInfo
topic_type:
- apiref
api_name:
- WM/StreamTypeInfo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c410b470e9ddb4ec874325d9c1cca2839c00b1d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104397486"
---
# <a name="wmstreamtypeinfo"></a><span data-ttu-id="10430-104">WM/StreamTypeInfo</span><span class="sxs-lookup"><span data-stu-id="10430-104">WM/StreamTypeInfo</span></span>

<span data-ttu-id="10430-105">L'attributo **WM/StreamTypeInfo** contiene le informazioni di configurazione per il flusso specificato nel file ASF.</span><span class="sxs-lookup"><span data-stu-id="10430-105">The **WM/StreamTypeInfo** attribute contains the configuration information for the specified stream in the ASF file.</span></span>

## <a name="global-constant"></a><span data-ttu-id="10430-106">Costante globale</span><span class="sxs-lookup"><span data-stu-id="10430-106">Global Constant</span></span>

<span data-ttu-id="10430-107">g \_ wszWMStreamTypeInfo</span><span class="sxs-lookup"><span data-stu-id="10430-107">g\_wszWMStreamTypeInfo</span></span>

## <a name="data-type"></a><span data-ttu-id="10430-108">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="10430-108">Data Type</span></span>

<span data-ttu-id="10430-109">[**WM \_ \_ \_ informazioni sul tipo di flusso**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_stream_type_info) (**\_ \_ Binary di tipo WMT**)</span><span class="sxs-lookup"><span data-stu-id="10430-109">[**WM\_STREAM\_TYPE\_INFO**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_stream_type_info) (**WMT\_TYPE\_BINARY**)</span></span>

## <a name="remarks"></a><span data-ttu-id="10430-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="10430-110">Remarks</span></span>

<span data-ttu-id="10430-111">Questo attributo si applica a flussi specifici.</span><span class="sxs-lookup"><span data-stu-id="10430-111">This attribute applies to specific streams.</span></span> <span data-ttu-id="10430-112">Non è possibile recuperare questo attributo per il flusso 0.</span><span class="sxs-lookup"><span data-stu-id="10430-112">You cannot retrieve this attribute for stream 0.</span></span>

<span data-ttu-id="10430-113">Questo attributo è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="10430-113">This attribute is read-only.</span></span>

<span data-ttu-id="10430-114">È possibile accedere a **WM/StreamTypeInfo** dall'oggetto dell'editor di metadati.</span><span class="sxs-lookup"><span data-stu-id="10430-114">**WM/StreamTypeInfo** can be accessed by the metadata editor object.</span></span> <span data-ttu-id="10430-115">Questo è l'unico modo per accedere alle informazioni di configurazione del flusso senza aprire il file con l'oggetto Reader (o l'oggetto Reader sincrono).</span><span class="sxs-lookup"><span data-stu-id="10430-115">This is the only way to access stream configuration information without opening the file with the reader object (or the synchronous reader object).</span></span>

## <a name="see-also"></a><span data-ttu-id="10430-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="10430-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10430-117">**Elenco degli attributi**</span><span class="sxs-lookup"><span data-stu-id="10430-117">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




