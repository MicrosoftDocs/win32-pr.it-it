---
title: Funzione glEdgeFlagv (Gl.h)
description: Contrassegna i bordi come limite o non associato. | Funzione glEdgeFlagv (Gl.h)
ms.assetid: 69b5ddbd-7c0c-47f0-a358-d8bf81755c88
keywords:
- Funzione glEdgeFlagv OpenGL
topic_type:
- apiref
api_name:
- glEdgeFlagv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9622cb3c7d80d241d0f12957094a06980f5fcf7f28b4f95eaa0de1595b34d1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118616533"
---
# <a name="gledgeflagv-function"></a>Funzione glEdgeFlagv

Contrassegna i bordi come limite o non associato.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glEdgeFlagv(
   const GLboolean *flag
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*flag* 
</dt> <dd>

Specifica un puntatore a una matrice che contiene un singolo elemento booleano, che sostituisce il valore del flag di bordo corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Ogni vertice di un poligono, un triangolo separato o un quadrilatero separato specificato tra una coppia [**glBegin**](/windows/desktop/OpenGL/glbegin)glEnd è contrassegnato come inizio di un limite o di un bordo / [](/windows/desktop/OpenGL/glend) non associato. Se il flag di bordo corrente **è TRUE** quando viene specificato il vertice, il vertice viene contrassegnato come inizio di un bordo limite. Se il flag di bordo corrente **è FALSE,** il vertice viene contrassegnato come inizio di un bordo non associato. La **funzione glEdgeFlagv** imposta il flag edge su **TRUE** se il flag è diverso da zero, FALSE **in caso** contrario.

I vertici dei triangoli connessi e dei quadrilateri connessi sono sempre contrassegnati come limite, indipendentemente dal valore del flag di bordo.

I flag limite e degli bordi non associati sui vertici sono significativi solo se GL POLYGON MODE è \_ impostato su GL POINT o GL \_ \_ \_ LINE. Vedere [**glPolygonMode.**](/windows/desktop/OpenGL/glpolygonmode)

Inizialmente, il bit del flag edge è **TRUE.**

Il flag edge corrente può essere aggiornato in qualsiasi momento. In particolare, **glEdgeFlagv** può essere chiamato tra una chiamata a [**glBegin**](/windows/desktop/OpenGL/glbegin) e la chiamata corrispondente a [**glEnd**](/windows/desktop/OpenGL/glend).

Le funzioni seguenti recuperano informazioni correlate **a glEdgeFlagv**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ EDGE \_ FLAG

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Libreria<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



 

