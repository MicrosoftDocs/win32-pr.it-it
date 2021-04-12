---
title: Serializzazione
description: La serializzazione è il processo di scrittura di valori in strutture di dati C (struct, matrici e valori primitivi) come elemento XML. La deserializzazione è il processo inverso.
ms.assetid: aa092156-30ae-4f8a-baa2-450f38a78153
keywords:
- Servizi Web di serializzazione per Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63f986c6cec9a035424aaafe1c51f4dc0d3ee014
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/12/2021
ms.locfileid: "104234454"
---
# <a name="serialization"></a><span data-ttu-id="bca23-107">Serializzazione</span><span class="sxs-lookup"><span data-stu-id="bca23-107">Serialization</span></span>

<span data-ttu-id="bca23-108">La serializzazione è il processo di scrittura di valori in strutture di dati C (struct, matrici e valori primitivi) come elemento XML.</span><span class="sxs-lookup"><span data-stu-id="bca23-108">Serialization is the process of writing values in C data structures (structs, arrays, and primitive values) as an XML element.</span></span> <span data-ttu-id="bca23-109">La deserializzazione è il processo inverso.</span><span class="sxs-lookup"><span data-stu-id="bca23-109">Deserialization is the reverse process.</span></span>


<span data-ttu-id="bca23-110">La serializzazione è il processo di scrittura di valori in strutture di dati C (strutture, matrici e valori primitivi) come elemento XML.</span><span class="sxs-lookup"><span data-stu-id="bca23-110">Serialization is the process of writing values in C data structures (structures, arrays, and primitive values) as an XML element.</span></span> <span data-ttu-id="bca23-111">La deserializzazione è il processo inverso.</span><span class="sxs-lookup"><span data-stu-id="bca23-111">Deserialization is the reverse process.</span></span>

<span data-ttu-id="bca23-112">Entrambi i processi si basano su una descrizione del mapping tra le strutture di dati C e il codice XML.</span><span class="sxs-lookup"><span data-stu-id="bca23-112">Both processes rely on a description of the mapping between the C data structures and the XML.</span></span>

![Diagramma che illustra in che modo la serializzazione e la deserializzazione si basano su una descrizione del mapping tra le strutture di dati C e il codice XML.](images/xmlmapping.png)

<span data-ttu-id="bca23-114">Per serializzare un valore, l'applicazione chiama [**WsWriteElement**](/windows/desktop/api/WebServices/nf-webservices-wswriteelement), [**WsWriteAttribute**](/windows/desktop/api/WebServices/nf-webservices-wswriteattribute) o [**WsWriteType**](/windows/desktop/api/WebServices/nf-webservices-wswritetype).</span><span class="sxs-lookup"><span data-stu-id="bca23-114">To serialize a value, the application calls [**WsWriteElement**](/windows/desktop/api/WebServices/nf-webservices-wswriteelement), [**WsWriteAttribute**](/windows/desktop/api/WebServices/nf-webservices-wswriteattribute) or [**WsWriteType**](/windows/desktop/api/WebServices/nf-webservices-wswritetype).</span></span>

<span data-ttu-id="bca23-115">Per deserializzare un valore, l'applicazione chiama [**WsReadElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadelement), [**WsReadAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsreadattribute) o [**WsReadType**](/windows/desktop/api/WebServices/nf-webservices-wsreadtype).</span><span class="sxs-lookup"><span data-stu-id="bca23-115">To deserialize a value, the application calls [**WsReadElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadelement), [**WsReadAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsreadattribute) or [**WsReadType**](/windows/desktop/api/WebServices/nf-webservices-wsreadtype).</span></span>

## <a name="security"></a><span data-ttu-id="bca23-116">Sicurezza</span><span class="sxs-lookup"><span data-stu-id="bca23-116">Security</span></span>

<span data-ttu-id="bca23-117">Il [lettore XML](xml-reader.md) viene utilizzato nel processo di deserializzazione.</span><span class="sxs-lookup"><span data-stu-id="bca23-117">[XML Reader](xml-reader.md) is used in deserialization process.</span></span> <span data-ttu-id="bca23-118">Per informazioni sulla sicurezza correlate a XML, vedere la sezione sicurezza in XML Reader.</span><span class="sxs-lookup"><span data-stu-id="bca23-118">Refer to the security section in XML Reader for XML related security information.</span></span>

