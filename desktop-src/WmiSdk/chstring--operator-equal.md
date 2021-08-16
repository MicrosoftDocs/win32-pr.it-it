---
description: L'operatore chString assignment (=) reinizializza un oggetto CHString esistente con nuovi dati.
ms.assetid: 6864aacf-ac18-4b5a-be3e-3a0d8bb31e74
ms.tgt_platform: multiple
title: CHString::operator= (ChString.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dde67bbf0f1a7326074bc7638cdd6b256ad763e115ad12e2c193e6bcdc66605e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131783"
---
# <a name="chstringoperator"></a>CHString::operator=

\[La [**classe CHString**](chstring.md) fa parte del framework del provider WMI che è ora considerato in stato finale e non saranno disponibili altri aggiornamenti, miglioramenti o sviluppo per problemi non correlati alla sicurezza che interessano queste librerie. Le [API MI devono essere](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) usate per tutti i nuovi sviluppi.\]

[**L'operatore chString**](chstring.md) assignment (=) reinizializza un oggetto CHString esistente con nuovi dati.

``` syntax
const CHString& operator =(
  const CHString& stringSrc )
throw( CHeap_Exception );

const CHString& operator =(
  WCHAR ch )
throw( CHeap_Exception );

const CHString& operator =(
  const unsigned char* psz )
throw( CHeap_Exception );

const CHString& operator =(
  LPCWSTR lpsz )
throw( CHeap_Exception );

const CHString& operator =(
  LPCSTR lpsz )
throw( CHeap_Exception );

const CHString& operator =(
  CHString *p )
throw( CHeap_Exception );

const CHString& operator =(
  char ch )
throw( CHeap_Exception );
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="stringSrc__p"></span><span id="stringsrc__p"></span><span id="STRINGSRC__P"></span>*stringSrc*, *p*
</dt> <dd>

Assegna una [**stringa CHString**](chstring.md) a questo oggetto.

</dd> <dt>

<span id="ch"></span><span id="CH"></span>*Ch*
</dt> <dd>

Assegna un carattere a questo oggetto.

</dd> <dt>

<span id="lpsz__psz"></span><span id="LPSZ__PSZ"></span>*lpsz*, *psz*
</dt> <dd>

Assegna una **stringa con** terminazione NULL a questo oggetto.

</dd> </dl>

## <a name="remarks"></a>Commenti

Se la stringa di destinazione (ovvero il lato sinistro) è già sufficientemente grande per archiviare i nuovi dati, non viene eseguita alcuna nuova allocazione di memoria. Tuttavia, le eccezioni di memoria possono verificarsi ogni volta che si usa l'operatore di assegnazione perché viene spesso allocata una nuova risorsa di archiviazione per contenere [**l'oggetto CHString**](chstring.md) risultante.

## <a name="examples"></a>Esempio

L'esempio di codice seguente illustra l'uso **di CHString::operator =**:


```C++
CHString s1, s2;        // Empty CHString objects

s1 = L"cat";            // s1 = "cat"
s2 = s1;                // s1 and s2 each = "cat"
s1 = L"the " + s1;      // Or expressions
s1 = 'x';               // Or just individual characters
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                                                                                      |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                                                                                |
| Intestazione<br/>                   | <dl> <dt>ChString.h (includere FwCommon.h)</dt> </dl>                                                    |
| Libreria<br/>                  | <dl> <dt>FrameDyn.lib</dt> </dl>                                                                       |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CHString**](chstring.md)
</dt> </dl>

 

