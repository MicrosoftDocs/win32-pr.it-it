---
description: Converte una matrice di byte definita come SAFEARRAY in un buffer universale di byte (oggetto IStream).
ms.assetid: faa07bb5-cfdb-4181-b86a-f82a9c6b251a
title: Metodo ISCardTypeConv::ConvertSafeArrayToByteBuffer (Scarddat.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.ConvertSafeArrayToByteBuffer
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: dc7132cbc37a4716adb0dcb192571f9e83597b5aa8b58933962c9366a0c9de2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118922437"
---
# <a name="iscardtypeconvconvertsafearraytobytebuffer-method"></a>Metodo ISCardTypeConv::ConvertSafeArrayToByteBuffer

\[Il **metodo ConvertSafeArrayToByteBuffer** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli smart card offrono](/previous-versions/windows/desktop/secsmart/smart-card-modules) funzionalità simili.\]

Il **metodo ConvertSafeArrayToByteBuffer** converte una matrice di byte definita come SAFEARRAY in un buffer universale di byte **(oggetto IStream).**

Il buffer di byte creato è un flusso mappato su un blocco di memoria. Per accedere o gestire il buffer, usare i metodi forniti **dall'interfaccia IStream.** Una funzionalità univoca di questa implementazione di matrice è che quando si chiama il metodo **IStream::Release,** la memoria sottostante verrà rilasciata automaticamente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ConvertSafeArrayToByteBuffer(
  [in]  LPSAFEARRAY  pbyArray,
  [out] LPBYTEBUFFER *ppbyBuff
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pbyArray* \[ Pollici\]
</dt> <dd>

Puntatore a SAFEARRAY da convertire.

</dd> <dt>

*ppbyBuff* \[ Cambio\]
</dt> <dd>

Puntatore **all'oggetto IStream** da restituire.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti:



| Codice restituito                                                                                   | Descrizione                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Memoria allocata correttamente.<br/>                                                        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Si è verificato un errore in uno o più parametri passati alla funzione.<br/> |
| <dl> <dt>**PUNTATORE E \_**</dt> </dl>     | Un parametro di tipo puntatore non è corretto.<br/>                                            |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria disponibile insufficiente per soddisfare la richiesta.<br/>                                            |



 

## <a name="remarks"></a>Commenti

La memoria allocata è spostabile. Usare il **metodo IStream::Release** per liberare la memoria.

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
</dt> </dl>

 

 
