---
description: Il metodo Seek modifica il puntatore di ricerca in un nuovo percorso relativo all'inizio del buffer, alla fine del buffer o al puntatore di ricerca corrente.
ms.assetid: 3541f3dd-7b92-4f72-89b7-4e04e007aaa3
title: 'Metodo IByteBuffer:: Seek (scardssp. h)'
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
ms.openlocfilehash: eacfedc3ed23a7a4cf1f60e6c6ac21936c3c94f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884514"
---
# <a name="ibytebufferseek-method"></a>Metodo IByteBuffer:: Seek

\[Il metodo **Seek** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. L'interfaccia [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) fornisce funzionalità simili.\]

Il metodo **Seek** modifica il puntatore di ricerca in un nuovo percorso relativo all'inizio del buffer, alla fine del buffer o al puntatore di ricerca corrente.

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

*dlibMove* \[ in\]
</dt> <dd>

Spostamento da aggiungere alla posizione indicata da *dwOrigin*. Se *dwOrigin* è \_ \_ un set di ricerca del flusso, viene interpretato come un valore senza segno anziché con segno.

</dd> <dt>

*dwOrigin* \[ in\]
</dt> <dd>

Specifica l'origine per lo spostamento specificato in *dlibMove*. L'origine può essere uno dei valori riportati nella tabella seguente.



| Valore                                                                                                                                                                | Significato                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="STREAM_SEEK_SET"></span><span id="stream_seek_set"></span><dl> <dt>**\_set di ricerca di flusso \_**</dt> </dl> | Il nuovo puntatore di ricerca è un offset relativo all'inizio del flusso. In questo caso, il parametro *dlibMove* è la nuova posizione di ricerca relativa all'inizio del flusso.<br/> |
| <span id="STREAM_SEEK_CUR"></span><span id="stream_seek_cur"></span><dl> <dt>**\_cur ricerca \_ flusso**</dt> </dl> | Il nuovo puntatore di ricerca è un offset relativo alla posizione corrente del puntatore di ricerca. In questo caso, il parametro *dlibMove* è lo spostamento firmato dalla posizione di ricerca corrente.<br/>  |
| <span id="STREAM_SEEK_END"></span><span id="stream_seek_end"></span><dl> <dt>**\_fine ricerca \_ flusso**</dt> </dl> | Il nuovo puntatore di ricerca è un offset relativo alla fine del flusso. In questo caso, il parametro *dlibMove* è la nuova posizione di ricerca relativa alla fine del flusso.<br/>             |



 

</dd> <dt>

*plibNewPosition* \[ out\]
</dt> <dd>

Puntatore alla posizione in cui questo metodo scrive il valore del nuovo puntatore di ricerca dall'inizio del flusso. È possibile impostare questo puntatore su **null** per indicare che non si è interessati a questo valore. In questo caso, questo metodo non fornisce il nuovo puntatore di ricerca.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è un valore **HRESULT**. Il valore S \_ OK indica che la chiamata è stata eseguita correttamente.

## <a name="remarks"></a>Commenti

Il metodo **Seek** modifica il puntatore di ricerca in modo che le operazioni di lettura e scrittura successive possano avvenire in un percorso diverso nell'oggetto flusso. Si tratta di un errore di ricerca prima dell'inizio del flusso. Non è, tuttavia, un errore di ricerca oltre la fine del flusso. La ricerca oltre la fine del flusso è utile per le successive operazioni di scrittura, poiché il flusso verrà esteso alla posizione di ricerca immediatamente prima del termine dell'operazione di scrittura.

È anche possibile usare questo metodo per ottenere il valore corrente del puntatore di ricerca chiamando questo metodo con il parametro *dwOrigin* impostato su Stream \_ Seek \_ cur e il parametro *dlibMove* impostato su zero, in modo che il puntatore Seek non venga modificato. Il puntatore di ricerca corrente viene restituito nel parametro *plibNewPosition* .

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
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| Fine del supporto client<br/>    | Windows XP<br/>                                                                   |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Scardssp. h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Scardssp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ IByteBuffer è definito come E126F8FE-A7AF-11D0-B88A-00C04FD424B9<br/>          |



 

