---
description: Il metodo Write scrive un numero specificato da byte nell'oggetto flusso a partire dal puntatore di ricerca corrente.
ms.assetid: 0019cd10-8f8a-4190-bae4-e134e7b76882
title: Metodo IByteBuffer::Write (Scardssp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Write
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 0033d4f4ee03629d2bedf9f232a43607100bcdca8bfaab457c2236bbfad603d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127351"
---
# <a name="ibytebufferwrite-method"></a>Metodo IByteBuffer::Write

\[Il **metodo** Write è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. [**L'interfaccia IStream**](/windows/desktop/api/objidl/nn-objidl-istream) offre funzionalità simili.\]

Il **metodo Write** scrive un numero specificato da byte nell'oggetto flusso a partire dal puntatore di ricerca corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Write(
  [in]  BYTE *pByte,
  [in]  LONG cb,
  [out] LONG *pcbWritten
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pByte* \[ Pollici\]
</dt> <dd>

Indirizzo del buffer contenente i dati da scrivere nel flusso. È necessario fornire un puntatore valido per questo parametro anche quando *cb* è zero.

</dd> <dt>

*cb* \[ Pollici\]
</dt> <dd>

Numero di byte di dati da tentare di scrivere nel flusso. Questo parametro può essere zero.

</dd> <dt>

*pcbWritten* \[ Cambio\]
</dt> <dd>

Indirizzo di una **variabile LONG** in cui questo metodo scrive il numero effettivo di byte scritti nell'oggetto flusso. Il chiamante può impostare questo **puntatore su NULL,** nel qual caso questo metodo non fornisce il numero effettivo di byte scritti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è **HRESULT.** Il valore S \_ OK indica che la chiamata è riuscita.

## <a name="remarks"></a>Commenti

Il **metodo IByteBuffer::Write** scrive i dati specificati in un oggetto flusso. Il puntatore di ricerca viene regolato in base al numero di byte effettivamente scritti. Il numero di byte effettivamente scritti viene restituito nel *parametro pcbWritten.* Se il numero di byte è pari a zero byte, l'operazione di scrittura non ha alcun effetto.

Se il puntatore di ricerca è attualmente oltre la fine del flusso e il numero di byte è diverso da zero, questo metodo aumenta le dimensioni del flusso nel puntatore di ricerca e scrive i byte specificati a partire dal puntatore di ricerca. I byte di riempimento scritti nel flusso non vengono inizializzati su un valore specifico. Si tratta dello stesso comportamento della fine del file nel file FAT MS-DOS file system.

Con un numero di byte pari a zero e un puntatore seek oltre la fine del flusso, questo metodo non crea i byte di riempimento per aumentare il flusso fino al puntatore di ricerca. In questo caso, è necessario chiamare il [**metodo IByteBuffer::SetSize**](ibytebuffer-setsize.md) per aumentare le dimensioni del flusso e scrivere i byte di riempimento.

Il *parametro pcbWritten* può avere un valore anche se si verifica un errore.

Nell'implementazione fornita da COM gli oggetti flusso non sono di tipo sparse. Tutti i byte di riempimento vengono infine allocati sul disco e assegnati al flusso.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrata la scrittura di byte nell'oggetto flusso.


```C++
LONG     lWrite;
HRESULT  hr;

// Write to the buffer.
// byData is an array of 64 bytes.
hr = pIByteBuff->Write(byData,
                       64,
                       &lWrite);
if (FAILED(hr))
  printf("Failed IByteBuffer::Write\n");
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



 

