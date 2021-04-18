---
description: Specifica se un gestore del flusso di byte può utilizzare un flusso di byte aperto per la scrittura da un altro thread.
ms.assetid: d9d97880-a563-420c-b598-c3ebd1ae8b74
title: Attributo MF_BYTESTREAMHANDLER_ACCEPTS_SHARE_WRITE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b46a3402585cbce9c1d1464ceb9fb161527673c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309586"
---
# <a name="mf_bytestreamhandler_accepts_share_write-attribute"></a><span data-ttu-id="c5c61-103">MF \_ BYTESTREAMHANDLER \_ accetta \_ l' \_ attributo Share Write</span><span class="sxs-lookup"><span data-stu-id="c5c61-103">MF\_BYTESTREAMHANDLER\_ACCEPTS\_SHARE\_WRITE attribute</span></span>

<span data-ttu-id="c5c61-104">Specifica se un gestore del flusso di byte può utilizzare un flusso di byte aperto per la scrittura da un altro thread.</span><span class="sxs-lookup"><span data-stu-id="c5c61-104">Specifies whether a byte-stream handler can use a byte stream that is opened for writing by another thread.</span></span>

## <a name="data-type"></a><span data-ttu-id="c5c61-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="c5c61-105">Data type</span></span>

<span data-ttu-id="c5c61-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="c5c61-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="c5c61-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="c5c61-107">Get/set</span></span>

<span data-ttu-id="c5c61-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="c5c61-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="c5c61-109">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="c5c61-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="c5c61-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="c5c61-110">Remarks</span></span>

<span data-ttu-id="c5c61-111">I gestori del flusso di byte possono supportare questo attributo.</span><span class="sxs-lookup"><span data-stu-id="c5c61-111">Byte-stream handlers can support this attribute.</span></span> <span data-ttu-id="c5c61-112">Per ottenere o impostare l'attributo, eseguire prima una query sul gestore del flusso di byte per l'interfaccia [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="c5c61-112">To get or set the attribute, first query the byte-stream handler for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span> <span data-ttu-id="c5c61-113">Chiamare quindi [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) o [**IMFAttributes:: seuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)</span><span class="sxs-lookup"><span data-stu-id="c5c61-113">Then call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) or [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)</span></span>

<span data-ttu-id="c5c61-114">Se questo attributo è **true**, significa che il gestore del flusso di byte può leggere da un flusso mentre un altro thread scrive nello stesso flusso.</span><span class="sxs-lookup"><span data-stu-id="c5c61-114">If this attribute is **TRUE**, it means that the byte-stream handler can read from a stream while another thread writes to the same stream.</span></span> <span data-ttu-id="c5c61-115">Quando un flusso viene aperto per la scrittura da parte di un altro thread, il metodo [**IMFByteStream:: GetCapabilities**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getcapabilities) restituisce il flag di **\_ \_ scrittura della condivisione MFBYTESTREAM** .</span><span class="sxs-lookup"><span data-stu-id="c5c61-115">When a stream is opened for writing by another thread, the [**IMFByteStream::GetCapabilities**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getcapabilities) method returns the **MFBYTESTREAM\_SHARE\_WRITE** flag.</span></span>

<span data-ttu-id="c5c61-116">Questo attributo influiscono sulla risoluzione dell'origine.</span><span class="sxs-lookup"><span data-stu-id="c5c61-116">This attribute affects source resolution.</span></span> <span data-ttu-id="c5c61-117">Se per un flusso di byte è impostato il flag di **\_ \_ scrittura della condivisione MFBYTESTREAM** , il [resolver di origine](source-resolver.md) non passerà il flusso a un gestore del flusso di byte, a meno che il gestore non abbia l' \_ attributo MF BYTESTREAMHANDLER \_ accepts \_ per la scrittura della condivisione \_ impostata su **true**.</span><span class="sxs-lookup"><span data-stu-id="c5c61-117">If a byte stream has the **MFBYTESTREAM\_SHARE\_WRITE** flag set, the [Source Resolver](source-resolver.md) will not pass that stream to a byte-stream handler unless the handler has the MF\_BYTESTREAMHANDLER\_ACCEPTS\_SHARE\_WRITE attribute set to **TRUE**.</span></span>

<span data-ttu-id="c5c61-118">Il flag di **\_ \_ scrittura della condivisione MFBYTESTREAM** è un suggerimento che la lunghezza del flusso potrebbe cambiare durante la lettura da parte del gestore.</span><span class="sxs-lookup"><span data-stu-id="c5c61-118">The **MFBYTESTREAM\_SHARE\_WRITE** flag is a hint that the length of the stream might change while the handler is reading from it.</span></span>

<span data-ttu-id="c5c61-119">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="c5c61-119">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5c61-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c5c61-120">Requirements</span></span>



| <span data-ttu-id="c5c61-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5c61-121">Requirement</span></span> | <span data-ttu-id="c5c61-122">Valore</span><span class="sxs-lookup"><span data-stu-id="c5c61-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c5c61-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c5c61-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c5c61-124">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="c5c61-124">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="c5c61-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c5c61-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c5c61-126">App desktop di Windows Server 2008 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="c5c61-126">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="c5c61-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c5c61-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5c61-128"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5c61-128"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5c61-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c5c61-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5c61-130">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c5c61-130">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c5c61-131">Gestori di schemi e gestori di Byte-Stream</span><span class="sxs-lookup"><span data-stu-id="c5c61-131">Scheme Handlers and Byte-Stream Handlers</span></span>](scheme-handlers-and-byte-stream-handlers.md)
</dt> </dl>

 

 




