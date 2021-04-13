---
title: ISAN
description: L'attributo ISAN contiene il numero audiovisivo standard internazionale (ISAN) che identifica il contenuto.
ms.assetid: 2937d422-f062-4373-845e-dd200512ed0b
keywords:
- Formato ISAN Windows Media
topic_type:
- apiref
api_name:
- ISAN
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88dc4a850edc43178deb043143ee8f9b37140507
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "104398672"
---
# <a name="isan"></a>ISAN

L'attributo **ISAN** contiene il numero audiovisivo standard internazionale (ISAN) che identifica il contenuto.

## <a name="global-constant"></a>Costante globale

g \_ wszISAN

## <a name="data-type"></a>Tipo di dati

**\_stringa di tipo WMT \_**

## <a name="remarks"></a>Commenti

ISAN è uno standard internazionale per l'identificazione dei lavori audiovisivi. Per informazioni su ISAN, visitare il [sito Web](https://www.isan.org/)standard.

L'oggetto dell'editor di metadati verifica la stringa ISAN quando si imposta questo attributo. La formattazione della stringa accettabile, come descritto nella sezione 4,1 della specifica ISAN, è costituita da 16 cifre esadecimali, separate facoltativamente da spazi vuoti o trattini in segmenti a 4 cifre. Il numero formattato deve essere seguito, anch ' esso separato da uno spazio o un trattino, da un carattere di controllo valido. Il carattere di controllo può essere una cifra decimale o una lettera maiuscola. Per informazioni su come derivare il numero di controllo, vedere l'allegato A del manuale dell'utente di ISAN.

La stringa ISAN standard può essere seguita dalle informazioni sulla versione. Se presente, le informazioni sulla versione sono costituite da otto cifre esadecimali seguite da un numero di controllo. La formattazione di questi caratteri segue le stesse regole della stringa di base.

## <a name="examples"></a>Esempio

Di seguito sono riportate tre stringhe formattate in modo accettabile per un esempio ISAN.


```
00003BAB93520000G
0000 3BAB 9352 0000 G
0000-3BAB-9352-0000-G
```



La stringa seguente mostra il formato di un ISAN con le informazioni sulla versione.


```C++
0000-3BAB-9352-0000-G-0000-0000-Q
```



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elenco degli attributi**](attribute-list.md)
</dt> </dl>

 

 