<span data-ttu-id="bca23-119">Il deserializzatore continua a deserializzare i dati fino al completamento della lettura dell'elemento da deserializzare.</span><span class="sxs-lookup"><span data-stu-id="bca23-119">The deserializer continues to deserialize data until it has completed reading the element being deserialized.</span></span> <span data-ttu-id="bca23-120">Il processo di deserializzazione non riesce quando viene rilevato un documento XML non conforme alla descrizione dei dati da deserializzare.</span><span class="sxs-lookup"><span data-stu-id="bca23-120">Deserialization process fails when it encounter any XML document that does not conform to the description of the data being deserialized.</span></span> <span data-ttu-id="bca23-121">A questo punto, il lettore XML utilizzato diventa non valido e viene restituito un errore.</span><span class="sxs-lookup"><span data-stu-id="bca23-121">At that point XML reader being used becomes invalid, and an error is returned.</span></span>

<span data-ttu-id="bca23-122">Per impostazione predefinita, la deserializzazione è rigida.</span><span class="sxs-lookup"><span data-stu-id="bca23-122">By default deserialization is strict.</span></span> <span data-ttu-id="bca23-123">Alcune condizioni che provocano un errore di deserializzazione includono:</span><span class="sxs-lookup"><span data-stu-id="bca23-123">Some conditions that cause deserialization to fail include but not limited to:</span></span>

