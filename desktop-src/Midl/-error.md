---
title: Opzione /error
description: L'opzione /error determina i tipi di controllo degli errori che verranno eseguiti dagli stub generati in fase di esecuzione.
ms.assetid: abd3616a-2d2c-4a7d-bf3a-c84a43387894
keywords:
- Opzione /error MIDL
topic_type:
- apiref
api_name:
- /error
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7af27de3d83171c8f1f89d0b860bf0b38ddfb6639a12bf40f90a58f06a273cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105631"
---
# <a name="error-switch"></a>Opzione /error

**L'opzione /error** determina i tipi di controllo degli errori che verranno eseguiti dagli stub generati in fase di esecuzione.

> [!Note]  
> Questa funzionalità è obsoleta e non è più supportata. È consigliabile usare [**l'opzione /robust.**](-robust.md)

 

``` syntax
midl /error { allocation | stub_data | ref | bounds_check | none | all }
```

## <a name="switch-options"></a>Opzioni switch

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="allocation"></span><span id="ALLOCATION"></span>

<span id="allocation"></span><span id="ALLOCATION"></span>allocation****


</dt> <dd>

Controlla se [**midl \_ user \_ allocate**](midl-user-allocate-1.md) restituisce **un valore NULL,** che indica un errore di memoria insufficiente.

</dd> <dt>

<span id="stub_data"></span><span id="STUB_DATA"></span>

<span id="stub_data"></span><span id="STUB_DATA"></span>dati \_ stub****


</dt> <dd>

Genera uno stub che rileva le eccezioni di unmarshaling sul lato server e le propaga di nuovo al client.

</dd> <dt>

<span id="ref"></span><span id="REF"></span>

<span id="ref"></span><span id="REF"></span>ref****


</dt> <dd>

Genera codice che esegue un controllo in fase di esecuzione per garantire che non venga passato alcun puntatore di riferimento **NULL** agli stub client e genera un'eccezione RPC X NULL REF POINTER se ne \_ trova \_ \_ \_ uno.

</dd> <dt>

<span id="bounds_check"></span><span id="BOUNDS_CHECK"></span>

<span id="bounds_check"></span><span id="BOUNDS_CHECK"></span>controllo dei \_ limiti****


</dt> <dd>

Controlla le dimensioni delle matrici variabili e variabili in base alla specifica della lunghezza della trasmissione.

</dd> <dt>

<span id="none"></span><span id="NONE"></span>

<span id="none"></span><span id="NONE"></span>none****


</dt> <dd>

Non esegue alcun controllo degli errori.

</dd> <dt>

<span id="all"></span><span id="ALL"></span>

<span id="all"></span><span id="ALL"></span>all****


</dt> <dd>

Esegue tutti i controlli degli errori. Efficace con MIDL versione 5.0, si tratta di un'opzione del compilatore predefinita.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

**L'opzione /error** seleziona il numero di controlli degli errori che verranno eseguiti dai file stub generati. Efficace con MIDL versione 5.0, l'impostazione predefinita è **/error all**.

Gli errori di enumerazione verificati (per impostazione predefinita in tutte le versioni di MIDL) sono errori di troncamento causati dalla conversione tra tipi di enumerazione **long** (integer a 32 bit) e tipi **enum** brevi (la rappresentazione dei dati di rete dell'enumerazione [**)**](enum.md)e il numero di identificatori in un'enumerazione superiore a 32.767.

Il controllo degli errori di accesso alla memoria (anche per impostazione predefinita in tutte le versioni di MIDL) è per i puntatori che superano la fine del buffer nel codice di marshalling e per le matrici conformi la cui dimensione è minore di zero. Usare il flag **di controllo /error bounds \_** per verificare la presenza di altri limiti di matrice non validi.

Quando si specifica **l'allocazione /error**, gli stub includono codice che genera un'eccezione quando [**midl \_ user \_ allocate**](midl-user-allocate-1.md) restituisce 0.

**L'opzione /error stub \_ data** impedisce l'arresto anomalo del server dei dati del client durante l'unmarshaling, offrendo in modo efficace un metodo più affidabile per gestire l'operazione di unmarshaling.

A differenza di Windows 2000, il motore di marshalling NDR di runtime sottostante esegue la maggior parte di questi controlli. Ciò significa che se si usa una delle modalità completamente interpretate ([**/Oi**](-oi.md), **/Oif**) della generazione di stub, la scelta di opzioni di controllo degli errori diverse non avrà un effetto contrassegnato sulle prestazioni.

## <a name="examples"></a>Esempio

**midl /error allocation filename.idl**

**midl /error none filename.idl**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi generale della riga di comando MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/robust**](-robust.md)
</dt> </dl>

 

 




