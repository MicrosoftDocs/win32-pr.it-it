---
description: Libera il puntatore ai byte che punta al blocco di memoria HGLOBAL gestito da un'interfaccia COM IStream.
ms.assetid: a76c97a9-d0e9-4eb0-9f97-15f22111187d
title: Metodo ISCardTypeConv::FreeIStreamMemoryPtr (Scarddat.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.FreeIStreamMemoryPtr
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 62e91f9d8fca06c812370091b407edb73fed433a4c576857a7e089db28d6d856
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118922390"
---
# <a name="iscardtypeconvfreeistreammemoryptr-method"></a>Metodo ISCardTypeConv::FreeIStreamMemoryPtr

\[Il **metodo FreeIStreamMemoryPtr** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli smart card offrono](/previous-versions/windows/desktop/secsmart/smart-card-modules) funzionalità simili.\]

Il **metodo FreeIStreamMemoryPtr** libera il puntatore di byte che punta al blocco di memoria HGLOBAL gestito da **un'interfaccia COM IStream.**

## <a name="syntax"></a>Sintassi


```C++
HRESULT FreeIStreamMemoryPtr(
  [in] LPSTREAM pStrm,
  [in] LPBYTE   pMem
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pStrm* \[ Pollici\]
</dt> <dd>

Puntatore **all'interfaccia IStream** che gestisce il blocco di memoria a cui punta *pMem*.

</dd> <dt>

*pMem* \[ Pollici\]
</dt> <dd>

Puntatore al blocco di memoria gestito **dall'interfaccia IStream.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti:



| Codice restituito                                                                                   | Descrizione                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Memoria allocata correttamente.<br/>                                                        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Si è verificato un errore in uno o più parametri passati alla funzione.<br/> |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl>     | Un parametro di tipo puntatore non è corretto.<br/>                                            |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente per soddisfare la richiesta.<br/>                                            |



 

## <a name="remarks"></a>Commenti

Questa funzione rilascia completamente e correttamente il puntatore di byte che punta al blocco di memoria HGLOBAL gestito **dall'interfaccia IStream.** Il puntatore di byte viene acquisito da una [**chiamata a GetAtIStreamMemory.**](iscardtypeconv-getatistreammemory.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                    |
| Fine del supporto client<br/>    | Windows XP<br/>                                                                   |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Scarddat.h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Scarddat.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardTypeConv è definito come 53B6AA63-3F56-11D0-916B-00AA00C18068<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ISCardTypeConv**](iscardtypeconv.md)
</dt> <dt>

[Valori restituiti dalla smart card](authentication-return-values.md)
</dt> <dt>

[**GetAtIStreamMemory**](iscardtypeconv-getatistreammemory.md)
</dt> </dl>

 

 
