---
title: include (attributo)
description: L'istruzione include di ACF specifica uno o più file di intestazione da includere nel codice stub generato.
ms.assetid: f83a704b-2f6e-4498-97ff-593fef2e92dc
keywords:
- Includi attributo MIDL
topic_type:
- apiref
api_name:
- include
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2aab7b7262bceb330e3f4645e4f16035b783197
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104116989"
---
# <a name="include-attribute"></a>include (attributo)

L'istruzione **include** di ACF specifica uno o più file di intestazione da includere nel codice stub generato.

``` syntax
include filenames;
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*nomi* 
</dt> <dd>

Specifica il nome di uno o più file di intestazione del linguaggio C. Usare il nome file completo, incluso il. Estensione H e racchiudere ogni nome di file tra virgolette. Separare più nomi di file di intestazione in linguaggio C con virgole.

</dd> </dl>

## <a name="remarks"></a>Commenti

In seguito all'istruzione **include** , il codice stub generato conterrà un'istruzione di **\# inclusione** del preprocessore C. Quando si compilano gli stub, è necessario specificare il file di intestazione del linguaggio C. Le istruzioni include si basano sul meccanismo del compilatore C di ricerca della struttura di directory per i file inclusi.

> [!Note]  
> Utilizzare la direttiva [**Import**](import.md) anziché la direttiva **include** per i file di sistema che contengono i tipi di dati che si desidera rendere disponibili per il file IDL. La direttiva **Import** ignora i prototipi di funzione e consente di usare le opzioni del compilatore MIDL per ottimizzare la generazione delle routine di supporto.

 

## <a name="examples"></a>Esempi

``` syntax
include "local.h";
include "gendefs.h", "protos.h", "mystuff.h";
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[File di configurazione dell'applicazione (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**importare**](import.md)
</dt> <dt>

[Importazione di file e librerie dei tipi](importing-files-and-type-libraries.md)
</dt> <dt>

[Importazione di file di intestazione di sistema](importing-system-header-files.md)
</dt> </dl>

 

 




