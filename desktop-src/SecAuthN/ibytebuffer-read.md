---
description: Il metodo Read legge un numero specificato di byte dall'oggetto buffer in memoria a partire dal puntatore di ricerca corrente.
ms.assetid: 98c4de75-9ecf-4c57-9075-9d0e3675079f
title: Metodo IByteBuffer::Read (Scardssp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Read
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: eb78726228e333205032a3179e5c3bedb05786b072d02e78d5cc85cea7a97336
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119482671"
---
# <a name="ibytebufferread-method"></a>Metodo IByteBuffer::Read

\[Il **metodo** Read è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. [**L'interfaccia IStream**](/windows/desktop/api/objidl/nn-objidl-istream) offre funzionalità simili.\]

Il **metodo Read** legge un numero specificato di byte dall'oggetto buffer in memoria a partire dal puntatore di ricerca corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Read(
  [out] BYTE *pByte,
  [in]  LONG cb,
  [out] LONG *pcbRead
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pByte* \[ Cambio\]
</dt> <dd>

Punta al buffer in cui vengono letti i dati del flusso. Se si verifica un errore, questo valore è **NULL.**

</dd> <dt>

*cb* \[ Pollici\]
</dt> <dd>

Numero di byte di dati da tentare di leggere dall'oggetto flusso.

</dd> <dt>

*pcbRead* \[ Cambio\]
</dt> <dd>

Indirizzo di una **variabile LONG** che riceve il numero effettivo di byte letti dall'oggetto flusso. È possibile impostare questo **puntatore su NULL** per indicare che non si è interessati a questo valore. In questo caso, questo metodo non fornisce il numero effettivo di byte letti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è **HRESULT.** Il valore S \_ OK indica che la chiamata è riuscita.

## <a name="remarks"></a>Commenti

Questo metodo legge i byte da questo oggetto flusso in memoria. L'oggetto flusso deve essere aperto in modalità STGM \_ READ. Questo metodo regola il puntatore di ricerca in base al numero effettivo di byte letti.

Anche il numero di byte letti viene restituito nel *parametro pcbRead.*

Note per i chiamanti

Il numero effettivo di byte letti può essere inferiore al numero di byte richiesti se si verifica un errore o se viene raggiunta la fine del flusso durante l'operazione di lettura.

Alcune implementazioni potrebbero restituire un errore se viene raggiunta la fine del flusso durante la lettura. È necessario essere pronti a gestire i valori restituiti dall'errore o S \_ OK alla fine delle operazioni di lettura del flusso.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrata la lettura di byte dal buffer.


```C++
BYTE     byAtr[32];
long     lBytesRead, i;
HRESULT  hr;

// pAtr is a pointer to a previously instantiated IByteBuffer.
// It was used in an earlier call by ISCard::get_Atr.
// Use IByteBuffer::Read to access the retrieved ATR bytes.
hr = pAtr->Read(byAtr, 32, &lBytesRead);
// Use the ATR value. (This example merely displays the bytes.)
for ( i = 0; i < lBytesRead; i++)
    printf("%c", *(byAtr + i));
printf("\n");
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



 

