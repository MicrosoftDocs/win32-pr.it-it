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
# <a name="serialization"></a>Serializzazione

La serializzazione è il processo di scrittura di valori in strutture di dati C (struct, matrici e valori primitivi) come elemento XML. La deserializzazione è il processo inverso.


La serializzazione è il processo di scrittura di valori in strutture di dati C (strutture, matrici e valori primitivi) come elemento XML. La deserializzazione è il processo inverso.

Entrambi i processi si basano su una descrizione del mapping tra le strutture di dati C e il codice XML.

![Diagramma che illustra in che modo la serializzazione e la deserializzazione si basano su una descrizione del mapping tra le strutture di dati C e il codice XML.](images/xmlmapping.png)

Per serializzare un valore, l'applicazione chiama [**WsWriteElement**](/windows/desktop/api/WebServices/nf-webservices-wswriteelement), [**WsWriteAttribute**](/windows/desktop/api/WebServices/nf-webservices-wswriteattribute) o [**WsWriteType**](/windows/desktop/api/WebServices/nf-webservices-wswritetype).

Per deserializzare un valore, l'applicazione chiama [**WsReadElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadelement), [**WsReadAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsreadattribute) o [**WsReadType**](/windows/desktop/api/WebServices/nf-webservices-wsreadtype).

## <a name="security"></a>Sicurezza

Il [lettore XML](xml-reader.md) viene utilizzato nel processo di deserializzazione. Per informazioni sulla sicurezza correlate a XML, vedere la sezione sicurezza in XML Reader.

Il deserializzatore continua a deserializzare i dati fino al completamento della lettura dell'elemento da deserializzare. Il processo di deserializzazione non riesce quando viene rilevato un documento XML non conforme alla descrizione dei dati da deserializzare. A questo punto, il lettore XML utilizzato diventa non valido e viene restituito un errore.

Per impostazione predefinita, la deserializzazione è rigida. Alcune condizioni che provocano un errore di deserializzazione includono:

