---
description: Limita l'accesso a un intervallo di byte specificato nell'oggetto buffer.
ms.assetid: 7bcb3c1e-5739-41f7-a3aa-2943542943ed
title: 'Metodo IByteBuffer:: LockRegion (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.LockRegion
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: ae227d11892b604ab1382cb328dc492e4596f278
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233280"
---
# <a name="ibytebufferlockregion-method"></a>Metodo IByteBuffer:: LockRegion

\[Il metodo **LockRegion** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. L'interfaccia [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) fornisce funzionalità simili.\]

Il metodo **LockRegion** limita l'accesso a un intervallo di byte specificato nell'oggetto buffer.

## <a name="syntax"></a>Sintassi


```C++
HRESULT LockRegion(
  [in] LONG libOffset,
  [in] LONG cb,
  [in] LONG dwLockType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*libOffset* \[ in\]
</dt> <dd>

Integer che specifica l'offset di byte per l'inizio dell'intervallo.

</dd> <dt>

*CB* \[ in\]
</dt> <dd>

Integer che specifica la lunghezza dell'intervallo, in byte, da limitare.

</dd> <dt>

*dwLockType* \[ in\]
</dt> <dd>

Specifica le restrizioni richieste per l'accesso all'intervallo. Può corrispondere a uno dei valori riportati nella tabella seguente.



| Valore                                                                                                                                                            | Significato                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LOCK_WRITE"></span><span id="lock_write"></span><dl> <dt>**\_scrittura blocco**</dt> </dl>             | L'intervallo di byte specificato può essere aperto e letto un numero qualsiasi di volte, ma non è consentito scrivere nell'intervallo bloccato, ad eccezione del proprietario a cui è stato concesso il blocco.<br/>                                                                      |
| <span id="LOCK_EXCLUSIVE"></span><span id="lock_exclusive"></span><dl> <dt>**BLOCCO \_ esclusivo**</dt> </dl> | La scrittura nell'intervallo di byte specificato non è consentita ad eccezione del proprietario a cui è stato concesso il blocco.<br/>                                                                                                                                       |
| <span id="LOCK_ONLYONCE"></span><span id="lock_onlyonce"></span><dl> <dt>**BLOCCA \_ ONLYONCE**</dt> </dl>    | Se questo blocco viene concesso, non è \_ possibile ottenere nessun altro blocco ONLYONCE di blocco sull'intervallo. In genere questo tipo di blocco è un alias per un altro tipo di blocco. In questo modo, le implementazioni specifiche possono avere un comportamento aggiuntivo associato a questo tipo di blocco.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è un valore **HRESULT**. Il valore S \_ OK indica che la chiamata è stata eseguita correttamente.

## <a name="remarks"></a>Commenti

L'intervallo di byte può estendersi oltre la fine corrente del flusso. Il blocco oltre la fine di un flusso è utile come metodo di comunicazione tra istanze diverse del flusso senza modificare i dati che fanno effettivamente parte del flusso.

È possibile supportare tre tipi di blocco: blocco per escludere altri writer, blocco per escludere altri Reader o writer e blocco che consente a un solo richiedente di ottenere un blocco sull'intervallo specificato, che è in genere un alias per uno degli altri due tipi di blocco. Un'istanza del flusso specificata può supportare uno dei primi due tipi o entrambi. Il tipo di blocco viene specificato da *dwLockType*, usando un valore dell'enumerazione [**LockType**](/windows/win32/api/objidl/ne-objidl-locktype) .

Qualsiasi area bloccata con **LockRegion** deve essere sbloccata in seguito in modo esplicito tramite la chiamata a [**IByteBuffer:: UnlockRegion**](ibytebuffer-unlockregion.md) con esattamente gli stessi valori per i parametri *libOffset*, *CB* e *dwLockType* . L'area deve essere sbloccata prima che il flusso venga rilasciato. Due aree adiacenti non possono essere bloccate separatamente e quindi sbloccate con una singola chiamata di sblocco.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato come limitare l'accesso a un intervallo di byte.


```C++
HRESULT  hr;

// Lock a region.
hr = pIByteBuff->LockRegion(0, 10, LOCK_EXCLUSIVE);
if (FAILED(hr))
  printf("Failed IByteBuffer::LockRegion\n");
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



 

