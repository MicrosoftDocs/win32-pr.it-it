---
description: Il metodo Revert rimuove tutte le modifiche apportate a un flusso transazione dall'ultima chiamata IByteBuffer::Commit.
ms.assetid: da3d9810-6511-43d5-af87-03a392f8be75
title: Metodo IByteBuffer::Revert (Scardssp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Revert
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 46e535560332c43d250b0a26183036342c8cca29144e3d2d1803582387af6bd8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101261"
---
# <a name="ibytebufferrevert-method"></a>Metodo IByteBuffer::Revert

\[Il **metodo Revert** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. [**L'interfaccia IStream**](/windows/desktop/api/objidl/nn-objidl-istream) fornisce funzionalità simili.\]

Il **metodo Revert** rimuove tutte le modifiche apportate a un flusso transazione dall'ultima chiamata [**IByteBuffer::Commit.**](ibytebuffer-commit.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT Revert();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Il valore restituito è **HRESULT.** Il valore S OK indica che la chiamata ha avuto esito positivo e che il flusso è stato \_ ripristinato alla versione precedente.

## <a name="remarks"></a>Commenti

Questo metodo rimuove le modifiche apportate a un flusso transazione dall'ultima operazione di commit.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato il ripristino di un flusso transazione all'ultima operazione di cui è stato eseguito il commit.


```C++
HRESULT  hr;

hr = pIByteBuff->Revert();
if (FAILED(hr))
  printf("Failed IByteBuffer::Revert\n");
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                    |
| Fine del supporto client<br/>    | Windows XP<br/>                                                                   |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Scardssp.h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Scardssp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ IByteBuffer è definito come E126F8FE-A7AF-11D0-B88A-00C04FD424B9<br/>          |



 

