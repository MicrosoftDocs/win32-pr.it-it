---
description: Crea un buffer universale di byte di cui è stato eseguito il mapping in un oggetto IStream (IByteBuffer).
ms.assetid: 8015c7e8-2cbb-4ba8-9bd0-2f84751840f1
title: Metodo ISCardTypeConv::CreateByteBuffer (Scarddat.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.CreateByteBuffer
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: e95ab8989027cb79dfd48720b08d27042c7bd8f9252d1438152dafbae017d762
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118922410"
---
# <a name="iscardtypeconvcreatebytebuffer-method"></a>Metodo ISCardTypeConv::CreateByteBuffer

\[Il **metodo CreateByteBuffer** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli smart card offrono](/previous-versions/windows/desktop/secsmart/smart-card-modules) funzionalità simili.\]

Il **metodo CreateByteBuffer** crea un buffer universale di byte mappati in un **oggetto IStream** ([**IByteBuffer**](ibytebuffer.md)).

Il buffer di byte creato è un flusso mappato su un blocco di memoria. Per accedere o gestire il buffer, usare i metodi forniti **dall'interfaccia IStream.** Una funzionalità univoca di questa implementazione di matrice è che quando si chiama il metodo **IStream::Release,** la memoria sottostante verrà rilasciata automaticamente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CreateByteBuffer(
  [in]  DWORD        dwAllocSize,
  [out] LPBYTEBUFFER *ppbyBuff
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwAllocSize* \[ Pollici\]
</dt> <dd>

Dimensione in byte della memoria da allocare per la matrice.

</dd> <dt>

*ppbyBuff* \[ Cambio\]
</dt> <dd>

Puntatore all'oggetto IStream da restituire.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

I possibili valori restituiti sono i seguenti:



| Codice restituito                                                                                   | Descrizione                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Memoria allocata correttamente.<br/>                                                        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Si è verificato un errore in uno o più parametri passati alla funzione.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria disponibile insufficiente per soddisfare la richiesta.<br/>                                            |



 

## <a name="remarks"></a>Commenti

La memoria allocata è mobile. Usare il **metodo IStream::Release** per liberare la memoria.

Per creare una tipica matrice di byte C/C++, chiamare [**CreateByteArray**](iscardtypeconv-createbytearray.md).

Per creare un SAFEARRAY di automazione di caratteri senza segno (byte), chiamare [**CreateSafeArray**](iscardtypeconv-createsafearray.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                    |
| Fine del supporto client<br/>    | Windows XP<br/>                                                                   |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Scarddat.h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Scarddat.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID ISCardTypeConv è definito come \_ 53B6AA63-3F56-11D0-916B-00AA00C18068<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ISCardTypeConv**](iscardtypeconv.md)
</dt> <dt>

[Valori restituiti da smart card](authentication-return-values.md)
</dt> <dt>

[**CreateByteArray**](iscardtypeconv-createbytearray.md)
</dt> <dt>

[**CreateSafeArray**](iscardtypeconv-createsafearray.md)
</dt> </dl>

 

 
