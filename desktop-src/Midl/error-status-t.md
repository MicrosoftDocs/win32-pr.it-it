---
title: error_status_t attributo
description: La parola chiave error status t definisce un tipo per un oggetto che contiene informazioni sullo stato \_ di comunicazione o di \_ errore.
ms.assetid: 7eff0d20-c058-4f16-a3db-0b4c82303135
keywords:
- error_status_t attributo MIDL
topic_type:
- apiref
api_name:
- error_status_t
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b02e404992e8fca98eba41f5ea85571160582827816a945d7ab8db505b28ba0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067271"
---
# <a name="error_status_t-attribute"></a>error \_ status \_ t attribute

La **parola chiave error status \_ \_ t** definisce un tipo per un oggetto che contiene informazioni sullo stato di comunicazione o di errore.

``` syntax
[ [ , ACF-function-attributes ] ] error_status_t function-name(
        [ [ ACF-parameter-attributes ] ] parameter-name
        , ...);

[ [ ACF-function-attributes ] ] function-name(
    [ [ ACF-parameter-attributes ] ] error_status_t parameter-name
    , ...);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*ACF-function-attributes* 
</dt> <dd>

Specifica zero o più attributi della funzione ACF, ad esempio **\[** [**comm \_ status,**](comm-status.md) **\]** **\[** [**fault \_ status**](fault-status.md) **\]** o **\[** [**nocode.**](nocode.md) **\]** Gli attributi della funzione sono racchiusi tra parentesi quadre. A una funzione possono essere applicati zero o più attributi. Separare più attributi di funzione con virgole.

</dd> <dt>

*function-name* 
</dt> <dd>

Specifica il nome della funzione come definito nel file IDL.

</dd> <dt>

*ACF-parameter-attributes* 
</dt> <dd>

Specifica gli attributi che si applicano a un parametro. Si noti che al parametro possono essere applicati zero, uno o più attributi. Separare più attributi di parametro con virgole. Gli attributi dei parametri sono racchiusi tra parentesi quadre. Gli attributi dei parametri IDL, ad esempio gli attributi direzionali, non sono consentiti in ACF.

</dd> <dt>

*parameter-name* 
</dt> <dd>

Specifica il parametro per la funzione come definito nel file IDL. Ogni parametro per la funzione deve essere specificato nella stessa sequenza, usando lo stesso nome definito nel file IDL.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il tipo di stato di errore **\_ \_ t** viene usato come parte dell'architettura di gestione delle eccezioni in IDL. Questo tipo esegue il mapping a [**un oggetto long senza**](unsigned.md) [**segno.**](long.md) Le applicazioni che rilevano situazioni di errore hanno un parametro out o un tipo restituito di una routine specificata come stato di errore t e qualificano lo stato di errore t con gli attributi dello stato comm o **\[** [](out-idl.md) **\]** fault **\_ \_** **\_ \_** **\[** [**\_**](comm-status.md) **\]** **\[** [**\_ status**](fault-status.md) **\]** in ACF. Se il parametro o il tipo restituito non è stato qualificato con gli attributi **\[ comm \_ status \]** o **\[ fault \_ status, \]** il parametro funziona come se fosse un valore unsigned long.

A partire dalla versione 2.0, il compilatore MIDL genera stub contenenti l'architettura di gestione degli errori appropriata. Tuttavia, le versioni precedenti del compilatore MIDL gestivano un parametro o un tipo restituito dello stato di errore **\_ \_ t** come se fossero stati applicati gli attributi di stato comm e di errore, anche se non lo **\[** [**\_**](comm-status.md) **\]** **\[** [**\_**](fault-status.md) **\]** erano. Con MIDL 2.0 o versione successiva, è necessario applicare in modo esplicito gli attributi **\[ comm \_ status \]** e **\[ fault \_ status \]** al parametro o alla procedura in ACF.

Il tipo di stato di errore **\_ \_ t** è uno dei tipi predefiniti del linguaggio di definizione dell'interfaccia. I tipi predefiniti possono essere visualizzati come identificatori di tipo nelle dichiarazioni [**typedef,**](typedef.md) nelle dichiarazioni generali e nei dichiaratori di funzione (come function-return-type o come identificatori di tipo di parametro).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**stato \_ comm**](comm-status.md)
</dt> <dt>

[**stato di \_ errore**](fault-status.md)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**long**](long.md)
</dt> <dt>

[**in uscita**](out-idl.md)
</dt> <dt>

[**Typedef**](typedef.md)
</dt> <dt>

[**Unsigned**](unsigned.md)
</dt> </dl>

 

 




