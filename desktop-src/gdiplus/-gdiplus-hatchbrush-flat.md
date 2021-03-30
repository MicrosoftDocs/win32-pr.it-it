---
description: Windows GDI+ espone un'API Flat costituita da circa 600 funzioni, implementate in Gdiplus.dll e dichiarate in Gdiplusflat. h.
ms.assetid: c7d9e633-8c3d-4e77-811d-306cd785a7ad
title: Funzioni HatchBrush
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d444fea500ce1e56e4c59420b913d5ff6cee965c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994221"
---
# <a name="hatchbrush-functions"></a>Funzioni HatchBrush

Windows GDI+ espone un'API Flat costituita da circa 600 funzioni, implementate in Gdiplus.dll e dichiarate in Gdiplusflat. h. Le funzioni nell'API flat di GDI+ sono racchiuse tra una raccolta di circa 40 classi C++. Si consiglia di non chiamare direttamente le funzioni nell'API flat. Quando si effettuano chiamate a GDI+, è necessario chiamare i metodi e le funzioni forniti dai wrapper C++. Il servizio supporto tecnico Microsoft non fornirà il supporto per il codice che chiama direttamente l'API flat. Per altre informazioni sull'uso di questi metodi wrapper, vedere [GDI+ Flat API](-gdiplus-flatapi-flat.md).

Le funzioni API Flat seguenti sono incapsulate dalla classe C++ [**HatchBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush) .

## <a name="hatchbrush-functions-and-corresponding-wrapper-methods"></a>Funzioni HatchBrush e metodi wrapper corrispondenti



| Flat-funzione                                                                                                               | Wrapper (metodo)                                                                                                                                                                                   | Commenti                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| GpStatus WINGDIPAPI GdipCreateHatchBrush (GpHatchStyle HatchStyle, ARGB forecol, ARGB backcol, GpHatch \* \* Brush)<br/> | [**HatchBrush:: HatchBrush (IN HatchStyle hatchStyle, nel colore const& foreColor, nel colore const& BackColor = Color ())**](/windows/win32/api/gdiplusbrush/nf-gdiplusbrush-hatchbrush-hatchbrush(consthatchbrush_)) | Crea un oggetto [**HatchBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush) in base a uno stile tratteggiato, un colore di primo piano e un colore di sfondo. |
| GpStatus WINGDIPAPI GdipGetHatchStyle (GpHatch \* Brush, GpHatchStyle \* HatchStyle)<br/>                                | [**HatchStyle HatchBrush:: GetHatchStyle () const**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-hatchbrush-gethatchstyle)                                                                                                 | Ottiene lo stile di tratteggio del pennello per il tratteggio.                                                                                                  |
| GpStatus WINGDIPAPI GdipGetHatchForegroundColor (GpHatch \* Brush, ARGB \* forecol)<br/>                                 | [**Status HatchBrush:: GetForegroundColor (OUT Color Color \* ) const**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-hatchbrush-getforegroundcolor)                                                                    | Ottiene il colore di primo piano di questo pennello di tratteggio.                                                                                             |
| GpStatus WINGDIPAPI GdipGetHatchBackgroundColor (GpHatch \* Brush, ARGB \* backcol)<br/>                                 | [**Status HatchBrush:: GetBackgroundColor (OUT Color Color \* ) const**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-hatchbrush-getbackgroundcolor)                                                                    | Ottiene il colore di sfondo di questo pennello di tratteggio.                                                                                             |



 

 

 
