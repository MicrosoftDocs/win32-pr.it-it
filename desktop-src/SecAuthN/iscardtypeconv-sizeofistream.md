---
description: Determina le dimensioni, in byte, dell'interfaccia COM IStream.
ms.assetid: 8c2f081d-cc41-409e-a868-bcf834e1f128
title: Metodo ISCardTypeConv::SizeOfIStream (Scarddat.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.SizeOfIStream
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: ec150fdf5a6f296b5728131cd59bb6863016fe46fe0769e6159e43b236f77a95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013691"
---
# <a name="iscardtypeconvsizeofistream-method"></a>Metodo ISCardTypeConv::SizeOfIStream

\[Il **metodo SizeOfIStream** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli smart card offrono](/previous-versions/windows/desktop/secsmart/smart-card-modules) funzionalità simili.\]

Il **metodo SizeOfIStream** determina le dimensioni, in byte, dell'interfaccia COM **IStream.**

## <a name="syntax"></a>Sintassi


```C++
HRESULT SizeOfIStream(
  [in]  LPSTREAM       pStrm,
  [out] ULARGE_INTEGER *puliSize
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pStrm* \[ Pollici\]
</dt> <dd>

Puntatore all'interfaccia COM **IStream.**

</dd> <dt>

*puliSize* \[ Cambio\]
</dt> <dd>

Puntatore all'intero di grandi dimensioni senza segno che può contenere l'intero valore sizeof a 64 bit **dell'interfaccia COM IStream.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti.



| Codice restituito                                                                                  | Descrizione                                                                                             |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | La funzione ha avuto esito positivo e *\* puliSize* è la dimensione, in byte, dell'interfaccia COM IStream.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>       | Si è verificato un errore non specificato.<br/>                                                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Il *parametro puliSize* non è corretto.<br/>                                                       |
| <dl> <dt>**PUNTATORE E \_**</dt> </dl>    | Il *parametro pStrm* non è corretto.<br/>                                                          |
| <dl> <dt>**E \_ IMPREVISTO**</dt> </dl> | Si è verificato un errore imprevisto.<br/>                                                                   |



 

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

 

 
