---
description: Determina la dimensione, in byte, dell'interfaccia COM IStream.
ms.assetid: 8c2f081d-cc41-409e-a868-bcf834e1f128
title: 'Metodo ISCardTypeConv:: SizeOfIStream (Scarddat. h)'
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
ms.openlocfilehash: 603a01dc6cb4727d59a7fb82c3270c08a495f021
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313296"
---
# <a name="iscardtypeconvsizeofistream-method"></a>Metodo ISCardTypeConv:: SizeOfIStream

\[Il metodo **SizeOfIStream** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]

Il metodo **SizeOfIStream** determina la dimensione, in byte, dell'interfaccia com **IStream** .

## <a name="syntax"></a>Sintassi


```C++
HRESULT SizeOfIStream(
  [in]  LPSTREAM       pStrm,
  [out] ULARGE_INTEGER *puliSize
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pStrm* \[ in\]
</dt> <dd>

Puntatore all'interfaccia com **IStream** .

</dd> <dt>

*puliSize* \[ out\]
</dt> <dd>

Puntatore all'intero senza segno di grandi dimensioni che può ospitare l'intero valore sizeof a 64 bit dell'interfaccia com **IStream** .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti.



| Codice restituito                                                                                  | Descrizione                                                                                             |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | La funzione ha avuto esito positivo e *\* puliSize* è la dimensione, in byte, dell'interfaccia COM IStream.<br/> |
| <dl> <dt>**E \_ non riescono**</dt> </dl>       | Si è verificato un errore non specificato.<br/>                                                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Il parametro *puliSize* non è corretto.<br/>                                                       |
| <dl> <dt>**\_puntatore E**</dt> </dl>    | Il parametro *pStrm* non è corretto.<br/>                                                          |
| <dl> <dt>**E \_ imprevisto**</dt> </dl> | Si è verificato un errore imprevisto.<br/>                                                                   |



 

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

 

 
