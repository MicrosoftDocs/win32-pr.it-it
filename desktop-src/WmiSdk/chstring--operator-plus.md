---
description: L'operatore di concatenazione + unisce due stringhe e restituisce un oggetto CHString.
ms.assetid: b7ed6379-ccfa-40f9-9607-d9033179b674
ms.tgt_platform: multiple
title: 'CHString:: operator + (ChString. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5053a4d3059a66cb2c8e4a89a3bdd531d5f42de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758219"
---
# <a name="chstringoperator"></a>CHString:: operator +

\[La classe [**CHString**](chstring.md) fa parte del Framework del provider WMI, che è ora considerato nello stato finale e non sono disponibili ulteriori sviluppi, miglioramenti o aggiornamenti per i problemi non correlati alla sicurezza che interessano queste librerie. Le [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devono essere usate per tutte le nuove attività di sviluppo.\]

L'operatore di concatenazione + unisce due stringhe e restituisce un oggetto [**CHString**](chstring.md) .

``` syntax
friend CHString operator +(
  const CHString& str1,
  const CHString& str2 )
throw( CHeap_Exception );

friend CHString operator +(
  const CHString& str,
  WCHAR ch )
throw( CHeap_Exception );

friend CHString operator +(
  WCHAR ch,
  const CHString& str )
throw( CHeap_Exception );

friend CHString operator +(
  const CHString& str,
  LPCWSTR lpsz )
throw( CHeap_Exception );

friend CHString operator +(
  LPCWSTR lpsz,
  const CHString& str )
throw( CHeap_Exception );

friend CHString operator +(
  const CHString& str,
  char ch )
throw( CHeap_Exception );

friend CHString operator +(
  char ch,
  const CHString& str )
throw( CHeap_Exception );
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="str__str1__str2"></span><span id="STR__STR1__STR2"></span>*Str, str1, str2*
</dt> <dd>

[**CHString**](chstring.md) stringhe concatenate.

</dd> <dt>

<span id="ch"></span><span id="CH"></span>*ch*
</dt> <dd>

Carattere che concatena a una stringa o una stringa concatenata a un carattere.

</dd> <dt>

<span id="lpsz"></span><span id="LPSZ"></span>*lpsz*
</dt> <dd>

Puntatore a una stringa di caratteri con terminazione **null**.

</dd> </dl>

## <a name="return-values"></a>Valori restituiti

Questo operatore di concatenazione restituisce un oggetto [**CHString**](chstring.md) che rappresenta il risultato temporaneo della concatenazione. Questo valore restituito rende possibile combinare più concatenazioni nella stessa espressione.

## <a name="remarks"></a>Commenti

Una delle due stringhe di argomento deve essere un oggetto [**CHString**](chstring.md) . l'altro può essere un puntatore a caratteri o un carattere. Tenere presente che le eccezioni di memoria possono verificarsi quando si usa l'operatore di concatenazione perché è possibile allocare una nuova risorsa di archiviazione per contenere dati temporanei.

## <a name="examples"></a>Esempio

L'esempio di codice seguente illustra l'uso di **CHString:: operator +**:


```C++
CHString s1( L"abc" );
CHString s2( L"def" );
assert( (s1 + s2 ) == L"abcdef" );

CHString s3;
s3 = CHString( L"abc" ) + "def" ; // Correct
s3 = "abc" + "def"; // Wrong. The first argument must be a CHString.
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                                                                                      |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                                                                                |
| Intestazione<br/>                   | <dl> <dt>ChString. h (include FwCommon. h)</dt> </dl>                                                    |
| Libreria<br/>                  | <dl> <dt>FrameDyn. lib</dt> </dl>                                                                       |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CHString**](chstring.md)
</dt> </dl>

 

