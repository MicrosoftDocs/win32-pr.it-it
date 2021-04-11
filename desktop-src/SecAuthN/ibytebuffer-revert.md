---
description: "Il metodo Revert Elimina tutte le modifiche apportate a un flusso sottoposto a transazione dall'ultima chiamata a IByteBuffer:: commit."
ms.assetid: da3d9810-6511-43d5-af87-03a392f8be75
title: 'Metodo IByteBuffer:: Revert (scardssp. h)'
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
ms.openlocfilehash: cf7873407196c98868ca45c73db503568f8259e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226024"
---
# <a name="ibytebufferrevert-method"></a>Metodo IByteBuffer:: Revert

\[Il metodo **Revert** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. L'interfaccia [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) fornisce funzionalità simili.\]

Il metodo **Revert** Elimina tutte le modifiche apportate a un flusso sottoposto a transazione dall'ultima chiamata a [**IByteBuffer:: commit**](ibytebuffer-commit.md) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT Revert();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Il valore restituito è un valore **HRESULT**. Un valore di S \_ OK indica che la chiamata è stata completata e che il flusso è stato ripristinato alla versione precedente.

## <a name="remarks"></a>Commenti

Questo metodo ignora le modifiche apportate a un flusso sottoposto a transazione dall'ultima operazione di commit.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato il ripristino di un flusso transazionale all'ultima operazione di cui è stato eseguito il commit.


```C++
HRESULT  hr;

hr = pIByteBuff->Revert();
if (FAILED(hr))
  printf("Failed IByteBuffer::Revert\n");
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| Fine del supporto client<br/>    | Windows XP<br/>                                                                   |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Scardssp. h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Scardssp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ IByteBuffer è definito come E126F8FE-A7AF-11D0-B88A-00C04FD424B9<br/>          |



 

