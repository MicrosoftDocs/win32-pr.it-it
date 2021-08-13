---
description: Il metodo CopyTo copia un numero specificato di byte dal puntatore di ricerca corrente nell'oggetto al puntatore di ricerca corrente in un altro oggetto.
ms.assetid: 2044965f-665f-4aa1-abc0-42f5278dd647
title: Metodo IByteBuffer::CopyTo (Scardssp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.CopyTo
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 4c4dc3861120d56dd5bff13fe1e77fd97e1fc32efed9622f18ee51b5160d1c35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119417641"
---
# <a name="ibytebuffercopyto-method"></a>Metodo IByteBuffer::CopyTo

\[Il **metodo CopyTo** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. [**L'interfaccia IStream**](/windows/desktop/api/objidl/nn-objidl-istream) offre funzionalità simili.\]

Il **metodo CopyTo** copia un numero specificato di byte dal puntatore di ricerca corrente nell'oggetto al puntatore di ricerca corrente in un altro oggetto.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CopyTo(
  [in]  LPBYTEBUFFER *pByteBuffer,
  [in]  LONG         cb,
  [out] LONG         *pcbRead,
  [out] LONG         *pcbWritten
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pByteBuffer* \[ Pollici\]
</dt> <dd>

Punta al flusso di destinazione. Il flusso a cui punta *pByteBuffer* può essere un nuovo flusso o un clone del flusso di origine.

</dd> <dt>

*cb* \[ Pollici\]
</dt> <dd>

Numero di byte da copiare dal flusso di origine.

</dd> <dt>

*pcbRead* \[ Cambio\]
</dt> <dd>

Puntatore alla posizione in cui questo metodo scrive il numero effettivo di byte letti dall'origine. È possibile impostare questo **puntatore su NULL** per indicare che non si è interessati a questo valore. In questo caso, questo metodo non fornisce il numero effettivo di byte letti.

</dd> <dt>

*pcbWritten* \[ Cambio\]
</dt> <dd>

Puntatore alla posizione in cui questo metodo scrive il numero effettivo di byte scritti nella destinazione. È possibile impostare questo **puntatore su NULL** per indicare che non si è interessati a questo valore. In questo caso, questo metodo non fornisce il numero effettivo di byte scritti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è **HRESULT.** Il valore S \_ OK indica che la chiamata è riuscita.

## <a name="remarks"></a>Commenti

Questo metodo copia i byte specificati da un flusso a un altro. Può anche essere usato per copiare un flusso in se stesso. Il puntatore di ricerca in ogni istanza del flusso viene regolato in base al numero di byte letti o scritti.

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



 

