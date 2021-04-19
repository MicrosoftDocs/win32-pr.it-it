---
title: Writer XML
description: Il writer XML è un'API per la creazione di codice XML. Al suo nucleo, un writer XML scrive un nodo XML alla volta, ma sono disponibili API helper aggiuntive per semplificare la scrittura di una sequenza di nodi.
ms.assetid: 69d50793-1d5b-4fc7-bf69-128f8e23a98d
keywords:
- Servizi Web writer XML per Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 085a02b3aca33ffa3b31e4579d47068a683ee4d8
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "106300691"
---
# <a name="xml-writer"></a><span data-ttu-id="fc69f-107">Writer XML</span><span class="sxs-lookup"><span data-stu-id="fc69f-107">XML Writer</span></span>

<span data-ttu-id="fc69f-108">Il writer XML è un'API per la creazione di codice XML.</span><span class="sxs-lookup"><span data-stu-id="fc69f-108">XML Writer is an API for emitting XML.</span></span> <span data-ttu-id="fc69f-109">Al suo nucleo, un writer XML scrive un [nodo XML](xml-node.md) alla volta, ma sono disponibili API helper aggiuntive per semplificare la scrittura di una sequenza di nodi.</span><span class="sxs-lookup"><span data-stu-id="fc69f-109">At its core, an XML Writer writes one [XML Node](xml-node.md) at a time, but there are additional helper APIs to make writing a sequence of nodes easier.</span></span>


<span data-ttu-id="fc69f-110">Sono supportati i tipi di output del writer seguenti:</span><span class="sxs-lookup"><span data-stu-id="fc69f-110">The following types of writer output are supported:</span></span>

-   [<span data-ttu-id="fc69f-111">**Un buffer in memoria di byte codificati**</span><span class="sxs-lookup"><span data-stu-id="fc69f-111">**An in-memory buffer of encoded bytes**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_buffer_output)
-   [<span data-ttu-id="fc69f-112">**Un flusso**</span><span class="sxs-lookup"><span data-stu-id="fc69f-112">**A stream**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_stream_output)
-   <span data-ttu-id="fc69f-113">Un [buffer XML](xml-buffer.md)</span><span class="sxs-lookup"><span data-stu-id="fc69f-113">An [XML Buffer](xml-buffer.md)</span></span>

<span data-ttu-id="fc69f-114">Con il writer XML vengono utilizzati i callback seguenti:</span><span class="sxs-lookup"><span data-stu-id="fc69f-114">The following callbacks are used with the XML writer:</span></span>

-   [<span data-ttu-id="fc69f-115">**\_ \_ callback stringa dinamica \_ WS**</span><span class="sxs-lookup"><span data-stu-id="fc69f-115">**WS\_DYNAMIC\_STRING\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_dynamic_string_callback)
-   [<span data-ttu-id="fc69f-116">**CALLBACK di WS \_ pull \_ byte \_**</span><span class="sxs-lookup"><span data-stu-id="fc69f-116">**WS\_PULL\_BYTES\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_pull_bytes_callback)
-   [<span data-ttu-id="fc69f-117">**CALLBACK di WS \_ push \_ bytes \_**</span><span class="sxs-lookup"><span data-stu-id="fc69f-117">**WS\_PUSH\_BYTES\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_push_bytes_callback)
-   [<span data-ttu-id="fc69f-118">**\_callback WS Write \_**</span><span class="sxs-lookup"><span data-stu-id="fc69f-118">**WS\_WRITE\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_write_callback)

<span data-ttu-id="fc69f-119">Con il writer XML vengono utilizzate le enumerazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="fc69f-119">The following enumerations are used with the XML writer:</span></span>

-   [<span data-ttu-id="fc69f-120">**\_set di caratteri WS**</span><span class="sxs-lookup"><span data-stu-id="fc69f-120">**WS\_CHARSET**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_charset)
-   [<span data-ttu-id="fc69f-121">**\_tipo di codifica WS XML \_ writer \_ \_**</span><span class="sxs-lookup"><span data-stu-id="fc69f-121">**WS\_XML\_WRITER\_ENCODING\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_writer_encoding_type)
-   [<span data-ttu-id="fc69f-122">**\_tipo di \_ output del writer XML \_ WS \_**</span><span class="sxs-lookup"><span data-stu-id="fc69f-122">**WS\_XML\_WRITER\_OUTPUT\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_writer_output_type)
-   [<span data-ttu-id="fc69f-123">**\_ID della \_ proprietà del writer XML \_ WS \_**</span><span class="sxs-lookup"><span data-stu-id="fc69f-123">**WS\_XML\_WRITER\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_writer_property_id)

