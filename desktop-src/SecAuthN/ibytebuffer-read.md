---
description: Il metodo Read legge un numero specificato di byte dall'oggetto buffer in memoria a partire dal puntatore di ricerca corrente.
ms.assetid: 98c4de75-9ecf-4c57-9075-9d0e3675079f
title: 'Metodo IByteBuffer:: Read (scardssp. h)'
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
ms.openlocfilehash: 0574fb640d60fd8af824ff54abce5d109675ba87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233278"
---
# <a name="ibytebufferread-method"></a>Metodo IByteBuffer:: Read

\[Il metodo **Read** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. L'interfaccia [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) fornisce funzionalità simili.\]

Il metodo **Read** legge un numero specificato di byte dall'oggetto buffer in memoria a partire dal puntatore di ricerca corrente.

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

*pByte* \[ out\]
</dt> <dd>

Punta al buffer in cui vengono letti i dati del flusso. Se si verifica un errore, questo valore è **null**.

</dd> <dt>

*CB* \[ in\]
</dt> <dd>

Numero di byte di dati da tentare di leggere dall'oggetto flusso.

</dd> <dt>

*pcbRead* \[ out\]
</dt> <dd>

Indirizzo di una variabile **Long** che riceve il numero effettivo di byte letti dall'oggetto flusso. È possibile impostare questo puntatore su **null** per indicare che non si è interessati a questo valore. In questo caso, questo metodo non fornisce il numero effettivo di byte letti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è un valore **HRESULT**. Il valore S \_ OK indica che la chiamata è stata eseguita correttamente.

## <a name="remarks"></a>Commenti

Questo metodo legge i byte da questo oggetto flusso in memoria. L'oggetto flusso deve essere aperto in \_ modalità di lettura STGM. Questo metodo regola il puntatore di ricerca in base al numero effettivo di byte letti.

Il numero di byte effettivamente letti viene restituito anche nel parametro *pcbRead* .

Note per i chiamanti

Il numero effettivo di byte letti può essere inferiore al numero di byte richiesti se si verifica un errore o se viene raggiunta la fine del flusso durante l'operazione di lettura.

Alcune implementazioni potrebbero restituire un errore se viene raggiunta la fine del flusso durante la lettura. È necessario essere pronti a gestire la restituzione dell'errore o i \_ valori restituiti OK alla fine delle letture del flusso.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato come leggere i byte dal buffer.


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
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| Fine del supporto client<br/>    | Windows XP<br/>                                                                   |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Scardssp. h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Scardssp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ IByteBuffer è definito come E126F8FE-A7AF-11D0-B88A-00C04FD424B9<br/>          |



 

