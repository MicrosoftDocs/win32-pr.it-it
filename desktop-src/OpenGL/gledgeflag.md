---
title: Funzione glEdgeFlag (Gl.h)
description: Contrassegna i bordi come limite o non associato. | Funzione glEdgeFlag (Gl.h)
ms.assetid: cebaa4af-a3bc-4396-9ee0-8cc10bcaf256
keywords:
- Funzione glEdgeFlag OpenGL
topic_type:
- apiref
api_name:
- glEdgeFlag
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c7f78575c79b3da5b48125203d88c9b20e7eb1dc11ee860deea01dfa7dcea28
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081591"
---
# <a name="gledgeflag-function"></a>Funzione glEdgeFlag

Contrassegna i bordi come limite o non associato.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glEdgeFlag(
   GLboolean flag
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*flag* 
</dt> <dd>

Specifica il valore corrente del flag di bordo, **TRUE** o **FALSE.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Ogni vertice di un poligono, un triangolo separato o un quadrilatero separato specificato tra una coppia [**glBegin**](/windows/desktop/OpenGL/glbegin)glEnd è contrassegnato come inizio di un limite o di un bordo / [](/windows/desktop/OpenGL/glend) non associato. Se il flag di bordo corrente **è TRUE** quando viene specificato il vertice, il vertice viene contrassegnato come inizio di un bordo limite. Se il flag di bordo corrente **è FALSE,** il vertice viene contrassegnato come inizio di un bordo non associato. La **funzione glEdgeFlag** imposta il flag edge su **TRUE** se il flag è diverso da zero, FALSE **in caso** contrario.

I vertici dei triangoli connessi e dei quadrilateri connessi sono sempre contrassegnati come limite, indipendentemente dal valore del flag di bordo.

I flag di limite e di bordo non associati sui vertici sono significativi solo se GL POLYGON MODE è \_ impostato su GL POINT o GL \_ \_ \_ LINE. Vedere [**glPolygonMode.**](/windows/desktop/OpenGL/glpolygonmode)

Inizialmente, il bit del flag edge è **TRUE.**

Il flag edge corrente può essere aggiornato in qualsiasi momento. In particolare, **glEdgeFlag** può essere chiamato tra una chiamata a [**glBegin**](/windows/desktop/OpenGL/glbegin) e la chiamata corrispondente a [**glEnd**](/windows/desktop/OpenGL/glend).

Le funzioni seguenti recuperano informazioni correlate **a glEdgeFlag**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ EDGE \_ FLAG

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Libreria<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



 

