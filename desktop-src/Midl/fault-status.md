---
title: attributo fault_status
description: L'attributo \ fault \_ status \ ACF specifica che un codice di errore di tipo Error \_ status \_ t indica un errore della procedura remota, anziché altri tipi di problemi, ad esempio gli errori di comunicazione.
ms.assetid: 9da7bd3d-cef0-4ad4-b2a4-3f8aa156e8e0
keywords:
- attributo fault_status MIDL
topic_type:
- apiref
api_name:
- fault_status
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 134d9772e167fe63e133d569b9985a7735668d3c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718076"
---
# <a name="fault_status-attribute"></a>\_attributo stato errore

L'attributo ACF **\[ \_ dello stato \]** di errore specifica che un codice di errore di tipo [**Error \_ status \_ t**](error-status-t.md) indica un errore della procedura remota, anziché altri tipi di problemi, ad esempio gli errori di comunicazione.

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

*ACF-Function-Attributes* 
</dt> <dd>

Specifica zero o più attributi di funzione ACF, ad esempio **\[ \_ lo stato \] di errore** e **\[** [**NoCode**](nocode.md) **\]** . Gli attributi della funzione sono racchiusi tra parentesi quadre. Si noti che è possibile applicare zero o più attributi a una funzione. Separare più attributi di funzione con virgole. Si noti inoltre che se **\[ \_ lo \] stato di errore** viene visualizzato come attributo di funzione, non può essere visualizzato anche come attributo di parametro.

</dd> <dt>

*Nome funzione* 
</dt> <dd>

Specifica il nome della funzione come definito nel file IDL.

</dd> <dt>

*ACF-parametri-attributi* 
</dt> <dd>

Specifica gli attributi che si applicano a un parametro. Si noti che è possibile applicare zero o più attributi al parametro. Gli attributi di parametro sono racchiusi tra parentesi quadre. Separare più attributi di parametro con virgole. Gli attributi dei parametri IDL, ad esempio gli attributi direzionali, non sono consentiti in ACF. Si noti che se **\[ \_ lo \] stato di errore** viene visualizzato come attributo di parametro, non può essere visualizzato anche come attributo di funzione.

</dd> <dt>

*Nome parametro* 
</dt> <dd>

Specifica il parametro per la funzione come definito nel file IDL. Ogni parametro per la funzione deve essere specificato nella stessa sequenza, usando lo stesso nome definito nel file IDL.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'attributo **\[ fault \_ status \]** può essere utilizzato come attributo di funzione o come attributo di parametro, ma può essere visualizzato solo una volta per ogni funzione. Può essere applicato alla funzione stessa o a un parametro in ogni funzione.

L'attributo **\[ fault \_ status \]** può essere applicato solo a funzioni che restituiscono lo [**stato di errore del tipo \_ \_ t**](error-status-t.md). Quando la procedura remota ha esito negativo in modo che causi la restituzione di un errore PDU, viene restituito un codice di errore.

Quando **\[ \_ lo stato \] di errore** viene usato come attributo di parametro, il parametro deve essere un **\[** parametro [**out**](out-idl.md) **\]** di tipo [**Error \_ status \_ t**](error-status-t.md). Se si verifica un errore del server, il parametro viene impostato sul codice di errore. Quando la chiamata remota viene completata correttamente, la procedura imposta il valore.

Non è necessario specificare il parametro associato all'attributo **\[ \_ dello stato \] di errore** nel file IDL. Quando il parametro non viene specificato, viene generato un nuovo parametro [**out**](out-idl.md) di tipo [**Error \_ status \_ t**](error-status-t.md) dopo l'ultimo parametro definito nel file IDL DCE.

È possibile che lo **\[ \_ stato \] di errore** e **\[** gli attributi di [**\_ stato di comunicazione**](comm-status.md) siano **\]** visualizzati in una singola funzione, come attributi di funzione o attributi di parametro. Se entrambi gli attributi sono attributi di funzione o se si applicano allo stesso parametro e non si verificano errori, la funzione o il parametro presenta lo stato di errore del valore **\_ \_ OK**. In caso contrario, contiene il valore del codice di stato appropriato. Poiché i valori restituiti per **\[ \_ lo \] stato di errore** sono diversi dai valori restituiti per **\[ \_ lo stato \] di comunicazione**, i valori restituiti vengono immediatamente interpretati.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[File di configurazione dell'applicazione (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**stato di comunicazione \_**](comm-status.md)
</dt> <dt>

[**stato di errore \_ \_ t**](error-status-t.md)
</dt> <dt>

[**NoCode**](nocode.md)
</dt> <dt>

[**out**](out-idl.md)
</dt> </dl>

 

 




