---
title: Codici di errore DirectComposition (Dcomp.h)
description: Questa sezione descrive i codici di errore specifici di DirectComposition.
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
ms.openlocfilehash: 7d86ab61574af84e0b4b51223c69b181697dc0ebbdd7995c1bff112e286cc3ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119891981"
---
# <a name="directcomposition-error-codes"></a>Codici di errore di DirectComposition

Se si verifica un errore, Microsoft DirectComposition restituisce un codice come **valore HRESULT.** Questa sezione descrive i codici di errore specifici di DirectComposition. Per un elenco dei codici di errore Component Object Model (COM), vedere [Codici di errore COM](/windows/desktop/com/com-error-codes).

<dl> <dt>

<span id="DCOMPOSITION_ERROR_ACCESS_DENIED"></span><span id="dcomposition_error_access_denied"></span>**ACCESSO CON ERRORE DCOMPOSITION \_ \_ \_ NEGATO**
</dt> <dd> <dl> <dt>


</dt> <dt>



L'handle di finestra specificato in una chiamata al metodo [**IDCompositionDevice::CreateTargetForHwnd**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtargetforhwnd) appartiene a un processo diverso da quello che ha creato l'oggetto dispositivo.


</dt> </dl> </dd> <dt>

<span id="DCOMPOSITION_ERROR_SURFACE_BEING_RENDERED"></span><span id="dcomposition_error_surface_being_rendered"></span>**SUPERFICIE DI ERRORE DCOMPOSITION \_ \_ SOTTOPOSTA A \_ \_ RENDERING**
</dt> <dd> <dl> <dt>


</dt> <dt>



Il rendering della superficie è già in corso quando l'applicazione ha chiamato il metodo [**IDCompositionSurface::BeginDraw,**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) [**IDCompositionSurface::SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw)o [**IDCompositionSurface::ResumeDraw.**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw) Per altre informazioni, vedere la sezione Osservazioni.


</dt> </dl> </dd> <dt>

<span id="DCOMPOSITION_ERROR_SURFACE_NOT_BEING_RENDERED"></span><span id="dcomposition_error_surface_not_being_rendered"></span>**SUPERFICIE DI ERRORE DCOMPOSITION \_ \_ NON SOTTOPOSTA A \_ \_ \_ RENDERING**
</dt> <dd> <dl> <dt>


</dt> <dt>



L'applicazione ha chiamato il metodo [**IDCompositionSurface::SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw), [**IDCompositionSurface::ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)o [**IDCompositionSurface::EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) per una superficie di cui non viene eseguito il rendering. Per altre informazioni, vedere la sezione Osservazioni.


</dt> </dl> </dd> <dt>

<span id="DCOMPOSITION_ERROR_WINDOW_ALREADY_COMPOSED"></span><span id="dcomposition_error_window_already_composed"></span>**FINESTRA DI ERRORE DCOMPOSITION \_ \_ GIÀ \_ \_ COMPOSTA**
</dt> <dd> <dl> <dt>


</dt> <dt>



Il [**metodo IDCompositionDevice::CreateTargetForHwnd**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtargetforhwnd) è stato chiamato con i parametri *hwnd* e *topmost* per i quali esiste già una struttura ad albero visuale.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Se una chiamata a [**IDCompositionSurface::BeginDraw è**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) l'azione più recente:



| Chiamare questo metodo:                                    | Restituisce questo valore:                               |
|---------------------------------------------------------|---------------------------------------------------|
| [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)     | **SUPERFICIE DI ERRORE DCOMPOSITION \_ \_ SOTTOPOSTA A \_ \_ RENDERING** |
| [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)         | S \_ OK                                             |
| [**SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) | S \_ OK                                             |
| [**ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)   | **SUPERFICIE DI ERRORE DCOMPOSITION \_ \_ SOTTOPOSTA A \_ \_ RENDERING** |



 

Se una chiamata a [**IDCompositionSurface::SuspendDraw è**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) l'azione più recente:



| Chiamare questo metodo:                                    | Restituisce questo valore:                               |
|---------------------------------------------------------|---------------------------------------------------|
| [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)     | **SUPERFICIE DI ERRORE DCOMPOSITION \_ \_ SOTTOPOSTA A \_ \_ RENDERING** |
| [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)         | S \_ OK                                             |
| [**SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) | **SUPERFICIE DI ERRORE DCOMPOSITION \_ \_ SOTTOPOSTA A \_ \_ RENDERING** |
| [**ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)   | S \_ OK                                             |



 

Se una chiamata a [**IDCompositionSurface::ResumeDraw è**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw) l'azione più recente:



| Chiamare questo metodo:                                    | Restituisce questo valore:                                |
|---------------------------------------------------------|----------------------------------------------------|
| [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)     | **SUPERFICIE DI ERRORE DCOMPOSITION \_ \_ SOTTOPOSTA A \_ \_ RENDERING**  |
| [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)         | S \_ OK                                              |
| [**SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) | S \_ OK                                              |
| [**ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)   | **SUPERFICIE DI ERRORE DCOMPOSITION \_ \_ SOTTOPOSTA A \_ \_ RENDERING.** |



 

Se una chiamata a [**IDCompositionSurface::EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) è l'azione più recente:



| Chiamare questo metodo:                                    | Restituisce questo valore:                                     |
|---------------------------------------------------------|---------------------------------------------------------|
| [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)     | S \_ OK                                                   |
| [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)         | **SUPERFICIE DI ERRORE DCOMPOSITION \_ \_ NON SOTTOPOSTA A \_ \_ \_ RENDERING.** |
| [**SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) | **SUPERFICIE DI ERRORE DCOMPOSITION \_ \_ NON SOTTOPOSTA A \_ \_ \_ RENDERING.** |
| [**ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)   | **SUPERFICIE DI ERRORE DCOMPOSITION \_ \_ NON SOTTOPOSTA A \_ \_ \_ RENDERING.** |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                         |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Dcomp.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Informazioni di riferimento su DirectComposition](reference.md)
</dt> </dl>

 

