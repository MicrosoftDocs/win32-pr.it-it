---
description: L'operatore di concatenazione + = unisce i caratteri alla fine di questa stringa. L'operatore accetta un altro oggetto CHString, un puntatore a caratteri o un singolo carattere.
ms.assetid: 026ff9af-4cda-4261-aa27-e215d49b80ce
ms.tgt_platform: multiple
title: 'CHString:: operator + = (ChString. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 683ca6b6264169cd156e89c3447c63fa59f03585
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313200"
---
# <a name="chstringoperator"></a>CHString:: operator + =

\[La classe [**CHString**](chstring.md) fa parte del Framework del provider WMI, che è ora considerato nello stato finale e non sono disponibili ulteriori sviluppi, miglioramenti o aggiornamenti per i problemi non correlati alla sicurezza che interessano queste librerie. Le [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devono essere usate per tutte le nuove attività di sviluppo.\]

L'operatore di concatenazione + = unisce i caratteri alla fine di questa stringa. L'operatore accetta un altro oggetto [**CHString**](chstring.md) , un puntatore a caratteri o un singolo carattere.

``` syntax
const CHString& operator +=(
  const CHString& string )
throw( CHeap_Exception );

const CHString& operator +=(
  WCHAR ch )
throw( CHeap_Exception );

const CHString& operator +=(
  LPCWSTR lpsz )
throw( CHeap_Exception );

const CHString operator +=(
  char ch )
throw( CHeap_Exception );
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="string"></span><span id="STRING"></span>*stringa*
</dt> <dd>

Stringa [**CHString**](chstring.md) che concatena a questa stringa.

</dd> <dt>

<span id="ch"></span><span id="CH"></span>*ch*
</dt> <dd>

Carattere da concatenare a questa stringa.

</dd> <dt>

<span id="lpsz"></span><span id="LPSZ"></span>*lpsz*
</dt> <dd>

Puntatore a una stringa con terminazione **null** da concatenare a questa stringa.

</dd> </dl>

## <a name="remarks"></a>Commenti

Tenere presente che le eccezioni di memoria possono verificarsi quando si usa questo operatore di concatenazione perché è possibile allocare una nuova risorsa di archiviazione per i caratteri aggiunti a questo oggetto [**CHString**](chstring.md) .

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato l'utilizzo di **CHString:: operator + =**:


```C++
CHString s( L"abc" );
assert( ( s += L"def" ) == L"abcdef" );
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

 

