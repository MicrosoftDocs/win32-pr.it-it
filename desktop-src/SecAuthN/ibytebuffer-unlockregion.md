---
description: 'Rimuove la restrizione di accesso in un intervallo di byte precedentemente limitato utilizzando IByteBuffer:: LockRegion.'
ms.assetid: f2a1162e-7fc7-4a55-befb-0b017edb9fe2
title: 'Metodo IByteBuffer:: UnlockRegion (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.UnlockRegion
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 92e49ba000177326ad14d3b83002613a15e96e18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968295"
---
# <a name="ibytebufferunlockregion-method"></a>Metodo IByteBuffer:: UnlockRegion

\[Il metodo **UnlockRegion** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. L'interfaccia [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) fornisce funzionalità simili.\]

Il metodo **UnlockRegion** rimuove la restrizione di accesso in un intervallo di byte precedentemente limitato tramite [**IByteBuffer:: LockRegion**](ibytebuffer-lockregion.md).

## <a name="syntax"></a>Sintassi


```C++
HRESULT UnlockRegion(
  [in] LONG libOffset,
  [in] LONG cb,
  [in] LONG dwLockType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*libOffset* \[ in\]
</dt> <dd>

Offset di byte per l'inizio dell'intervallo.

</dd> <dt>

*CB* \[ in\]
</dt> <dd>

Lunghezza, in byte, dell'intervallo da limitare.

</dd> <dt>

*dwLockType* \[ in\]
</dt> <dd>

Restrizioni di accesso inserite in precedenza nell'intervallo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è un valore **HRESULT**. Il valore S \_ OK indica che la chiamata è stata eseguita correttamente.

## <a name="remarks"></a>Commenti

Il metodo **IByteBuffer:: UnlockRegion** Sblocca un'area precedentemente bloccata usando il metodo [**IByteBuffer:: LockRegion**](ibytebuffer-lockregion.md) . Le aree bloccate devono essere sbloccate in seguito in modo esplicito chiamando **IByteBuffer:: UnlockRegion** con esattamente gli stessi valori per i parametri *libOffset*, *CB* e *dwLockType* . L'area deve essere sbloccata prima che il flusso venga rilasciato. Due aree adiacenti non possono essere bloccate separatamente e quindi sbloccate con una singola chiamata di sblocco.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato lo sblocco di un intervallo di byte.


```C++
HRESULT  hr;

// Unlock a region.
hr = pIByteBuff->UnlockRegion(0, 10, LOCK_EXCLUSIVE);
if (FAILED(hr))
  printf("Failed IByteBuffer::UnlockRegion\n");
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| Fine del supporto client<br/>    | Windows XP<br/>                                                                   |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Scardssp. h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Scardssp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ IByteBuffer è definito come E126F8FE-A7AF-11D0-B88A-00C04FD424B9<br/>          |



 

