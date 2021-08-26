---
description: Il metodo Seek modifica il puntatore seek in una nuova posizione relativa all'inizio del buffer, alla fine del buffer o al puntatore di ricerca corrente.
ms.assetid: 3541f3dd-7b92-4f72-89b7-4e04e007aaa3
title: Metodo IByteBuffer::Seek (Scardssp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Seek
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 70c4af327fad5014c5d6dec80dd29441f51a03639a108249991c83f53e5d2be8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120016251"
---
# <a name="ibytebufferseek-method"></a>Metodo IByteBuffer::Seek

\[Il **metodo Seek** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. [**L'interfaccia IStream**](/windows/desktop/api/objidl/nn-objidl-istream) offre funzionalità simili.\]

Il **metodo Seek** modifica il puntatore seek in una nuova posizione relativa all'inizio del buffer, alla fine del buffer o al puntatore di ricerca corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Seek(
  [in]  LONG dlibMove,
  [in]  LONG dwOrigin,
  [out] LONG *plibNewPosition
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dlibMove* \[ Pollici\]
</dt> <dd>

Spostamento da aggiungere alla posizione indicata da *dwOrigin*. Se *dwOrigin* è STREAM \_ SEEK \_ SET, viene interpretato come un valore senza segno anziché con segno.

</dd> <dt>

*dwOrigin* \[ Pollici\]
</dt> <dd>

Specifica l'origine per lo spostamento specificato in *dlibMove.* L'origine può essere uno dei valori nella tabella seguente.



| Valore                                                                                                                                                                | Significato                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="STREAM_SEEK_SET"></span><span id="stream_seek_set"></span><dl> <dt>**STREAM \_ SEEK \_ SET**</dt> </dl> | Il nuovo puntatore di ricerca è un offset relativo all'inizio del flusso. In questo caso, il *parametro dlibMove* è la nuova posizione di ricerca relativa all'inizio del flusso.<br/> |
| <span id="STREAM_SEEK_CUR"></span><span id="stream_seek_cur"></span><dl> <dt>**STREAM \_ SEEK \_ CUR**</dt> </dl> | Il nuovo puntatore di ricerca è un offset relativo alla posizione corrente del puntatore di ricerca. In questo caso, il *parametro dlibMove* è lo spostamento con segno dalla posizione di ricerca corrente.<br/>  |
| <span id="STREAM_SEEK_END"></span><span id="stream_seek_end"></span><dl> <dt>**STREAM \_ SEEK \_ END**</dt> </dl> | Il nuovo puntatore di ricerca è un offset relativo alla fine del flusso. In questo caso, il *parametro dlibMove* è la nuova posizione di ricerca relativa alla fine del flusso.<br/>             |



 

</dd> <dt>

*plibNewPosition* \[ Cambio\]
</dt> <dd>

Puntatore alla posizione in cui questo metodo scrive il valore del nuovo puntatore seek dall'inizio del flusso. È possibile impostare questo **puntatore su NULL** per indicare che non si è interessati a questo valore. In questo caso, questo metodo non fornisce il nuovo puntatore seek.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è **HRESULT.** Il valore S \_ OK indica che la chiamata è riuscita.

## <a name="remarks"></a>Commenti

Il **metodo Seek** modifica il puntatore seek in modo che le successive operazioni di lettura e scrittura possano essere eseguite in una posizione diversa nell'oggetto flusso. È un errore eseguire la ricerca prima dell'inizio del flusso. Non è tuttavia un errore cercare oltre la fine del flusso. La ricerca oltre la fine del flusso è utile per le operazioni di scrittura successive, in quanto il flusso in quel momento verrà esteso alla posizione di ricerca immediatamente prima dell'esecuzione dell'operazione di scrittura.

È anche possibile usare questo metodo per ottenere il valore corrente del puntatore seek chiamando questo metodo con il parametro *dwOrigin* impostato su STREAM SEEK CUR e il \_ \_ parametro *dlibMove* impostato su zero in modo che il puntatore di ricerca non sia modificato. Il puntatore di ricerca corrente viene restituito nel *parametro plibNewPosition.*

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato il posizionamento del puntatore di ricerca in una nuova posizione.


```C++
LONG     lNewPos;
HRESULT  hr;

// Change the seek pointer.
hr = pIByteBuff->Seek(5, STREAM_SEEK_SET, &lNewPos);
if (FAILED(hr))
  printf("Failed IByteBuffer::Seek\n");
else
  printf("New position is %x\n", lNewPos);
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



 

