---
title: Attributo nocode
description: L'attributo \ nocode\ viene usato nelle intestazioni ACF o con singole funzioni per impedire la generazione di codice stub client.
ms.assetid: d3b6e4c8-103c-4ea2-8748-11d844fdda97
keywords:
- Attributo nocode MIDL
topic_type:
- apiref
api_name:
- nocode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86ec4612bc1bd5db1a8cdcbecdced51911591cdf5c482c83381f86deafd66a9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066961"
---
# <a name="nocode-attribute"></a>Attributo nocode

**\[ L'attributo \] nocode** viene usato nelle intestazioni ACF o con singole funzioni per impedire la generazione di codice stub client.

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

*ACF-interface-attributes* 
</dt> <dd>

Specifica un elenco di uno o più attributi che si applicano all'intera interfaccia. Gli attributi validi includono **\[** [**\_ l'handle automatico o**](auto-handle.md) **\]** **\[** [**\_ l'handle implicito**](implicit-handle.md) **\]** e il **\[** [**codice**](code.md) **\]** o **\[ nocode \]**. Quando sono presenti due o più attributi di interfaccia, devono essere separati da virgole.

</dd> <dt>

*interface-name* 
</dt> <dd>

Specifica il nome dell'interfaccia. In modalità di compatibilità DCE, il nome dell'interfaccia deve corrispondere al nome dell'interfaccia specificata nel file IDL. Quando si usa l'opzione del compilatore MIDL [**/acf**](-acf.md), il nome dell'interfaccia in ACF e il nome dell'interfaccia nel file IDL possono essere diversi.

</dd> <dt>

*filename-list* 
</dt> <dd>

Specifica un elenco di uno o più nomi di file di intestazione del linguaggio C, separati da virgole. È necessario specificare il nome file completo, inclusa l'estensione.

</dd> <dt>

*type-attribute-list* 
</dt> <dd>

Specifica un elenco di uno o più attributi, separati da virgole, che si applicano al tipo specificato. Gli attributi di tipo validi includono **\[** [**allocare**](allocate.md) **\]** .

</dd> <dt>

*Typename* 
</dt> <dd>

Specifica un tipo definito nel file IDL. Gli attributi di tipo in ACF possono essere applicati solo ai tipi definiti in precedenza nel file IDL.

</dd> <dt>

*ACF-function-attributes* 
</dt> <dd>

Specifica gli attributi applicabili all'intera funzione, ad esempio **\[** [**comm \_ status**](comm-status.md) **\]** . Gli attributi della funzione sono racchiusi tra parentesi quadre. Separare più attributi di funzione con virgole.

</dd> <dt>

*function-name* 
</dt> <dd>

Specifica il nome della funzione come definito nel file IDL.

</dd> <dt>

*ACF-parameter-attributes* 
</dt> <dd>

Specifica gli attributi ACF che si applicano a un parametro. Si noti che è possibile applicare zero o più attributi al parametro . Separare più attributi di parametro con virgole. Gli attributi dei parametri ACF sono racchiusi tra parentesi quadre.

</dd> <dt>

*parameter-name* 
</dt> <dd>

Specifica un parametro della funzione come definito nel file IDL. Ogni parametro per la funzione deve essere specificato nella stessa sequenza e usando lo stesso nome definito nel file IDL.

</dd> </dl>

## <a name="remarks"></a>Commenti

**\[ L'attributo \] nocode** può essere visualizzato nell'intestazione ACF oppure può essere applicato a una singola funzione.

Quando **\[ l'attributo \] nocode** viene visualizzato nell'intestazione ACF, il codice stub client non viene generato per qualsiasi funzione remota, a meno che non abbia l'attributo **\[** [**della**](code.md) funzione **\]** di codice. È possibile eseguire **\[ l'override dell'attributo nocode \]** nell'intestazione per una singola funzione specificando l'attributo **\[ code \]** come attributo di funzione.

Quando **\[ l'attributo nocode \]** viene visualizzato nell'elenco di attributi della funzione, non viene generato alcun codice stub client per la funzione.

Il codice stub client non viene generato quando:

-   L'intestazione ACF include **\[ l'attributo \] nocode.**
-   **\[ L'attributo \] nocode** viene applicato alla funzione.
-   **\[** [**L'attributo**](local.md) **\]** locale si applica alla funzione nel file di interfaccia.

Il **\[** [**codice**](code.md) **\]** o **\[ \] nocode** può essere visualizzato nell'elenco di attributi di una funzione e quello scelto può essere visualizzato esattamente una volta.

**\[ L'attributo \] nocode** viene ignorato quando vengono generati stub del server. Non è possibile applicarlo durante la generazione di stub del server in modalità di compatibilità DCE.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[File di configurazione dell'applicazione (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**/acf**](-acf.md)
</dt> <dt>

[**Allocare**](allocate.md)
</dt> <dt>

[**handle \_ automatico**](auto-handle.md)
</dt> <dt>

[**Codice**](code.md)
</dt> <dt>

[**Stato \_ comm**](comm-status.md)
</dt> <dt>

[**handle \_ implicito**](implicit-handle.md)
</dt> </dl>

 

 




