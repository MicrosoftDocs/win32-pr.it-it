---
description: Converte una matrice di byte C/C++ tipica in un buffer universale di byte (oggetto IStream).
ms.assetid: 512c561a-63f1-463e-9bae-9bec1ebdbe9b
title: 'Metodo ISCardTypeConv:: ConvertByteArrayToByteBuffer (Scarddat. h)'
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
ms.openlocfilehash: 406e7aecb7e86802ad67c07669ca199b158ad954
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884482"
---
# <a name="iscardtypeconvconvertbytearraytobytebuffer-method"></a>Metodo ISCardTypeConv:: ConvertByteArrayToByteBuffer

\[Il metodo **ConvertByteArrayToByteBuffer** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]

Il metodo **ConvertByteArrayToByteBuffer** converte una matrice di byte C/C++ tipica in un buffer universale di byte (oggetto **IStream** ).

Il buffer di byte creato è un flusso mappato su un blocco di memoria. Per accedere o gestire il buffer, usare i metodi forniti dall'interfaccia **IStream** . Una funzionalità univoca di questa implementazione di matrice è che, quando si chiama il metodo **IStream:: Release** , la memoria sottostante verrà rilasciata per l'utente.

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

*pbyArray* \[ in\]
</dt> <dd>

Puntatore alla matrice di byte da convertire.

</dd> <dt>

*dwArraySize* \[ in\]
</dt> <dd>

Dimensioni della matrice di byte da convertire.

</dd> <dt>

*ppbyBuffer* \[ out\]
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

La memoria allocata è movibile. Usare il metodo **IStream:: Release** per liberare la memoria.

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

 

 
