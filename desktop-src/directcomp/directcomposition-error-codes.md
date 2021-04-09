---
title: Codici di errore DirectComposition (Dcomp. h)
description: In questa sezione vengono descritti i codici di errore specifici per DirectComposition.
ms.assetid: 8DFBFC34-DBD0-4731-8305-B33E90C96C54
topic_type:
- apiref
api_name:
- DCOMPOSITION_ERROR_ACCESS_DENIED
- DCOMPOSITION_ERROR_SURFACE_BEING_RENDERED
- DCOMPOSITION_ERROR_SURFACE_NOT_BEING_RENDERED
- DCOMPOSITION_ERROR_WINDOW_ALREADY_COMPOSED
api_location:
- Dcomp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96a76a7527bacf8caa756a0fad75ca70f4bf9a77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120579"
---
# <a name="directcomposition-error-codes"></a>Codici di errore DirectComposition

Se si verifica un errore, Microsoft DirectComposition restituisce un codice come valore **HRESULT** . In questa sezione vengono descritti i codici di errore specifici per DirectComposition. Per un elenco di codici di errore generali Component Object Model (COM), vedere [codici di errore com](/windows/desktop/com/com-error-codes).

<dl> <dt>

<span id="DCOMPOSITION_ERROR_ACCESS_DENIED"></span><span id="dcomposition_error_access_denied"></span>**\_accesso agli errori di DCOMPOSITION \_ \_ negato**
</dt> <dd> <dl> <dt>


</dt> <dt>



L'handle di finestra specificato in una chiamata al metodo [**IDCompositionDevice:: CreateTargetForHwnd**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtargetforhwnd) appartiene a un processo diverso da quello che ha creato l'oggetto dispositivo.


</dt> </dl> </dd> <dt>

<span id="DCOMPOSITION_ERROR_SURFACE_BEING_RENDERED"></span><span id="dcomposition_error_surface_being_rendered"></span>**\_ \_ \_ viene \_ eseguito il rendering della superficie di errore DCOMPOSITION**
</dt> <dd> <dl> <dt>


</dt> <dt>



È stato già eseguito il rendering della superficie quando l'applicazione ha chiamato il metodo [**IDCompositionSurface:: BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw), [**IDCompositionSurface:: SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw)o [**IDCompositionSurface:: ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw) . Per altre informazioni, vedere la sezione Osservazioni.


</dt> </dl> </dd> <dt>

<span id="DCOMPOSITION_ERROR_SURFACE_NOT_BEING_RENDERED"></span><span id="dcomposition_error_surface_not_being_rendered"></span>**\_ \_ \_ non \_ è stato eseguito il \_ rendering della superficie di errore DCOMPOSITION**
</dt> <dd> <dl> <dt>


</dt> <dt>



L'applicazione ha chiamato il metodo [**IDCompositionSurface:: SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw), [**IDCompositionSurface:: ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)o [**IDCompositionSurface:: EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) per una superficie di cui non è stato eseguito il rendering. Per altre informazioni, vedere la sezione Osservazioni.


</dt> </dl> </dd> <dt>

<span id="DCOMPOSITION_ERROR_WINDOW_ALREADY_COMPOSED"></span><span id="dcomposition_error_window_already_composed"></span>**\_finestra di errore DCOMPOSITION \_ \_ già \_ composta**
</dt> <dd> <dl> <dt>


</dt> <dt>



Il metodo [**IDCompositionDevice:: CreateTargetForHwnd**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtargetforhwnd) è stato chiamato con HWND *e i* parametri in primo piano per i quali è già presente una struttura ad albero visuale. 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Se una chiamata a [**IDCompositionSurface:: BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) è stata l'azione più recente:



| Chiamata a questo metodo:                                    | Restituisce questo valore:                               |
|---------------------------------------------------------|---------------------------------------------------|
| [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)     | **\_ \_ \_ viene \_ eseguito il rendering della superficie di errore DCOMPOSITION** |
| [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)         | \_OK                                             |
| [**SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) | \_OK                                             |
| [**ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)   | **\_ \_ \_ viene \_ eseguito il rendering della superficie di errore DCOMPOSITION** |



 

Se una chiamata a [**IDCompositionSurface:: SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) è stata l'azione più recente:



| Chiamata a questo metodo:                                    | Restituisce questo valore:                               |
|---------------------------------------------------------|---------------------------------------------------|
| [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)     | **\_ \_ \_ viene \_ eseguito il rendering della superficie di errore DCOMPOSITION** |
| [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)         | \_OK                                             |
| [**SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) | **\_ \_ \_ viene \_ eseguito il rendering della superficie di errore DCOMPOSITION** |
| [**ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)   | \_OK                                             |



 

Se una chiamata a [**IDCompositionSurface:: ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw) è stata l'azione più recente:



| Chiamata a questo metodo:                                    | Restituisce questo valore:                                |
|---------------------------------------------------------|----------------------------------------------------|
| [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)     | **\_ \_ \_ viene \_ eseguito il rendering della superficie di errore DCOMPOSITION**  |
| [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)         | \_OK                                              |
| [**SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) | \_OK                                              |
| [**ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)   | **\_viene eseguito il rendering della superficie di errore DCOMPOSITION \_ \_ \_ .** |



 

Se una chiamata a [**IDCompositionSurface:: EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) è stata l'azione più recente:



| Chiamata a questo metodo:                                    | Restituisce questo valore:                                     |
|---------------------------------------------------------|---------------------------------------------------------|
| [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)     | \_OK                                                   |
| [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)         | **\_ \_ \_ non \_ è stato eseguito il rendering della superficie di errore DCOMPOSITION \_ .** |
| [**SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) | **\_ \_ \_ non \_ è stato eseguito il rendering della superficie di errore DCOMPOSITION \_ .** |
| [**ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)   | **\_ \_ \_ non \_ è stato eseguito il rendering della superficie di errore DCOMPOSITION \_ .** |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                         |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Dcomp. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Riferimento a DirectComposition](reference.md)
</dt> </dl>

 

