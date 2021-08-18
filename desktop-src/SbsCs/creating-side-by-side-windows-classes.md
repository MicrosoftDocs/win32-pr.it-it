---
description: I contesti dell'applicazione possono essere usati per creare classi Windows side-by-side.
ms.assetid: 4941ae1b-f9c6-45ff-b39b-a4078a12a58c
title: Creazione di classi Windows side-by-side
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8317712b333963f9864e195bb1c5f18896dcd73eec059c9c4ae670ff2fb6a4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142344"
---
# <a name="creating-side-by-side-windows-classes"></a>Creazione di classi Windows side-by-side

I contesti dell'applicazione possono essere usati per creare classi Windows side-by-side. Usando le classi di Windows side-by-side, l'applicazione può avere versioni diverse di una classe attive contemporaneamente in una sola finestra padre. Per creare una classe Windows side-by-side, l'applicazione deve attivare un contesto di attivazione prima di chiamare [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) per ottenere un handle per la nuova finestra.

Ad esempio, Windows i controlli comuni versione 5.82 e 6.0 avevano entrambi un controllo Edit. Windows usa per impostazione predefinita il controllo Edit versione 5.82. Per ottenere una finestra affiancata con il controllo Edit versione 6.0, prima di chiamare [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) come di consueto, l'applicazione può fare riferimento a un assembly che espone classi di finestre denominate e quindi attivare il contesto di attivazione che fa riferimento ai controlli della versione 6.0.

 

 
