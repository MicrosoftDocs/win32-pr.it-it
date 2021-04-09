---
description: Indica se il \_ \_ blocco try di un gestore di terminazione è terminato normalmente. La funzione può essere chiamata solo dall'interno del \_ \_ blocco finally di un gestore di terminazione.
ms.assetid: 0ddaef1f-03f0-45fc-9c5e-8d6a26a73245
title: AbnormalTermination (macro)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AbnormalTermination
api_type:
- NA
api_location: ''
ms.openlocfilehash: 7c4869f36d8ba70c8dcd8ca526949d489f455e8c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966286"
---
# <a name="abnormaltermination-macro"></a>AbnormalTermination (macro)

Indica se il blocco **\_ \_ try** di un gestore di terminazione è terminato normalmente. La funzione può essere chiamata solo dall'interno del blocco **\_ \_ finally** di un gestore di terminazione.

> [!Note]  
> Il compilatore di ottimizzazione di Microsoft C/C++ interpreta questa funzione come una parola chiave e il suo utilizzo al di fuori della sintassi di gestione delle eccezioni appropriata genera un errore del compilatore.

 

## <a name="syntax"></a>Sintassi


```C++
BOOL AbnormalTermination(void);
```



## <a name="parameters"></a>Parametri

Questa macro non contiene parametri.

## <a name="return-value"></a>Valore restituito

Se il blocco **\_ \_ try** termina in modo anomalo, il valore restituito è diverso da zero.

Se il blocco **\_ \_ try** termina normalmente, il valore restituito è zero.

## <a name="remarks"></a>Commenti

Il blocco **\_ \_ try** termina normalmente solo se l'esecuzione lascia il blocco in sequenza dopo l'esecuzione dell'ultima istruzione nel blocco. Le istruzioni, ad esempio **return**, **goto**, **continue** o **break**, che fanno sì che l'esecuzione lasci il blocco **\_ \_ try** causando una chiusura anomala del blocco. Questa situazione si verifica anche se tale istruzione rappresenta l'ultima istruzione nel blocco **\_ \_ try** .

Una chiusura anomala di un blocco **\_ \_ try** causa la ricerca all'indietro di tutti gli stack frame da parte del sistema per determinare se è necessario chiamare i gestori di terminazione. Questo può comportare l'esecuzione di centinaia di istruzioni, quindi è importante evitare la chiusura anomala di un blocco **\_ \_ try** a causa di un'istruzione **return**, **goto**, **continue** o **break** . Si noti che queste istruzioni non generano un'eccezione, anche se la chiusura è anomala.

Per evitare la chiusura anomala, l'esecuzione deve proseguire fino alla fine del blocco. È anche possibile eseguire l'istruzione **\_ \_ Leave** . L'istruzione **\_ \_ Leave** consente la chiusura immediata del blocco **\_ \_ try** senza causare la terminazione anomala e la riduzione delle prestazioni. Controllare la documentazione del compilatore per determinare se l'istruzione **\_ \_ Leave** è supportata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di gestione delle eccezioni strutturate](structured-exception-handling-functions.md)
</dt> <dt>

[Cenni preliminari sulla gestione delle eccezioni strutturata](structured-exception-handling.md)
</dt> </dl>

 

 




