---
title: comm_status attributo
description: L'attributo \ comm status\ ACF fa sì che un codice di errore viene restituito quando si verifica un errore di \_ comunicazione durante l'esecuzione di una funzione.
ms.assetid: 3ea9ce62-8bd4-40fe-b838-bfebd52b5a15
keywords:
- comm_status'attributo MIDL
topic_type:
- apiref
api_name:
- comm_status
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 719f66d6849a21d67d9349a9e9fd728defb4a0663e4436701d06f20209f4d5b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118384702"
---
# <a name="comm_status-attribute"></a>Attributo comm \_ status

L'attributo ACF di stato **\[ comm \_ \]** fa sì che un codice di errore viene restituito quando si verifica un errore di comunicazione durante l'esecuzione di una funzione.

``` syntax
[comm_status [ , ACF-function-attributes ] ] 
    error_status_t function-name(
        [ [ ACF-parameter-attributes ] ] parameter-name
        , ...);

[ [ ACF-function-attributes ] ] function-name(
    [comm_status [ , ACF-parameter-attributes ] ] error_status_t name
    , ...);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*ACF-function-attributes* 
</dt> <dd>

Specifica zero o più attributi della funzione ACF, ad esempio **\[ comm \_ status \]** e **\[** [**nocode.**](nocode.md) **\]** Gli attributi della funzione sono racchiusi tra parentesi quadre. A una funzione possono essere applicati zero o più attributi. Separare più attributi di funzione con virgole. Si noti che **\[ se lo stato \_ comm \]** viene visualizzato come attributo di funzione, non può essere visualizzato anche come attributo di parametro.

</dd> <dt>

*function-name* 
</dt> <dd>

Specifica il nome della funzione come definito nel file IDL.

</dd> <dt>

*ACF-parameter-attributes* 
</dt> <dd>

Specifica gli attributi che si applicano a un parametro. Si noti che al parametro possono essere applicati zero, uno o più attributi. Separare più attributi di parametro con virgole. Gli attributi dei parametri sono racchiusi tra parentesi quadre. Gli attributi dei parametri IDL, ad esempio gli attributi direzionali, non sono consentiti in ACF. Si noti che se **\[ lo stato \_ comm \]** viene visualizzato come attributo di parametro, non può essere visualizzato anche come attributo di funzione.

</dd> <dt>

*parameter-name* 
</dt> <dd>

Specifica il parametro per la funzione come definito nel file IDL. Ogni parametro per la funzione deve essere specificato nella stessa sequenza, usando lo stesso nome definito nel file IDL.

</dd> </dl>

## <a name="remarks"></a>Commenti

**\[ L'attributo \_ \] comm status** può essere usato come attributo di funzione o come attributo di parametro, ma può essere visualizzato una sola volta per ogni funzione. Può essere applicato alla funzione o a un parametro in ogni funzione.

**\[ L'attributo \_ \] comm status** può essere applicato solo alle funzioni che restituiscono lo stato [**di errore del tipo \_ \_ t**](error-status-t.md). Quando si verifica un errore di comunicazione durante l'esecuzione della funzione, viene restituito un codice di errore.

Quando **\[ lo stato comm \_ \]** viene usato come attributo di parametro, il parametro deve essere definito nel file IDL e deve essere un parametro out di **\[** [](out-idl.md) **\]** tipo [**error status \_ \_ t**](error-status-t.md). Quando si verifica un errore di comunicazione durante l'esecuzione della funzione, il parametro viene impostato sul codice di errore. Quando la chiamata remota viene completata correttamente, la procedura imposta il valore .

È possibile che sia lo **\[ stato comm \_ \]** che gli attributi dello stato di errore vengano visualizzati in una singola funzione, come attributi di funzione o attributi **\[** [**\_**](fault-status.md) di **\]** parametro. Se entrambi gli attributi sono attributi di funzione o se si applicano allo stesso parametro e non si verifica alcun errore, la funzione o il parametro ha lo stato **di \_ errore \_ ok**. In caso contrario, contiene il valore **\[ appropriato per lo \_ stato \] comm** o **\[ \_ fault. \]** Poiché i valori restituiti **\[ per lo \_ stato \] comm** sono diversi dai valori restituiti per lo stato **\[ di \_ \]** errore, i valori restituiti vengono interpretati immediatamente.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[File di configurazione dell'applicazione (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**error \_ status \_ t**](error-status-t.md)
</dt> <dt>

[**stato di \_ errore**](fault-status.md)
</dt> <dt>

[**nocode**](nocode.md)
</dt> <dt>

[**in uscita**](out-idl.md)
</dt> </dl>

 

 