<span data-ttu-id="fc69f-124">Con il writer XML vengono utilizzate le funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="fc69f-124">The following functions are used with the XML writer:</span></span>

-   [<span data-ttu-id="fc69f-125">**WsCopyNode**</span><span class="sxs-lookup"><span data-stu-id="fc69f-125">**WsCopyNode**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscopynode)
-   [<span data-ttu-id="fc69f-126">**WsCreateWriter**</span><span class="sxs-lookup"><span data-stu-id="fc69f-126">**WsCreateWriter**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscreatewriter)
-   [<span data-ttu-id="fc69f-127">**WsFlushWriter**</span><span class="sxs-lookup"><span data-stu-id="fc69f-127">**WsFlushWriter**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsflushwriter)
-   [<span data-ttu-id="fc69f-128">**WsFreeWriter**</span><span class="sxs-lookup"><span data-stu-id="fc69f-128">**WsFreeWriter**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsfreewriter)
-   [<span data-ttu-id="fc69f-129">**WsGetPrefixFromNamespace**</span><span class="sxs-lookup"><span data-stu-id="fc69f-129">**WsGetPrefixFromNamespace**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetprefixfromnamespace)
-   [<span data-ttu-id="fc69f-130">**WsGetWriterPosition**</span><span class="sxs-lookup"><span data-stu-id="fc69f-130">**WsGetWriterPosition**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterposition)
-   [<span data-ttu-id="fc69f-131">**WsGetWriterProperty**</span><span class="sxs-lookup"><span data-stu-id="fc69f-131">**WsGetWriterProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterproperty)
-   [<span data-ttu-id="fc69f-132">**WsMoveWriter**</span><span class="sxs-lookup"><span data-stu-id="fc69f-132">**WsMoveWriter**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsmovewriter)
-   [<span data-ttu-id="fc69f-133">**WsPullBytes**</span><span class="sxs-lookup"><span data-stu-id="fc69f-133">**WsPullBytes**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wspullbytes)
-   [<span data-ttu-id="fc69f-134">**WsPushBytes**</span><span class="sxs-lookup"><span data-stu-id="fc69f-134">**WsPushBytes**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wspushbytes)
-   [<span data-ttu-id="fc69f-135">**WsSetOutput**</span><span class="sxs-lookup"><span data-stu-id="fc69f-135">**WsSetOutput**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wssetoutput)
-   [<span data-ttu-id="fc69f-136">**WsSetOutputToBuffer**</span><span class="sxs-lookup"><span data-stu-id="fc69f-136">**WsSetOutputToBuffer**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wssetoutputtobuffer)
-   [<span data-ttu-id="fc69f-137">**WsSetWriterPosition**</span><span class="sxs-lookup"><span data-stu-id="fc69f-137">**WsSetWriterPosition**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wssetwriterposition)
-   [<span data-ttu-id="fc69f-138">**WsWriteArray**</span><span class="sxs-lookup"><span data-stu-id="fc69f-138">**WsWriteArray**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritearray)
-   [<span data-ttu-id="fc69f-139">**WsWriteBytes**</span><span class="sxs-lookup"><span data-stu-id="fc69f-139">**WsWriteBytes**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritebytes)
-   [<span data-ttu-id="fc69f-140">**WsWriteChars**</span><span class="sxs-lookup"><span data-stu-id="fc69f-140">**WsWriteChars**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritechars)
-   [<span data-ttu-id="fc69f-141">**WsWriteCharsUtf8**</span><span class="sxs-lookup"><span data-stu-id="fc69f-141">**WsWriteCharsUtf8**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritecharsutf8)
-   [<span data-ttu-id="fc69f-142">**WsWriteEndAttribute**</span><span class="sxs-lookup"><span data-stu-id="fc69f-142">**WsWriteEndAttribute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswriteendattribute)
-   [<span data-ttu-id="fc69f-143">**WsWriteEndCData**</span><span class="sxs-lookup"><span data-stu-id="fc69f-143">**WsWriteEndCData**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswriteendcdata)
-   [<span data-ttu-id="fc69f-144">**WsWriteEndElement**</span><span class="sxs-lookup"><span data-stu-id="fc69f-144">**WsWriteEndElement**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswriteendelement)
-   [<span data-ttu-id="fc69f-145">**WsWriteNode**</span><span class="sxs-lookup"><span data-stu-id="fc69f-145">**WsWriteNode**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritenode)
-   [<span data-ttu-id="fc69f-146">**WsWriteQualifiedName**</span><span class="sxs-lookup"><span data-stu-id="fc69f-146">**WsWriteQualifiedName**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritequalifiedname)
-   [<span data-ttu-id="fc69f-147">**WsWriteStartAttribute**</span><span class="sxs-lookup"><span data-stu-id="fc69f-147">**WsWriteStartAttribute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritestartattribute)
-   [<span data-ttu-id="fc69f-148">**WsWriteStartCData**</span><span class="sxs-lookup"><span data-stu-id="fc69f-148">**WsWriteStartCData**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritestartcdata)
-   [<span data-ttu-id="fc69f-149">**WsWriteStartElement**</span><span class="sxs-lookup"><span data-stu-id="fc69f-149">**WsWriteStartElement**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritestartelement)
-   [<span data-ttu-id="fc69f-150">**WsWriteText**</span><span class="sxs-lookup"><span data-stu-id="fc69f-150">**WsWriteText**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritetext)
-   [<span data-ttu-id="fc69f-151">**WsWriteValue**</span><span class="sxs-lookup"><span data-stu-id="fc69f-151">**WsWriteValue**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritevalue)
-   [<span data-ttu-id="fc69f-152">**WsWriteXmlnsAttribute**</span><span class="sxs-lookup"><span data-stu-id="fc69f-152">**WsWriteXmlnsAttribute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritexmlnsattribute)

