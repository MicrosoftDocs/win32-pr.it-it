---
title: NoCode (attributo)
description: L'attributo \ NoCode \ viene usato nelle intestazioni ACF o con singole funzioni per impedire la generazione di codice stub del client.
ms.assetid: d3b6e4c8-103c-4ea2-8748-11d844fdda97
keywords:
- NoCode (attributo MIDL)
topic_type:
- apiref
api_name:
- nocode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64f5138dc1794e9b2714e5f64762c1af17b47fb2
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104333575"
---
# <a name="nocode-attribute"></a>NoCode (attributo)

L'attributo **\[ NoCode \]** viene usato nelle intestazioni ACF o con singole funzioni per impedire la generazione di codice stub del client.

``` syntax
[ 
    nocode 
    [ , ACF-interface-attributes ] 
] 
interface interface-name
{
  [ include filename-list ; ]
  [ typedef [type-attribute-list] typename; ] 
  [ [ nocode [ , ACF-function-attributes ] ] function-name (
        [ ACF-parameter-attributes ] parameter-name ;
        ...);
  ]
    ...
}
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*Attributi di interfaccia ACF* 
</dt> <dd>

Specifica un elenco di uno o più attributi che si applicano all'interfaccia nel suo complesso. Gli attributi validi includono **\[** [**\_ handle automatico**](auto-handle.md) **\]** o **\[** [**\_ handle implicito**](implicit-handle.md) **\]** e **\[** [**codice**](code.md) **\]** o **\[ NoCode \]**. Quando sono presenti due o più attributi di interfaccia, devono essere separati da virgole.

</dd> <dt>

*Nome interfaccia* 
</dt> <dd>

Specifica il nome dell'interfaccia. In modalità di compatibilità DCE, il nome dell'interfaccia deve corrispondere al nome dell'interfaccia specificata nel file IDL. Quando si usa l'opzione del compilatore MIDL [**/ACF**](-acf.md), il nome dell'interfaccia in ACF e il nome dell'interfaccia nel file IDL possono essere diversi.

</dd> <dt>

*elenco filename* 
</dt> <dd>

Specifica un elenco di uno o più nomi di file di intestazione del linguaggio C, separati da virgole. È necessario specificare il nome completo del file, inclusa l'estensione.

</dd> <dt>

*tipo-Attribute-List* 
</dt> <dd>

Specifica un elenco di uno o più attributi, separati da virgole, che si applicano al tipo specificato. Gli attributi di tipo validi includono **\[** [**allocate**](allocate.md) **\]** .

</dd> <dt>

*typeName* 
</dt> <dd>

Specifica un tipo definito nel file IDL. Gli attributi di tipo in ACF possono essere applicati solo ai tipi definiti in precedenza nel file IDL.

</dd> <dt>

*ACF-Function-Attributes* 
</dt> <dd>

Specifica gli attributi che si applicano alla funzione nel suo complesso, ad esempio **\[** [**\_ lo stato della comunicazione**](comm-status.md) **\]** . Gli attributi della funzione sono racchiusi tra parentesi quadre. Separare più attributi di funzione con virgole.

</dd> <dt>

*Nome funzione* 
</dt> <dd>

Specifica il nome della funzione come definito nel file IDL.

</dd> <dt>

*ACF-parametri-attributi* 
</dt> <dd>

Specifica gli attributi ACF che si applicano a un parametro. Si noti che è possibile applicare zero o più attributi al parametro. Separare più attributi di parametro con virgole. Gli attributi del parametro ACF sono racchiusi tra parentesi quadre.

</dd> <dt>

*Nome parametro* 
</dt> <dd>

Specifica un parametro della funzione come definito nel file IDL. Ogni parametro per la funzione deve essere specificato nella stessa sequenza e utilizzando lo stesso nome definito nel file IDL.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'attributo **\[ NoCode \]** può essere visualizzato nell'intestazione ACF oppure può essere applicato a una singola funzione.

Quando l'attributo **\[ \] NoCode** viene visualizzato nell'intestazione ACF, il codice stub del client non viene generato per alcuna funzione remota a meno che non disponga dell'attributo della funzione di **\[** [**codice**](code.md) **\]** . È possibile eseguire l'override dell'attributo **\[ NoCode \]** nell'intestazione per una singola funzione specificando l'attributo **\[ Code \]** come attributo della funzione.

Quando l'attributo **\[ NoCode \]** viene visualizzato nell'elenco di attributi della funzione, per la funzione non viene generato alcun codice stub client.

Il codice stub client non viene generato quando:

-   L'intestazione ACF include l'attributo **\[ NoCode \]** .
-   L'attributo **\[ NoCode \]** viene applicato alla funzione.
-   L' **\[** attributo [**local**](local.md) **\]** si applica alla funzione nel file di interfaccia.

Il **\[** [**codice**](code.md) **\]** o **\[ NoCode \]** può essere visualizzato nell'elenco di attributi di una funzione e quello scelto può essere visualizzato esattamente una volta.

L'attributo **\[ NoCode \]** viene ignorato quando vengono generati stub server. Non è possibile applicarlo quando si generano stub server in modalità di compatibilità DCE.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[File di configurazione dell'applicazione (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**/acf**](-acf.md)
</dt> <dt>

[**allocare**](allocate.md)
</dt> <dt>

[**\_handle automatico**](auto-handle.md)
</dt> <dt>

[**codice**](code.md)
</dt> <dt>

[**stato di comunicazione \_**](comm-status.md)
</dt> <dt>

[**handle implicito \_**](implicit-handle.md)
</dt> </dl>

 

 




