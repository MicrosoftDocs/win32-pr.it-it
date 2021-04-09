---
description: Il metodo sesize modifica la dimensione dell'oggetto flusso.
ms.assetid: e4027a98-fce4-4db4-a9fe-e7e7436b5147
title: 'Metodo IByteBuffer:: sesize (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.SetSize
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 85a6abc11f3e007f3c8d1057cb5c8785c8519ebf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968296"
---
# <a name="ibytebuffersetsize-method"></a>Metodo IByteBuffer:: sesize

\[Il metodo **sesize** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. L'interfaccia [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) fornisce funzionalità simili.\]

Il metodo **sesize** modifica la dimensione dell'oggetto flusso.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetSize(
  [in] LONG libNewSize
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*libNewSize* \[ in\]
</dt> <dd>

Nuove dimensioni del flusso come numero di byte

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è un valore **HRESULT**. Il valore S \_ OK indica che la chiamata è stata eseguita correttamente.

## <a name="remarks"></a>Commenti

Il metodo **IByteBuffer:: sesize** modifica la dimensione dell'oggetto flusso. Chiamare questo metodo per preallocare lo spazio per il flusso. Se il parametro *libNewSize* è maggiore della dimensione corrente del flusso, il flusso viene esteso alle dimensioni indicate riempiendo lo spazio corrispondente con i byte di un valore non definito. Questa operazione è simile al metodo [**IByteBuffer:: Write**](ibytebuffer-write.md) se il puntatore di ricerca è oltre la fine del flusso corrente.

Se il parametro *libNewSize* è minore del flusso corrente, il flusso viene troncato alla dimensione indicata.

Il puntatore di ricerca non è influenzato dalla modifica delle dimensioni del flusso.

La chiamata di **IByteBuffer:: sesize** può essere un modo efficace per ottenere un grande blocco di spazio contiguo.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrata l'impostazione delle dimensioni del buffer.


```C++
LONG     lNewSize = 256;
HRESULT  hr;

// Change the buffer size.
hr = pIByteBuff->SetSize(lNewSize);
if (FAILED(hr))
  printf("Failed IByteBuffer::SetSize\n");
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



 

