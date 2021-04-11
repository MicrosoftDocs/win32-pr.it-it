---
title: attributo Code
description: L'attributo \ code \ ACF causa la generazione del codice stub client per le funzioni remote.
ms.assetid: 735a8c25-29d4-4073-a2db-88bc8615ccc1
keywords:
- attributo Code MIDL
topic_type:
- apiref
api_name:
- code
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa041859c0bffca2771695b7055105b8ae846221
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104334668"
---
# <a name="code-attribute"></a>attributo Code

L'attributo **\[ Code \]** ACF causa la generazione di codice stub client per le funzioni remote.

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

*Attributi di interfaccia ACF* 
</dt> <dd>

Specifica un elenco di uno o più attributi che si applicano all'interfaccia nel suo complesso. Gli attributi validi includono [**\[ \_ handle \] automatico**](auto-handle.md) o [**\[ \_ handle \] implicito**](implicit-handle.md) , ovvero **\[ codice \]**, [**\[ NoCode \]**](nocode.md)o [**\[ optimize \]**](optimize.md). Quando sono presenti due o più attributi di interfaccia, devono essere separati da virgole.

</dd> <dt>

*Nome interfaccia* 
</dt> <dd>

Specifica il nome dell'interfaccia.

</dd> <dt>

*elenco filename* 
</dt> <dd>

Specifica un elenco di uno o più nomi di file di intestazione C separati da virgole. È necessario specificare il nome completo del file, inclusa l'estensione.

</dd> <dt>

*tipo-Attribute-List* 
</dt> <dd>

Specifica un elenco di uno o più attributi, separati da virgole, che si applicano al tipo specificato. Gli attributi di tipo validi includono [**\[ \] allocate**](allocate.md) e [**\[ rappresentano \_ come \]**](represent-as.md).

</dd> <dt>

*typeName* 
</dt> <dd>

Specifica un tipo definito nel file IDL. Gli attributi di tipo in ACF possono essere applicati solo ai tipi definiti in precedenza nel file IDL.

</dd> <dt>

*ACF-Function-Attributes* 
</dt> <dd>

Specifica zero o più attributi che si applicano alla funzione nel suo complesso, ad esempio [**\[ \_ lo \] stato della comunicazione**](comm-status.md). Gli attributi della funzione sono racchiusi tra parentesi quadre. Separare più attributi di funzione con virgole.

</dd> <dt>

*Nome funzione* 
</dt> <dd>

Specifica il nome della funzione come definito nel file IDL.

</dd> <dt>

*ACF-parametri-attributi* 
</dt> <dd>

Specifica gli attributi ACF che si applicano a un parametro. Si noti che è possibile applicare zero, uno o più attributi al parametro. Separare più attributi di parametro con virgole. Gli attributi del parametro ACF sono racchiusi tra parentesi quadre.

</dd> <dt>

*Nome parametro* 
</dt> <dd>

Specifica un parametro della funzione come definito nel file IDL. Ogni parametro per la funzione deve essere specificato nella stessa sequenza e con lo stesso nome definito nel file IDL.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'attributo **\[ Code \]** può essere visualizzato nell'intestazione ACF o essere applicato a una singola funzione.

Quando l'attributo **\[ Code \]** viene visualizzato nell'intestazione ACF, viene generato il codice stub client per tutte le funzioni remote che non dispongono dell'attributo della funzione [**\[ NoCode \]**](nocode.md) . È possibile eseguire l'override dell'attributo **\[ Code \]** nell'intestazione per una singola funzione specificando l'attributo **\[ NoCode \]** come attributo della funzione.

Quando l'attributo **\[ Code \]** viene visualizzato nell'elenco di attributi della funzione remota, viene generato il codice stub client per la funzione. Il codice stub client non viene generato quando:

-   L'intestazione ACF include l'attributo [**\[ NoCode \]**](nocode.md) .
-   L'attributo [**\[ NoCode \]**](nocode.md) viene applicato alla funzione.
-   L'attributo [**\[ Local \]**](local.md) si applica alla funzione nel file di interfaccia.

Il **\[ codice \]** o [**\[ NoCode \]**](nocode.md) può essere visualizzato nell'elenco di attributi dell'interfaccia o della funzione, ma quello scelto può comparire una sola volta nell'elenco.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[File di configurazione dell'applicazione (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**allocare**](allocate.md)
</dt> <dt>

[**\_handle automatico**](auto-handle.md)
</dt> <dt>

[**stato di comunicazione \_**](comm-status.md)
</dt> <dt>

[**handle implicito \_**](implicit-handle.md)
</dt> <dt>

[**locale**](local.md)
</dt> <dt>

[**NoCode**](nocode.md)
</dt> <dt>

[**ottimizzare**](optimize.md)
</dt> <dt>

[**rappresenta \_ come**](represent-as.md)
</dt> </dl>

 

 




