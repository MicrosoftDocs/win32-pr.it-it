---
description: Windows GDI+ un'API flat costituita da circa 600 funzioni. Queste funzioni api flat vengono incapsulate dalla classe HatchBrush C++.
ms.assetid: c7d9e633-8c3d-4e77-811d-306cd785a7ad
title: Funzioni di HatchBrush
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74f550f3f3567a5835c7a220d0384dc1c6bbd24133577b9b89a6a37a0aae8840
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118067015"
---
# <a name="hatchbrush-functions"></a>Funzioni di HatchBrush

Windows GDI+ un'API flat costituita da circa 600 funzioni, implementate in Gdiplus.dll e dichiarate in Gdiplusflat.h. Le funzioni nell'API GDI+ flat vengono incapsulate da una raccolta di circa 40 classi C++. È consigliabile non chiamare direttamente le funzioni nell'API flat. Ogni volta che si effettuano GDI+, è consigliabile eseguire questa operazione chiamando i metodi e le funzioni forniti dai wrapper C++. Il Servizio Supporto Tecnico Clienti Microsoft non fornirà il supporto per il codice che chiama direttamente l'API flat. Per altre informazioni sull'uso di questi metodi wrapper, [vedere GDI+'API Flat.](-gdiplus-flatapi-flat.md)

Le funzioni API flat seguenti vengono incapsulate dalla [**classe HatchBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush) C++.

## <a name="hatchbrush-functions-and-corresponding-wrapper-methods"></a>Funzioni HatchBrush e metodi wrapper corrispondenti



| Funzione flat                                                                                                               | Metodo wrapper                                                                                                                                                                                   | Commenti                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| GpStatus WINGDIPAPI GdipCreateHatchBrush(Stile tratteggio GpHatchStyle, forecol ARGB, backcol ARGB, pennello \* \* GpHatch)<br/> | [**HatchBrush::HatchBrush(IN HatchStyle hatchStyle, IN const Color& foreColor, IN const Color& backColor = Color())**](/windows/win32/api/gdiplusbrush/nf-gdiplusbrush-hatchbrush-hatchbrush(consthatchbrush_)) | Crea un [**oggetto HatchBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush) basato su uno stile tratteggio, un colore di primo piano e un colore di sfondo. |
| GpStatus WINGDIPAPI GdipGetHatchStyle(pennello GpHatch, \* stile tratteggio GpHatchStyle) \*<br/>                                | [**HatchStyle HatchBrush::GetHatchStyle() const**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-hatchbrush-gethatchstyle)                                                                                                 | Ottiene lo stile del tratteggio di questo pennello tratteggio.                                                                                                  |
| GpStatus WINGDIPAPI GdipGetHatchForegroundColor(GpHatch \* brush, ARGB \* forecol)<br/>                                 | [**Stato HatchBrush::GetForegroundColor(OUT Color \* color) const**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-hatchbrush-getforegroundcolor)                                                                    | Ottiene il colore di primo piano di questo pennello tratteggio.                                                                                             |
| GpStatus WINGDIPAPI GdipGetHatchBackgroundColor(pennello GpHatch, \* \* backcol ARGB)<br/>                                 | [**Stato HatchBrush::GetBackgroundColor(OUT Color \* color) const**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-hatchbrush-getbackgroundcolor)                                                                    | Ottiene il colore di sfondo di questo pennello tratteggio.                                                                                             |



 

 

 
