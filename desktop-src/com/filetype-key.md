---
title: Chiave filetype
description: Usato da GetClassFile per trovare la corrispondenza dei modelli con diversi byte di file in un file non composto.
ms.assetid: ced23cdb-c184-43fe-ba37-fe1af8664b66
keywords:
- Chiave del registro di sistema filetype COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a2e331588b627ee5ce9a9c1b69631f1e8a1dbe4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045280"
---
# <a name="filetype-key"></a>Chiave filetype

Usato da [**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) per trovare la corrispondenza dei modelli con diversi byte di file in un file non composto.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\FileType
   {CLSID}
      n = offset, cb, mask, value
```

<dl> <dt>

<span id="offset"></span><span id="OFFSET"></span>*offset*
</dt> <dd>

Determina la distanza dall'inizio o dalla fine del file per iniziare il confronto. Se l'offset è un valore negativo, il confronto inizia dalla fine del file meno il valore di offset. Il valore di offset è un tipo decimale, a meno che non sia preceduto da "0x".

</dd> <dt>

<span id="cb"></span><span id="CB"></span>*CB*
</dt> <dd>

Rappresenta la lunghezza in byte dall'inizio alla fine del file. Rappresenta l'intervallo di byte nel file. Il valore *CB* è un numero decimale, a meno che non sia preceduto da "0x".

</dd> <dt>

<span id="mask"></span><span id="MASK"></span>*maschera*
</dt> <dd>

Valore binario utilizzato per la maschera, che viene eseguito utilizzando un'operazione AND logica e l'intervallo di byte specificato da *offset* e *CB*. Se questo valore viene omesso, i byte vengono impostati su tutti quelli. Questo valore è sempre esadecimale.

</dd> <dt>

<span id="value"></span><span id="VALUE"></span>*valore*
</dt> <dd>

Rappresenta il criterio che deve corrispondere a un file di questo tipo di file. Il modello viene usato per identificare correttamente un formato di file noto dal contenuto, non dalla relativa estensione.

</dd> </dl>

## <a name="remarks"></a>Commenti

Le voci vengono usate dalla funzione [**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) per trovare la corrispondenza dei modelli con i diversi byte di file in un file non composto. **FileType** dispone di sottochiavi CLSID, ognuna delle quali contiene una serie di sottochiavi **0**, **1**, **2**, **3**. Questi valori contengono modelli che, se uno corrisponde, producono il CLSID indicato. Ad esempio, il valore "0, 4, FFFFFFFF, ABCD1234" indica che i primi 4 byte devono essere ABCD1234, in questo ordine. Il valore "-4, 4, FEFEFEFE" indica che gli ultimi quattro byte nel file devono essere FEFEFEFE. Se uno dei due criteri corrisponde, viene restituito il CLSID.

La chiave delle **\_ \_ \\ \\ classi software del computer locale HKEY** corrisponde alla chiave **\_ \_ radice delle classi HKEY** , che è stata mantenuta per la compatibilità con le versioni precedenti di com.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**<estensione di file \_>**](-file-extension--key.md)
</dt> <dt>

[**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile)
</dt> </dl>

 

 




