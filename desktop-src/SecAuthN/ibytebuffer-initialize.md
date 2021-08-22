---
description: Il metodo Initialize prepara l'oggetto IByteBuffer per l'uso. Questo metodo deve essere chiamato prima di chiamare qualsiasi altro metodo nell'interfaccia IByteBuffer.
ms.assetid: 1b22e693-0add-4b80-a2c4-925ebd3ab3a6
title: Metodo IByteBuffer::Initialize (Scardssp.h)
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
ms.openlocfilehash: 28a525b26d49dd5df8a2be3ba6a5af5a16459c26e191368badae34ca381488e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119417631"
---
# <a name="ibytebufferinitialize-method"></a>Metodo IByteBuffer::Initialize

\[Il **metodo Initialize** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive. [**L'interfaccia IStream**](/windows/desktop/api/objidl/nn-objidl-istream) offre funzionalità simili.\]

Il **metodo Initialize** prepara l'oggetto [**IByteBuffer**](ibytebuffer.md) per l'uso. Questo metodo deve essere chiamato prima di chiamare qualsiasi altro metodo **nell'interfaccia IByteBuffer.**

## <a name="syntax"></a>Sintassi


```C++
HRESULT Initialize(
  [in] LONG lSize,
  [in] BYTE *pData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lSize* \[ Pollici\]
</dt> <dd>

Dimensioni iniziali, in byte, dei dati che il flusso deve contenere.

</dd> <dt>

*pData* \[ Pollici\]
</dt> <dd>

Se non **è NULL,** i dati iniziali da scrivere nel flusso.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è **HRESULT.** Il valore S \_ OK indica che la chiamata ha avuto esito positivo.

## <a name="remarks"></a>Commenti

Quando si usa un [**nuovo flusso IByteBuffer,**](ibytebuffer.md) chiamare questo metodo prima di usare uno degli altri **metodi IByteBuffer.**

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrata l'inizializzazione [**dell'oggetto IByteBuffer.**](ibytebuffer.md)


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
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                    |
| Fine del supporto client<br/>    | Windows XP<br/>                                                                   |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Scardssp.h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Scardssp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID IByteBuffer è definito \_ come E126F8FE-A7AF-11D0-B88A-00C04FD424B9<br/>          |



 

