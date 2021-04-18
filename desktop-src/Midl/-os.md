---
title: Opzione/OS
description: L'opzione/OS specifica il metodo in modalità mista per il marshalling del codice stub passato tra client e server.
ms.assetid: dc5cafbb-dcc6-4fcb-a04f-1bc9720a13cb
keywords:
- /OS switch MIDL
topic_type:
- apiref
api_name:
- /Os
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbbef54501e195c91bdcc0cec8045f2eec763820
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299051"
---
# <a name="os-switch"></a>Opzione/OS

L'opzione **/OS** specifica il metodo in modalità mista per il marshalling del codice stub passato tra client e server.

``` syntax
midl /Os
```

## <a name="switch-options"></a>Opzioni switch

Questa opzione non ha parametri.

## <a name="remarks"></a>Commenti

Ci sono aspetti importanti da considerare prima di decidere il metodo per il marshalling del codice. Questi problemi riguardano le dimensioni e le prestazioni. Il compilatore MIDL fornisce due metodi per il marshalling del codice: modalità mista (**/OS**) e completamente interpretato ([**/OI**](-oi.md)). Il metodo completamente interpretato esegue il marshalling dei dati completamente offline. In questo modo si riduce considerevolmente le dimensioni del codice dello stub, ma si riducono anche le prestazioni.

Usare la modalità predefinita MIDL **/Oicf** /robust per tutti gli scopi diversi dalla compatibilità con le versioni precedenti. Questa modalità è la modalità standard sicura del compilatore MIDL; tutte le altre modalità devono essere utilizzate solo dopo un'attenta considerazione per le implicazioni di sicurezza, con la consapevolezza che le future estensioni verranno implementate solo per la modalità predefinita. In modalità mista, il compilatore esegue il marshalling di alcuni parametri inline negli stub generati. Anche se ciò comporta dimensioni di stub più grandi, può offrire prestazioni migliori.

MIDL fornisce supporto completo per le matrici multidimensionali e i puntatori di dimensioni multidimensionali solo in modalità [**/Oicf**](-oi.md) . Nelle modalità **/OS** e **/OI** il compilatore supporta i casi semplici, ad esempio le matrici a dimensione fissa. L'utilizzo di matrici multidimensionali in modalità **/OS** o **/OI** può causare parametri di cui non è stato effettuato il marshalling correttamente. Microsoft consiglia di utilizzare l'opzione della riga di comando **/Oicf** quando l'interfaccia definisce parametri che sono matrici multidimensionali o puntatori di dimensioni multidimensionali.

Per definire ulteriormente il livello di gradazione nel modo in cui viene effettuato il marshalling dei dati, questa versione di RPC fornisce un \[ attributo [**optimize**](optimize.md) \] . Questo attributo viene usato come attributo dell'interfaccia ACF o attributo Operation per selezionare la modalità di marshalling.

## <a name="examples"></a>Esempio

**MIDL/OS nomefile. idl**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md)
</dt> <dt>

[**/OI**](-oi.md)
</dt> <dt>

[**ottimizzare**](optimize.md)
</dt> <dt>

[**/No \_ Format \_ opz**](-no-format-opt.md)
</dt> </dl>

 

 




