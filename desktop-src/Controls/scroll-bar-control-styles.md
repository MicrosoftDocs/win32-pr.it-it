---
title: Stili del controllo barra di scorrimento (winuser. h)
description: Per creare un controllo barra di scorrimento usando la funzione CreateWindow o CreateWindowEx, specificare la classe SCROLLBAR, le costanti di stile della finestra appropriate e una combinazione degli stili del controllo barra di scorrimento seguenti.
ms.assetid: 07195a95-eff8-4a47-926a-9d503fa7b299
topic_type:
- apiref
api_name:
- SBS_BOTTOMALIGN
- SBS_HORZ
- SBS_LEFTALIGN
- SBS_RIGHTALIGN
- SBS_SIZEBOX
- SBS_SIZEBOXBOTTOMRIGHTALIGN
- SBS_SIZEBOXTOPLEFTALIGN
- SBS_SIZEGRIP
- SBS_TOPALIGN
- SBS_VERT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cc5de721fd4cc44867fca0dbe1b35dcaf58c6dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327848"
---
# <a name="scroll-bar-control-styles"></a>Stili del controllo barra di scorrimento

Per creare un controllo barra di scorrimento usando la funzione [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , specificare la classe ScrollBar, le costanti di stile della finestra appropriate e una combinazione degli stili del controllo barra di scorrimento seguenti. Alcuni stili creano un controllo barra di scorrimento che usa una larghezza o un'altezza predefinita. Tuttavia, quando si chiama **CreateWindow** o **CreateWindowEx**, è necessario specificare sempre le coordinate x e y e le altre dimensioni della barra di scorrimento.



| Costante                                                                                                                                                                                                | Descrizione                                                                                                                                                                                                                                                                                                                                |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SBS_BOTTOMALIGN"></span><span id="sbs_bottomalign"></span><dl> <dt>**SBS \_ BOTTOMALIGN**</dt> </dl>                                     | Allinea il bordo inferiore della barra di scorrimento al bordo inferiore del rettangolo definito dai parametri *x*, *y*, *NWidth* e *nHeight* della funzione [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) . La barra di scorrimento ha l'altezza predefinita per le barre di scorrimento del sistema. Usare questo stile con lo \_ stile SBS orizzontalmente.<br/>                      |
| <span id="SBS_HORZ"></span><span id="sbs_horz"></span><dl> <dt>**SBS \_ orizzontalmente**</dt> </dl>                                                          | Designa una barra di scorrimento orizzontale. Se non \_ si specifica né lo stile BOTTOMALIGN SBS né SBS \_ , la barra di scorrimento avrà l'altezza, la larghezza e la posizione specificate dai *parametri x*, *y*, *nWidth* e *nHeight* di [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa).<br/>                                                      |
| <span id="SBS_LEFTALIGN"></span><span id="sbs_leftalign"></span><dl> <dt>**SBS \_ LEFTALIGN**</dt> </dl>                                           | Allinea il bordo sinistro della barra di scorrimento al bordo sinistro del rettangolo definito dai parametri *x*, *y*, *nWidth* e *nHeight* di [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa). La barra di scorrimento ha la larghezza predefinita per le barre di scorrimento del sistema. Usare questo stile con lo stile di SBS \_ Vert.<br/>                                    |
| <span id="SBS_RIGHTALIGN"></span><span id="sbs_rightalign"></span><dl> <dt>**SBS \_ RIGHTALIGN**</dt> </dl>                                        | Allinea il bordo destro della barra di scorrimento al bordo destro del rettangolo definito dai parametri *x*, *y*, *nWidth* e *nHeight* di [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa). La barra di scorrimento ha la larghezza predefinita per le barre di scorrimento del sistema. Usare questo stile con lo stile di SBS \_ Vert.<br/>                                  |
| <span id="SBS_SIZEBOX"></span><span id="sbs_sizebox"></span><dl> <dt>**SBS \_ SIZEBOX**</dt> </dl>                                                 | Designa una casella delle dimensioni. Se non si specifica né lo \_ stile SBS SIZEBOXBOTTOMRIGHTALIGN né SBS \_ SIZEBOXTOPLEFTALIGN, la casella dimensioni ha altezza, larghezza e posizione specificati dai parametri *x*, *y*, *nWidth* e *nHeight* di [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa). <br/>                                          |
| <span id="SBS_SIZEBOXBOTTOMRIGHTALIGN"></span><span id="sbs_sizeboxbottomrightalign"></span><dl> <dt>**SBS \_ SIZEBOXBOTTOMRIGHTALIGN**</dt> </dl> | Allinea l'angolo inferiore destro della casella dimensione all'angolo inferiore destro del rettangolo specificato dai parametri *x*, *y*, *nWidth* e *nHeight* di [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa). La casella dimensioni ha le dimensioni predefinite per le caselle delle dimensioni del sistema. Usare questo stile con gli \_ stili SBS SIZEBOX o SBS \_ SIZEGRIP.<br/> |
| <span id="SBS_SIZEBOXTOPLEFTALIGN"></span><span id="sbs_sizeboxtopleftalign"></span><dl> <dt>**SBS \_ SIZEBOXTOPLEFTALIGN**</dt> </dl>             | Allinea l'angolo superiore sinistro della casella dimensione all'angolo superiore sinistro del rettangolo specificato dai parametri *x*, *y*, *nWidth* e *nHeight* di [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa). La casella dimensioni ha le dimensioni predefinite per le caselle delle dimensioni del sistema. Usare questo stile con gli \_ stili SBS SIZEBOX o SBS \_ SIZEGRIP.<br/>   |
| <span id="SBS_SIZEGRIP"></span><span id="sbs_sizegrip"></span><dl> <dt>**SBS \_ SIZEGRIP**</dt> </dl>                                              | Uguale a SBS \_ SIZEBOX, ma con un bordo elevato. <br/>                                                                                                                                                                                                                                                                                  |
| <span id="SBS_TOPALIGN"></span><span id="sbs_topalign"></span><dl> <dt>**SBS \_ ALlineata**</dt> </dl>                                              | Allinea il bordo superiore della barra di scorrimento al bordo superiore del rettangolo definito dai parametri *x*, *y*, *nWidth* e *nHeight* di [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa). La barra di scorrimento ha l'altezza predefinita per le barre di scorrimento del sistema. Usare questo stile con lo \_ stile SBS orizzontalmente.<br/>                                     |
| <span id="SBS_VERT"></span><span id="sbs_vert"></span><dl> <dt>**SBS \_ Vert**</dt> </dl>                                                          | Designa una barra di scorrimento verticale. Se non si specifica né lo \_ stile SBS RIGHTALIGN né SBS \_ LEFTALIGN, la barra di scorrimento avrà l'altezza, la larghezza e la posizione specificate dai parametri *x*, *y*, *nWidth* e *nHeight* di [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa).<br/>                                                     |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|--------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Winuser. h</dt> </dl> |



 

