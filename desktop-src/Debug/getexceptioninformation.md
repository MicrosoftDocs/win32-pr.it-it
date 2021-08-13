---
description: Recupera una descrizione indipendente dal computer di un'eccezione e informazioni sullo stato del computer esistente per il thread quando si verifica l'eccezione. Questa funzione può essere chiamata solo dall'interno dell'espressione di filtro di un gestore eccezioni.
ms.assetid: e982794a-d5f1-4fb4-a2b9-aa8da18cb8ae
title: Macro GetExceptionInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetExceptionInformation
api_type:
- NA
api_location: ''
ms.openlocfilehash: 425cfbe10ac2ee66f10e016489ff070b67b6fc243a472f95b4f5809724998a21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119279221"
---
# <a name="getexceptioninformation-macro"></a>Macro GetExceptionInformation

Recupera una descrizione indipendente dal computer di un'eccezione e informazioni sullo stato del computer esistente per il thread quando si verifica l'eccezione. Questa funzione può essere chiamata solo dall'interno dell'espressione di filtro di un gestore eccezioni.

> [!Note]  
> Il compilatore di ottimizzazione di Microsoft C/C++ interpreta questa funzione come una parola chiave e il relativo uso al di fuori della sintassi di gestione delle eccezioni appropriata genera un errore del compilatore.

 

## <a name="syntax"></a>Sintassi


```C++
LPEXCEPTION_POINTERS GetExceptionInformation(void);
```



## <a name="parameters"></a>Parametri

Questa macro non ha parametri.

## <a name="return-value"></a>Valore restituito

Puntatore a una [**struttura \_ EXCEPTION POINTERS**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) che contiene puntatori alle due strutture seguenti:

-   [**EXCEPTION \_ Struttura RECORD**](/windows/desktop/api/WinNT/ns-winnt-exception_record) contenente una descrizione dell'eccezione.
-   [**Struttura CONTEXT**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) che contiene le informazioni sullo stato del computer.

## <a name="remarks"></a>Commenti

L'espressione di filtro (da cui viene chiamata la funzione) viene valutata se si **\_ \_** verifica un'eccezione durante l'esecuzione del blocco **\_ \_ try** e determina se viene eseguito o meno il blocco except.

L'espressione di filtro può richiamare una funzione di filtro. La funzione di filtro non può chiamare **GetExceptionInformation.** Tuttavia, il valore restituito di **GetExceptionInformation** può essere passato come parametro a una funzione di filtro.

Per passare le informazioni [**EXCEPTION \_ POINTERS**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) al blocco del gestore eccezioni, l'espressione di filtro o la funzione di filtro deve copiare il puntatore o i dati in un archivio sicuro a cui il gestore può accedere in un secondo momento.

Nel caso di gestori annidati, ogni espressione di filtro viene valutata fino a quando un'espressione non viene valutata come **EXCEPTION \_ EXECUTE \_ HANDLER** o **EXCEPTION CONTINUE \_ \_ EXECUTION.** Ogni espressione di filtro può richiamare **GetExceptionInformation per** ottenere informazioni sull'eccezione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>          |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Contesto**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context)
</dt> <dt>

[**PUNTATORI \_ ALLE ECCEZIONI**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers)
</dt> <dt>

[**RECORD \_ ECCEZIONE**](/windows/desktop/api/WinNT/ns-winnt-exception_record)
</dt> <dt>

[**GetExceptionCode**](getexceptioncode.md)
</dt> <dt>

[**GetXStateFeaturesMask**](/windows/desktop/api/WinBase/nf-winbase-getxstatefeaturesmask)
</dt> <dt>

[Funzioni di gestione strutturata delle eccezioni](structured-exception-handling-functions.md)
</dt> <dt>

[Cenni preliminari sulla gestione strutturata delle eccezioni](structured-exception-handling.md)
</dt> <dt>

[Abilitare Windows supporto per Intel AVX](../win7appqual/enable-windows-7-support-for-intel-avx.md)
</dt> </dl>

 

 
