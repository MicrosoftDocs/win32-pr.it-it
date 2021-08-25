---
title: Isan
description: L'attributo ISAN contiene il numero ISAN (International Standard Audiovisual Number) che identifica il contenuto.
ms.assetid: 2937d422-f062-4373-845e-dd200512ed0b
keywords:
- Formato isan windows media
topic_type:
- apiref
api_name:
- ISAN
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec2af088938219ed48f2b281c627c0b64cc8e13fdea630b54a51a6f23db1b448
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808821"
---
# <a name="isan"></a>Isan

**L'attributo ISAN** contiene il numero ISAN (International Standard Audiovisual Number) che identifica il contenuto.

## <a name="global-constant"></a>Costante globale

g \_ wszISAN

## <a name="data-type"></a>Tipo di dati

**STRINGA DI TIPO WMT \_ \_**

## <a name="remarks"></a>Commenti

ISAN è uno standard internazionale per l'identificazione delle opere audiovisuali. Per informazioni su ISAN, visitare il sito [Web dello](https://www.isan.org/)standard.

L'oggetto editor di metadati verifica la stringa ISAN quando si imposta questo attributo. La formattazione di stringa accettabile, come descritto nella sezione 4.1 della specifica ISAN, è costituita da 16 cifre esadecimali, facoltativamente separate da spazi vuoti o trattini in segmenti a 4 cifre. Il numero formattato deve essere seguito, facoltativamente, anche da uno spazio o da un trattino, da un carattere di controllo valido. Il carattere di controllo può essere una cifra decimale o una lettera maiuscola. Per informazioni su come derivare il numero di assegno, vedere l'allegato A della guida dell'utente ISAN.

La stringa ISAN standard può essere seguita dalle informazioni sulla versione. Se presenti, le informazioni sulla versione sono costituite da otto cifre esadecimali seguite da un numero di controllo. La formattazione di questi caratteri segue le stesse regole della stringa di base.

## <a name="examples"></a>Esempio

Di seguito sono riportate tre stringhe in formato accettabile per un isan di esempio.


```
00003BAB93520000G
0000 3BAB 9352 0000 G
0000-3BAB-9352-0000-G
```



La stringa seguente mostra il formato di un ISAN con informazioni sulla versione.


```C++
0000-3BAB-9352-0000-G-0000-0000-Q
```



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elenco degli attributi**](attribute-list.md)
</dt> </dl>

 

 