<span data-ttu-id="fc69f-153">Il seguente handle viene utilizzato con il writer XML:</span><span class="sxs-lookup"><span data-stu-id="fc69f-153">The following handle is used with the XML writer:</span></span>

-   [<span data-ttu-id="fc69f-154">\_writer XML \_ WS</span><span class="sxs-lookup"><span data-stu-id="fc69f-154">WS\_XML\_WRITER</span></span>](ws-xml-writer.md)

<span data-ttu-id="fc69f-155">Con il writer XML vengono utilizzate le strutture seguenti:</span><span class="sxs-lookup"><span data-stu-id="fc69f-155">The following structures are used with the XML writer:</span></span>

-   [<span data-ttu-id="fc69f-156">**\_ \_ \_ codifica binaria WS writer XML \_**</span><span class="sxs-lookup"><span data-stu-id="fc69f-156">**WS\_XML\_WRITER\_BINARY\_ENCODING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_binary_encoding)
-   [<span data-ttu-id="fc69f-157">**\_ \_ output buffer del writer XML \_ WS \_**</span><span class="sxs-lookup"><span data-stu-id="fc69f-157">**WS\_XML\_WRITER\_BUFFER\_OUTPUT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_buffer_output)
-   [<span data-ttu-id="fc69f-158">**\_codifica WS XML \_ writer \_**</span><span class="sxs-lookup"><span data-stu-id="fc69f-158">**WS\_XML\_WRITER\_ENCODING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_encoding)
-   [<span data-ttu-id="fc69f-159">**\_ \_ codifica MTOM del writer XML \_ WS \_**</span><span class="sxs-lookup"><span data-stu-id="fc69f-159">**WS\_XML\_WRITER\_MTOM\_ENCODING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_mtom_encoding)
-   [<span data-ttu-id="fc69f-160">**\_output del \_ writer \_ XML WS**</span><span class="sxs-lookup"><span data-stu-id="fc69f-160">**WS\_XML\_WRITER\_OUTPUT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_output)
-   [<span data-ttu-id="fc69f-161">**\_proprietà del \_ writer \_ XML WS**</span><span class="sxs-lookup"><span data-stu-id="fc69f-161">**WS\_XML\_WRITER\_PROPERTIES**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_properties)
-   [<span data-ttu-id="fc69f-162">**WS \_ - \_ writer XML ( \_ proprietà)**</span><span class="sxs-lookup"><span data-stu-id="fc69f-162">**WS\_XML\_WRITER\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_property)
-   [<span data-ttu-id="fc69f-163">**\_output del \_ flusso del writer XML \_ WS \_**</span><span class="sxs-lookup"><span data-stu-id="fc69f-163">**WS\_XML\_WRITER\_STREAM\_OUTPUT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_stream_output)
-   [<span data-ttu-id="fc69f-164">**\_ \_ \_ codifica testo WS XML \_ writer**</span><span class="sxs-lookup"><span data-stu-id="fc69f-164">**WS\_XML\_WRITER\_TEXT\_ENCODING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_text_encoding)

 

 




