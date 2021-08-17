---
title: attributo code
description: L'attributo \ code\ ACF fa sì che il codice stub del client sia generato per le funzioni remote.
ms.assetid: 735a8c25-29d4-4073-a2db-88bc8615ccc1
keywords:
- attributo di codice MIDL
topic_type:
- apiref
api_name:
- code
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1d94f4f764fb25e5e2a5a43d1cdbe76f5288901846c2291daa4497947a486f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117991815"
---
# <a name="code-attribute"></a>attributo code

**\[ L'attributo \]** ACF del codice fa sì che il codice stub del client sia generato per le funzioni remote.

``` syntax
[
    code [ , ACF-interface-attributes ] 
] 
interface interface-name
{
  [ include filename-list ; ]
  [ typedef [type-attribute-list] typenam; ]
  [ [code [ , ACF-function-attributes ]] function-name (
            [ ACF-parameter-attributes ] parameter-name,
        ...);
  ]
    ...
}
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*ACF-interface-attributes* 
</dt> <dd>

Specifica un elenco di uno o più attributi che si applicano all'intera interfaccia. Gli attributi validi includono [**\[ handle automatico \_ o \]**](auto-handle.md) [**\[ handle \_ implicito \]**](implicit-handle.md) e **\[ \] codice**, [**\[ nocode \]**](nocode.md)o [**\[ ottimizzazione di \]**](optimize.md). Quando sono presenti due o più attributi di interfaccia, devono essere separati da virgole.

</dd> <dt>

*interface-name* 
</dt> <dd>

Specifica il nome dell'interfaccia.

</dd> <dt>

*filename-list* 
</dt> <dd>

Specifica un elenco di uno o più nomi di file di intestazione C, separati da virgole. È necessario specificare il nome completo del file, inclusa l'estensione.

</dd> <dt>

*type-attribute-list* 
</dt> <dd>

Specifica un elenco di uno o più attributi, separati da virgole, che si applicano al tipo specificato. Gli attributi di tipo validi [**\[ includono allocare \]**](allocate.md) e rappresentare [**\[ \_ come \]**](represent-as.md).

</dd> <dt>

*Typename* 
</dt> <dd>

Specifica un tipo definito nel file IDL. Gli attributi di tipo in ACF possono essere applicati solo ai tipi definiti in precedenza nel file IDL.

</dd> <dt>

*ACF-function-attributes* 
</dt> <dd>

Specifica zero o più attributi che si applicano all'intera funzione, ad esempio [**\[ comm \_ status \]**](comm-status.md). Gli attributi della funzione sono racchiusi tra parentesi quadre. Separare più attributi di funzione con virgole.

</dd> <dt>

*function-name* 
</dt> <dd>

Specifica il nome della funzione come definito nel file IDL.

</dd> <dt>

*ACF-parameter-attributes* 
</dt> <dd>

Specifica gli attributi ACF che si applicano a un parametro. Si noti che al parametro possono essere applicati zero, uno o più attributi. Separare più attributi di parametro con virgole. Gli attributi dei parametri ACF sono racchiusi tra parentesi quadre.

</dd> <dt>

*parameter-name* 
</dt> <dd>

Specifica un parametro della funzione come definito nel file IDL. Ogni parametro per la funzione deve essere specificato nella stessa sequenza e con lo stesso nome definito nel file IDL.

</dd> </dl>

## <a name="remarks"></a>Commenti

**\[ L'attributo \]** di codice può essere visualizzato nell'intestazione ACF o applicato a una singola funzione.

Quando **\[ l'attributo di \]** codice viene visualizzato nell'intestazione ACF, il codice stub del client viene generato per tutte le funzioni remote che non hanno l'attributo della funzione [**\[ nocode. \]**](nocode.md) È possibile eseguire **\[ l'override \] dell'attributo** di codice nell'intestazione per una singola funzione specificando l'attributo **\[ nocode \]** come attributo della funzione.

Quando **\[ l'attributo \]** di codice viene visualizzato nell'elenco di attributi della funzione remota, viene generato il codice stub client per la funzione. Il codice stub del client non viene generato quando:

-   L'intestazione ACF include [**\[ l'attributo \] nocode.**](nocode.md)
-   [**\[ L'attributo \] nocode**](nocode.md) viene applicato alla funzione.
-   [**\[ L'attributo \]**](local.md) locale si applica alla funzione nel file di interfaccia.

Il **\[ codice \]** o [**\[ nocode può \]**](nocode.md) essere visualizzato nell'elenco degli attributi dell'interfaccia o della funzione, ma quello scelto può essere visualizzato una sola volta nell'elenco.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[File di configurazione dell'applicazione (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**Allocare**](allocate.md)
</dt> <dt>

[**handle \_ automatico**](auto-handle.md)
</dt> <dt>

[**stato \_ comm**](comm-status.md)
</dt> <dt>

[**handle \_ implicito**](implicit-handle.md)
</dt> <dt>

[**Locale**](local.md)
</dt> <dt>

[**nocode**](nocode.md)
</dt> <dt>

[**Ottimizzare**](optimize.md)
</dt> <dt>

[**rappresentano \_ come**](represent-as.md)
</dt> </dl>

 

 




