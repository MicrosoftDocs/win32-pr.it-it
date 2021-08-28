---
description: L'operatore di concatenazione += unisce i caratteri alla fine di questa stringa. L'operatore accetta un altro oggetto CHString, un puntatore a caratteri o un singolo carattere.
ms.assetid: 026ff9af-4cda-4261-aa27-e215d49b80ce
ms.tgt_platform: multiple
title: CHString::operator+= (ChString.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 316f5272c7b5a4ef5b59e93dd480ade215e3279ea754f1da5432448d46fcce17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119679880"
---
# <a name="chstringoperator"></a>CHString::operator+=

\[La [**classe CHString**](chstring.md) fa parte del framework del provider WMI che è ora considerato in stato finale e non saranno disponibili altri aggiornamenti, miglioramenti o sviluppo per problemi non correlati alla sicurezza che interessano queste librerie. Le [API MI devono essere](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) usate per tutti i nuovi sviluppi.\]

L'operatore di concatenazione += unisce i caratteri alla fine di questa stringa. L'operatore accetta un [**altro oggetto CHString,**](chstring.md) un puntatore a caratteri o un singolo carattere.

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

<span id="string"></span><span id="STRING"></span>*Stringa*
</dt> <dd>

Stringa [**CHString**](chstring.md) concatenata a questa stringa.

</dd> <dt>

<span id="ch"></span><span id="CH"></span>*Ch*
</dt> <dd>

Carattere da concatenare a questa stringa.

</dd> <dt>

<span id="lpsz"></span><span id="LPSZ"></span>*lpsz*
</dt> <dd>

Puntatore a **una stringa con** terminazione NULL da concatenare a questa stringa.

</dd> </dl>

## <a name="remarks"></a>Commenti

Tenere presente che le eccezioni di memoria possono verificarsi ogni volta che si usa questo operatore di concatenazione perché è possibile allocare nuove risorse di archiviazione per i caratteri aggiunti a [**questo oggetto CHString.**](chstring.md)

## <a name="examples"></a>Esempio

L'esempio seguente illustra l'uso **di CHString::operator +=**:


```C++
CHString s( L"abc" );
assert( ( s += L"def" ) == L"abcdef" );
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

 

