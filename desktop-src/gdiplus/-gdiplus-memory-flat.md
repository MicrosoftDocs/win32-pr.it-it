---
description: Windows GDI+ un'API flat costituita da circa 600 funzioni. Queste funzioni API flat vengono incapsulate dalla classe C++ GdiplusBase.
ms.assetid: b4fcc02c-1b0f-4731-8312-29894b1f722f
title: Funzioni di memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ce4e75de3cf5c7ff96a794416b75a9bacadda5a0aade2f5a61e2607e620e3a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943811"
---
# <a name="memory-functions"></a>Funzioni di memoria

Windows GDI+ un'API flat costituita da circa 600 funzioni, implementate in Gdiplus.dll e dichiarate in Gdiplusflat.h. Le funzioni nell'API GDI+ flat vengono incapsulate da una raccolta di circa 40 classi C++. È consigliabile non chiamare direttamente le funzioni nell'API flat. Ogni volta che si effettuano GDI+, è consigliabile eseguire questa operazione chiamando i metodi e le funzioni forniti dai wrapper C++. Il Servizio Supporto Tecnico Clienti Microsoft non fornirà il supporto per il codice che chiama direttamente l'API flat. Per altre informazioni sull'uso di questi metodi wrapper, vedere [GDI+'API Flat.](-gdiplus-flatapi-flat.md)

Le funzioni API flat seguenti vengono incapsulate dalla [**classe C++ GdiplusBase.**](/windows/desktop/api/gdiplusbase/nl-gdiplusbase-gdiplusbase)

## <a name="memory-functions-and-corresponding-wrapper-methods"></a>Funzioni di memoria e metodi wrapper corrispondenti



| Funzione flat                                          | Metodo wrapper                                                                                                                                      | Commenti                                                                                                      |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| GpStatus WINGDIPAPI GdipAlloc(size \_ t size)<br/> | [**GpStatus WINGDIPAPI GdiplusBase void \* (operator new)(size \_ t in \_ size)**](/windows/win32/api/gdiplusbase/nf-gdiplusbase-gdiplusbase-operatornew)<br/>      | Alloca memoria per un Windows GDI+ oggetto . <br/> GdipAlloc viene dichiarato in GdiplusMem.h.<br/>  |
| GpStatus WINGDIPAPI GdipFree(void \* ptr);<br/>   | [**GpStatus WINGDIPAPI GdiplusBase void (operator delete)(void \* in \_ pVoid)**](/windows/win32/api/gdiplusbase/nf-gdiplusbase-gdiplusbase-operatordelete)<br/> | Dealloca la memoria per un Windows GDI+ oggetto . <br/> GdipFree è dichiarato in GdiplusMem.h.<br/> |



 

 

 
