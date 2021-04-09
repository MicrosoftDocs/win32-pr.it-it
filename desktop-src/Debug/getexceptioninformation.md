---
description: Recupera una descrizione indipendente dal computer di un'eccezione e le informazioni sullo stato del computer esistente per il thread quando si verifica l'eccezione. Questa funzione può essere chiamata solo dall'interno dell'espressione di filtro di un gestore di eccezioni.
ms.assetid: e982794a-d5f1-4fb4-a2b9-aa8da18cb8ae
title: GetExceptionInformation (macro)
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
ms.openlocfilehash: 243831a94a26b86df29d3a50413bfa9d6830a0e3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748890"
---
# <a name="getexceptioninformation-macro"></a>GetExceptionInformation (macro)

Recupera una descrizione indipendente dal computer di un'eccezione e le informazioni sullo stato del computer esistente per il thread quando si verifica l'eccezione. Questa funzione può essere chiamata solo dall'interno dell'espressione di filtro di un gestore di eccezioni.

> [!Note]  
> Il compilatore di ottimizzazione di Microsoft C/C++ interpreta questa funzione come una parola chiave e il suo utilizzo al di fuori della sintassi di gestione delle eccezioni appropriata genera un errore del compilatore.

 

## <a name="syntax"></a>Sintassi


```C++
LPEXCEPTION_POINTERS GetExceptionInformation(void);
```



## <a name="parameters"></a>Parametri

Questa macro non contiene parametri.

## <a name="return-value"></a>Valore restituito

Puntatore a una struttura [**di \_ puntatori di eccezione**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) che contiene puntatori alle due strutture seguenti:

-   [**Eccezione \_ di**](/windows/desktop/api/WinNT/ns-winnt-exception_record) Struttura di record che contiene una descrizione dell'eccezione.
-   Struttura del [**contesto**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) che contiene le informazioni sullo stato del computer.

## <a name="remarks"></a>Commenti

L'espressione di filtro (da cui viene chiamata la funzione) viene valutata se si verifica un'eccezione durante l'esecuzione del blocco **\_ \_ try** e determina se il blocco **\_ \_ except** viene eseguito.

L'espressione di filtro può richiamare una funzione di filtro. La funzione Filter non può chiamare **GetExceptionInformation**. Tuttavia, il valore restituito di **GetExceptionInformation** può essere passato come parametro a una funzione di filtro.

Per passare le informazioni sui [**\_ puntatori di eccezione**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) al blocco del gestore di eccezioni, l'espressione di filtro o la funzione di filtro deve copiare il puntatore o i dati nell'archiviazione sicura a cui il gestore può accedere in un secondo momento.

Nel caso di gestori annidati, ogni espressione di filtro viene valutata fino a quando non viene valutata come **\_ \_ gestore di esecuzione delle eccezioni** oppure **\_ \_ l'esecuzione dell'eccezione continua**. Ogni espressione di filtro può richiamare **GetExceptionInformation** per ottenere informazioni sull'eccezione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CONTESTO**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context)
</dt> <dt>

[**\_puntatori di eccezione**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers)
</dt> <dt>

[**RECORD di eccezione \_**](/windows/desktop/api/WinNT/ns-winnt-exception_record)
</dt> <dt>

[**GetExceptionCode**](getexceptioncode.md)
</dt> <dt>

[**GetXStateFeaturesMask**](/windows/desktop/api/WinBase/nf-winbase-getxstatefeaturesmask)
</dt> <dt>

[Funzioni di gestione delle eccezioni strutturate](structured-exception-handling-functions.md)
</dt> <dt>

[Cenni preliminari sulla gestione delle eccezioni strutturata](structured-exception-handling.md)
</dt> <dt>

[Abilita il supporto di Windows per Intel AVX](../win7appqual/enable-windows-7-support-for-intel-avx.md)
</dt> </dl>

 

 
