---
description: Windows GDI+ espone un'API Flat costituita da circa 600 funzioni, implementate in Gdiplus.dll e dichiarate in Gdiplusflat. h.
ms.assetid: b4fcc02c-1b0f-4731-8312-29894b1f722f
title: Funzioni di memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86e748f8a68cc6f04deba3c9676638ee48ee2e86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978986"
---
# <a name="memory-functions"></a>Funzioni di memoria

Windows GDI+ espone un'API Flat costituita da circa 600 funzioni, implementate in Gdiplus.dll e dichiarate in Gdiplusflat. h. Le funzioni nell'API flat di GDI+ sono racchiuse tra una raccolta di circa 40 classi C++. Si consiglia di non chiamare direttamente le funzioni nell'API flat. Quando si effettuano chiamate a GDI+, è necessario chiamare i metodi e le funzioni forniti dai wrapper C++. Il servizio supporto tecnico Microsoft non fornirà il supporto per il codice che chiama direttamente l'API flat. Per altre informazioni sull'uso di questi metodi wrapper, vedere [GDI+ Flat API](-gdiplus-flatapi-flat.md).

Le funzioni API Flat seguenti sono incapsulate dalla classe C++ [**GdiplusBase**](/windows/desktop/api/gdiplusbase/nl-gdiplusbase-gdiplusbase) .

## <a name="memory-functions-and-corresponding-wrapper-methods"></a>Funzioni di memoria e metodi wrapper corrispondenti



| Flat-funzione                                          | Wrapper (metodo)                                                                                                                                      | Commenti                                                                                                      |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| GpStatus WINGDIPAPI GdipAlloc (size \_ t size)<br/> | [**GpStatus WINGDIPAPI GdiplusBase void \* (operator new) (size \_ t size \_ )**](/windows/win32/api/gdiplusbase/nf-gdiplusbase-gdiplusbase-operatornew)<br/>      | Alloca memoria per un oggetto GDI+ di Windows. <br/> GdipAlloc viene dichiarata in GdiplusMem. h.<br/>  |
| GpStatus WINGDIPAPI GdipFree (void \* ptr);<br/>   | [**GpStatus WINGDIPAPI GdiplusBase void (operator delete) (void \* in \_ PVOID)**](/windows/win32/api/gdiplusbase/nf-gdiplusbase-gdiplusbase-operatordelete)<br/> | Dealloca la memoria per un oggetto GDI+ di Windows. <br/> GdipFree viene dichiarata in GdiplusMem. h.<br/> |



 

 

 
