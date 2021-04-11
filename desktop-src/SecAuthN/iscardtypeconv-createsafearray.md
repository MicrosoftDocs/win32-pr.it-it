---
description: Crea un SAFEARRAY di automazione di caratteri non firmati (byte).
ms.assetid: 67cc8cd1-95be-4498-ac25-6c418089af27
title: 'Metodo ISCardTypeConv:: CreateSafeArray (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.CreateSafeArray
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 6bc27a3f50f0740eca178787fd021f76c9b6729e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128095"
---
# <a name="iscardtypeconvcreatesafearray-method"></a>Metodo ISCardTypeConv:: CreateSafeArray

\[Il metodo **CreateSafeArray** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]

Il metodo **CreateSafeArray** crea un SAFEARRAY di automazione di caratteri non firmati (byte).

## <a name="syntax"></a>Sintassi


```C++
HRESULT CreateSafeArray(
  [in]  UINT        nAllocSize,
  [out] LPSAFEARRAY *ppArray
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*nAllocSize* \[ in\]
</dt> <dd>

Dimensioni in byte della memoria da allocare per la matrice.

</dd> <dt>

*ppArray* \[ out\]
</dt> <dd>

Puntatore all'oggetto SAFEARRAY da restituire.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti:



| Codice restituito                                                                                   | Descrizione                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Memoria allocata correttamente.<br/>                                                        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Si è verificato un problema con uno o più parametri passati nella funzione.<br/> |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | Memoria disponibile insufficiente per soddisfare la richiesta.<br/>                                            |



 

## <a name="remarks"></a>Commenti

Per creare una matrice di byte C/C++ tipica, chiamare [**CreateByteArray**](iscardtypeconv-createbytearray.md).

Per creare un buffer universale di byte mappato in un oggetto **IStream** ([**IByteBuffer**](ibytebuffer.md)), chiamare [**CreateByteBuffer**](iscardtypeconv-createbytebuffer.md).

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
</dt> <dt>

[**CreateByteArray**](iscardtypeconv-createbytearray.md)
</dt> <dt>

[**CreateByteBuffer**](iscardtypeconv-createbytebuffer.md)
</dt> </dl>

 

 
