---
description: Rimuove la restrizione di accesso per un intervallo di byte precedentemente limitato tramite IByteBuffer::LockRegion.
ms.assetid: f2a1162e-7fc7-4a55-befb-0b017edb9fe2
title: Metodo IByteBuffer::UnlockRegion (Scardssp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.UnlockRegion
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 798569621c1a46e73ea6fd8e2f4f3333c3a0cbcef32618797fcba39d35b55bf6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127391"
---
# <a name="ibytebufferunlockregion-method"></a>Metodo IByteBuffer::UnlockRegion

\[Il **metodo UnlockRegion** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. [**L'interfaccia IStream**](/windows/desktop/api/objidl/nn-objidl-istream) offre funzionalità simili.\]

Il **metodo UnlockRegion** rimuove la restrizione di accesso per un intervallo di byte precedentemente limitato tramite [**IByteBuffer::LockRegion.**](ibytebuffer-lockregion.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT UnlockRegion(
  [in] LONG libOffset,
  [in] LONG cb,
  [in] LONG dwLockType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*libOffset* \[ Pollici\]
</dt> <dd>

Offset di byte per l'inizio dell'intervallo.

</dd> <dt>

*cb* \[ Pollici\]
</dt> <dd>

Lunghezza, in byte, dell'intervallo da impostare come limitato.

</dd> <dt>

*dwLockType* \[ Pollici\]
</dt> <dd>

Restrizioni di accesso precedentemente inserite nell'intervallo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è **HRESULT.** Il valore S \_ OK indica che la chiamata è riuscita.

## <a name="remarks"></a>Commenti

Il **metodo IByteBuffer::UnlockRegion** sblocca un'area precedentemente bloccata usando il [**metodo IByteBuffer::LockRegion.**](ibytebuffer-lockregion.md) Le aree bloccate devono essere sbloccate in modo esplicito chiamando **IByteBuffer::UnlockRegion** con esattamente gli stessi valori per i parametri *libOffset*, *cb* e *dwLockType.* L'area deve essere sbloccata prima del rilascio del flusso. Due aree adiacenti non possono essere bloccate separatamente e quindi sbloccate con una singola chiamata di sblocco.

## <a name="examples"></a>Esempio

L'esempio seguente illustra lo sblocco di un intervallo di byte.


```C++
HRESULT  hr;

// Unlock a region.
hr = pIByteBuff->UnlockRegion(0, 10, LOCK_EXCLUSIVE);
if (FAILED(hr))
  printf("Failed IByteBuffer::UnlockRegion\n");
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                    |
| Fine del supporto client<br/>    | Windows XP<br/>                                                                   |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Scardssp.h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Scardssp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ IByteBuffer è definito come E126F8FE-A7AF-11D0-B88A-00C04FD424B9<br/>          |



 

