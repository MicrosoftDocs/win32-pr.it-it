---
description: Il metodo stat recupera le informazioni statistiche dall'oggetto flusso.
ms.assetid: 7dfb59e9-143a-402e-990a-a2b35e6443dd
title: 'Metodo IByteBuffer:: stat (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Stat
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: bbbf033fc9ad5a25b3bcf5c22028ac1237f46c14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317078"
---
# <a name="ibytebufferstat-method"></a>Metodo IByteBuffer:: stat

\[Il metodo **Stat** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. L'interfaccia [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) fornisce funzionalità simili.\]

Il metodo **Stat** recupera le informazioni statistiche dall'oggetto flusso.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Stat(
  [out] LPSTATSTRUCT pstatstg,
  [in]  LONG         grfStatFlag
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pstatstg* \[ out\]
</dt> <dd>

Punta a una struttura **STATSTRUCT** in cui questo metodo inserisce informazioni su questo oggetto flusso. Questo puntatore è **null** se si verifica un errore.

</dd> <dt>

*grfStatFlag* \[ in\]
</dt> <dd>

Specifica che questo metodo non restituisce alcuni dei campi nella struttura **STATSTRUCT** , salvando così un'operazione di allocazione della memoria. I valori vengono ricavati dall'enumerazione [**STATFLAG**](/windows/win32/api/wtypes/ne-wtypes-statflag)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è un valore **HRESULT**. Il valore S \_ OK indica che la chiamata è stata eseguita correttamente.

## <a name="remarks"></a>Commenti

Il metodo **IByteBuffer:: stat** recupera un puntatore alla struttura **STATSTRUCT** che contiene informazioni su questo flusso aperto.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato come recuperare informazioni statistiche dal flusso.


```C++
STATSTRUCT  statstr;
HRESULT     hr;

// Retrieve the statistical information.
hr = pIByteBuff->Stat(&statstr,
                      STATFLAG_DEFAULT);
if (FAILED(hr))
  printf("Failed IByteBuffer::Stat\n");
else
  // Use statstr as needed.
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



 

