---
title: Estensione di funzioni OpenGL
description: La libreria OpenGL supporta più implementazioni delle relative funzioni.
ms.assetid: 9eb08fd4-899a-4610-9491-d7f377a19b46
keywords:
- OpenGL per Windows, funzioni di estensione
- funzioni di estensione OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dcbb59aa15a9690ac05728548f0d8073a334a2e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955732"
---
# <a name="extending-opengl-functions"></a>Estensione di funzioni OpenGL

La libreria OpenGL supporta più implementazioni delle relative funzioni. Le funzioni di estensione supportate in un contesto di rendering non sono necessariamente supportate in un contesto di rendering diverso. Per un determinato contesto di rendering in un'applicazione che utilizza funzioni di estensione, utilizzare solo gli indirizzi di funzione restituiti dalla funzione [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress) .

 

 




