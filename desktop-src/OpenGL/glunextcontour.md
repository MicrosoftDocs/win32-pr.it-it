---
title: Funzione gluNextContour (Glu.h)
description: La funzione gluNextContour contrassegna l'inizio di un altro contorno.
ms.assetid: 622cd631-3426-4206-9e23-af2a74343da5
keywords:
- Funzione gluNextContour OpenGL
topic_type:
- apiref
api_name:
- gluNextContour
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4607fbeea8e8aa46b365204bf1853c392c1a38f5ded594d840c6e9eea063da2f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061599"
---
# <a name="glunextcontour-function"></a>Funzione gluNextContour

\[La **funzione gluNextContour** è obsoleta e viene fornita solo per la compatibilità con le versioni precedenti. La **funzione gluNextContour** viene mappata a [**gluTessEndContour**](glutessendcontour.md) seguita da [**gluTessBeginContour**](glutessbegincontour.md).\]

La **funzione gluNextContour** contrassegna l'inizio di un altro contorno.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI gluNextContour(
   GLUtesselator *tess,
   GLenum        type
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Tess* 
</dt> <dd>

Oggetto a tassellamento (creato con [**gluNewTess).**](glunewtess.md)

</dd> <dt>

*type* 
</dt> <dd>

Tipo del contorno da definire. I valori seguenti sono validi.



| Valore                                                                                                                                                                | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_EXTERIOR"></span><span id="glu_exterior"></span><dl> <dt>**ESTERNO \_ GLU**</dt> </dl>           | Un contorno esterno definisce un limite esterno del poligono.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="GLU_INTERIOR"></span><span id="glu_interior"></span><dl> <dt>**GLU \_ INTERIOR**</dt> </dl>           | Un contorno interno definisce un limite interno del poligono ,ad esempio un foro.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="GLU_UNKNOWN"></span><span id="glu_unknown"></span><dl> <dt>**GLU \_ UNKNOWN**</dt> </dl>              | Un contorno sconosciuto viene analizzato dalla libreria per determinare se è interno o esterno.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="GLU_CCW__GLU_CW"></span><span id="glu_ccw__glu_cw"></span><dl> <dt>**GLU \_ CCW, GLU \_ CW**</dt> </dl> | Il primo \_ contorno GLU CCW o GLU \_ CW definito è considerato esterno. Tutti gli altri contorni sono considerati esterni se sono orientati nella stessa direzione (in senso orario o in senso antiorario) del primo contorno e interni, in caso contrario.<br/> Se un contorno è di tipo GLU CCW o GLU CW, tutti i contorni devono essere dello stesso tipo (in caso contrario, tutti i contorni GLU CCW e GLU CW verranno modificati in \_ \_ GLU \_ \_ \_ UNKNOWN). Si noti che non esiste alcuna differenza reale tra i tipi di contorno \_ GLU CCW e GLU \_ CW.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Usare la **funzione gluNextContour** per descrivere i poligoni con più contorni. Dopo aver descritto il primo contorno tramite una serie di chiamate [**gluTessVertex,**](glutessvertex.md) una chiamata **gluNextContour** indica che il contorno precedente è completo e che il contorno successivo sta per iniziare. Eseguire **un'altra serie di chiamate gluTessVertex** per descrivere il nuovo contorno. Ripetere questo processo fino a quando non sono stati descritti tutti i contorni.

Il *parametro* di tipo definisce il tipo di contorno seguente.

Per definire il tipo del primo contorno, è possibile chiamare **gluNextContour** prima di descrivere il primo contorno. Se non si chiama **gluNextContour** prima del primo contorno, il primo contorno è contrassegnato come GLU \_ EXTERIOR.

## <a name="examples"></a>Esempio

È possibile descrivere un quadrilatero con un foro triangolare nel modo seguente:

``` syntax
gluBeginPolygon(tess); 
    gluTessVertex(tess, v1, v1); 
    gluTessVertex(tess, v2, v2); 
    gluTessVertex(tess, v3, v3); 
    gluTessVertex(tess, v4, v4);  
gluNextContour(tess, GLU_INTERIOR); 
    gluTessVertex(tess, v5, v5); 
    gluTessVertex(tess, v6, v6); 
    gluTessVertex(tess, v7, v7);  
gluEndPolygon(tess);
```

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Glu.h</dt> </dl>     |
| Libreria<br/>                  | <dl> <dt>Glu32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**gluNewTess**](glunewtess.md)
</dt> <dt>

[**gluTessBeginContour**](glutessbegincontour.md)
</dt> <dt>

[**gluTessBeginPolygon**](glubeginpolygon.md)
</dt> <dt>

[*gluTessCallback*](glutess.md)
</dt> <dt>

[**gluTessEndContour**](glutessendcontour.md)
</dt> <dt>

[**gluTessVertex**](glutessvertex.md)
</dt> </dl>

 

 