-   <span data-ttu-id="bca23-124">Elementi previsti mancanti</span><span class="sxs-lookup"><span data-stu-id="bca23-124">Expected elements is missing</span></span>
-   <span data-ttu-id="bca23-125">Campi di elementi imprevisti visualizzati tra gli elementi obbligatori</span><span class="sxs-lookup"><span data-stu-id="bca23-125">Unexpected element fields appear between required elements</span></span>
-   <span data-ttu-id="bca23-126">Contenuto dell'elemento aggiuntivo dopo i campi obbligatori, a meno che l' **WS_STRUCT_IGNORE_TRAILING_ELEMENT_CONTENT**</span><span class="sxs-lookup"><span data-stu-id="bca23-126">Extra element content after required fields, unless the **WS_STRUCT_IGNORE_TRAILING_ELEMENT_CONTENT**</span></span>
-   <span data-ttu-id="bca23-127">Attributi imprevisti, a meno che non sia specificato un flag [**WS \_ struct \_ Ignore \_ \_ attributi non gestiti**](https://msdn.microsoft.com/library/Dd323454(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="bca23-127">Unexpected attributes, unless [**WS\_STRUCT\_IGNORE\_UNHANDLED\_ATTRIBUTES**](https://msdn.microsoft.com/library/Dd323454(v=VS.85).aspx) flag is specified</span></span>
-   <span data-ttu-id="bca23-128">Valore del tipo di dati imprevisto non compreso nell'intervallo specificato</span><span class="sxs-lookup"><span data-stu-id="bca23-128">Unexpected data type value that is out of specified range</span></span>
-   <span data-ttu-id="bca23-129">Il numero di elementi ripetuti non è compreso nell'intervallo specificato</span><span class="sxs-lookup"><span data-stu-id="bca23-129">Count of repeating element is out of the specified range</span></span>

<span data-ttu-id="bca23-130">La serializzazione di grandi quantità di dati può causare un'allocazione eccessiva della memoria e causare attacchi di tipo Denial of Service.</span><span class="sxs-lookup"><span data-stu-id="bca23-130">Serializing large amount of data might cause excessive memory allocation and can cause denial of service attack.</span></span> <span data-ttu-id="bca23-131">L'utente che deserializza i dati deve specificare un oggetto heap per allocare i dati e l'utente può usare il limite di allocazione dell'heap per evitare attacchi di allocazione di memoria.</span><span class="sxs-lookup"><span data-stu-id="bca23-131">The user that is deserializing data must specify a Heap object to allocate the data, and the user can use the heap allocation limit to prevent memory allocation attack.</span></span>

<span data-ttu-id="bca23-132">Supporto dell'intervallo per i tipi di dati, inclusa la lunghezza massima per la stringa, il numero massimo di elementi nella matrice e così via. consente all'utente di controllare la dimensione massima per tipi di dati diversi.</span><span class="sxs-lookup"><span data-stu-id="bca23-132">Range support for data types, including max length for string, max element count in array, etc. allows the user to control the maximum size for different data types.</span></span> <span data-ttu-id="bca23-133">L'utente può specificare un intervallo nella descrizione dei dati o nello schema per limitare le dimensioni massime dei dati diversi.</span><span class="sxs-lookup"><span data-stu-id="bca23-133">User can specify range in data description or schema to limit the maximum size of different data.</span></span>

<span data-ttu-id="bca23-134">Un valore stringa contenente uno zero incorporato è supportato nei formati di trasmissione (testo, binario, MTOM).</span><span class="sxs-lookup"><span data-stu-id="bca23-134">A string value containing an embedded zero is supported in the wire formats (text, binary, MTOM).</span></span> <span data-ttu-id="bca23-135">Quando si deserializza una stringa con uno zero incorporato, l'utente deve usare una stringa calcolata (WS \_ String) in modo che lo zero non confonderà il calcolo della lunghezza della stringa.</span><span class="sxs-lookup"><span data-stu-id="bca23-135">When deserializing a string with an embedded zero, the user should use a counted string (WS\_STRING) so the zero will not confuse the calculation of the length of the string.</span></span> <span data-ttu-id="bca23-136">Se un valore stringa contenente uno zero incorporato viene deserializzato in un campo che prevede una stringa con terminazione zero, viene restituito un errore e la deserializzazione ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="bca23-136">If a string value containing an embedded zero is deserialized into a field that is expecting a zero-terminated string, an error is returned, and deserialization fails.</span></span> <span data-ttu-id="bca23-137">Se si usa WSUTIL per generare le descrizioni dei dati, \_ è necessario usare l'opzione/String: WS String se è prevista una stringa con zero incorporato.</span><span class="sxs-lookup"><span data-stu-id="bca23-137">If wsutil is used to generate data descriptions, /string:WS\_STRING option should be used if string with embedded zero is expected.</span></span>

<span data-ttu-id="bca23-138">Con la serializzazione vengono usati i callback seguenti:</span><span class="sxs-lookup"><span data-stu-id="bca23-138">The following callbacks are used with serialization:</span></span>

-   [<span data-ttu-id="bca23-139">**\_callback di \_ confronto \_ durata WS**</span><span class="sxs-lookup"><span data-stu-id="bca23-139">**WS\_DURATION\_COMPARISON\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_duration_comparison_callback)
-   [<span data-ttu-id="bca23-140">**\_callback del \_ tipo di lettura WS \_**</span><span class="sxs-lookup"><span data-stu-id="bca23-140">**WS\_READ\_TYPE\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_read_type_callback)
-   [<span data-ttu-id="bca23-141">**\_callback di \_ tipo WS Write \_**</span><span class="sxs-lookup"><span data-stu-id="bca23-141">**WS\_WRITE\_TYPE\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_write_type_callback)

<span data-ttu-id="bca23-142">Con la serializzazione vengono usate le enumerazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="bca23-142">The following enumerations are used with serialization:</span></span>

-   [<span data-ttu-id="bca23-143">**\_mapping dei campi WS \_**</span><span class="sxs-lookup"><span data-stu-id="bca23-143">**WS\_FIELD\_MAPPING**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_field_mapping)
-   [<span data-ttu-id="bca23-144">**\_Opzioni campo \_ WS**</span><span class="sxs-lookup"><span data-stu-id="bca23-144">**WS\_FIELD\_OPTIONS**</span></span>](/windows/win32/api/webservices/ne-webservices-ws_xml_reader_encoding_type)
-   [<span data-ttu-id="bca23-145">**\_opzione di lettura WS \_**</span><span class="sxs-lookup"><span data-stu-id="bca23-145">**WS\_READ\_OPTION**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_read_option)
-   [<span data-ttu-id="bca23-146">**\_tipo WS**</span><span class="sxs-lookup"><span data-stu-id="bca23-146">**WS\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_type)
-   [<span data-ttu-id="bca23-147">**\_mapping del tipo WS \_**</span><span class="sxs-lookup"><span data-stu-id="bca23-147">**WS\_TYPE\_MAPPING**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_type_mapping)
-   [<span data-ttu-id="bca23-148">**\_opzione WS Write \_**</span><span class="sxs-lookup"><span data-stu-id="bca23-148">**WS\_WRITE\_OPTION**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_write_option)

<span data-ttu-id="bca23-149">Con la serializzazione vengono usate le funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="bca23-149">The following functions are used with serialization:</span></span>

-   [<span data-ttu-id="bca23-150">**WsReadAttribute**</span><span class="sxs-lookup"><span data-stu-id="bca23-150">**WsReadAttribute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadattribute)
-   [<span data-ttu-id="bca23-151">**WsReadElement**</span><span class="sxs-lookup"><span data-stu-id="bca23-151">**WsReadElement**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadelement)
-   [<span data-ttu-id="bca23-152">**WsReadType**</span><span class="sxs-lookup"><span data-stu-id="bca23-152">**WsReadType**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadtype)
-   [<span data-ttu-id="bca23-153">**WsWriteAttribute**</span><span class="sxs-lookup"><span data-stu-id="bca23-153">**WsWriteAttribute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswriteattribute)
-   [<span data-ttu-id="bca23-154">**WsWriteElement**</span><span class="sxs-lookup"><span data-stu-id="bca23-154">**WsWriteElement**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswriteelement)
-   [<span data-ttu-id="bca23-155">**WsWriteType**</span><span class="sxs-lookup"><span data-stu-id="bca23-155">**WsWriteType**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritetype)

<span data-ttu-id="bca23-156">Con la serializzazione vengono utilizzate le strutture seguenti:</span><span class="sxs-lookup"><span data-stu-id="bca23-156">The following structures are used with serialization:</span></span>

-   [<span data-ttu-id="bca23-157">**\_Descrizione dell'attributo ws \_**</span><span class="sxs-lookup"><span data-stu-id="bca23-157">**WS\_ATTRIBUTE\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_attribute_description)
-   [<span data-ttu-id="bca23-158">**Descrizione di WS \_ bool \_**</span><span class="sxs-lookup"><span data-stu-id="bca23-158">**WS\_BOOL\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_bool_description)
-   [<span data-ttu-id="bca23-159">**Descrizione di WS \_ byte \_**</span><span class="sxs-lookup"><span data-stu-id="bca23-159">**WS\_BYTES\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_bytes_description)
-   [<span data-ttu-id="bca23-160">**\_ \_ Descrizione matrice WS \_ byte**</span><span class="sxs-lookup"><span data-stu-id="bca23-160">**WS\_BYTE\_ARRAY\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_byte_array_description)
-   [<span data-ttu-id="bca23-161">**\_ \_ Descrizione matrice WS \_ Char**</span><span class="sxs-lookup"><span data-stu-id="bca23-161">**WS\_CHAR\_ARRAY\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_char_array_description)
-   [<span data-ttu-id="bca23-162">**\_Descrizione del \_ tipo \_ personalizzato WS**</span><span class="sxs-lookup"><span data-stu-id="bca23-162">**WS\_CUSTOM\_TYPE\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_custom_type_description)
-   [<span data-ttu-id="bca23-163">**Descrizione di WS \_ DateTime \_**</span><span class="sxs-lookup"><span data-stu-id="bca23-163">**WS\_DATETIME\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_datetime_description)
-   [<span data-ttu-id="bca23-164">**\_Descrizione WS decimale \_**</span><span class="sxs-lookup"><span data-stu-id="bca23-164">**WS\_DECIMAL\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_decimal_description)
-   [<span data-ttu-id="bca23-165">**\_valore predefinito \_ WS**</span><span class="sxs-lookup"><span data-stu-id="bca23-165">**WS\_DEFAULT\_VALUE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_default_value)
-   [<span data-ttu-id="bca23-166">**\_Descrizione doppia \_ WS**</span><span class="sxs-lookup"><span data-stu-id="bca23-166">**WS\_DOUBLE\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_double_description)
-   [<span data-ttu-id="bca23-167">**\_Descrizione durata \_ WS**</span><span class="sxs-lookup"><span data-stu-id="bca23-167">**WS\_DURATION\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_duration_description)
-   [<span data-ttu-id="bca23-168">**\_Descrizione dell'elemento WS \_**</span><span class="sxs-lookup"><span data-stu-id="bca23-168">**WS\_ELEMENT\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_element_description)
-   [<span data-ttu-id="bca23-169">**\_ \_ Descrizione indirizzo endpoint \_ WS**</span><span class="sxs-lookup"><span data-stu-id="bca23-169">**WS\_ENDPOINT\_ADDRESS\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address_description)
-   [<span data-ttu-id="bca23-170">**Descrizione di WS \_ enum \_**</span><span class="sxs-lookup"><span data-stu-id="bca23-170">**WS\_ENUM\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_enum_description)
-   [<span data-ttu-id="bca23-171">**valore di WS \_ enum \_**</span><span class="sxs-lookup"><span data-stu-id="bca23-171">**WS\_ENUM\_VALUE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_enum_value)
-   [<span data-ttu-id="bca23-172">**\_Descrizione errore \_ WS**</span><span class="sxs-lookup"><span data-stu-id="bca23-172">**WS\_FAULT\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_fault_description)
-   [<span data-ttu-id="bca23-173">**\_Descrizione campo \_ WS**</span><span class="sxs-lookup"><span data-stu-id="bca23-173">**WS\_FIELD\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_field_description)
-   [<span data-ttu-id="bca23-174">**\_Descrizione WS float \_**</span><span class="sxs-lookup"><span data-stu-id="bca23-174">**WS\_FLOAT\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_float_description)
-   [<span data-ttu-id="bca23-175">**Descrizione di WS \_ GUID \_**</span><span class="sxs-lookup"><span data-stu-id="bca23-175">**WS\_GUID\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_guid_description)
-   [<span data-ttu-id="bca23-176">**\_Descrizione WS Int16 \_**</span><span class="sxs-lookup"><span data-stu-id="bca23-176">**WS\_INT16\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_int16_description)
-   [<span data-ttu-id="bca23-177">**Descrizione di WS \_ Int32 \_**</span><span class="sxs-lookup"><span data-stu-id="bca23-177">**WS\_INT32\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_int32_description)
-   [<span data-ttu-id="bca23-178">**\_Descrizione WS Int64 \_**</span><span class="sxs-lookup"><span data-stu-id="bca23-178">**WS\_INT64\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_int64_description)
-   [<span data-ttu-id="bca23-179">**Descrizione di WS \_ int8 \_**</span><span class="sxs-lookup"><span data-stu-id="bca23-179">**WS\_INT8\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_int8_description)
-   [<span data-ttu-id="bca23-180">**\_intervallo elemento \_ WS**</span><span class="sxs-lookup"><span data-stu-id="bca23-180">**WS\_ITEM\_RANGE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_item_range)
-   [<span data-ttu-id="bca23-181">**\_Descrizione della stringa WS \_**</span><span class="sxs-lookup"><span data-stu-id="bca23-181">**WS\_STRING\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_string_description)
-   [<span data-ttu-id="bca23-182">**\_Descrizione struct \_ WS**</span><span class="sxs-lookup"><span data-stu-id="bca23-182">**WS\_STRUCT\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_struct_description)
-   [<span data-ttu-id="bca23-183">**Descrizione di WS \_ TIMESPAN \_**</span><span class="sxs-lookup"><span data-stu-id="bca23-183">**WS\_TIMESPAN\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_timespan_description)
-   [<span data-ttu-id="bca23-184">**\_Descrizione WS UInt16 \_**</span><span class="sxs-lookup"><span data-stu-id="bca23-184">**WS\_UINT16\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_uint16_description)
-   [<span data-ttu-id="bca23-185">**\_Descrizione WS UInt32 \_**</span><span class="sxs-lookup"><span data-stu-id="bca23-185">**WS\_UINT32\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_uint32_description)
-   [<span data-ttu-id="bca23-186">**\_Descrizione WS UInt64 \_**</span><span class="sxs-lookup"><span data-stu-id="bca23-186">**WS\_UINT64\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_uint64_description)
-   [<span data-ttu-id="bca23-187">**Descrizione di WS \_ Uint8 \_**</span><span class="sxs-lookup"><span data-stu-id="bca23-187">**WS\_UINT8\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_uint8_description)
-   [<span data-ttu-id="bca23-188">**Descrizione di WS \_ Union \_**</span><span class="sxs-lookup"><span data-stu-id="bca23-188">**WS\_UNION\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_union_description)
-   [<span data-ttu-id="bca23-189">**\_ \_ Descrizione campo WS \_ Union**</span><span class="sxs-lookup"><span data-stu-id="bca23-189">**WS\_UNION\_FIELD\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_union_field_description)
-   [<span data-ttu-id="bca23-190">**\_ \_ Descrizione ID WS \_ Unique**</span><span class="sxs-lookup"><span data-stu-id="bca23-190">**WS\_UNIQUE\_ID\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_unique_id_description)
-   [<span data-ttu-id="bca23-191">**\_ \_ Descrizione matrice WS \_ UTF8**</span><span class="sxs-lookup"><span data-stu-id="bca23-191">**WS\_UTF8\_ARRAY\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_utf8_array_description)
-   [<span data-ttu-id="bca23-192">**\_Descrizione WS void \_**</span><span class="sxs-lookup"><span data-stu-id="bca23-192">**WS\_VOID\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_void_description)
-   [<span data-ttu-id="bca23-193">**Descrizione di WS \_ WSZ \_**</span><span class="sxs-lookup"><span data-stu-id="bca23-193">**WS\_WSZ\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_wsz_description)
-   [<span data-ttu-id="bca23-194">**Descrizione di WS \_ XML \_ QName \_**</span><span class="sxs-lookup"><span data-stu-id="bca23-194">**WS\_XML\_QNAME\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_qname_description)
-   [<span data-ttu-id="bca23-195">**\_ \_ Descrizione stringa WS \_ XML**</span><span class="sxs-lookup"><span data-stu-id="bca23-195">**WS\_XML\_STRING\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string_description)

 

 




