---
title: funzione glAddSwapHintRectWIN (GL. h)
description: La funzione di callback glAddSwapHintRectWIN specifica un set di rettangoli che devono essere copiati da SwapBuffers.
ms.assetid: f242e755-8e8a-471a-9884-47efa22a3de6
keywords:
- funzione glAddSwapHintRectWIN OpenGL
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
ms.openlocfilehash: 2ae3e10c2f51ff8d7c9763ff1dad7d09d800cd60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400711"
---
# <a name="gladdswaphintrectwin-function"></a>glAddSwapHintRectWIN (funzione)

La funzione di callback **glAddSwapHintRectWIN** specifica un set di rettangoli che devono essere copiati da [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers).

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

Coordinata *x*(in coordinate della finestra) dell'angolo inferiore sinistro del rettangolo dell'area dell'hint.

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

La funzione **glAddSwapHintRectWIN** accelera l'animazione riducendo la quantità di ridisegno tra i frame. Con **glAddSwapHintRectWIN** è possibile specificare un set di aree rettangolari che si desidera copiare quando si chiama [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers). Quando non si specifica alcun rettangolo con **glAddSwapHintRectWIN** prima di chiamare **SwapBuffers**, viene scambiato l'intero framebuffer. L'uso di **glAddSwapHintRectWIN** per copiare solo le parti modificate del buffer può migliorare significativamente le prestazioni di **SwapBuffers**, soprattutto quando **SwapBuffers** viene implementato nel software.

La funzione **glAddSwapHintRectWIN** aggiunge un rettangolo all'area del suggerimento. Quando \_ \_ viene impostato il flag di copia di scambio PFD della struttura del formato pixel [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) , **SwapBuffers** usa quest'area per ritagliare la copia del buffer nascosto nel buffer anteriore. Non viene specificata \_ \_ la copia di scambio PFD, che viene impostata da hardware idoneo. L'area del suggerimento viene cancellata dopo ogni chiamata a **SwapBuffers**. Con alcune configurazioni hardware, **SwapBuffers** può ignorare l'area del suggerimento ed scambiare l'intero buffer. **SwapBuffers** viene implementato dal sistema e non dall'applicazione.

OpenGL mantiene un'area di hint separata per ogni finestra. Quando si chiama **glAddSwapHintRectWIN** in tutti i contesti di rendering associati a una finestra, i rettangoli di hint vengono combinati in una singola area.

Chiamare **glAddSwapHintRectWIN** con un rettangolo di delimitazione per ogni oggetto disegnato per un frame e per ogni rettangolo cancellato per cancellare gli oggetti frame precedenti.

> [!Note]  
> La funzione **glAddSwapHintRectWIN** è una funzione di estensione che non fa parte della libreria OpenGL standard, ma fa parte dell' \_ estensione dell' \_ hint di scambio GL Win \_ . Per verificare se l'implementazione di OpenGL supporta **glAddSwapHintRectWIN**, chiamare **glGetString**(GL \_ Extensions). Se restituisce l'hint per lo \_ scambio di vittorie GL \_ \_ , **glAddSwapHintRectWIN** è supportato. Per ottenere l'indirizzo di una funzione di estensione, chiamare **wglGetProcAddress**.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                      |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                            |
| Intestazione<br/>                   | <dl> <dt>GL. h</dt> </dl> |



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

 

 





