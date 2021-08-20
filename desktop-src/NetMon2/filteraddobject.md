---
description: La funzione FilterAddObject aggiunge un singolo oggetto a un filtro di visualizzazione.
ms.assetid: 796216f4-a407-4a8c-98b3-8c3761d91913
title: Funzione FilterAddObject (Netmon.h)
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
ms.openlocfilehash: 2c7d814efbbc77816836d437161390b1e2af60e8bbf4932322dcbd606920be5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118938734"
---
# <a name="filteraddobject-function"></a>Funzione FilterAddObject

La **funzione FilterAddObject** aggiunge un singolo oggetto a un [*filtro di visualizzazione.*](d.md)

## <a name="syntax"></a>Sintassi


```C++
DWORD WINAPI FilterAddObject(
  _In_  HFILTER        hFilter,
  _Out_ LPFILTEROBJECT lpFilterObject
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hFilter* \[ Pollici\]
</dt> <dd>

Handle per il filtro di visualizzazione.

</dd> <dt>

*lpFilterObject* \[ Cambio\]
</dt> <dd>

Puntatore a [una struttura FILTEROBJECT](filterobject.md) che definisce l'oggetto da aggiungere al filtro. Ogni oggetto può essere un operatore, un valore o una proprietà.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è NMERR \_ SUCCESS.

Se la funzione ha esito negativo, il valore restituito è un codice di errore.



| Codice restituito                                                                                              | Descrizione                                                                  |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**PARAMETRO NON \_ VALIDO DI NMERR \_**</dt> </dl> | Il *parametro hFilter* ha un valore non valido.<br/>                     |
| <dl> <dt>**MEMORIA INSUFFICIENTE DI NMERR \_ \_ \_**</dt> </dl>    | Network Monitor memoria sufficiente per creare l'oggetto.<br/> |



 

## <a name="remarks"></a>Commenti

[*Esperti*](e.md) e [*parser possono*](p.md) chiamare la **funzione FilterAddObject.**

La **funzione FilterAddObject** viene chiamata ogni volta che un oggetto filtro viene aggiunto al filtro di visualizzazione. Il filtro di visualizzazione è uno stack suffisso di oggetti che possono essere un operatore, un valore o una proprietà.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[FILTEROBJECT](filterobject.md)
</dt> </dl>

 

 




