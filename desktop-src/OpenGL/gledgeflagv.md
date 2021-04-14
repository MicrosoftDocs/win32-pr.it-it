---
title: funzione glEdgeFlagv (GL. h)
description: Contrassegna i bordi come limite o non delimitato. | funzione glEdgeFlagv (GL. h)
ms.assetid: 69b5ddbd-7c0c-47f0-a358-d8bf81755c88
keywords:
- funzione glEdgeFlagv OpenGL
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
ms.openlocfilehash: fe031ab3981e3daa2e6b1aefd51c9eaa62c84483
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353171"
---
# <a name="gledgeflagv-function"></a>glEdgeFlagv (funzione)

Contrassegna i bordi come limite o non delimitato.

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

Specifica un puntatore a una matrice che contiene un singolo elemento booleano, che sostituisce il valore del flag perimetrale corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Ogni vertice di un poligono, un triangolo separato o un quadrilatero separato specificato tra una coppia [**glBegin**](/windows/desktop/OpenGL/glbegin) / [**glEnd**](/windows/desktop/OpenGL/glend) è contrassegnato come inizio di un limite o di un bordo non delimitatore. Se il flag del bordo corrente è **true** quando viene specificato il vertice, il vertice viene contrassegnato come inizio di un bordo limite. Se il flag perimetrale corrente è **false**, il vertice è contrassegnato come inizio di un bordo non associato. La funzione **glEdgeFlagv** imposta il flag Edge su **true** se flag è diverso da zero, **false** in caso contrario.

I vertici dei triangoli e dei quadrilateri connessi sono sempre contrassegnati come limite, indipendentemente dal valore del flag Edge.

I flag perimetrali e bordi non delimitativi sui vertici sono significativi solo se \_ la modalità del poligono GL \_ è impostata sulla \_ linea GL o sul punto GL \_ . Vedere [**glPolygonMode**](/windows/desktop/OpenGL/glpolygonmode).

Inizialmente, il bit del flag Edge è **true**.

Il flag perimetrale corrente può essere aggiornato in qualsiasi momento. In particolare, è possibile chiamare **glEdgeFlagv** tra una chiamata a [**glBegin**](/windows/desktop/OpenGL/glbegin) e la chiamata corrispondente a [**glEnd**](/windows/desktop/OpenGL/glend).

Le funzioni seguenti consentono di recuperare informazioni correlate a **glEdgeFlagv**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con flag di \_ bordo GL argomento \_

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>GL. h</dt> </dl>         |
| Libreria<br/>                  | <dl> <dt>Opengl32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



 

