---
title: include (attributo)
description: L'istruzione INCLUDE di ACF specifica uno o più file di intestazione da includere nel codice stub generato.
ms.assetid: f83a704b-2f6e-4498-97ff-593fef2e92dc
keywords:
- include attribute MIDL
topic_type:
- apiref
api_name:
- include
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 827ec8deec34a42d39fc3973dff73e9912ecb96bfee62e348ef7aebfee6ee9f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067205"
---
# <a name="include-attribute"></a>include (attributo)

L'istruzione **INCLUDE di** ACF specifica uno o più file di intestazione da includere nel codice stub generato.

``` syntax
include filenames;
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*Nomi* 
</dt> <dd>

Specifica il nome di uno o più file di intestazione del linguaggio C. Usare il nome completo del file, incluso . Estensione H e racchiudere ogni nome file tra virgolette. Separare più nomi di file di intestazione in linguaggio C con virgole.

</dd> </dl>

## <a name="remarks"></a>Commenti

In seguito all'istruzione **include,** il codice stub generato conterrà un'istruzione include del **\# preprocessore** C. Il file di intestazione del linguaggio C viene fornito durante la compilazione degli stub. Le istruzioni Include si basano sul meccanismo del compilatore C per cercare i file inclusi nella struttura di directory.

> [!Note]  
> Usare la [**direttiva import**](import.md) anziché la direttiva **include** per i file di sistema contenenti i tipi di dati che si desidera rendere disponibili per il file IDL. La **direttiva import** ignora i prototipi di funzione e consente di usare le opzioni del compilatore MIDL che ottimizzano la generazione di routine di supporto.

 

## <a name="examples"></a>Esempi

``` syntax
include "local.h";
include "gendefs.h", "protos.h", "mystuff.h";
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[File di configurazione dell'applicazione (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**Importazione**](import.md)
</dt> <dt>

[Importazione di file e librerie dei tipi](importing-files-and-type-libraries.md)
</dt> <dt>

[Importazione di file di intestazione di sistema](importing-system-header-files.md)
</dt> </dl>

 

 




