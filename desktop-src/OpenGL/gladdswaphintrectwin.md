---
title: Funzione glAddSwapHintRectWIN (Gl.h)
description: La funzione di callback glAddSwapHintRectWIN specifica un set di rettangoli che devono essere copiati da SwapBuffers.
ms.assetid: f242e755-8e8a-471a-9884-47efa22a3de6
keywords:
- Funzione glAddSwapHintRectWIN OpenGL
topic_type:
- apiref
api_name:
- glAddSwapHintRectWIN
api_location:
- Gl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75077ac2a93e3e952ae3c3daca3ea847f7b4b0efc340da0e980b1a4bec6efa64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118618051"
---
# <a name="gladdswaphintrectwin-function"></a>Funzione glAddSwapHintRectWIN

La funzione di callback **glAddSwapHintRectWIN** specifica un set di rettangoli che devono essere copiati [**da SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers).

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glAddSwapHintRectWIN(
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*x* 
</dt> <dd>

Coordinata *x*(in coordinate della finestra) dell'angolo inferiore sinistro del rettangolo dell'area dei suggerimenti.

</dd> <dt>

*y* 
</dt> <dd>

Coordinata *y*(in coordinate della finestra) dell'angolo inferiore sinistro del rettangolo dell'area del suggerimento.

</dd> <dt>

*width* 
</dt> <dd>

Larghezza del rettangolo dell'area del suggerimento.

</dd> <dt>

*height* 
</dt> <dd>

Altezza del rettangolo dell'area del suggerimento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

La **funzione glAddSwapHintRectWIN** accelera l'animazione riducendo la quantità di ridisegno tra i fotogrammi. Con **glAddSwapHintRectWIN** si specifica un set di aree rettangolari da copiare quando si chiama [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers). Quando non si specificano rettangoli **con glAddSwapHintRectWIN** prima di chiamare **SwapBuffers,** viene scambiato l'intero framebuffer. L'uso di **glAddSwapHintRectWIN** per copiare solo parti modificate del buffer può aumentare significativamente le prestazioni di **SwapBuffers,** soprattutto quando **SwapBuffers** viene implementato nel software.

La **funzione glAddSwapHintRectWIN** aggiunge un rettangolo all'area dei suggerimenti. Quando il flag PFD SWAP COPY della struttura in formato \_ \_ pixel [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) è impostato, **SwapBuffers** usa questa area per ritagliare la copia del buffer nascosto nel front buffer. Non si specifica PFD \_ SWAP \_ COPY, ma viene impostato dall'hardware con supporto. L'area dell'hint viene cancellata dopo ogni **chiamata a SwapBuffers**. Con alcune configurazioni hardware, **SwapBuffers** può ignorare l'area hint e scambiare l'intero buffer. **SwapBuffers** viene implementato dal sistema, non dall'applicazione.

OpenGL gestisce un'area dei suggerimenti separata per ogni finestra. Quando si chiama **glAddSwapHintRectWIN** in tutti i contesti di rendering associati a una finestra, i rettangoli dei suggerimenti vengono combinati in una singola area.

Chiamare **glAddSwapHintRectWIN** con un rettangolo di delimitazione per ogni oggetto disegnato per un frame e per ogni rettangolo cancellato per cancellare gli oggetti frame precedenti.

> [!Note]  
> La **funzione glAddSwapHintRectWIN** è una funzione di estensione che non fa parte della libreria OpenGL standard ma fa parte dell'estensione dell'hint di scambio GL \_ \_ \_ WIN. Per verificare se l'implementazione di OpenGL supporta **glAddSwapHintRectWIN,** chiamare **glGetString**(GL \_ EXTENSIONS). Se restituisce l'hint di scambio GL WIN, è supportato \_ \_ \_ **glAddSwapHintRectWIN.** Per ottenere l'indirizzo di una funzione di estensione, chiamare **wglGetProcAddress**.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                      |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                            |
| Intestazione<br/>                   | <dl> <dt>Gl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**glGetString**](glgetstring.md)
</dt> <dt>

[**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor)
</dt> <dt>

[**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers)
</dt> <dt>

[**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)
</dt> </dl>

 

 





