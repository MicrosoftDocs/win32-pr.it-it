---
title: Canonizzazione XML
description: La canonizzazione XML risolve il problema della conversione di un set di nodi XML in byte in modo che le modifiche semplici apportate al codice XML , ad esempio la modifica dell'ordine degli attributi in un elemento, non modificheranno il formato di byte risultante.
ms.assetid: a64303a1-efc4-4c91-ab8d-3e389a655b3e
keywords:
- Xml Canonicalization Web Services for Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8db77e449c4e3d6ee5f6e2cb474c84a6b1161a4fee87c35d01d278882b178cc7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082985"
---
# <a name="xml-canonicalization"></a>Canonizzazione XML

La canonizzazione XML risolve il problema della conversione di un set di nodi XML in byte in modo che le modifiche semplici apportate al codice XML , ad esempio la modifica dell'ordine degli attributi in un elemento, non modificheranno il formato di byte risultante. I byte ottenuti dalla canonizzazione vengono comunemente usati per generare una firma crittografica sul contenuto XML.


Gli algoritmi di canonizzazione XML di uso comune standardizzano gli aspetti seguenti:

-   Codifica dei caratteri (UTF-8 senza preambolo)
-   Avanzamento riga e altri formati di carattere
-   Ordine degli attributi in un elemento
-   Modulo di elemento vuoto
-   Rendering delle dichiarazioni dello spazio dei nomi

Le API [**WsStartReaderCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsstartreadercanonicalization) e [**WsEndReaderCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsendreadercanonicalization) forniscono la funzionalità di canonizzazione XML durante la lettura di un documento.

Le API [**WsStartWriterCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsstartwritercanonicalization) e [**WsEndWriterCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsendwritercanonicalization) forniscono la funzionalità di canonizzazione XML durante la scrittura di un documento.

Le enumerazioni seguenti vengono usate con la canonizzazione:

-   [**ALGORITMO \_ DI \_ CANONIZZAZIONE XML WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_canonicalization_algorithm)
-   [**ID PROPRIETÀ \_ \_ DI CANONIZZAZIONE XML \_ WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_canonicalization_property_id)

Con la canonizzazione vengono usate le funzioni seguenti:

-   [**WsEndReaderCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsendreadercanonicalization)
-   [**WsEndWriterCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsendwritercanonicalization)
-   [**WsStartReaderCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsstartreadercanonicalization)
-   [**WsStartWriterCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsstartwritercanonicalization)

Le strutture seguenti vengono usate con la canonizzazione:

-   [**PREFISSI \_ INCLUSIVI DI CANONIZZAZIONE XML \_ \_ \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_canonicalization_inclusive_prefixes)
-   [**PROPRIETÀ \_ DI \_ CANONIZZAZIONE XML WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_canonicalization_property)

 

 




