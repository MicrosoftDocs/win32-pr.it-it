---
title: opzione/error
description: L'opzione/error determina i tipi di controllo degli errori che gli stub generati eseguiranno in fase di esecuzione.
ms.assetid: abd3616a-2d2c-4a7d-bf3a-c84a43387894
keywords:
- /Error switch MIDL
topic_type:
- apiref
api_name:
- /error
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f84a56c1ae3d57ab1931ec175aa8dc9010ea6b8a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104397882"
---
# <a name="error-switch"></a>opzione/error

L'opzione **/Error** determina i tipi di controllo degli errori che gli stub generati eseguiranno in fase di esecuzione.

> [!Note]  
> Questa funzionalità è obsoleta e non è più supportata. È consigliabile usare l'opzione [**/robust**](-robust.md) .

 

``` syntax
midl /error { allocation | stub_data | ref | bounds_check | none | all }
```

## <a name="switch-options"></a>Opzioni switch

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="allocation"></span><span id="ALLOCATION"></span>

<span id="allocation"></span><span id="ALLOCATION"></span>allocazione * * * *


</dt> <dd>

Verifica se [**l' \_ utente MIDL \_ allocate**](midl-user-allocate-1.md) restituisce un valore **null** , che indica un errore di memoria insufficiente.

</dd> <dt>

<span id="stub_data"></span><span id="STUB_DATA"></span>

<span id="stub_data"></span><span id="STUB_DATA"></span>\_dati Stub * * * *


</dt> <dd>

Genera uno stub che rileva le eccezioni di unmarshalling sul lato server e le propaga nuovamente al client.

</dd> <dt>

<span id="ref"></span><span id="REF"></span>

<span id="ref"></span><span id="REF"></span>Ref * * * *


</dt> <dd>

Genera codice che esegue un controllo in fase di esecuzione per garantire che nessun puntatori di riferimento **null** venga passato agli stub client e genera un' \_ eccezione del \_ puntatore ref null di RPC X \_ \_ se ne trova uno.

</dd> <dt>

<span id="bounds_check"></span><span id="BOUNDS_CHECK"></span>

<span id="bounds_check"></span><span id="BOUNDS_CHECK"></span>controllo dei limiti \_ * * * *


</dt> <dd>

Verifica le dimensioni delle matrici variabili e variabili conformi rispetto alla specifica della lunghezza di trasmissione.

</dd> <dt>

<span id="none"></span><span id="NONE"></span>

<span id="none"></span><span id="NONE"></span>nessuno * * * *


</dt> <dd>

Non esegue alcun controllo degli errori.

</dd> <dt>

<span id="all"></span><span id="ALL"></span>

<span id="all"></span><span id="ALL"></span>tutti i * * * *


</dt> <dd>

Esegue tutto il controllo degli errori. Efficace con MIDL versione 5,0, si tratta di un'opzione predefinita del compilatore.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

L'opzione **/Error** consente di selezionare il numero di verifiche degli errori che i file stub generati eseguiranno. A partire da MIDL versione 5,0, l'impostazione predefinita è **/Error all**.

Gli errori di enumerazione controllati (per impostazione predefinita in tutte le versioni di MIDL) sono errori di troncamento causati dalla conversione tra tipi di **enumerazione Long** (interi a 32 bit) e tipi di **enumerazione Short** (la rappresentazione di dati di rete di [**enum**](enum.md)) e il numero di identificatori in un'enumerazione che supera 32.767.

Il controllo degli errori di accesso alla memoria (anche per impostazione predefinita in tutte le versioni di MIDL) è per i puntatori che superano la fine del buffer nel codice di marshalling e per le matrici conformi la cui dimensione è minore di zero. Usare il flag di **\_ controllo dei limiti di/Error** per verificare la presenza di altri limiti di matrice non validi.

Quando si specifica l' **allocazione/Error**, gli stub includono il codice che genera un'eccezione quando l' [**\_ utente MIDL \_ allocate**](midl-user-allocate-1.md) restituisce 0.

L'opzione **/Error Stub \_ Data** impedisce che i dati client arrestino in modo anomalo il server durante l'esecuzione dell'unmarshalling, fornendo un metodo più affidabile per gestire l'operazione di unmarshalling.

A partire da Windows 2000, il motore di marshalling del recapito di run-time sottostante esegue la maggior parte di questi controlli. Ciò significa che se si utilizza una delle modalità completamente interpretate ([**/OI**](-oi.md), **/OIF**) della generazione Stub, la scelta di diverse opzioni di controllo degli errori non avrà un effetto marcato sulle prestazioni.

## <a name="examples"></a>Esempio

**nome file di allocazione/Error MIDL. idl**

**MIDL/error none nomefile. idl**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md)
</dt> <dt>

[**/Robust**](-robust.md)
</dt> </dl>

 

 




