---
description: Acquisisce un puntatore di byte al blocco di memoria HGLOBAL gestito dall'interfaccia COM IStream.
ms.assetid: ea25eb98-b841-4f5e-b428-3d9cb8176142
title: Metodo ISCardTypeConv::GetAtIStreamMemory (Scarddat.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.GetAtIStreamMemory
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 6520b9af0cf8f322045dfbe92ffc66ef624eadfa7b1beef0f528c6b299d1c2bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118922400"
---
# <a name="iscardtypeconvgetatistreammemory-method"></a>Metodo ISCardTypeConv::GetAtIStreamMemory

\[Il **metodo GetAtIStreamMemory** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli smart card offrono](/previous-versions/windows/desktop/secsmart/smart-card-modules) funzionalità simili.\]

Il **metodo GetAtIStreamMemory** acquisisce un puntatore di byte al blocco di memoria HGLOBAL gestito dall'interfaccia COM **IStream.**

Si tratta di un modo per ottenere la memoria in **IStream** senza dover ottenere il valore sizeof per il blocco di memoria in byte e leggere i byte in una matrice di byte temporanea usando **l'interfaccia IStream.**

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetAtIStreamMemory(
  [in]  LPSTREAM    pStrm,
  [out] LPBYTEARRAY *ppMem
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pStrm* \[ Pollici\]
</dt> <dd>

Puntatore all'interfaccia COM **IStream** che gestisce il blocco di memoria HGLOBAL.

</dd> <dt>

*ppMem* \[ Cambio\]
</dt> <dd>

Puntatore al primo byte del blocco di memoria HGLOBAL in caso di esito positivo. else, **NULL se l'operazione** ha esito negativo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti.



| Codice restituito                                                                                   | Descrizione                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Memoria allocata correttamente.<br/>                                                        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Si è verificato un errore in uno o più parametri passati alla funzione.<br/> |
| <dl> <dt>**PUNTATORE E \_**</dt> </dl>     | Un parametro di tipo puntatore non è corretto.<br/>                                            |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente per soddisfare la richiesta.<br/>                                            |



 

## <a name="remarks"></a>Commenti

Il **conteggio dei riferimenti IStream** verrà incrementato per ogni *puntatore ppMem* acquisito.

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

 

 
