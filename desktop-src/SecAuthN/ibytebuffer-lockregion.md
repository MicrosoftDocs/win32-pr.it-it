---
description: Limita l'accesso a un intervallo specificato di byte nell'oggetto buffer.
ms.assetid: 7bcb3c1e-5739-41f7-a3aa-2943542943ed
title: Metodo IByteBuffer::LockRegion (Scardssp.h)
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
ms.openlocfilehash: 8575a568615a88552dd3907c7a5733c81dfe2d222661b4d8f9f82e32f0896ecf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119482681"
---
# <a name="ibytebufferlockregion-method"></a>Metodo IByteBuffer::LockRegion

\[Il **metodo LockRegion** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. [**L'interfaccia IStream**](/windows/desktop/api/objidl/nn-objidl-istream) offre funzionalità simili.\]

Il **metodo LockRegion** limita l'accesso a un intervallo specificato di byte nell'oggetto buffer.

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

*libOffset* \[ Pollici\]
</dt> <dd>

Intero che specifica l'offset di byte per l'inizio dell'intervallo.

</dd> <dt>

*cb* \[ Pollici\]
</dt> <dd>

Valore intero che specifica la lunghezza dell'intervallo, in byte, da impostare come limitato.

</dd> <dt>

*dwLockType* \[ Pollici\]
</dt> <dd>

Specifica le restrizioni richieste per l'accesso all'intervallo. Può trattarsi di uno dei valori nella tabella seguente.



| Valore                                                                                                                                                            | Significato                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LOCK_WRITE"></span><span id="lock_write"></span><dl> <dt>**LOCK \_ WRITE**</dt> </dl>             | L'intervallo di byte specificato può essere aperto e letto un numero qualsiasi di volte, ma la scrittura nell'intervallo bloccato non è consentita, ad eccezione del proprietario a cui è stato concesso questo blocco.<br/>                                                                      |
| <span id="LOCK_EXCLUSIVE"></span><span id="lock_exclusive"></span><dl> <dt>**BLOCCO \_ ESCLUSIVO**</dt> </dl> | La scrittura nell'intervallo di byte specificato non è consentita, ad eccezione del proprietario a cui è stato concesso questo blocco.<br/>                                                                                                                                       |
| <span id="LOCK_ONLYONCE"></span><span id="lock_onlyonce"></span><dl> <dt>**LOCK \_ ONLYONCE**</dt> </dl>    | Se questo blocco viene concesso, non è possibile ottenere altri blocchi LOCK \_ ONLYONCE nell'intervallo. In genere questo tipo di blocco è un alias per un altro tipo di blocco. Pertanto, implementazioni specifiche possono avere un comportamento aggiuntivo associato a questo tipo di blocco.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è **HRESULT.** Il valore S \_ OK indica che la chiamata è riuscita.

## <a name="remarks"></a>Commenti

L'intervallo di byte può estendersi oltre la fine corrente del flusso. Il blocco oltre la fine di un flusso è utile come metodo di comunicazione tra istanze diverse del flusso senza modificare i dati che fanno effettivamente parte del flusso.

Possono essere supportati tre tipi di blocco: blocco per escludere altri writer, blocco per escludere altri lettori o writer e blocco che consente a un solo richiedente di ottenere un blocco sull'intervallo specificato, che in genere è un alias per uno degli altri due tipi di blocco. Una determinata istanza del flusso può supportare uno dei primi due tipi o entrambi. Il tipo di blocco viene specificato *da dwLockType*, usando un valore dell'enumerazione [**LOCKTYPE.**](/windows/win32/api/objidl/ne-objidl-locktype)

Qualsiasi area bloccata con **LockRegion** deve essere sbloccata in modo esplicito chiamando [**IByteBuffer::UnlockRegion**](ibytebuffer-unlockregion.md) con esattamente gli stessi valori per i parametri *libOffset*, *cb* e *dwLockType.* L'area deve essere sbloccata prima del rilascio del flusso. Due aree adiacenti non possono essere bloccate separatamente e quindi sbloccate con una singola chiamata di sblocco.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrata la limitazione dell'accesso a un intervallo di byte.


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
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                    |
| Fine del supporto client<br/>    | Windows XP<br/>                                                                   |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Scardssp.h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Scardssp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ IByteBuffer è definito come E126F8FE-A7AF-11D0-B88A-00C04FD424B9<br/>          |



 