-   Elementi previsti mancanti
-   Campi di elementi imprevisti visualizzati tra gli elementi obbligatori
-   Contenuto dell'elemento aggiuntivo dopo i campi obbligatori, a meno che l' **WS_STRUCT_IGNORE_TRAILING_ELEMENT_CONTENT**
-   Attributi imprevisti, a meno che non sia specificato un flag [**WS \_ struct \_ Ignore \_ \_ attributi non gestiti**](https://msdn.microsoft.com/library/Dd323454(v=VS.85).aspx)
-   Valore del tipo di dati imprevisto non compreso nell'intervallo specificato
-   Il numero di elementi ripetuti non è compreso nell'intervallo specificato

La serializzazione di grandi quantità di dati può causare un'allocazione eccessiva della memoria e causare attacchi di tipo Denial of Service. L'utente che deserializza i dati deve specificare un oggetto heap per allocare i dati e l'utente può usare il limite di allocazione dell'heap per evitare attacchi di allocazione di memoria.

Supporto dell'intervallo per i tipi di dati, inclusa la lunghezza massima per la stringa, il numero massimo di elementi nella matrice e così via. consente all'utente di controllare la dimensione massima per tipi di dati diversi. L'utente può specificare un intervallo nella descrizione dei dati o nello schema per limitare le dimensioni massime dei dati diversi.

Un valore stringa contenente uno zero incorporato è supportato nei formati di trasmissione (testo, binario, MTOM). Quando si deserializza una stringa con uno zero incorporato, l'utente deve usare una stringa calcolata (WS \_ String) in modo che lo zero non confonderà il calcolo della lunghezza della stringa. Se un valore stringa contenente uno zero incorporato viene deserializzato in un campo che prevede una stringa con terminazione zero, viene restituito un errore e la deserializzazione ha esito negativo. Se si usa WSUTIL per generare le descrizioni dei dati, \_ è necessario usare l'opzione/String: WS String se è prevista una stringa con zero incorporato.

Con la serializzazione vengono usati i callback seguenti:

-   [**\_callback di \_ confronto \_ durata WS**](/windows/desktop/api/WebServices/nc-webservices-ws_duration_comparison_callback)
-   [**\_callback del \_ tipo di lettura WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_read_type_callback)
-   [**\_callback di \_ tipo WS Write \_**](/windows/desktop/api/WebServices/nc-webservices-ws_write_type_callback)

Con la serializzazione vengono usate le enumerazioni seguenti:

-   [**\_mapping dei campi WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_field_mapping)
-   [**\_Opzioni campo \_ WS**](/windows/win32/api/webservices/ne-webservices-ws_xml_reader_encoding_type)
-   [**\_opzione di lettura WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_read_option)
-   [**\_tipo WS**](/windows/desktop/api/WebServices/ne-webservices-ws_type)
-   [**\_mapping del tipo WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_type_mapping)
-   [**\_opzione WS Write \_**](/windows/desktop/api/WebServices/ne-webservices-ws_write_option)

Con la serializzazione vengono usate le funzioni seguenti:

-   [**WsReadAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsreadattribute)
-   [**WsReadElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadelement)
-   [**WsReadType**](/windows/desktop/api/WebServices/nf-webservices-wsreadtype)
-   [**WsWriteAttribute**](/windows/desktop/api/WebServices/nf-webservices-wswriteattribute)
-   [**WsWriteElement**](/windows/desktop/api/WebServices/nf-webservices-wswriteelement)
-   [**WsWriteType**](/windows/desktop/api/WebServices/nf-webservices-wswritetype)

Con la serializzazione vengono utilizzate le strutture seguenti:

-   [**\_Descrizione dell'attributo ws \_**](/windows/desktop/api/WebServices/ns-webservices-ws_attribute_description)
-   [**Descrizione di WS \_ bool \_**](/windows/desktop/api/WebServices/ns-webservices-ws_bool_description)
-   [**Descrizione di WS \_ byte \_**](/windows/desktop/api/WebServices/ns-webservices-ws_bytes_description)
-   [**\_ \_ Descrizione matrice WS \_ byte**](/windows/desktop/api/WebServices/ns-webservices-ws_byte_array_description)
-   [**\_ \_ Descrizione matrice WS \_ Char**](/windows/desktop/api/WebServices/ns-webservices-ws_char_array_description)
-   [**\_Descrizione del \_ tipo \_ personalizzato WS**](/windows/desktop/api/WebServices/ns-webservices-ws_custom_type_description)
-   [**Descrizione di WS \_ DateTime \_**](/windows/desktop/api/WebServices/ns-webservices-ws_datetime_description)
-   [**\_Descrizione WS decimale \_**](/windows/desktop/api/WebServices/ns-webservices-ws_decimal_description)
-   [**\_valore predefinito \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_default_value)
-   [**\_Descrizione doppia \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_double_description)
-   [**\_Descrizione durata \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_duration_description)
-   [**\_Descrizione dell'elemento WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description)
-   [**\_ \_ Descrizione indirizzo endpoint \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address_description)
-   [**Descrizione di WS \_ enum \_**](/windows/desktop/api/WebServices/ns-webservices-ws_enum_description)
-   [**valore di WS \_ enum \_**](/windows/desktop/api/WebServices/ns-webservices-ws_enum_value)
-   [**\_Descrizione errore \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_description)
-   [**\_Descrizione campo \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_field_description)
-   [**\_Descrizione WS float \_**](/windows/desktop/api/WebServices/ns-webservices-ws_float_description)
-   [**Descrizione di WS \_ GUID \_**](/windows/desktop/api/WebServices/ns-webservices-ws_guid_description)
-   [**\_Descrizione WS Int16 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_int16_description)
-   [**Descrizione di WS \_ Int32 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_int32_description)
-   [**\_Descrizione WS Int64 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_int64_description)
-   [**Descrizione di WS \_ int8 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_int8_description)
-   [**\_intervallo elemento \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_item_range)
-   [**\_Descrizione della stringa WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_string_description)
-   [**\_Descrizione struct \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_struct_description)
-   [**Descrizione di WS \_ TIMESPAN \_**](/windows/desktop/api/WebServices/ns-webservices-ws_timespan_description)
-   [**\_Descrizione WS UInt16 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_uint16_description)
-   [**\_Descrizione WS UInt32 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_uint32_description)
-   [**\_Descrizione WS UInt64 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_uint64_description)
-   [**Descrizione di WS \_ Uint8 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_uint8_description)
-   [**Descrizione di WS \_ Union \_**](/windows/desktop/api/WebServices/ns-webservices-ws_union_description)
-   [**\_ \_ Descrizione campo WS \_ Union**](/windows/desktop/api/WebServices/ns-webservices-ws_union_field_description)
-   [**\_ \_ Descrizione ID WS \_ Unique**](/windows/desktop/api/WebServices/ns-webservices-ws_unique_id_description)
-   [**\_ \_ Descrizione matrice WS \_ UTF8**](/windows/desktop/api/WebServices/ns-webservices-ws_utf8_array_description)
-   [**\_Descrizione WS void \_**](/windows/desktop/api/WebServices/ns-webservices-ws_void_description)
-   [**Descrizione di WS \_ WSZ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_wsz_description)
-   [**Descrizione di WS \_ XML \_ QName \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_qname_description)
-   [**\_ \_ Descrizione stringa WS \_ XML**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string_description)

 

 




