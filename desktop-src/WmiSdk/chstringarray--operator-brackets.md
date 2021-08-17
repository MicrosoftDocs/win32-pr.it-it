---
description: Questi operatori di indice impostano o ottengono l'elemento in corrispondenza dell'indice specificato. Questi operatori sono un comodo sostituto dei metodi SetAt e GetAt.
ms.assetid: 93b10bef-908e-4c5e-aac3-b13051b2e7c9
ms.tgt_platform: multiple
title: CHStringArray::operator [ ] (ChStrArr.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 859cfe52535aea0fb43d6195648215431f80cff86f0525b9ef7c5247b6a831a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131773"
---
# <a name="chstringarrayoperator--"></a>CHStringArray::operator \[\]

\[La [**classe CHStringArray**](/windows/desktop/api/ChStrArr/nl-chstrarr-chstringarray) fa parte del framework del provider WMI che è ora considerato in stato finale e non saranno disponibili altri aggiornamenti, miglioramenti o sviluppo per problemi non correlati alla sicurezza che interessano queste librerie. Le [API mi devono essere usate](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) per tutti i nuovi progetti di sviluppo.\]

Questi operatori di indice impostano o ottengono l'elemento in corrispondenza dell'indice specificato. Questi operatori sono un comodo sostituto dei [**metodi SetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-setat(int_lpcwstr)) [**e GetAt.**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getat(int))

``` syntax
CHString& operator []( 
  int nIndex
);

CHString operator []( 
  int nIndex
) const;
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="nIndex"></span><span id="nindex"></span><span id="NINDEX"></span>*Nindex*
</dt> <dd>

Indice intero maggiore o uguale a zero e minore o uguale al valore restituito da [ **GetUpperBound**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getupperbound)

</dd> </dl>

## <a name="return-values"></a>Valori restituiti

Gli operatori di indice restituiscono [**l'elemento puntatore CHString**](chstring.md) attualmente in corrispondenza di questo indice.

## <a name="remarks"></a>Commenti

È possibile usare il primo operatore , che chiama per le matrici che non sono **const**, a destra (r-value) o a sinistra (l-value) di un'istruzione di assegnazione. Il secondo, che chiama **per le matrici const,** può essere usato solo a destra.

La versione di debug della libreria asserzione se l'indice (a sinistra o a destra di un'istruzione di assegnazione) non è in limiti.

## <a name="examples"></a>Esempio

Nell'esempio di codice seguente viene illustrato l'uso di [**\[ \] CHStringArray::operator**](/previous-versions/windows/desktop/legacy/aa384934(v=vs.85)).


```C++
CHStringArray array;
CHString s;

array.Add( L"String 1" ); // Element 0 
array.Add( L"String 2" ); // Element 1 
s = array[0]; // Get element 0
assert( s == L"String 1" ); 

array[0] = L"String 3"; // Replace element 0 
assert( array[0] == L"String 3" );
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                                                                                      |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                                                                                |
| Intestazione<br/>                   | <dl> <dt>ChStrArr.h (includere FwCommon.h)</dt> </dl>                                                    |
| Libreria<br/>                  | <dl> <dt>FrameDyn.lib</dt> </dl>                                                                       |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CHStringArray::Add**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-add)
</dt> <dt>

[**CHStringArray::GetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getat(int))
</dt> <dt>

[**CHStringArray::SetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-setat(int_lpcwstr))
</dt> </dl>

