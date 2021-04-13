---
description: La funzione FilterAddObject aggiunge un singolo oggetto a un filtro di visualizzazione.
ms.assetid: 796216f4-a407-4a8c-98b3-8c3761d91913
title: Funzione FilterAddObject (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FilterAddObject
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 7fc6c41a675bfe560c060e271e4f9f48f88cd58c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484332"
---
# <a name="filteraddobject-function"></a>FilterAddObject (funzione)

La funzione **FilterAddObject** aggiunge un singolo oggetto a un [*filtro di visualizzazione*](d.md).

## <a name="syntax"></a>Sintassi


```C++
DWORD WINAPI FilterAddObject(
  _In_  HFILTER        hFilter,
  _Out_ LPFILTEROBJECT lpFilterObject
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hFilter* \[ in\]
</dt> <dd>

Handle per il filtro di visualizzazione.

</dd> <dt>

*lpFilterObject* \[ out\]
</dt> <dd>

Puntatore a una struttura [FILTEROBJECT](filterobject.md) che definisce l'oggetto da aggiungere al filtro. Ogni oggetto può essere un operatore, un valore o una proprietà.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è NMERR \_ Success.

Se la funzione ha esito negativo, il valore restituito è un codice di errore.



| Codice restituito                                                                                              | Descrizione                                                                  |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**\_parametro NMERR non valido \_**</dt> </dl> | Il parametro *hFilter* contiene un valore non valido.<br/>                     |
| <dl> <dt>**\_ \_ \_ memoria insufficiente NMERR**</dt> </dl>    | Network Monitor non dispone di memoria sufficiente per creare l'oggetto.<br/> |



 

## <a name="remarks"></a>Commenti

Gli [*esperti*](e.md) e i [*parser*](p.md) possono chiamare la funzione **FilterAddObject** .

La funzione **FilterAddObject** viene chiamata ogni volta che un oggetto filtro viene aggiunto al filtro di visualizzazione. Il filtro di visualizzazione è uno stack di oggetti suffisso che può essere un operatore, un valore o una proprietà.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmap. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[FILTEROBJECT](filterobject.md)
</dt> </dl>

 

 




