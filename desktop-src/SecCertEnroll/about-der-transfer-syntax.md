---
description: L'applicazione di una regola di codifica alle strutture di dati descritte da una sintassi astratta fornisce una sintassi di trasferimento che regola l'organizzazione dei byte in un flusso quando vengono inviati tra computer.
ms.assetid: 674e88f9-4b65-4b42-8c44-d24fc03ae2f3
title: Sintassi di trasferimento DER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6757a22743a2c44abb5ef4c46154a08e425e2b1b7045beaacc7fb4f4f206fed3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118904520"
---
# <a name="der-transfer-syntax"></a>Sintassi di trasferimento DER

L'applicazione di una regola di codifica alle strutture di dati descritte da una sintassi astratta fornisce una sintassi di trasferimento che regola l'organizzazione dei byte in un flusso quando vengono inviati tra computer. La sintassi di trasferimento usata Distinguished Encoding Rules segue sempre un *formato tag, lunghezza,* valore. Il formato viene in genere definito tripletta TLV in cui ogni campo (T, L o V) contiene uno o più byte.

![der type, length, and value (tlv) triplet](images/der-tlv-basic.png)

Il *campo Tag* specifica il tipo di struttura di dati inviata, il campo *Lunghezza* specifica  il numero di byte di contenuto trasferito e il campo Valore contiene il contenuto. Si noti che *il campo Value* può essere una tripletta se contiene un tipo di dati costruito, come illustrato nella figura seguente.

![der tlv triplet recursion](images/der-tlv-recursive.png)

Per informazioni dettagliate sui componenti di una tripletta TLV, vedere gli argomenti seguenti.

-   [Byte tag codificati](about-encoded-tag-bytes.md)
-   [Lunghezza codificata e byte valore](about-encoded-length-and-value-bytes.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi costruiti](about-constructed-types.md)
</dt> <dt>

[Distinguished Encoding Rules](distinguished-encoding-rules.md)
</dt> </dl>

 

 



