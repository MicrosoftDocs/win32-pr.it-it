---
description: Il metodo Initialize prepara l'oggetto IByteBuffer per l'utilizzo. Questo metodo deve essere chiamato prima di chiamare altri metodi nell'interfaccia IByteBuffer.
ms.assetid: 1b22e693-0add-4b80-a2c4-925ebd3ab3a6
title: 'Metodo IByteBuffer:: Initialize (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Initialize
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 245f9282174ddeef66b130597f0f20ddf21ededc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317080"
---
# <a name="ibytebufferinitialize-method"></a>Metodo IByteBuffer:: Initialize

\[Il metodo **Initialize** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive. L'interfaccia [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) fornisce funzionalità simili.\]

Il metodo **Initialize** prepara l'oggetto [**IByteBuffer**](ibytebuffer.md) per l'utilizzo. Questo metodo deve essere chiamato prima di chiamare altri metodi nell'interfaccia **IByteBuffer** .

## <a name="syntax"></a>Sintassi


```C++
HRESULT Initialize(
  [in] LONG lSize,
  [in] BYTE *pData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lSize* \[ in\]
</dt> <dd>

Dimensioni iniziali, in byte, dei dati che devono essere contenuti nel flusso.

</dd> <dt>

*pData* \[ in\]
</dt> <dd>

Se non è **null**, i dati iniziali da scrivere nel flusso.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è un valore **HRESULT**. Il valore S \_ OK indica che la chiamata è stata eseguita correttamente.

## <a name="remarks"></a>Commenti

Quando si usa un nuovo flusso [**IByteBuffer**](ibytebuffer.md) , chiamare questo metodo prima di usare uno degli altri metodi **IByteBuffer** .

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato come inizializzare l'oggetto [**IByteBuffer**](ibytebuffer.md) .


```C++
UCHAR    ucFileName[] = {0x3f, 0x00};    // Master File (MF)
HRESULT  hr;

// pIByteRequest is a pointer to an instantiated IByteBuffer object.
hr = pIByteRequest->Initialize(2, ucFileName);
if (FAILED(hr))
    printf("Failed IByteBuffer::Initialize\n");
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



 

