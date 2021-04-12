---
title: import (attributo)
description: La direttiva Import specifica un altro file IDL, FAD o di intestazione contenente le definizioni a cui si vuole fare riferimento dal file IDL principale.
ms.assetid: b52fb2c7-ce60-474f-8833-7a821844f747
keywords:
- Importa attributo MIDL
topic_type:
- apiref
api_name:
- import
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64ff13c069c6bba819720a9d1120a42c25af4b51
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104336983"
---
# <a name="import-attribute"></a>import (attributo)

La direttiva **Import** specifica un altro file IDL, FAD o di intestazione contenente le definizioni a cui si vuole fare riferimento dal file IDL principale.

``` syntax
import "filename" [[ , ... ]] ;
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*filename* 
</dt> <dd>

Specifica il nome del file di intestazione, IDL o FAD da importare.

</dd> </dl>

## <a name="remarks"></a>Commenti

Con la direttiva **Import** , tutte le istruzioni IDL nel file importato, ad esempio i typedef, le dichiarazioni di costanti e le definizioni di interfaccia, diventano disponibili per l'importazione. File IDL.

Il file importato viene elaborato separatamente (ovvero il preprocessore CPP viene richiamato in modo indipendente) dal file IDL di importazione. In questo modo, le direttive del preprocessore, ad esempio \# define, non vengono riportate da un'intestazione importata o da un file IDL al file IDL di importazione.

Come la macro del preprocessore del linguaggio C **\# include**, la direttiva **Import** indica al compilatore di includere i tipi di dati definiti nei file IDL importati. A differenza della direttiva **\# include** , la direttiva **Import** ignora i prototipi di routine, perché non vengono generati stub per alcun elemento nel file importato.

Per informazioni specifiche sull'utilizzo di **Importa** per includere i file di intestazione in un file IDL, vedere [importazione di file di intestazione di sistema](importing-system-header-files.md).

Intestazione del linguaggio C (. H) il file generato per l'interfaccia non contiene direttamente i tipi importati, ma genera invece una direttiva **\# include** per il file di intestazione corrispondente all'interfaccia importata. Ad esempio, quando si importa BASE. IDL nel derivato. IDL, il file di intestazione generato derivato. H conterrà la direttiva **\# include** base. h.

Sono applicabili le regole seguenti:

-   La parola chiave **Import** è facoltativa e può essere visualizzata zero o più volte nel file IDL.
-   Ogni parola chiave **Import** può essere associata a più di un nome di file.
-   Separare più nomi di file con virgole.
-   È necessario racchiudere il nome file tra virgolette e terminare l'istruzione import con un punto e virgola (;).
-   È possibile importare un'interfaccia senza attributi in un altro file IDL. Tuttavia, l'interfaccia deve contenere solo tipi di oggetto. non può contenere alcuna routine. Se nell'interfaccia importata è inclusa anche una routine, è necessario specificare un attributo [**local**](local.md) o [**UUID**](uuid.md) .
-   La funzione di **importazione** è idempotentÂ â € ", ovvero l'importazione di un'interfaccia più di una volta non ha alcun effetto aggiuntivo.

> [!Note]  
> Il comportamento della direttiva **Import** è indipendente dalle modalità del compilatore MIDL Switch [**/MS \_ ext**](-ms-ext.md) (impostazione predefinita), [**/OSF**](-osf.md)e [**/app \_ config**](-app-config.md). Tuttavia, la modalità del compilatore (**/OSF** o **/MS \_ ext**) può influenzare la decorazione degli attributi dei puntatori sui tipi importati. Per informazioni dettagliate [, vedere ereditarietà del tipo di attributo puntatore](/windows/desktop/Rpc/pointer-attribute-type-inheritance).

 

## <a name="examples"></a>Esempi

``` syntax
import "myoldodl.odl";  
import "unknwn.idl";
import "part1.idl", "part2.idl", "part3.idl"; 
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[**configurazione di/app \_**](-app-config.md)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**importlib**](importlib.md)
</dt> <dt>

[**includere**](include.md)
</dt> <dt>

[Importazione di file di intestazione di sistema](importing-system-header-files.md)
</dt> <dt>

[Importazione di file e librerie dei tipi](importing-files-and-type-libraries.md)
</dt> <dt>

[**/MS \_ ext**](-ms-ext.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> </dl>

 

 