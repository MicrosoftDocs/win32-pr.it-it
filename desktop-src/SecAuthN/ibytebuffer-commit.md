---
description: Il metodo Commit garantisce che tutte le modifiche apportate a un oggetto aperto in modalità transazione siano riflesse nell'archiviazione padre.
ms.assetid: 00986e48-c5b9-4ac9-a204-a0774cb5e03e
title: Metodo IByteBuffer::Commit (Scardssp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Commit
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: af165e6f0a805532eade820dcb67968a77186cee3f90cfc48a240d387b1f31b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127411"
---
# <a name="ibytebuffercommit-method"></a>Metodo IByteBuffer::Commit

\[Il **metodo Commit** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. [**L'interfaccia IStream**](/windows/desktop/api/objidl/nn-objidl-istream) fornisce funzionalità simili.\]

Il **metodo Commit** garantisce che tutte le modifiche apportate a un oggetto aperto in modalità transazione siano riflesse nell'archiviazione padre.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Commit(
  [in] LONG grfCommitFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*grfCommitFlags* \[ Pollici\]
</dt> <dd>

Controlla la modalità di esecuzione del commit delle modifiche dell'oggetto flusso. Per una definizione di questi valori, vedere l'enumerazione STGC.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è **HRESULT.** Il valore S \_ OK indica che la chiamata ha avuto esito positivo.

## <a name="remarks"></a>Commenti

Questo metodo garantisce che le modifiche apportate a un oggetto flusso aperto in modalità transazione siano riflesse nell'archiviazione padre. Le modifiche apportate al flusso dopo l'apertura o l'ultimo commit vengono riflesse nell'oggetto di archiviazione padre. Se l'elemento padre viene aperto in modalità transazione, l'elemento padre potrebbe comunque ripristinare in un secondo momento il rollback delle modifiche apportate a questo oggetto flusso. L'implementazione del file composto non supporta l'apertura di flussi in modalità transazione, quindi questo metodo ha un effetto molto poco diverso da quello di scaricare i buffer di memoria.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato il commit delle modifiche nell'archiviazione.


```C++
HRESULT  hr;

// Commit the buffer.
hr = pIByteBuff->Commit(STGC_DEFAULT | STGC_CONSOLIDATE);
if (FAILED(hr))
  printf("Failed IByteBuffer::Commit\n");
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                    |
| Fine del supporto client<br/>    | Windows XP<br/>                                                                   |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Scardssp.h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Scardssp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ IByteBuffer è definito come E126F8FE-A7AF-11D0-B88A-00C04FD424B9<br/>          |



 

