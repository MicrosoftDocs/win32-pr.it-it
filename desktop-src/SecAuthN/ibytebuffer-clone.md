---
description: Il metodo Clone crea un nuovo oggetto con il proprio puntatore di ricerca che fa riferimento agli stessi byte dell'oggetto IByteBuffer originale.
ms.assetid: 41530f1d-81e5-4bea-a254-d7d741976904
title: 'Metodo IByteBuffer:: Clone (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Clone
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: d994ef55665b03da2a7d657689682f893fdf071f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232838"
---
# <a name="ibytebufferclone-method"></a>Metodo IByteBuffer:: Clone

\[Il metodo **Clone** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. L'interfaccia [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) fornisce funzionalità simili.\]

Il metodo **Clone** crea un nuovo oggetto con il proprio puntatore di ricerca che fa riferimento agli stessi byte dell'oggetto [**IByteBuffer**](ibytebuffer.md) originale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Clone(
  [out] LPBYTEBUFFER *ppByteBuffer
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppByteBuffer* \[ out\]
</dt> <dd>

Quando ha esito positivo, punta alla posizione di un puntatore [**IByteBuffer**](ibytebuffer.md) al nuovo oggetto flusso. Al termine dell'uso del puntatore **IByteBuffer** , rilasciarlo chiamando la funzione [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) . Se si verifica un errore, questo parametro è **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è un valore **HRESULT**. Il valore S \_ OK indica che la chiamata è stata eseguita correttamente.

## <a name="remarks"></a>Commenti

Questo metodo crea un nuovo oggetto flusso per accedere agli stessi byte ma utilizzando un puntatore di ricerca separato. Il nuovo oggetto flusso Visualizza gli stessi dati dell'oggetto flusso di origine. Le modifiche scritte in un oggetto sono immediatamente visibili nell'altra. Il blocco di intervallo è condiviso tra gli oggetti flusso.

L'impostazione iniziale del puntatore di ricerca nell'istanza del flusso clonato è uguale all'impostazione corrente del puntatore di ricerca nel flusso originale al momento dell'operazione di clonazione.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrata la clonazione dell'interfaccia [**IByteBuffer**](ibytebuffer.md) .


```C++
HRESULT  hr;

// Clone the buffer.
hr = pIByteBuff->Clone(&pIByteClone);
if (FAILED(hr))
  printf("Failed IByteBuffer::Clone\n");
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



 

