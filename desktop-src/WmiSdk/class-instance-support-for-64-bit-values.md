---
description: Fornisce restrizioni per l'utilizzo di valori a 64 bit come parte di un percorso.
ms.assetid: 63f4f6c5-7803-425d-912f-bb1dd716e617
ms.tgt_platform: multiple
title: Supporto dell'istanza di classe per i valori a 64 bit
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 80f8a48f253cf2ef1902938ca6c54d01404b8466
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315242"
---
# <a name="class-instance-support-for-64-bit-values"></a>Supporto dell'istanza di classe per i valori a 64 bit

È possibile usare un valore di chiave a 64 bit come parte di un percorso, con le restrizioni seguenti:

-   Fino a quando non si supera l'intervallo di 32 bit, è possibile assegnare e recuperare i valori dalla chiave come si farebbe con una proprietà a 32 bit.
-   Dopo aver superato il valore integer di 0x7FFFFFFF (per i tipi con segno), 0x80000000 (per i tipi senza segno) o 32 bit, è necessario utilizzare le virgolette.
-   L'unico percorso valido per un valore a 64 bit si trova nelle proprietà **\_ \_ RelPath** o **\_ \_ path** dell'istanza. Di conseguenza, WMI non supporta la notazione esadecimale per il valore equivalente.
-   Se WMI registra la chiave di istanza come numero negativo, è necessario utilizzare il numero originale per recuperare l'istanza.

La semantica di query non è interessata e si comporta come previsto. Questo comportamento influiscono solo sulle operazioni Path dell'oggetto, [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)e [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) .

Nell'esempio seguente viene illustrato che le istanze della classe possono avere valori di chiave a 64 bit.

``` syntax
class MyBig
{
  [key] sint64 k;
  sint64 p;
};

instance of MyBig
{
  k = 2;
  p = 3;
};
```

 

 



