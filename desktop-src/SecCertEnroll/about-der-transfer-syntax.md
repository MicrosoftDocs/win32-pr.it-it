---
description: L'applicazione di una regola di codifica alle strutture di dati descritte da una sintassi astratta fornisce una sintassi di trasferimento che determina la modalità di organizzazione dei byte in un flusso quando viene inviato tra computer.
ms.assetid: 674e88f9-4b65-4b42-8c44-d24fc03ae2f3
title: Sintassi di trasferimento DER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a12f0ced0c47643db8f0e6e3c8f4ba2a36326e3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104569194"
---
# <a name="der-transfer-syntax"></a>Sintassi di trasferimento DER

L'applicazione di una regola di codifica alle strutture di dati descritte da una sintassi astratta fornisce una sintassi di trasferimento che determina la modalità di organizzazione dei byte in un flusso quando viene inviato tra computer. La sintassi di trasferimento utilizzata da Distinguished Encoding Rules segue sempre il formato di un *tag, una lunghezza e un valore* . Il formato viene in genere definito tripletta TLV in cui ogni campo (T, L o V) contiene uno o più byte.

![tipo der, lunghezza e tripletta del valore (TLV)](images/der-tlv-basic.png)

Il campo *tag* specifica il tipo di struttura dei dati da inviare, il campo *lunghezza* specifica il numero di byte di contenuto da trasferire e il campo *valore* contiene il contenuto. Si noti che il campo *valore* può essere una tripletta se contiene un tipo di dati costruito, come illustrato nella figura seguente.

![ricorsione tripletta der TLV](images/der-tlv-recursive.png)

Per informazioni dettagliate sui componenti di una tripletta TLV, vedere gli argomenti seguenti.

-   [Byte tag codificati](about-encoded-tag-bytes.md)
-   [Byte di lunghezza e valore codificati](about-encoded-length-and-value-bytes.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi costruiti](about-constructed-types.md)
</dt> <dt>

[Distinguished Encoding Rules](distinguished-encoding-rules.md)
</dt> </dl>

 

 



