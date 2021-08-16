---
description: Fornisce restrizioni per l'uso di valori a 64 bit come parte di un percorso.
ms.assetid: 63f4f6c5-7803-425d-912f-bb1dd716e617
ms.tgt_platform: multiple
title: Supporto dell'istanza della classe per i valori a 64 bit
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ae778bcaad724d727bbda6d6a421ae19c562acdd50c33aa7764bea3b1861273e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118556828"
---
# <a name="class-instance-support-for-64-bit-values"></a>Supporto dell'istanza della classe per i valori a 64 bit

È possibile usare un valore di chiave a 64 bit come parte di un percorso, con le restrizioni seguenti:

-   Se non si supera l'intervallo a 32 bit, è possibile assegnare e recuperare valori dalla chiave come si farebbe con una proprietà a 32 bit.
-   Dopo aver superato il valore integer di 0x7FFFFFFF (per i tipi con segno), 0x80000000 (per i tipi senza segno) o 32 bit, è necessario usare le virgolette.
-   L'unico percorso valido per un valore a 64 bit si trova nelle proprietà **\_ \_ RELPATH** o **\_ \_ PATH** dell'istanza di . Di conseguenza, WMI non supporta la notazione esadecimale per il valore equivalente.
-   Se WMI registra la chiave dell'istanza come numero negativo, è necessario usare il numero originale per recuperare l'istanza.

La semantica delle query non è influenzata e si comporta come previsto. Questo comportamento influisce solo sul percorso dell'oggetto, [**sulle operazioni GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)e [**GetObjectAsync.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)

L'esempio seguente mostra che le istanze della classe possono avere valori di chiave a 64 bit.

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

 

 



