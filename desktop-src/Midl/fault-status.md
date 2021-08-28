---
title: fault_status attributo
description: L'attributo \ fault status\ ACF specifica che un codice di errore di tipo error status t indica un errore della procedura remota, anziché altri tipi di problemi, ad esempio errori \_ \_ di \_ comunicazione.
ms.assetid: 9da7bd3d-cef0-4ad4-b2a4-3f8aa156e8e0
keywords:
- fault_status attributo MIDL
topic_type:
- apiref
api_name:
- fault_status
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f5126c5ee089729089179fa99f881f1e236859e3111ed3937323eb8b122d2fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013909"
---
# <a name="fault_status-attribute"></a>attributo di \_ stato dell'errore

**\[ L'attributo \_ \]** ACF dello stato di errore specifica che un codice di errore di tipo [**error status \_ \_ t**](error-status-t.md) indica un errore della procedura remota, anziché altri tipi di problemi, ad esempio gli errori di comunicazione.

``` syntax
[fault_status [ , ACF-function-attributes ] ] function-name(
    [ [ ACF-parameter-attributes ] ] parameter-name
    , ... );

[ [ ACF-function-attributes ] ] function-name(
    [fault_status [ , ACF-parameter-attributes ] ] parameter-name
    , ... );
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*ACF-function-attributes* 
</dt> <dd>

Specifica zero o più attributi della funzione ACF, ad esempio **\[ lo stato di \_ errore \]** e **\[** [**nocode.**](nocode.md) **\]** Gli attributi della funzione sono racchiusi tra parentesi quadre. Si noti che è possibile applicare zero o più attributi a una funzione. Separare più attributi di funzione con virgole. Si noti anche che se **\[ lo stato \_ dell'errore \]** viene visualizzato come attributo di funzione, non può essere visualizzato anche come attributo di parametro.

</dd> <dt>

*function-name* 
</dt> <dd>

Specifica il nome della funzione come definito nel file IDL.

</dd> <dt>

*ACF-parameter-attributes* 
</dt> <dd>

Specifica gli attributi applicabili a un parametro. Si noti che è possibile applicare zero o più attributi al parametro . Gli attributi dei parametri sono racchiusi tra parentesi quadre. Separare più attributi di parametro con virgole. Gli attributi dei parametri IDL, ad esempio gli attributi direzionali, non sono consentiti in ACF. Si noti che **\[ se lo stato \_ dell'errore \]** viene visualizzato come attributo di parametro, non può essere visualizzato anche come attributo di funzione.

</dd> <dt>

*parameter-name* 
</dt> <dd>

Specifica il parametro per la funzione come definito nel file IDL. Ogni parametro per la funzione deve essere specificato nella stessa sequenza, usando lo stesso nome definito nel file IDL.

</dd> </dl>

## <a name="remarks"></a>Commenti

**\[ L'attributo fault \_ status \]** può essere usato come attributo di funzione o come attributo di parametro, ma può essere visualizzato una sola volta per ogni funzione. Può essere applicato alla funzione stessa o a un parametro in ogni funzione.

**\[ L'attributo di \_ stato \]** dell'errore può essere applicato solo alle funzioni che restituiscono lo stato [**di errore di tipo \_ \_ t**](error-status-t.md). Quando la procedura remota non riesce in modo da restituire una PDU di errore, viene restituito un codice di errore.

Quando **\[ lo stato \_ di \]** errore viene usato come attributo di parametro, il parametro deve essere un **\[** [**parametro out**](out-idl.md) di **\]** tipo error status [**\_ \_ t**](error-status-t.md). Se si verifica un errore del server, il parametro viene impostato sul codice di errore. Al termine della chiamata remota, la procedura imposta il valore .

Il parametro associato **\[ all'attributo di \_ stato \]** dell'errore non deve essere specificato nel file IDL. Quando il parametro non viene specificato, viene generato un nuovo [**parametro out**](out-idl.md) di tipo error [**status \_ \_ t**](error-status-t.md) dopo l'ultimo parametro definito nel file IDL DCE.

È possibile che gli attributi **\[ di stato \_ \] dell'errore** e di stato comm vengano visualizzati in una singola funzione, sia come attributi di funzione che come attributi **\[** [**\_**](comm-status.md) **\]** di parametro. Se entrambi gli attributi sono attributi di funzione o se si applicano allo stesso parametro e non si verifica alcun errore, la funzione o il parametro ha il valore **error \_ status \_ ok**. In caso contrario, contiene il valore del codice di stato appropriato. Poiché i valori **\[ restituiti per \_ lo stato di \]** errore sono diversi dai valori restituiti per lo stato **\[ comm \_ \]**, i valori restituiti vengono interpretati facilmente.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[File di configurazione dell'applicazione (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**Stato \_ comm**](comm-status.md)
</dt> <dt>

[**stato \_ \_ dell'errore t**](error-status-t.md)
</dt> <dt>

[**nocode**](nocode.md)
</dt> <dt>

[**in uscita**](out-idl.md)
</dt> </dl>

 

 




