---
description: La classe COARefTime converte i tempi di riferimento tra i secondi e le unità da 100 nanosecondi.
ms.assetid: 724420fc-9252-468f-9516-174be0a82999
title: Classe COARefTime (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 569da24d4487a1c7259c71ac0e2cda3ae7f31a88b69a74575186bdeb3b21445b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087271"
---
# <a name="coareftime-class"></a>Classe COARefTime

![Gerarchia di classi coareftime](images/cutil05.png)

La `COARefTime` classe converte i tempi di riferimento tra i secondi e le unità di 100 nanosecondi.

Questa classe esegue la conversione tra tempi di riferimento compatibili con Automazione e tempi di riferimento compatibili con C/C++. Le interfacce compatibili con l'automazione usano **valori double** per rappresentare il tempo in secondi. Altre interfacce usano valori **LONGLONG** a 64 bit per rappresentare l'ora in unità da 100 nanosecondi. Per questi valori sono definiti i tipi seguenti:

``` syntax
typedef LONGLONG  REFERENCE_TIME;
typedef double    REFTIME;
```

I filtri possono usare `COARefTime` la classe per eseguire la conversione tra i due formati. Questa classe è derivata dalla [**classe CRefTime.**](creftime.md)



| Metodi pubblici                                          | Descrizione                                                           |
|---------------------------------------------------------|-----------------------------------------------------------------------|
| [**COARefTime**](coareftime-coareftime.md)             | Metodo del costruttore.                                                   |
| Operatori                                               | Descrizione                                                           |
| [**Doppia**](coareftime-double.md)                     | Converte l'ora di riferimento in **un valore** double.                    |
| [**TEMPO DI \_ RIFERIMENTO**](coareftime-reference-time.md)    | Esegue il cast dell'oggetto a un **valore REFERENCE \_ TIME.**                      |
| [**operatore =**](coareftime-operator-assign.md)        | Assegna una nuova ora di riferimento.                                         |
| [**operatore ==**](coareftime-operator-eq.md)           | Verifica l'uguaglianza tra due tempi di riferimento.                       |
| [**operatore !=**](cmediatype-operator-neq.md)          | Verifica la disuguaglianza tra due tempi di riferimento.                     |
| [**operatore <**](coareftime-operator-lt.md)         | Verifica se un'ora di riferimento è minore di un'altra.                     |
| [**operatore >**](coareftime-operator-gt.md)         | Verifica se un'ora di riferimento è maggiore di un'altra.                  |
| [**operatore <=**](coareftime-operator-lteq.md)      | Verifica se un'ora di riferimento è minore o uguale a un'altra.         |
| [**operatore >=**](coareftime-operator-gteq.md)      | Verifica se un'ora di riferimento è maggiore o uguale a un'altra.      |
| [**operatore +**](coareftime-operator-plus.md)          | Aggiunge due tempi di riferimento.                                             |
| [**operatore **](coareftime-operator-minus.md)         | Sottrae un'ora di riferimento da un'altra.                            |
| [**operatore +=**](coareftime-operator-plus-assign.md)  | Aggiunge due tempi di riferimento e assegna il risultato a questo oggetto .      |
| [**operatore =**](coareftime-operator-minus-assign.md) | Sottrae due volte di riferimento e assegna il risultato a questo oggetto . |
| [**Operatore \***](coareftime-operator-mult.md)         | Moltiplica un tempo di riferimento per un valore.                               |
| [**operatore /**](coareftime-operator-div.md)           | Divide un'ora di riferimento per un valore.                                  |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



 

 




