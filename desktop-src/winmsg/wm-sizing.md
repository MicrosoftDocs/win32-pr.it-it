---
description: Inviato a una finestra che l'utente sta ridimensionando. Elaborando questo messaggio, un'applicazione può monitorare le dimensioni e la posizione del rettangolo di trascinamento e, se necessario, modificarne le dimensioni o la posizione.
ms.assetid: 8cf56194-8a10-48e1-b0eb-aa3d66896599
title: Messaggio WM_SIZING (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0ab865994352eba28cdebaff3faab72a484ce0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756632"
---
# <a name="wm_sizing-message"></a>\_Messaggio di ridimensionamento WM

Inviato a una finestra che l'utente sta ridimensionando. Elaborando questo messaggio, un'applicazione può monitorare le dimensioni e la posizione del rettangolo di trascinamento e, se necessario, modificarne le dimensioni o la posizione.

Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_SIZING                       0x0214
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Bordo della finestra da ridimensionare. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                                                                         | Significato                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WMSZ_BOTTOM"></span><span id="wmsz_bottom"></span><dl> <dt>**WMSZ \_ ULTIMI**</dt> <dt>6</dt> </dl>                | Bordo inferiore<br/>         |
| <span id="WMSZ_BOTTOMLEFT"></span><span id="wmsz_bottomleft"></span><dl> <dt>**WMSZ \_ BOTTOMLEFT**</dt> <dt>7</dt> </dl>    | Angolo inferiore sinistro<br/>  |
| <span id="WMSZ_BOTTOMRIGHT"></span><span id="wmsz_bottomright"></span><dl> <dt>**WMSZ \_ BOTTOMRIGHT**</dt> <dt>8</dt> </dl> | Angolo inferiore destro<br/> |
| <span id="WMSZ_LEFT"></span><span id="wmsz_left"></span><dl> <dt>**WMSZ \_ A sinistra**</dt> <dt>1</dt> </dl>                      | Bordo sinistro<br/>           |
| <span id="WMSZ_RIGHT"></span><span id="wmsz_right"></span><dl> <dt>**WMSZ \_ DIRITTO**</dt> <dt>2</dt> </dl>                   | Bordo destro<br/>          |
| <span id="WMSZ_TOP"></span><span id="wmsz_top"></span><dl> <dt>**WMSZ \_ PRIMI**</dt> <dt>3</dt> </dl>                         | Bordo superiore<br/>            |
| <span id="WMSZ_TOPLEFT"></span><span id="wmsz_topleft"></span><dl> <dt>**WMSZ \_ In uscita**</dt> <dt>4</dt> </dl>             | Angolo superiore sinistro<br/>     |
| <span id="WMSZ_TOPRIGHT"></span><span id="wmsz_topright"></span><dl> <dt>**WMSZ \_ In destra**</dt> <dt>5</dt> </dl>          | Angolo superiore destro<br/>    |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) con le coordinate dello schermo del rettangolo di trascinamento. Per modificare le dimensioni o la posizione del rettangolo di trascinamento, un'applicazione deve modificare i membri di questa struttura.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **LRESULT**

Un'applicazione deve restituire **true** se elabora questo messaggio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**\_trasferimento WM**](wm-moving.md)
</dt> <dt>

[**\_dimensioni WM**](wm-size.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**RECT**](/previous-versions//dd162897(v=vs.85))
</dt> </dl>

 

 
