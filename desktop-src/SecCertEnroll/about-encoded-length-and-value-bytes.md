---
description: Il campo Lunghezza in una tripletta TLV identifica il numero di byte codificati nel campo Valore.
ms.assetid: d72371f9-fe55-468d-b15b-0f8948674619
title: Lunghezza codificata e byte dei valori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea44ec9892e9407cbe587dbb60219b758ac95392e64dfabcf4866e02a1ad9343
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118904476"
---
# <a name="encoded-length-and-value-bytes"></a>Lunghezza codificata e byte dei valori

Il *campo Lunghezza* in una tripletta TLV identifica il numero di byte codificati nel *campo* Valore. Il *campo Valore* contiene il contenuto inviato tra computer. Se il *campo Valore* contiene meno di 128 byte, il *campo Lunghezza* richiede un solo byte. Il bit 7 del *campo Length* è zero (0) e i bit rimanenti identificano il numero di byte di contenuto inviato. Se il campo *Valore* contiene più di 127 byte, il bit 7 del campo *Lunghezza* è uno (1) e i bit rimanenti identificano il numero di byte necessari per contenere la lunghezza. Nella figura seguente sono illustrati alcuni esempi.

![der tlv length byte](images/der-tlv-lengthbyte.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sintassi di trasferimento DER](about-der-transfer-syntax.md)
</dt> <dt>

[Byte tag codificati](about-encoded-tag-bytes.md)
</dt> </dl>

 

 



