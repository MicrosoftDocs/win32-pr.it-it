---
description: Il campo lunghezza in una tripletta TLV identifica il numero di byte codificati nel campo valore.
ms.assetid: d72371f9-fe55-468d-b15b-0f8948674619
title: Byte di lunghezza e valore codificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b45eaec36875446d7493f37fc150f7b5f9d1a59c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310756"
---
# <a name="encoded-length-and-value-bytes"></a>Byte di lunghezza e valore codificati

Il campo *lunghezza* in una tripletta TLV identifica il numero di byte codificati nel campo *valore* . Il campo *valore* contiene il contenuto inviato tra computer. Se il campo del *valore* contiene meno di 128 byte, il campo *lunghezza* richiede un solo byte. Il bit 7 del campo *length* è zero (0) e i bit rimanenti identificano il numero di byte del contenuto inviato. Se il campo del *valore* contiene più di 127 byte, il bit 7 del campo *length* è uno (1) e i bit rimanenti identificano il numero di byte necessari per contenere la lunghezza. Nella figura seguente sono illustrati alcuni esempi.

![byte Lunghezza der TLV](images/der-tlv-lengthbyte.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sintassi di trasferimento DER](about-der-transfer-syntax.md)
</dt> <dt>

[Byte tag codificati](about-encoded-tag-bytes.md)
</dt> </dl>

 

 



