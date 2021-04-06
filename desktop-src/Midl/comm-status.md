---
title: attributo comm_status
description: L'attributo \ Comm \_ status \ ACF causa la restituzione di un codice di errore quando si verifica un errore di comunicazione durante l'esecuzione di una funzione.
ms.assetid: 3ea9ce62-8bd4-40fe-b838-bfebd52b5a15
keywords:
- attributo comm_status MIDL
topic_type:
- apiref
api_name:
- comm_status
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd4952d03a80dbbffb135043d024b0c0eb18966f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718778"
---
# <a name="comm_status-attribute"></a>\_attributo status di comunicazione

L'attributo di **\[ \_ stato \]** di comunicazione ACF causa la restituzione di un codice di errore quando si verifica un errore di comunicazione durante l'esecuzione di una funzione.

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

*ACF-Function-Attributes* 
</dt> <dd>

Specifica zero o più attributi della funzione ACF, ad esempio **\[ \_ stato \] di comunicazione** e **\[** [**NoCode**](nocode.md) **\]** . Gli attributi della funzione sono racchiusi tra parentesi quadre. È possibile applicare zero o più attributi a una funzione. Separare più attributi di funzione con virgole. Si noti che se **\[ \_ lo \] stato di comunicazione** viene visualizzato come attributo di funzione, non può essere visualizzato anche come attributo di parametro.

</dd> <dt>

*Nome funzione* 
</dt> <dd>

Specifica il nome della funzione come definito nel file IDL.

</dd> <dt>

*ACF-parametri-attributi* 
</dt> <dd>

Specifica gli attributi che si applicano a un parametro. Si noti che è possibile applicare zero, uno o più attributi al parametro. Separare più attributi di parametro con virgole. Gli attributi di parametro sono racchiusi tra parentesi quadre. Gli attributi dei parametri IDL, ad esempio gli attributi direzionali, non sono consentiti in ACF. Si noti che se **\[ \_ lo \] stato di comunicazione** viene visualizzato come attributo di parametro, non può essere visualizzato anche come attributo di funzione.

</dd> <dt>

*Nome parametro* 
</dt> <dd>

Specifica il parametro per la funzione come definito nel file IDL. Ogni parametro per la funzione deve essere specificato nella stessa sequenza, usando lo stesso nome definito nel file IDL.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'attributo **\[ \_ status \] di comunicazione** può essere usato come attributo di funzione o come attributo di parametro, ma può essere visualizzato solo una volta per ogni funzione. Può essere applicato alla funzione o a un parametro in ogni funzione.

L'attributo **\[ \_ status \] di comunicazione** può essere applicato solo a funzioni che restituiscono lo stato di errore del tipo [**\_ \_ t**](error-status-t.md). Quando si verifica un errore di comunicazione durante l'esecuzione della funzione, viene restituito un codice di errore.

Quando **\[ \_ lo stato \] di comunicazione** viene usato come attributo di parametro, il parametro deve essere definito nel file IDL e deve essere un **\[** parametro [**out**](out-idl.md) **\]** di tipo [**Error \_ status \_ t**](error-status-t.md). Quando si verifica un errore di comunicazione durante l'esecuzione della funzione, il parametro viene impostato sul codice di errore. Quando la chiamata remota viene completata correttamente, il valore viene impostato dalla procedura.

È possibile che sia lo **\[ \_ \] stato di comunicazione** che **\[** gli attributi di [**\_ stato di errore**](fault-status.md) **\]** vengano visualizzati in una singola funzione, come attributi di funzione o attributi di parametro. Se entrambi gli attributi sono attributi di funzione o se si applicano allo stesso parametro e non si verificano errori, la funzione o il parametro presenta lo stato di errore del valore **\_ \_ OK**. In caso contrario, contiene lo **\[ \_ stato \] di comunicazione** appropriato o il valore **\[ \_ dello stato \] di errore** . Poiché i valori restituiti per **\[ \_ lo \] stato di comunicazione** sono diversi dai valori restituiti per **\[ \_ lo stato \] di errore**, i valori restituiti vengono immediatamente interpretati.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[File di configurazione dell'applicazione (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**stato di errore \_ \_ t**](error-status-t.md)
</dt> <dt>

[**stato di errore \_**](fault-status.md)
</dt> <dt>

[**NoCode**](nocode.md)
</dt> <dt>

[**out**](out-idl.md)
</dt> </dl>

 

 




