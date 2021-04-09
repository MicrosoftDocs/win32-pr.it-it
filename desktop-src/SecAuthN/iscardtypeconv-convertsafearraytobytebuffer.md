---
description: Converte una matrice di byte definita come SAFEARRAY in un buffer universale di byte (oggetto IStream).
ms.assetid: faa07bb5-cfdb-4181-b86a-f82a9c6b251a
title: 'Metodo ISCardTypeConv:: ConvertSafeArrayToByteBuffer (Scarddat. h)'
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
ms.openlocfilehash: aa6503f474d96e3c25da3f2780ac43976b6507a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966627"
---
# <a name="iscardtypeconvconvertsafearraytobytebuffer-method"></a>Metodo ISCardTypeConv:: ConvertSafeArrayToByteBuffer

\[Il metodo **ConvertSafeArrayToByteBuffer** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]

Il metodo **ConvertSafeArrayToByteBuffer** converte una matrice di byte definita come SafeArray in un buffer universale di byte (oggetto **IStream** ).

Il buffer di byte creato è un flusso mappato su un blocco di memoria. Per accedere o gestire il buffer, usare i metodi forniti dall'interfaccia **IStream** . Una funzionalità univoca di questa implementazione di matrice è che, quando si chiama il metodo **IStream:: Release** , la memoria sottostante verrà rilasciata per l'utente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ConvertSafeArrayToByteBuffer(
  [in]  LPSAFEARRAY  pbyArray,
  [out] LPBYTEBUFFER *ppbyBuff
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pbyArray* \[ in\]
</dt> <dd>

Puntatore all'elemento SAFEARRAY da convertire.

</dd> <dt>

*ppbyBuff* \[ out\]
</dt> <dd>

Puntatore all'oggetto **IStream** da restituire.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti:



| Codice restituito                                                                                   | Descrizione                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Memoria allocata correttamente.<br/>                                                        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Si è verificato un problema con uno o più parametri passati nella funzione.<br/> |
| <dl> <dt>**\_puntatore E**</dt> </dl>     | Un parametro di tipo puntatore non è corretto.<br/>                                            |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | Memoria disponibile insufficiente per soddisfare la richiesta.<br/>                                            |



 

## <a name="remarks"></a>Commenti

La memoria allocata è mobile. Usare il metodo **IStream:: Release** per liberare la memoria.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| Fine del supporto client<br/>    | Windows XP<br/>                                                                   |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Scarddat. h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Scarddat. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardTypeConv è definito come 53B6AA63-3F56-11D0-916B-00AA00C18068<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ISCardTypeConv**](iscardtypeconv.md)
</dt> <dt>

[Valori restituiti da Smart Card](authentication-return-values.md)
</dt> </dl>

 

 
