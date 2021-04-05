---
title: Canonizzazione XML
description: La canonizzazione XML risolve il problema della conversione di un set di nodi XML in byte in modo tale che le modifiche banali apportate al codice XML, ad esempio la modifica dell'ordine degli attributi in un elemento, non modifichino il formato di byte risultante.
ms.assetid: a64303a1-efc4-4c91-ab8d-3e389a655b3e
keywords:
- Servizi Web per la canonizzazione XML per Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bab8b1aa00b99b604276a479f1a47aacb5bd8b1e
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "103873129"
---
# <a name="xml-canonicalization"></a>Canonizzazione XML

La canonizzazione XML risolve il problema della conversione di un set di nodi XML in byte in modo tale che le modifiche banali apportate al codice XML, ad esempio la modifica dell'ordine degli attributi in un elemento, non modifichino il formato di byte risultante. I byte ottenuti dalla canonizzazione vengono comunemente utilizzati per generare una firma crittografica sul contenuto XML.


Gli algoritmi di canonizzazione XML di uso comune standardizzano gli aspetti seguenti:

-   Codifica di caratteri (UTF-8 senza preambolo)
-   Avanzamento riga e altri formati carattere
-   Ordine degli attributi in un elemento
-   Form elemento vuoto
-   Rendering delle dichiarazioni dello spazio dei nomi

Le API [**WsStartReaderCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsstartreadercanonicalization) e [**WsEndReaderCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsendreadercanonicalization) forniscono la funzionalità di canonizzazione XML durante la lettura di un documento.

Le API [**WsStartWriterCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsstartwritercanonicalization) e [**WsEndWriterCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsendwritercanonicalization) forniscono la funzionalità di canonizzazione XML durante la scrittura di un documento.

Con la canonizzazione vengono usate le enumerazioni seguenti:

-   [**\_algoritmo di \_ canonizzazione WS XML \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_canonicalization_algorithm)
-   [**\_ID della \_ proprietà di canonizzazione di WS XML \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_canonicalization_property_id)

Con la canonizzazione vengono usate le funzioni seguenti:

-   [**WsEndReaderCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsendreadercanonicalization)
-   [**WsEndWriterCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsendwritercanonicalization)
-   [**WsStartReaderCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsstartreadercanonicalization)
-   [**WsStartWriterCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsstartwritercanonicalization)

Con la canonizzazione vengono utilizzate le strutture seguenti:

-   [**\_prefissi \_ inclusivi di canonizzazione WS XML \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_canonicalization_inclusive_prefixes)
-   [**\_proprietà di \_ canonizzazione WS XML \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_canonicalization_property)

 

 




