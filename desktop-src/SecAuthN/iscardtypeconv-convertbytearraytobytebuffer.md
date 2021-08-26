---
description: Converte una tipica matrice di byte C/C++ in un buffer universale di byte (oggetto IStream).
ms.assetid: 512c561a-63f1-463e-9bae-9bec1ebdbe9b
title: Metodo ISCardTypeConv::ConvertByteArrayToByteBuffer (Scarddat.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.ConvertByteArrayToByteBuffer
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 5616dc56ac893d6298e12014f3ee31d38bf1c55fb5367f354bf97da704ade0c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013811"
---
# <a name="iscardtypeconvconvertbytearraytobytebuffer-method"></a>Metodo ISCardTypeConv::ConvertByteArrayToByteBuffer

\[Il **metodo ConvertByteArrayToByteBuffer** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli smart card offrono](/previous-versions/windows/desktop/secsmart/smart-card-modules) funzionalità simili.\]

Il **metodo ConvertByteArrayToByteBuffer** converte una tipica matrice di byte C/C++ in un buffer universale di byte **(oggetto IStream).**

Il buffer di byte creato è un flusso mappato su un blocco di memoria. Per accedere o gestire il buffer, usare i metodi forniti **dall'interfaccia IStream.** Una funzionalità univoca di questa implementazione di matrice è che quando si chiama il metodo **IStream::Release,** la memoria sottostante verrà rilasciata automaticamente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ConvertByteArrayToByteBuffer(
  [in]  LPBYTE       pbyArray,
  [in]  DWORD        dwArraySize,
  [out] LPBYTEBUFFER *ppbyBuffer
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pbyArray* \[ Pollici\]
</dt> <dd>

Puntatore alla matrice di byte da convertire.

</dd> <dt>

*dwArraySize* \[ Pollici\]
</dt> <dd>

Dimensione della matrice di byte da convertire.

</dd> <dt>

*ppbyBuffer* \[ Cambio\]
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

La memoria allocata è mobile. Usare il **metodo IStream::Release** per liberare la memoria.

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

 

 
